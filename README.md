# 2a_Stop_and_Wait_Protocol
# NAME:k.pujitha
# REG NO :212223240074
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
```
# CLIENT:
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

# SERVER
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
print(s.recv(1024).decode())
s.send("Acknowledgement Recived".encode())
```
## OUTPUT
# CLIENT:
![Screenshot 2024-09-14 184429](https://github.com/user-attachments/assets/d6c4eddd-7d94-42c5-9abc-ec0e8907ee6d)
# SERVER: 
![Screenshot 2024-09-14 184445](https://github.com/user-attachments/assets/113b2aff-8af0-40f5-b5ee-f5d30c8b702e)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
