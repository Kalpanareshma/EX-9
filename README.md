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
![EX-09](https://github.com/Kalpanareshma/EX-9/assets/122040453/4cf56973-530a-4c8b-ae72-313875b7fec6)
### CLIENT :
![EX-09 CLIENT](https://github.com/Kalpanareshma/EX-9/assets/122040453/8debd57a-b56e-4466-867c-7d19d83a3afe)






## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
