# 2a_Stop_and_Wait_Protocol
NAME:DHANA LAKSHMI A

REG NO:212223040033
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## client
```
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
```
## server
```
import socket   
s=socket.socket()   
s.connect(('localhost',8000))   
while True:   
print(s.recv(1024).decode())   
s.send("Acknowledgement Recived".encode())
```
## OUTPUT
## client
![image](https://github.com/iniyasri4464/2a_Stop_and_Wait_Protocol/assets/152419072/d5c1b3e2-18ac-425d-a246-d4f3791f70c1)
## server
![image](https://github.com/iniyasri4464/2a_Stop_and_Wait_Protocol/assets/152419072/6866a1a4-5780-4ac6-8258-6d408e13f5c0)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
