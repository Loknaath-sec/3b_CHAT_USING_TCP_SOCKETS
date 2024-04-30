# 3b.CREATION FOR CHAT USING TCP SOCKETS
### Name: LOKNAATH P
### Register Number: 212223240080
## AIM:
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Client
```python
import socket
s=socket.socket()
s.connect(('localhost',4000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```
### Server
```python
import socket
s=socket.socket()
s.bind(('localhost',4000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUPUT:
### Client
![image](https://github.com/Loknaath-sec/3b_CHAT_USING_TCP_SOCKETS/assets/145742558/37890b5e-5996-4d39-8bd0-b844e15d3268)

### Server
![image](https://github.com/Loknaath-sec/3b_CHAT_USING_TCP_SOCKETS/assets/145742558/37bf0b79-6d87-4556-997a-2cb258531b89)

## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
