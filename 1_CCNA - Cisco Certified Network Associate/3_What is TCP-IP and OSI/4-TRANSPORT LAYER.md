
Packaging the different date that going to be send

It choose the **shippping carrier** (Like BPost, GSL, Fedex...) and the PROTOCOL

1) **shipping carrier**
	- TCP (TRANSMISSION CONTROL PROTOCOL) - reliable
		- Wait for a response that u get the 1st info before sending the 2nd info. If it doesnt, he will send it again
		- 3-WAY HANDSHAKE
			- 1st - SYN message (YT to PC)
			- 2nd - SYN ACK message (PC to YT)
			- 3rd - ACK message (YT to PC)
		- 
	- UDP (QUIC) - faster
		- Launching a video on YT used UDP (QUIC) instead of TCP but why ?
		- For video game it is the same : if your connexion drop out for a sec. if we used TCP, it will send it back to your previous position (sending missing data). With a video its going to be like missing a frame (a sec of video) and that second will be send 3 sec. after. In real-time flux it is gonna be annoying 
	- 17.197.191.167:443 
		- Is the IP address we want to go (https://youtube.com) with the port 443 (HTTPS protocol)
			- 443 (port) : HTTPS
			- 21 (port): FTP
			- 22 (port): SSH
			- 3389 (port): RDP
		- 57095 is my own (ephemeral) port