## Section 1:

Firewalls have become extremely complex overtime and as a result necessitate a clear standard for measuring there performance.

## Section 2:

General language used by RFCs. (ie. MUST, SHOULD, MAY, etc)

## Section 3:

This testing methodology is designed for Next Generation security devices that are setup and actively running. This is not designed for systems that use ML or behavioral analysis.

## Section 4:

Devices must be tested in a isolated environment, and without any limitations due to other network devices (switchs, routers, etc). It's recommended that the DUT be connected to an emulator that will simulate traffic from routers to avoid physical hardware limitations.

During testing the DUT must be configured as if it where a regular device. It must also be put in "inline" mode so that it inspects traffic. Tested feature are broken down into the following categories:

- TLS Inspection
- IDS/IPS
- Anti-Malware
- Anti-Spyware
- Anti-Botnet
- Anti-Evasion
- Web Filtering
- Data Loss Protection (DLP)
- Certificate Validation
- Logging/Reporting
- Application Identity
- Deep Packet Inspection (DPI)

DLP, certificate validation, and web filtering are optional. TLS inspection is sometimes optional.

Fore NGFW we only need these ones:

- TLS Inspection
- Anti-Malware
- Anti-Spyware
- Anti-Botnet
- Application ID
- Deep Packet Inspection
- Anti-Evasion

### General Device Config

During testing devices must be configured as follows:

- DUT must be set to "inline" mode
- "Fail-Open" MUST be disabled
- All available security features MUST be enabled
- Logging and Reporting MUST be enabled
- Geo Location filtering SHOULD be enabled. If its not you should NOTE it in the report
- Application Identity and Control is configured based on the predetermined traffic mix

Along with these you should also configure ACLs as needed. There is a big table fore this below:

| DUT/SUT Classification Rules |                              |                                                                                                  |        |     |     |     |     |
| ---------------------------- | ---------------------------- | ------------------------------------------------------------------------------------------------ | ------ | --- | --- | --- | --- |
| Rules Type                   | Match Criteria               | Description                                                                                      | Action | XS  | S   | M   | L   |
| Application layer            | Application                  | Any application not included in the measurement traffic                                          | block  | 5   | 10  | 20  | 50  |
| Transport layer              | SRC IP and TCP/UDP DST ports | Any SRC IP prefix used and any DST ports not used in the measurement traffic                     | block  | 25  | 50  | 100 | 250 |
| IP layer                     | SRC/DST IP                   | Any SRC/DST IP subnet not used in the measurement traffic                                        | block  | 25  | 50  | 100 | 250 |
| Application layer            | Application                  | Half of the applications included in the measurement traffic (see the note below)                | allow  | 10  | 10  | 10  | 10  |
| Transport layer              | SRC IP and TCP/UDP DST ports | Half of the SRC IPs used and any DST ports used in the measurement traffic (one rule per subnet) | allow  | >1  | >1  | >1  | >1  |
| IP layer                     | SRC IP                       | The rest of the SRC IP prefix range used in the measurement traffic (one rule per subnet)        | allow  | >1  | >1  | >1  | >1  |

These features must be setup to detect and prevent vulnerabilities from atleast 500 CVEs. These CVEs must be from within the past 10 years, and should have scores from 7-10. If security is not tested for whatever reason, this MUST be explained in the report.

### Test Equipment Config

Test equipment is broken down into 2 groups: client, and server. The client is the device making requests, the server receives them. This allows us to test how the DUT responds to large amount of traffic as well as malicious traffic.

#### Client Config

For TCP stack use below:

