# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name: Mugil Raj S A
## Register No : 212223220062
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server:
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

## OUTPUT
## client:

![Screenshot 2024-05-14 183820](https://github.com/MugilRaj1105/3b_CHAT_USING_TCP_SOCKETS/assets/154905390/2c9acdf1-1069-46d8-aa82-302cc59fe174)

## server:

![Screenshot 2024-05-14 183838](https://github.com/MugilRaj1105/3b_CHAT_USING_TCP_SOCKETS/assets/154905390/e55f99b6-313f-4b03-bfee-7ad3722571a1)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
