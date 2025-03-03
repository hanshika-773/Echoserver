# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

## server.py
```
import socket
HOST , PORT = '127.0.0.1',65432
with socket.create_server((HOST,PORT)) as s:
    conn , addr = s.accept()
    with conn:
        print(f'connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
## client.py
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Thenukishore, 2122223100059')
    print(f'Received: {s.recv(1024)!r}')
```
## OUTPUT:
![Screenshot 2025-03-03 141404](https://github.com/user-attachments/assets/448dfd8a-54b6-4024-a2a2-3ef94eae4808)

![Screenshot 2025-03-03 141056](https://github.com/user-attachments/assets/4a211b8e-b813-4e1f-b00b-d824ff025b81)

## RESULT:
The program is executed successfully
