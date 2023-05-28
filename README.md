# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE :

## AIM :
        To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
          1.Start the program.
          2.Get the frame size from the user.
          3.To create the frame based on the user request.
          4.To send frames to server from the client side.
          5.If your frames reach the server, it will send ACK signal to client otherwise it will send NACK signal to client.
          6. Stop the program.

## PROGRAM :
```
Developed by JANANI.S
Register Number:212222230049

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
````

## OUTPUT :

CLIENT:

![6client](https://github.com/JananiSoundararajan/EX-9/assets/119477549/73b2c8c0-d7fb-4ac9-9915-49fbe9c14c38)

SERVER:

![6server](https://github.com/JananiSoundararajan/EX-9/assets/119477549/3fcc4b68-7808-486b-9b15-dd952bea1347)

## RESULT :

         Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
