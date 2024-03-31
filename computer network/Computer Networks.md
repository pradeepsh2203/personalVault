*A course on fundamentals of networking by Hussain Nasser*

## Section 1:- Fundamentals of Networking

In this section we get to learn about 
- Client Server Architecture - 
	  The reason why we need networking is that we can give heavy task to be performed on a remote server and thus our client can be lightweight. So as per the author **RPC** is the reason that networking exists.
- OSI Model :-
	  The 7 Layer model to classify about the networking
- Host to Host Communication :-
	  The reason why IP address and mac address exists.

## Section 2:- Internet Protocol (IP)

The Internet Protocol is a layer 3 protocol and helps us to route the IP Packets using [[IP Address]]

### Anatomy of IP Packet
- The IP packet has headers and data sections
- The IP header is 20 bytes long. (and can go upto 60 bytes if certain options are available)

![[Pasted image 20231218152645.png]]

** **ICMP Protocol** - Internet control message protocol

- Packets needs to get fragmented If they can't fit in a frame.