
- Layer 3 property
- Can be set automatically or statically
- 4 bytes or 32 bits address in case of IPV4 for ex :- 192.128.1.0
- 16 bytes or 128 bits address in case of IPV6 for  ex:- **2001:0db8:85a3:0000:0000:8a2e:0370:7334**

IP address classification using subnet is represented as follows a.b.c.d/x where x represent the network bits.

So for the IP address 192.128.1.0/24, 24 out of 32 bits are network bits and the remaining 8 bits are host bits.

## Subnet Mask
The subnet mask is used to identify if two IP address belongs to same subnet or not and is made up of 1s and 0s for the above example the subnet mask would look like this 24 times 1s followed by 8 zeros.

## Default gateway
It is the host in the subnet that can communicate with the outside network and thus handles all the traffic external to subnet.

