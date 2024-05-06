# 2(A) _Stop_and_Wait_Protocol

### Name: Oswald Shilo
### Reg No: 212223040139

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

##Client
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
##Server
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
## OUTPUT

### Client

![image](https://github.com/YASHWINISEC/2a_Stop_and_Wait_Protocol/assets/139361633/18a671df-2999-4954-ba0d-7aa058c190c3)

### Server

![image](https://github.com/YASHWINISEC/2a_Stop_and_Wait_Protocol/assets/139361633/ca45b27c-fe77-4b74-b13c-1d4113c5bae4)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
