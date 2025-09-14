# Network+ Notes

## Section 1 - Networking Theory

### General Info:

A network can best be described as an interconnected system. Traditionally when we think of the internet we think of a network of computers.

Within a network we have a number of components:

- Devices
  - All of the devices that make up a network\
  - Hosts
  - Routers
- Media
  - The means of transmitting information between devices
  - Physical cables (Ethernet, Fiber, etc.)
  - Wireless Communication
- Adapters
  - Provide the connection between devices and the media being used to transport information
  - Network Interface Card (NIC)
- Operating system
  - The software that makes devices work.
  - Windows/Linux for Hosts
  - Cisco IOS

Generally when we discuss networks we may use the term **Node**. This is used to refer to ANY device that is connected, including hosts, routers, and everything in between.

When I use the term **Host** I am more formally referring to an **Endpoint**, which is any device that does not intself connect multiple other devices.

Technically routers, switches, and hubs would be referred to as **Redistribution** nodes, but no one actually uses this terminology.

### Network Backbone

The network backbone is core structure of the network typically used in reference to WANs and ISPs.

- Serial - A network structure where devices are connected 1 to 1 without any redundancy.
- Distributed - Creating a hierarchical structure of routers/switches traditionally used in LANs.
- Parallel - Using link aggregation to add redundancy to a network connection.

## Section 2 - Categorizing Networks

When we talk about networks we tend to classify them based on size, often with acronyms. (LAN, WAN, MAN, PAN, etc.)

### Acronyms

- Local Area Networks (LANs)
  - Traditionally use Ethernet or Wifi for communication.
  - Entirely self-contained without the need for an ISP
  - Under a single administration/organization
  -
- Wide Area Networks (WANs)
  - Cover large geographical distances
  - Often connects LANs, and MANs
  - Described as Public or Private
    - Public WANs are operated by ISPs and can be used by pretty much anyone (this makes up the internet)
    - Private WANs are operated by organization for internal use only (often connecting different branches/offices)
- Personal Area Networks (PANs)
  - Similar to a LAN but encompasses the devices within your personal bubble
  - This is usually used to refer to bluetooth devices that you use.
- Campus Area Networks (CANs)
  - Represents the network of a campus or facility that may contain multiple LANs.
  - The destination with CANs is that they may contain multiple LANs, but they are still **operated by a singular organization**
  - Think of a company with multiple buildings in the single area. This will usually mean there are multiple LANs for each building, but the actually network is still under one organization.
- Metropolitan/Municipal Area Networks (MANs)
  - Represents a network within a specific city/metro area.
- Global Area Networks (GAN)
  - Almost entirely redundant.
  - No one actually uses this terminology, but CompTIA.

**Sometimes the term Enterprise Network (EN) is used to refer to a corporate network thats somewhere between a LAN/WAN.**

### Internet vs Intranet vs Extranet

The Internet is any large scale network. When we use the term Internet we are almost always referring to the public internet that we connect to through an ISP.

An Intranet represents an internal network usually for some organization. This intranet has web pages and services provided within the organization for use by the organization.

An Extranet represents a part of an organizations network that is open to specific external users. An extranet is a part of an organizations intranet, but is separated for the sake of security since there is at least some external access.

### Client vs. Server

A model for providing services over a network without the need for a centralized system.

**Servers** can be set up to provide specific services (using ports) and then separate **Clients** can request access to those services over the network. This should be obvious, but in this setup both Clients and Servers are endpoints (or hosts).

- Clients make requests for information
- Servers accept incoming requests and return some data.

### Peer to Peer (P2P)

The Peer to Peer model flips the whole client/server separation on its head. Instead of having a clear distinction between the service provider (server) and the user of the service (client), in a P2P setup both hosts will operate in both roles.

This means that the both devices are able to request information, as well as return information to one another.

## Section 3 - Network Topologies

A network topology is just the layout or arragement of stuff in a network. When we document the design and layout of the network we almost always do it either **Physically** or **Logically**.

### Physical Topology

Represents the actual layout/location of the devices in the real world, including how they are connected together. Thios might include the location/room number of the device, or the actual location within a server rack.

### Logical Topology

Represents how devices are connected together without care for how they are physically setup. Think how we look at networks in packet tracer. We simply see where each device is connected to one another.

### Network Connections

### Message Types

- Unicast - packets with a singular destination.
- Multicast - packets that are destined to multiple destinations typically within some group.
- Broadcast - packets destined for all destinations on a given link.

### Common Topologies

- **Bus Topology** - Nodes are each connected to a single cable and traffic is sent down the line to all nodes.
- **Ring Topology** - Each node is connected to an upstream and downstream node and packets are effectively sent in a circle until it reaches the target node. (Typically data is sent in 1 directions only)
- **Star Topology** - Nodes are connected to a intermediary device like a switch forming a start shape.
- **Mesh Topology** - Each node is connected to every other node. Mesh topologies are fast and fault tolerant but difficult to manage. (Often you will see partial mesh topologies)
- **Hybrid Topologies** - Are any topology that combine multiple of these.

**Bus/Ring topologies are pretty much legacy and no one actually uses them.**

## Section 4 - Network Media

Network media represents what is actually being used to transmit data between devices.

## Bounded Media

Represents physical cabling that is used to transmit data (as opposed to unbounded/wireless media).

## Copper Media

Any type of cable that uses copper to transmit information. There are a number of different kinds fo copper media as described below.

- **Coaxial** -
- **Twisted Pair** - Cables that use pairs of twisted copper cables. These are type CAT # cables and often use RJ-45 connectors.

## T568A vs. T568B

When terminating Twisted Pair cables (using RJ-45 connectors) there are 2 primary pinouts that you can use as defined by ANSI/TIA.

## UTP vs. STP

When we talk about Twisted Pair cables its important to make the distinction between **Unshielded Twisted Pairs (UTP)** and **Shielded Twisted Pairs (STP)**.

## Fiber Optic Media
