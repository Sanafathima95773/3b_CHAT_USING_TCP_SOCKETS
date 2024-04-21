# 3b.CREATION FOR CHAT USING TCP SOCKETS
REGISTER NO:212223240145
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8080)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
server:
```
 
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
client
![image](https://github.com/Sanafathima95773/3b_CHAT_USING_TCP_SOCKETS/assets/147084627/64714e9d-aeca-4209-81e8-3d127e01a81d)

server

![image](https://github.com/Sanafathima95773/3b_CHAT_USING_TCP_SOCKETS/assets/147084627/88aa4901-d47f-4a43-8254-5946e26e23ec)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
