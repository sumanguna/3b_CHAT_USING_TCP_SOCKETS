
# Ex-3b CREATION FOR CHAT USING TCP SOCKETS
## Register Number:212223240163
## Name: Suman G
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server:
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
## OUTPUT:
### Client:
<img width="936" alt="Screenshot 2024-04-18 at 7 52 07 PM" src="https://github.com/aaron-h-2k5/3b_CHAT_USING_TCP_SOCKETS/assets/144250957/c02236f1-35cf-46d8-8267-900f6eceddfd">

### Server:
<img width="936" alt="Screenshot 2024-04-18 at 7 52 13 PM" src="https://github.com/aaron-h-2k5/3b_CHAT_USING_TCP_SOCKETS/assets/144250957/a3662207-5d22-4e49-b19d-31ff9c738993">

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
