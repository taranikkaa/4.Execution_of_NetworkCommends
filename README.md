 4.Execution_of_NetworkCommands
 TARANIKKA A
 212223220115
 B.TECH (IT)
 
 AIM :Use of Network commands in Real Time environment
 Software : Command Prompt And Network Protocol
 Analyzer
<BR>Procedure: To do this EXPERIMENT- follows these steps:
 In this EXPERIMENT- students have to understand basic networking commands e.g
 cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs
 using a network protocol analyzer
 All commands related to Network configuration which includes how to switch to privilege
 mode
 and normal mode and how to configure router interface and how to save this
 configuration to
 flash memory or permanent memory.
 This commands includes
 • Configuring the Router commands
 • General Commands to configure network
 • Privileged Mode commands of a router
 • Router Processes & Statistics
 • IP Commands
 • Other IP Commands e.g. show ip route etc
 ## program
 ## ping command
 ## client
 
``` import socket 
 
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
        
## server
 ```
py

 import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

    ip=input("Enter the website you want to ping ")

    s.send(ip.encode())

    print(s.recv(1024).decode())
  ```
 ## Tranceroute command

```
py
from scapy.all import
target = ["www.google.com"]
result, unans = traceroute(target,maxttl=32)
print(result,unans)
```
Output

## Ping command

## client
![image](https://github.com/aswethaashok/4.Execution_of_NetworkCommends/assets/149987410/f38cc423-7fbc-4d7c-84ad-9955709037c4)

## server
![image](https://github.com/aswethaashok/4.Execution_of_NetworkCommends/assets/149987410/ef30a767-f917-494b-b793-41b1c66a66e4)

## tranceroute command
![image](https://github.com/aswethaashok/4.Execution_of_NetworkCommends/assets/149987410/8dc43da5-86ea-4418-837f-5d0a14f9a065)

## Result
Thus Execution of Network commands Performed
