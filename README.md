# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
client 
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
server
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT

client

![WhatsApp Image 2025-04-08 at 11 23 37_de985cbe](https://github.com/user-attachments/assets/93d508ed-a179-48e3-8263-370e618b4db4)

server

![WhatsApp Image 2025-04-08 at 11 23 51_eda7ae7a](https://github.com/user-attachments/assets/1d076a37-a134-4ebf-b2d2-84a0dead6d7f)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
