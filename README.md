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
SERVER:
~~~
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept()
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())
~~~
## OUPUT
CLIENT:

<img width="850" height="143" alt="Screenshot 2026-05-25 111838" src="https://github.com/user-attachments/assets/a7d9f688-e2f3-4574-a994-e1ae442e1b4b" />


SERVER:

<img width="957" height="299" alt="Screenshot 2026-05-25 111855" src="https://github.com/user-attachments/assets/b259d01c-5f7b-4374-be4c-db597a560f43" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
