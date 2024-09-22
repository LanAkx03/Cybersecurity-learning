

On 'CPT' only look on simulation for HTTP & HTTPS

- Open Jonhy's laptop
- Desktop
- Web Browser
- https//networkchuck.coffee


**Analyse traffic step by step** :
- 2 HTTPS (2 separates messages)
	- one is saying getting ready
	- one is sending up to the switch

Layer 7 : HTTPS 
- the HTTP client sends a HTTP request to the server
![[Layer 7.png]]
Layer 6 : /

Layer 5 : /

Layer 4 : *TCP Src Port: 1025, Dst Port: 443* 
1) *send fragment information: the sequence number 1, the ACK number 1, and the data lenght 108*
	- The DATA need to be TRANSPORT. For that we can use TCP or UDP
	- We going to use TCP that is more RELIABLE when UDP is more FASTER
	- 443 is reserved fot HTTPS traffic
	- 80 is for HTTP traffic
	- Layer 4 Header say "we going to use TCP protocol and port 443"
	- DATA + L4 Header = **SEGMENT**
![[Layer 4.png]]

Layer 3 : *IP Header Src. IP: 10.1.1.3, Dest. IP:23.227.38.65*
1) *The destination IP Address 23.227.38.65 is not the same subnet and is not the broadcast address.*
2) *The default gateway is set. The device sets the next-hop default gateway.* 
	- Data + L4 Header + L3 Header = **PACKET**

![[Layer 3.png]]

Layer 2 (Data Link): *Ethernet II Header 00D0.9752.8936 >> 0002.17EB.1D01*
1) *The next-hop IP address is a unicast. The ARP process looks it up in the ARP table.*
2) *The next-hop IP address is in the ARP table. The ARP process sets the frame's destination MAC address to the one found in the table*
3) the device encapsulates the PDU into the Ethernet Frame
	- It is the DATA LINK layer
	- MAC addresses (of the router here)
	- L2 header tell the switch where it have to delivered the message
	- L2 Trailer + DATA + L4 Header + L3 Header + L2 Header = **FRAME**
	
![[Layer 2.png]]

**When the frame arrived to the SWITCH** :
1) the switch only open "the first enveloppe"/the frame and see Layer 1 & Layer 2 ![[Switch 1.png]]
2) he got the MAC address and looking the the CAM (Content-Addressable Memory) table 
3) From this table he can see that the MAC address belong to this PORT
	- FastEthernet0/6 is where the router is connected

**FRAME arrived to the ROUTER** :
1) It is going to DE-ENCAPSULATED the message
![[6_Router 1.png]]
3) he make sure the MAC address is his own
4) The router look only the PACKET (there is DE-ENCAPSULATION)
5) PACKET = L3 Header + L4 Header + Data
6) Router look at the L3 (where he need to send)

**FROM ROUTER TO SWITCH**
1) Switch can only deal with L2
2) Router have to somehow tell the SWITCH to send the message at "networkchuck.coffee"
3) CAM table and match the MAC address to the IP address and [RE-ENCAPSULATE] the IP in a NEW L2 HEADER

**FRAME arrived to the switch2**

Same, MAC address and looking in his CAM table for the MAC address and set the right Ethernet Port (layer 1)

**When the FRAME arrived to the SERVER**

1) the server is looking L2 to verified if he belong the message 
	1) Layer 2 - Mac address
2) DE-ENCAPSULATED and open up the Layer 3 
	1) Layer 3 - Ip address
3) DE-ENCAPSULATED again and open up the Layer 4
	1) TCP protocol and port 443 
4) The server send it to the application and application see the HTTP request (DATA)