# LuCI firewall configurations

In this section I will discuss the configurations of the routers firewall in LuCI. In the network firewall settings, under general setting was a section called "zones". This section displayed the input, output, and forwarding rules of the LAN, WAN, and guest zones. Below is a screen shot showing these settings.

- Picture 1:

  <img width="1500" height="382" alt="Firewall forwarding" src="https://github.com/user-attachments/assets/3e3dc7a7-a69f-4e4e-89ab-902a8a16a46f" />

- Figure 1: What this shows is that all LAN to WAN packet forwarding is accepted.


- Figure 2: This shows that all traffic attempting to pass through the WAN side is rejected or dropped. Any traffic output from the WAN side is accepted. 


- Figure 3: This shows that device connected to a guest network outside the WAN cannot send traffic into the WAN. A Guest network inside the WAN is allowed to send Traffic outbound from the WAN.

## LuCI traffic rules 

The firewall traffic rules act above the default zone rules. They allow exceptions to be made for specific protocols and services passing through the network.
Some of the firewall traffic rules found within LuCI are as follows.

- Allow-DHCP-Renew: Allows the Flint router to self renew its own IP address via DHCP
- Allow-IGMP: permits IGMP traffic
- Allow-ISAKMP: Permits ISAKMP. This protocol is used in encryption for negotiating how the encryption keys are to be used.
- wan_drop_leaked_dns: Prevents un-encrypted DNS traffic from being sent out to an external DNS server.

These are just a few of the traffic rules. Certain rules such as wan_drop_leaked_dns were not enabled by default, so i had to enable them within LuCI. 
Below is a screenshot showing some of the fire wall traffic rules.

<img width="1200" height="900" alt="Screenshot 2026-10-06 075137" src="https://github.com/user-attachments/assets/7952362e-a6e1-4d83-ae01-f3b5faff847b" />

