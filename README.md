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
```python
import socket

s=socket.socket()
s.connect(('localhost',8001))

while True:
    d=input("Enter message: ")
    if d=="exit": break
    s.sendall(d.encode())
    print("Echo:",s.recv(1024).decode())

s.close()
```

## Server.py:
```python
import socket

s=socket.socket()
s.bind(('localhost',8001))
s.listen(1)
c,a=s.accept()

while True:
    d=c.recv(1024).decode()
    if not d: break
    print("Received:",d)
    c.sendall(d.encode())

c.close()
```


## OUPUT
<img width="1741" height="1029" alt="image" src="https://github.com/user-attachments/assets/d1c83be5-783d-4014-8e60-2a24dae2b700" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
