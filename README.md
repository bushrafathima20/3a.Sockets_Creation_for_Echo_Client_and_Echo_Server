# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client.py:
```
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
## Server.py
```
import socket 
s=socket.socket() 
s.connect(('localhost',9000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUTPUT
## Client.py:
<img width="727" height="327" alt="Screenshot 2026-05-21 192118" src="https://github.com/user-attachments/assets/a198a51f-63c5-44cb-b2ef-e37113a85b93" />

<img width="711" height="150" alt="Screenshot 2026-05-21 192151" src="https://github.com/user-attachments/assets/48451a6f-a586-40aa-acc1-0ebb2dc5e4c4" />

## Server.py:
<img width="535" height="227" alt="Screenshot 2026-05-21 192249" src="https://github.com/user-attachments/assets/7e15a0fd-ab37-4a13-84b3-e643dd55bcb6" />

<img width="515" height="203" alt="Screenshot 2026-05-21 192316" src="https://github.com/user-attachments/assets/4656a41e-e922-4dfe-b1e1-02a408badd22" />

## Developed By: BUSHRA FATHIMA I
## Register Number: 212225040051

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
