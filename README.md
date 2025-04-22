# 2a_Stop_and_Wait_Protocol
## AIM 
## NAME:DHARSHAN R
## REGISTER NUMBER : 212224230060
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
CLIENT 
import socket 
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5) 
c,addr=s.accept() 
while True: 
    i=input("Enter a data: ") 
    c.send(i.encode()) 
    ack=c.recv(1024).decode() 
    if ack: 
        print(ack) 
        continue 
    else: 
        c.close() 
        break 
SERVER 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())
```
   
## OUTPUT
![WhatsApp Image 2025-04-22 at 21 35 12_8a0e9b9f](https://github.com/user-attachments/assets/99838509-c2d5-481d-aabf-ede9a2eacc52)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
