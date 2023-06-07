# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

DATE :26-04-2023

# AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

# ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server.
4.Send and receive the message using the send function in socket.
```
# PROGRAM :
```
Developed By: Parshwanath M
Register Number: 212221230073
```
## CLIENT :
```

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER :
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
# OUTPUT :
## CLIENT :
![#8](https://github.com/parsh2004/EX-8/assets/95388047/ebf755dd-4dc5-4862-9ac7-de1d82072f04)


## SERVER :
![##8](https://github.com/parsh2004/EX-8/assets/95388047/9508509b-b45b-4873-a904-df76dc39e384)


# RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
