# Network Setup

## Router
**Model:** Cisco 1841

## Switch 0
**Model:** Cisco 2960-24TT  
**Devices connected:**
- **Server (PT Server0):** IP Address: `168.90.0.1`
- **PC (PC-PT PC0):** IP Address: `168.90.0.3`
- **PC (PC-PT PC1):** IP Address: `168.90.0.4`
- **Laptop (Laptop-PT Laptop0):** IP Address: `168.90.0.5`
- **PC(PC-PT PC5):** IP Address:`168.90.0.6`

## Switch 1
**Model:** Cisco 2960-24TT  
**Devices connected:**
- **Server (PT Server1):** IP Address: `210.3.14.2`
- **Server (PT Server2):** IP Address: `210.3.14.3`
- **PC (PC-PT PC2):** IP Address: `210.3.14.4`
- **PC (PC-PT PC6):** IP Address: `210.3.14.5`

DHCP Configuration on Router:

To enable DHCP on the router and allow it to dynamically assign IP addresses to devices, the following steps were performed:
	1.	Exclude IP Address Range for Static Devices:
	•	The IP address range 192.168.1.1 - 192.168.1.10 was excluded from the DHCP pool to reserve these IPs for static devices (such as servers).
	2.	Create the DHCP Pool:
	•	A DHCP pool named “LAN” was created to handle IP address assignments for devices that connect to the router.
	3.	Define the Network Range:
	•	The DHCP pool was configured to assign IP addresses in the range 192.168.1.0 - 192.168.1.255, with a subnet mask of 255.255.255.0.
	4.	Set the Default Gateway:
	•	The router’s IP address 192.168.1.1 was set as the default gateway for the network, so devices can route their traffic correctly.
	5.	Set the DNS Server:
	•	The DNS server was set to Google’s DNS server 8.8.8.8, which helps devices resolve domain names into IP addresses.