# **Miscellaneous test cases**

This folder contains miscellaneous flows.  


This is the sample topology: ![picture](/topo.png).  

## Flow 'Allow_AfterBlacklist_usingL3Address':  
Implement universal blacklist. Permit all traffic between Host A and Host D using Layer 3 addresses. Verify using random ICMP, UDP and TCP ports.  

**verification for UDP** : use Ping utility from mininet console to check ping results.  

**verification for TCP**: use netcat to start a server and connect from client. For netcat an xterm console will be needed from each of the hosts.  
from **mininet console**.  
type in   
```
xterm host  
```
where host can be h1,h2,h3,h4 (for this topology).  

**For tcp server**:
in the console where server has to be setup type in:  
```
nc -l ip port  
```
where *ip-> ip* of *host* and *port-> port number* on which server has to be setup.  

**for udp server**: 
```
nc -lu ip port  
```

**for client**:  
```
echo "hello" | nc ip port  
```
where ip-> ip of server , port -> port number on which server is running.  

Depending upon deny/permit flow,one can verify if the communication goes through.  


## Flow 'Deny_TCP_h4_h1':
This flow denies all **TCP** communications from **Host4** to **Host1**.  

For verification use steps mentioned above.  

## Flow 'ICMP_Allow_after_UnivBlacklist':

This flow allows only **ICMP** communications after a **Universal Blacklist**.  

## Flow 'ICMPallow_h1_h4':

This flow allows ICMP communications between **Host 4** and **Host 1** after **Universal Blacklist**.  

## Flow 'TCPallow_after_univBlacklist':

This flow allows TCP communications after a **Universal Blacklist**.  

## Flow 'Universal Blacklist':

This flow doesnt allow any communication and drops all packets.

## Flow wildcard_permit_ip

This flow demonstrates usage of wildcard in Ip addresses.











