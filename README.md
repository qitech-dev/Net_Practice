*This project has been created as part of the 42 curriculum by qijin.*

# NetPractice

## Description

NetPractice is a networking exercise from the 42 curriculum.

The goal of the project is to understand the fundamentals of TCP/IP networking by solving a series of simulated network configuration problems. Each exercise asks for valid IP addresses, masks, gateways, and routes so that every required machine can communicate with the correct target.

The project contains 10 levels. In each level, some parts of the network configuration are incorrect or missing. The objective is to configure the network so that all required hosts can communicate correctly.

The main concepts covered are:

- IPv4 addressing
- Subnet masks and CIDR notation
- Network and broadcast addresses
- Default gateways
- Routers and routing tables
- Static routes
- Switches
- TCP/IP networking
- OSI layers

## Instructions

### Running NetPractice

Extract the NetPractice files and run:

```bash
./run.sh
```

This starts a local web server and opens the training interface in a web browser.

If `run.sh` does not work, the interface can also be started manually:

```bash
python3 -m http.server 49242
```

Then open:

```text
http://localhost:49242
```

Enter your 42 login before starting the exercises.

### Solving a level

Each level contains a network topology with configurable fields such as:

* IP addresses
* Subnet masks
* Gateways
* Routing table entries

Modify the available fields and use **Check again** to test the configuration.

The logs displayed by NetPractice can help identify routing, addressing, or gateway errors.

### Exporting configurations

After successfully completing a level, click:

```text
Get my config
```

to export the configuration.

Do this before moving to the next level.

## Submission

The repository must contain 10 exported configuration files, with one file for each level.

All 10 exported configuration files must be placed at the root of the Git repository.

Example structure:

```text
NetPractice/
├── README.md
├── level1.json
├── level2.json
├── level3.json
├── level4.json
├── level5.json
├── level6.json
├── level7.json
├── level8.json
├── level9.json
└── level10.json
```

The exact exported filenames may depend on the NetPractice interface.

## Networking Concepts

### IP Address

An IPv4 address identifies an interface on an IP network.

Example:

```text
192.168.1.10
```

### Subnet Mask

A subnet mask determines which part of an IP address represents the network and which part represents the host.

For example:

```text
255.255.255.0
```

is equivalent to:

```text
/24
```

### Network Address

The network address identifies the subnet itself and cannot normally be assigned to a host.

For:

```text
192.168.1.10/24
```

the network address is:

```text
192.168.1.0
```

### Broadcast Address

The broadcast address represents all hosts in a subnet.

For:

```text
192.168.1.10/24
```

the broadcast address is:

```text
192.168.1.255
```

### Default Gateway

When a destination is outside the host's local subnet, packets are sent to the default gateway.

The gateway must normally be reachable directly from the host's local network.

### Router

A router connects different networks.

Each router interface belongs to a network, and the router uses its routing table to decide where packets should be forwarded.

### Routing Table

A routing table contains routes in the form:

```text
destination network -> next hop
```

For example:

```text
192.168.2.0/24 -> 10.0.0.2
```

The default route:

```text
0.0.0.0/0
```

matches destinations for which no more specific route exists.

### Switch

A switch connects devices within the same local network and mainly operates at Layer 2 of the OSI model.

### OSI Model

The OSI model separates network communication into seven layers:

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

NetPractice mainly focuses on concepts related to Layers 2 and 3, especially Ethernet/IP addressing and routing.

## Resources

The main networking concepts studied in this project include TCP/IP addressing, IPv4 subnet masks and CIDR notation, network and broadcast addresses, default gateways, routers, routing tables, static routes, switches, and the OSI layers.

Useful references for this project:

* [RFC 791 — Internet Protocol](https://datatracker.ietf.org/doc/html/rfc791)
* [RFC 1122 — Requirements for Internet Hosts](https://datatracker.ietf.org/doc/html/rfc1122)
* [RFC 4632 — Classless Inter-domain Routing (CIDR)](https://datatracker.ietf.org/doc/html/rfc4632)
* [Cisco — IP Addressing and Subnetting](https://www.cisco.com/)
* [Wikipedia — IPv4](https://en.wikipedia.org/wiki/IPv4)
* [Wikipedia — Subnetwork](https://en.wikipedia.org/wiki/Subnetwork)
* [Wikipedia — Routing table](https://en.wikipedia.org/wiki/Routing_table)
* [Wikipedia — OSI model](https://en.wikipedia.org/wiki/OSI_model)

### Use of AI

AI tools were used as a learning aid during the project.

They were used to:

* Clarify networking concepts such as TCP/IP addressing, subnet masks, CIDR notation, default gateways, routers, switches, routing tables, and OSI layers
* Explain why particular network configurations were invalid
* Review reasoning used to solve exercises
* Help structure and review this README

All network configurations were tested using the NetPractice interface, and the networking concepts used in the project were reviewed and understood before submission.
