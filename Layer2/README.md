# **Layer 2 flows**

This folder contains flows related to Layer 2  

This is the sample toplogy:![picture](/topo.png)     

Flow 'Deny_ethernet_src':  

This flow blocks all ipv4 communications to destination with MAC address specified in the 'ethernet-destination' field.  
This flow can be pushed on switches where the packets need to be dropped.  

Flow 'Deny_ethernet_srcdest':  

This flow blocks all ipv4 communcations between the source and destination specified in 'ethernet-source' and 'ethernet-destination' field.  
Flow can be pushed on switches where the packets need to be dropped.



