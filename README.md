# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

DATE:
```
DATE: 16-03-2023
```
### AIM :
To write a python program to perform stop and wait protocol.


### ALGORITHM :
```
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK 
   signal to client.
6. Stop the program
```

### PROGRAM :
```
Developed By: M Gautham
Reg. No.: 212221230027
```
## Client:
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
 ## Server:
 ```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT :
 client:
 
 ![image](https://github.com/muppirgautham/EX-2/assets/94810884/ff9500e7-4bea-4da3-8207-0da531e1e42c)
 
 Server:
 
 ![image](https://github.com/muppirgautham/EX-2/assets/94810884/5b0982ca-a554-4e89-9596-49c861b86c08)


## RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.