- Should use all TCP config [here](https://www.rfc-editor.org/rfc/rfc9293#appendix-B)
- Max Segment Size for IPv4 is 1460 and for IPv6 its 1440.
- Maximum ACK delay is 200 ms.

For QUIC use:

- UDP payloads should be 1252 bytes for IPv4 and 1232 bytes for IPv6.
- The stream type should be "Client Initiated Bidirectional".
- 0-RTT should be disabled.

Testing should use multiple discontinuous blocks of IP addresses. Type of Service and Traffic Class should be set to 0000. IPv6 MAY use more than 1 extension header.

Vendors may select from one of the following distributions of IP addresses.

- 100% IPv4
- 80% IPv4, 20% IPv6
- 50% IPv4, 50% IPv6
- 20% IPv4, 80% IPv6
- 100% IPv6

The web browser used by a client must adhere to the following:

- HTTP version must be 1.1 or Higher.
- Browser must enforce content length validation
- HTTP header compression is allowed (But must be documented in NOTES)
- Multiple connection (or streams) may be opened at one time.
- If using QUIC the browser must initiate the connection with TLS 1.3
- Any encrypted traffic must use TLS 1.2 or higher.
  - TLS 1.2 use these ciphers:
    - ECDHE-ECDSA-AES128-GCM-SHA256 with Prime256v1
    - ECDHE-RSA-AES128-GCM-SHA256 with RSA 2048
    - ECDHE-ECDSA-AES256-GCM-SHA384 with Secp384r1
    - ECDHE-RSA-AES256-GCM-SHA384 with RSA 4096
  - TLS 1.3 use these ones:
    - TLS_AES_128_GCM_SHA256
    - TLS_AES_256_GCM_SHA384
    - TLS_CHACHA20_POLY1305_SHA256
    - TLS_AES_128_CCM_SHA256

#### Server Config

TCP & QUIC must be configured the same way as the client.

For IP addressing the server is required to use multiple discontinuous blocks of addresses. Each FQDN must map to a single IP address. The server must use the same IPv4/v6 distribution as the client.

The server is require to listen on ports 80 and 443, and should emulate the same HTTP version as the client device. For HTTPS there is a maximum record size of 16 KB.

### Traffic Load During Test

The actual test (sending a lot of traffic through firewall at once) is broken up into 5 stages, as described below:

- Init Phase
  - At this point the Clients and Servers are set up and negotiate layer 2-3 connectivity (ie. ARP, Neighbor Discovery). This DOES NOT include creating HTTP/S connections.
- Ramp Up Phase
  - This parts starts when clients begin generating traffic. During this time the load on the network goes from 0 to the target throughput.
- Sustain Phase
  - This stage is reached when all devices are active and the desired load the network is reached. At this point load on the network should remain constant, and all devices should continue generating traffic.
- Ramp Down Phase
  - This stage encompasses the total throughput going from the target amount down to 0.
- Collection Phase
  - This stage is more administrative as its just when all the traffic stops.

All KPIs should be taken during the Sustain Phase of testing.

## Section 5:

Before testing you will want to do a pre-test run of things without the DUT setup. You will need to run through the same Traffic load steps as before and record the same KPIs so you have a baseline of what to expect on the network.

## Section 6:

This covers the contents of the report. In general this is broken up into an Intro and then a detailed report of the results. For the intro it should contain the following:

- Time/Date of Tests
- Summary of testbed equipment
  - This include the DUT and any test equiptment.
  - This should include version numbers, and hardware (like CPU cores, and RAM).
  - If any virtualization was used, you should include version and resources for that.
  - Any additional config done on the DUT
- A table including the enabled features should be included
  - This should indicate if the feature was supported or not.
- We should additonally include the test config. Including the Ciphers used, IP distribution, number of ACLs, and TCP/QUIC settings.
- We should also include a breakdown of the traffic types, and amount of encrypted traffic.

For the Test Results include the following:

- For each benchmark test run you should include a table with all applicable PKIs.
- We should also include graphs of the metrics over the sustain phase.

In terms of KPIs we should collect the following:

- Concurrent TCP Connections
- Concurrent QUIC Connections
- TCP Connections Per Second
- QUIC Connections Per Second
- Application Transactions Per Second
- TLS Handshake Rate
- Inspected Throughput
- Time to First Byte (TTFB)
- URL Response Time (Time to Last Byte)
