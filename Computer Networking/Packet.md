#computer-networking, #computer-science, #CSE
[resource]([What is a packet? | Network packet definition | Cloudflare](https://www.cloudflare.com/en-in/learning/network-layer/what-is-a-packet/))

	 Packet is smallest segment of larger message.

Data sent over the internet is not sent as the single file of data or in a one go but it is divided into `packets`. These packets are then recombined by the computer or device at the receiving end.

# Why use packets?
It is possible to send data as one large piece of data over the internet through cables, radio waves, or wires. However when this is being sent over, say, wire, then that means for the time when data is being sent no other computer/client can use this wire to send their data. Hence this approach is impractical. In contrast to this approach, the Internet is a `packet switching` network.
## What is packet switching?
`Packet switching` refers to the ability of the networking equipment to process each individual packet differently from each other. 
Note: Different packets can take different paths to reach the same destination.

> Because of packet switching the different packets from multiple computers can travel through same route, say, wire in any order.

## Package Header:
Now that you understood that in packet switching each packet is processed individually different from each other then one obvious question is "how does these packets are reached to their destination even after being processed differently?". There Have to have some label on these packets containing information about where the package should go, where the packet came from and some other useful information for the delivery of the packet to its intended destination. These labels are called as `package headers`.
	Package header is a label of sorts, which contains the information about packet's origin, destination and contents.

Packets consists of two portions: The header and payload. 
### Header
Header consists of the information on the packet such as origin and destination IP address.

### Payload
Payload consists of contents of the packet (actual data).


	Take the example of the image -> If you send someone an image  then that image is broken down into thousands of packets each having header and payload. Header consisting the origin and destination of packet and payload consisting small part of the image.

## Where do packet headers come from?
Headers are attached by networking protocols to the packets.
In practice, packets actually have more than one header, each header is used by a different part of the networking process.
At minimum most packets that traverse the internet will include a TCP (Transmission control protocol) header and IP (Internet Protocol) header.


# What are packet trailers and footers?
Packets headers go on the front of the each packet. Routers, switches, computers and anything else that processes these or receives the packet first sees the header first. A packet can also have a trailers and footers attached to their end which contains additional information about the packet. 

Only certain protocols attach trailers and footers to the packet. (ESP of IPSec suite is n/w layer protocol which attaches trailers to the packet.)

# What is an IP packet?
IP (Internet protocol ) is a n/w layer protocol that has to do with routing. It is used to make sure that packets arrive at the correct destination.
==="Packets are defined by the protocol they are using."===
So packet with using Internet protocol would be called an "IP Packet." IP packet will contain the IP header which contains the information on where the packet is came from and where it is going, how large the packet is and, how long network routers should continue to forward the packet before `dropping`it. It can also indicate whether or not packet can be fragmented and information about reassembling the fragmented packets.

# Packets vs. Datagrams
"Datagram" is a segment of data sent over a packet-switched network. A datagram contains enough info to be routed from its source to destination. By this definition, an IP packet is one example of a datagram. 

===Essentially Datagram is alternative term for packet.===

# What is n/w traffice? What is malicious n/w traffic?
N/w traffic is a term refers to the packet that pass through a network in the same way that automobile traffic passes on the road (car, bus, truck, etc.).

Not all packets in the traffic are useful or good and not all n/w traffic is safe. Attackers can generate malicious n/w traffic - Data packet designed to compromise or overwhelm a network.


