# CompTIA Network+ (Exam N10-007) Cheatsheet

## Chapter 1

## Chapter 2

## Chapter 3

### Diagrams
#### Ethernet Header
preamble (+SFD)|dst address|src address|Ehtertype|payload
---|---|---|---|---
8 bytes|6 bytes|6 bytes|2 bytes|64 - 1500 bytes

#### TIA/EIA 568A/568B Wiring Diagram
![TIA/EIA 586A and 568B wiring diagram](tia568ab.png)

### Tables
#### Layer 1 and 2 Network devices
Device|OSI Layer|Ports|Use
---|---|---|---
repeater|1|2|dumb, physical layer device used to join two networks into a single network. Used to extend the distance of a cable run.
bridge|2|2|like a repeater but learns which MAC addresses live on each side and only repeats traffic when the destination MAC is on the other side or if it doesn't know which side it is on.
hub|1|varies|a multi-port repeater. Used to join several cables into a single network.  Seldom used as hubs create a single collision domain for all devices and bandwidth is shared among all devices (half-duplex operation results in only one device on the entire network able to send data at any given time).
switch|2|varies|a multi-port bridge. Used to join several cables into a single network.  Has replaced hubs as standard device for creating networks as each port is its own collision domain (i.e. no collisions when using full-duplex) and each device can use the full bandwidth of the switch (i.e. a Gigabit switch provides Gigabit speeds to each port).

#### Older Ethernet Specifications
Specification|Max Nodes|Speed|Max Cable Length|Min. Cable Type|Connector
---|---|---|---|---|---
10BaseT|1024 nodes|10Mbps|100m|Cat 3 UTP|RJ45
10BaseFL|1024 nodes|10Mbps|2000m|multimode fiber|SC or ST

### Definitions
Term|Definition
---|---
BPDU guard|disables PC ports (ports assigned the PortFast flag) if it sees a BPDU packet
BPDU|Bridge Protocol Data Unit.  Used instead of "packet" when talking about</br> Spanning Tree Protocol (STP)
Baseband| A connection that carries only a single signal.
Broadband| A connection that carries multiple signals at different frequencies.
Broadcast Domain|
Broadcast|
CAM table|Content Addressable Memory table
CSMA/CD| Carrier Sense Multiple Access/Collision Detection. A term describing how</br> Ethernet works.  Multiple devices access the network simultaneously and</br> listen for traffic.  They only send when they do not hear other traffic and they</br> listen for collisions while sending.  When a collision is detected, both</br> senders stop, wait a random amount of time, and then try again.
Collision Domain|The area in which a collision can occur in a network.  All</br> devices connected to a hub are in a single collision domain.  Switch ports</br> in half-duplex mode are each their own collision domain.
Collision|When two devices attempt to send at the same time causing their signals</br> to interfere with each other.
Full-duplex| A connection state where devices on the connection can send and</br> receive data simultaneously
Half-duplex| A connection state where devices on the connection can send or</br> receive data, but can not do both at the same time.
Multicast|
Network|A collection of devices connected through a shared media
Node| A device connected to the network.
PortFast|
RJ-45| A plastic wire connector used on Ethernet cables with 8 pins.  Also known</br> as 8P8C.
RSTP|Rapid Spanning Tree Protocol. A replacement for the older Spanning Tree</br> Protocol (STP)k which converges faster after a link fails (6 seconds vs 50 seconds)
Root Guard|
STP|Spanning Tree Protocol
Source Address Table|(aka CAM table)
TCN|Topology Change Notification. A specific BPDU message used to communicate</br> changes in link status
UTP|
Unicast|

### Notes
- Defective Ethernet patch cables are often defective at the ends and re-crimping or replacing one or both ends may fix it.

## Chapter 4
100BaseTX(Fast Ethernet), 1024 nodes, 100Mbps, 100m, Cat 5, RJ-45/8P8C
Auto-negotiation

100BaseFX, 1024 nodes, 100Mbps, 2000m, multimode, SC or ST

full duplex
Can a hub be full-duplex?
Can a PC configured for full duplex experience slowness due to collisions?  What happens if the switch is half-duplex?

1000BaseT(802.3ab), 1024 nodes, 1000Mbps, 100m, Cat 5e/6, RJ-45/8P8C
1000BaseSX(802.3z), 1024 nodes, 1000Mbps, 220m-500m, multi-mode fiber (LED), variable (commonly LC)
1000BaseLX(802.3z), 1024 nodes, 1000Mbps, 5km, single-mode fiber (laser), variable (commonly LC and SC)

Small Form Factor (SFF) fiber connectors
- Mechanical Transfer Registered Jack (MT-RT)
- Lucient Connector (LC)

Physical Contact (PC)
Ultra Physical Contact (UPC)
Angled Physical Contact (APC)

Fiber cable attributes
- connector type
- contact type
- material (single- or multi-mode)
- length

media converters (aka transcievers)

Gigabit Interface Converter (GBIC)

Small form-factor pluggable (SPF)

10GBaseSR, 10Gbps, 26-300m, multi-mode fiber (850nm), LAN signaling
10GBaseSW, 10Gbps, 26-300m, multi-mode fiber (850nm), SONET/WAN signaling
10GBaseLR, 10Gbps, 10km, single-mode fiber (1310nm), LAN signaling
10GBaseLW, 10Gbps, 10km, single-mode fiber (1310nm), SONET/WAN signaling
10GBaseER, 10Gbps, 40km, single-mode fiber (1550nm), LAN signaling
10GBaseEW, 10Gbps, 40km, single-mode fiber (1550nm), SONET/WAN signaling

10GBaseT, 10Gbps, 55m/100m, Cat 6/Cat 6a, RJ-45

Multisource agreements (MSA)
XENPAK
Enhanced small form-factor pluggable (SPF+)


Wave division multi-plexing (WDM) allows multiple signals on the same fiber.  Bidirection (BiDi) transceivers use a single fiber for both directions.

1000Base BiDi, SFP
10GBase BiDi, SFP+
40GBase BiDi, QSFP (Quad SFP)

Backbone
802.3ba defines 40GbE and 100GbE.

## Chapter 5

## Chapter 6

## Chapter 7

## Chapter 8

## Chapter 9

## Chapter 10

## Chapter 11

## Chapter 12

## Chapter 13

## Chapter 14

## Chapter 15

## Chapter 16

## Chapter 17

## Chapter 18

## Chapter 19

## Chapter 20

## Chapter 21

