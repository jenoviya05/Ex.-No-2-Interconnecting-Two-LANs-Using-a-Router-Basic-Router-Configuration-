# Date : 27.10.26
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective :
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required :
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram :
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180406" src="https://github.com/user-attachments/assets/514284d8-f01d-4733-9943-b2cce2392123" />


________________________________________
# IP Addressing Table : 
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure :
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
# Commands Used (Router CLI) :
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
# Output (Screenshots) : 
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>

## CONFIGURATION :

## LAN 1

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180131" src="https://github.com/user-attachments/assets/6c187505-2ecc-40d6-8b70-557156ea2d03" />

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180140" src="https://github.com/user-attachments/assets/1de6c055-900d-4201-bf1c-c6eca7e66c95" />

<img width="1908" height="1077" alt="Screenshot 2026-10-27 180148" src="https://github.com/user-attachments/assets/1eef8265-699e-47ef-a6e6-a149b3d21044" />

## LAN 2

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180157" src="https://github.com/user-attachments/assets/cd71018c-32e0-4d03-a92c-842d41283b83" />

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180213" src="https://github.com/user-attachments/assets/d80ffbc2-1365-4cb6-a709-e59e965b017e" />

<img width="1913" height="1077" alt="Screenshot 2026-10-27 180246" src="https://github.com/user-attachments/assets/1e7e8b5b-9cbd-4b84-804c-c9b42a33c7d8" />

## SWITCH

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180419" src="https://github.com/user-attachments/assets/be354103-8242-41c2-9661-82f962990347" />

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180429" src="https://github.com/user-attachments/assets/23052230-5368-47e8-9d35-52fdd082d0b3" />

## ROUTER

<img width="1916" height="1078" alt="Screenshot 2026-10-27 180438" src="https://github.com/user-attachments/assets/82e13cd0-9826-4dcb-b3f1-4ce5787553b3" />

## PING :

## LAN1 :
<img width="1917" height="1078" alt="Screenshot 2026-10-27 180541" src="https://github.com/user-attachments/assets/8f004c75-4688-4ec9-9514-86d57144d4db" />

<img width="1916" height="1078" alt="Screenshot 2026-10-27 180608" src="https://github.com/user-attachments/assets/206a9d1e-5489-4263-875c-eaacdf839c21" />

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180635" src="https://github.com/user-attachments/assets/823df395-b33a-453f-a863-dfa3b87e6022" />


## LAN2 :
<img width="1917" height="1078" alt="Screenshot 2026-10-27 180731" src="https://github.com/user-attachments/assets/8bc80d38-7413-420e-95d4-291b84b0dd22" />

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180758" src="https://github.com/user-attachments/assets/8f988617-6b3d-4920-99c3-dd2b2f44c13a" />

<img width="1917" height="1078" alt="Screenshot 2026-10-27 180826" src="https://github.com/user-attachments/assets/db04e63c-484f-429d-a342-189283a09f9d" />

## BOTH LAN :
<img width="1842" height="1040" alt="Screenshot 2026-10-27 181613" src="https://github.com/user-attachments/assets/045220c8-7739-4d56-b9d3-c4a9e1040e9c" />

<img width="1917" height="1078" alt="Screenshot 2026-10-27 181645" src="https://github.com/user-attachments/assets/3ea957e7-cd86-4934-abc4-d0b86d69b57f" />


## SWITCH CONFIG :

## SWITCH 0
<img width="1917" height="1078" alt="Screenshot 2026-10-27 180930" src="https://github.com/user-attachments/assets/559448d0-ed9b-49d0-a9da-808985db9839" />

## SWITCH 1
<img width="1913" height="1077" alt="Screenshot 2026-10-27 180920" src="https://github.com/user-attachments/assets/a0347bc1-fdf7-4bc7-9a77-3de636c12118" />







________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

