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

SERVER:
~~~
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
~~~
CLIENT:
~~~
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
~~~
## OUPUT
SERVER:

<img width="937" height="238" alt="image" src="https://github.com/user-attachments/assets/04a3672f-71be-4e1f-91cd-e2c3034dc14c" />


CLIENT:

<img width="942" height="235" alt="image" src="https://github.com/user-attachments/assets/5dbd5a5b-7de9-4a62-b8bb-117aeeac23d4" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
