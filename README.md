# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE : 04-05-2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.


## ALGORITHM :
### STEP 1: Start the program.
### STEP 2: Get the frame size from the user.
### STEP 3: To create the frame based on the user request.
### STEP 4: To send frames to server from the client side.
### STEP 5: If your frames reach the server, it will send ACK signal to client otherwise it will sendNACK signal to client.
### STEP 6: Stop the program


## CLIENT PROGRAM :
### Developed : Kalpana S
### Reg no : 212222040069
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
    
### SERVER PROGRAM :
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



## OUTPUT :
### SERVER :
![ex09 server output](https://github.com/Kalpanareshma/EX-9/assets/122040453/4489d5c6-20ad-45e8-a518-b906ead956fd)
### CLIENT :
![ex09 client output](https://github.com/Kalpanareshma/EX-9/assets/122040453/5e8a749e-d051-44b6-8544-fa41b2ea0bc4)

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
