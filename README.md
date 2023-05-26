### EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

### DATE:15-03-2023

### AIM :

To write a python program to perform stop and wait protocol

### ALGORITHM :

1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to        client.
6. Stop the program

### PROGRAM :

### CLIENT :

Developed by : A.ARUVI

Register Number : 212222230014
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

### SERVER :

 Developed by :A.ARUVI

Register Number : 212222230014
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Received".encode())
```

### OUTPUT :

### CLIENT :

![image](https://github.com/Anandanaruvi/EX-2/assets/120443233/15a6c033-f9af-47e4-87fd-9a826911d3cc)

### SERVER :

![image](https://github.com/Anandanaruvi/EX-2/assets/120443233/5dd1fdd9-5be8-459d-ae46-592f5dca7a92)

### RESULT :

Thus, python program to perform stop and wait protocol was successfully executed.
