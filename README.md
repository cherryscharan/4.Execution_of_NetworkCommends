# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Program
## Client:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
## Server:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```

## Output
## PING COMMAND:
## Client:
![WhatsApp Image 2024-05-10 at 11 38 50_33ad3f92](https://github.com/cherryscharan/4.Execution_of_NetworkCommends/assets/146930617/16f72c98-9d80-49c0-81cb-d1cff3bfa4ff)

## Server:
![WhatsApp Image 2024-05-10 at 11 38 53_76c7ece1](https://github.com/cherryscharan/4.Execution_of_NetworkCommends/assets/146930617/f82a0c2d-a6e3-406d-a4ab-3692941bfa39)

## TRACERT COMMAND:
![WhatsApp Image 2024-05-10 at 11 38 56_40601b35](https://github.com/cherryscharan/4.Execution_of_NetworkCommends/assets/146930617/96d62bc7-ef26-4096-b49e-a7e791ea3126)



## Result
Thus Execution of Network commands Performed
