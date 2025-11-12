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
```
python
CLIENT: 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
msg=input("Client > ") 
s.send(msg.encode()) 
print("Server > ",s.recv(1024).decode())

SERVER: 
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
## Client: <img width="893" height="269" alt="Screenshot 2025-11-12 105926" src="https://github.com/user-attachments/assets/a0225574-59a0-40f2-b367-fa1411ae5490" />

## Server:<img width="845" height="261" alt="Screenshot 2025-11-12 105938" src="https://github.com/user-attachments/assets/acca3b66-e963-4dc8-a31f-ef754c65a5b2" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
