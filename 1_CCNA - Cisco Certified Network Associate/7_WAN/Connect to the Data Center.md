
How do YOU connect to the Data Center ?


1) LAN 
		Local Aera Network
2) WAN
		Wide Aera Network


Why de we need to connect with Corporate Office ? Why the Corporate Office need to communicate with the Data Center ?

Nowadays we have **Centralized services** 

3) Least Line
	- T1 Speed - 1.54 mbps
	- T3 Speed - 43.736 mbps
		- In Europe : 
			- E1 : 2.048 mbps
			- E3: 34.368 mbps
1) WAN Topologies
	1) Leased lines
	
	3) Frame relay (OLD)
	
	4) ATM
	
	5) **[[MPLS.canvas|MPLS]]** *is dying*
		- Multi Protocol Label Switching
		- THIS IS NOT INTERNET
		- Only our traffic will be allowed to cross this stuff
		- This is Standard of how company branch offices to they corporate office to the data center for a wild now  
		- IT IS PRIVATE
			- Because they create **Virtual circuits** of private network just for you 
			- Multi Protocol ***LABEL*** Switching 
			- Kinda like **VPN** - Virutal Private Network **BUT** there is **NO ENCRYPTION** 
		- It works between **LAYER 2** & **LAYER 3** (2.5) where it gonnna applied a **LABEL** 
		
	1) **[[Metro-Ethernet.canvas|Metro-Ethernet]]**
		- I want CRAZY connexion between Corporate Office and Data Center
		- 1 gbps or 10 gbps
		- P2P (Point to point) connexion 
			- **E-LINE** or **Ethernet Private Line** (EPL)
				- Mostly in the same city 
					- ***METRO*** - Ethernet
				- Point-to-point Ethernet connectivity for organizations with two locations
				- Too expensive to connect difrents offices from diferents cities BUT
			- **E-LAN** or **Ethernet Private LAN** (EP-LAN) 
				- True multipoint connectivity 
				- Transparent WAN extension of their LAN architecture 
				- can connect diferents offices from diferents cities BUT 
				- There is a middle Option :
			- **E-TREE** or **Ethernet Virtual Private Line** (EVPL)
				- connect diferents ***SPOKE*** to one ***HUB***
				- Point-to-multipoint for companies with central office and satellite locations
				
1) **[[Public Internet.canvas|Public Internet]]
	- Using the Public Internet ***WE NEED*** encrypted the connections 
	- we use **VPN** to do that - **Virtual Private Network** 
		-**site-to-site VPN** 
		but its SLOW and it can't **prioritize Traffic** like MPLS does
		QoS - Quality of Service
		BUT MPLS is dying cuz alternative called
	
1) Software-designed - WAN (SD-WAN)


