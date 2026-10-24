# Date :24-10-2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration
# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
<img width="1600" height="1000" alt="WhatsApp Image 2026-10-24 at 9 59 54 AM" src="https://github.com/user-attachments/assets/0b51ad8c-c9ee-4eba-8738-7840d3177baa" />

________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>
<img width="1600" height="1000" alt="WhatsApp Image 2026-10-24 at 10 22 14 AM" src="https://github.com/user-attachments/assets/d3c07f60-5764-4deb-aec0-65a91db8408e" />
<img width="1600" height="1000" alt="WhatsApp Image 2026-10-24 at 10 22 35 AM" src="https://github.com/user-attachments/assets/44d70b3c-899a-4ff9-a995-da6bfa19b7d2" />
<img width="1600" height="1000" alt="WhatsApp Image 2026-10-24 at 10 23 10 AM" src="https://github.com/user-attachments/assets/14b135e5-a4a9-4fb7-8578-7e7f14812c5d" />
<img width="1600" height="1000" alt="WhatsApp Image 2026-10-24 at 10 23 25 AM" src="https://github.com/user-attachments/assets/29acf964-d065-41a7-864b-07be76b5d520" />
<img width="1600" height="1000" alt="WhatsApp Image 2026-10-24 at 10 21 25 AM" src="https://github.com/user-attachments/assets/610b1546-c3a6-4491-9553-422e3c863acf" />
________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

