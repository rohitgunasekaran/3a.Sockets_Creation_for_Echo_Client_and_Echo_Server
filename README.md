# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### NAME:G.ROHIT
### REGISTER NUMBER:2122222240083
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CILENT :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```
## SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())

```
## OUPUT:
### CLIENT:

<img width="700" alt="image" src="https://github.com/rohitgunasekaran/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/119404546/4d1d0b3c-f257-4c6a-b1c4-079eb0c6ba08">

### SERVER:

<img width="700" alt="image" src="https://github.com/rohitgunasekaran/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/119404546/66df9fca-f2e6-47f2-8387-f49da73cebce">

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
