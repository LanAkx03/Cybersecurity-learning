
1) check our ¨**Public IP Address**
	- WhatIsMyIPaddress
		- IPv4 : 193.121.86.250
		- IPv6 : not detected
	- From it we can now your exact position 
	- From it we can exploit weakness from your network

2) TWO WAY (ez and hard)
	- 1st Way 
		- Open web browser and go to pentest-tool (https://pentest-tools.com)
		- Fast scan your IP address (using nmap)
			1) Scan for open ports 
				1) your ports are like hole/door in your network
				2) your router have **Firewall** but every ports is an hole to connect to the internet
	- 2nd way
		- Create a Linux server (with Linode.com for example)
		- Once created, launch consol
		- type 'root' for logged in
		- type your password
		- type apt-get install nmap -y
			- then 'nmzp - sT <Ip address'
				- it gonna show all analyzed port and which one are open
				- you can also 'nmap --script vuln  <Ip address'
				- 'nmap -sT -O 192.168.1.0/24
					- tell what operating sys. device in your network have
			
3) **To protect** from this : USE A VPN

4) BUT if hacker analyzed your Devices at home (which are using the real Public IP Address they might be able to hack your network)

5) go check your **router** configuration and set up a **Firewall**
	1) For proximus : 192.168.1.1
	2) If u see any open port u can 
		1) 'nmap -sT -p <number of port <Public Ip Address'

6) change default usename and password
7) disable ping to wan or lan 



UUID : Universally unique identifier
			
			-  then 'nmap -sT  <Ip address>	