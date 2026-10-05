# LuCI firewall configurations

In this section I will discuss the configurations of the routers firewall in LuCI. In the network firewall settings, under general setting was a section called "zones". This section displayed the input, output, and forwarding rules of the LAN, WAN, and guest zones. Below is a screen shot showing these settings.

- Picture 1:

  <img width="1500" height="382" alt="Firewall forwarding" src="https://github.com/user-attachments/assets/3e3dc7a7-a69f-4e4e-89ab-902a8a16a46f" />

### Figure 1: What this shows is that all LAN to WAN packet forwarding is accepted.


### Figure 2: This shows that all traffic attempting to pass through the WAN side is rejected or dropped. Any traffic output from the WAN side is accepted. 


### Figure 3: This shows that device connected to a guest network outside the WAN cannot send traffic into the WAN. A Guest network inside the WAN is allowed to send Traffic outbound from the WAN.

## LuCI traffic rules 

