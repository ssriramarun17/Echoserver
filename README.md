# Echoserver
Echo server and client using python socket

DEVELOPED BY: SRIRAM ARUN S

REGISTER NUMBER: 212225040429

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
```
SERVER CODE:
# echo-server.py


import socket


HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)


with socket.socket(socket.AF_INE
T, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)


```
CLIENT CODE:
```
# echo-client.py


import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)


print(f"Received {data!r}")


```

## OUTPUT:
<img width="1911" height="1072" alt="Screenshot 2026-10-29 173256" src="https://github.com/user-attachments/assets/9e5483e5-5baa-4b04-9438-61a4a88404d6" />
<img width="1917" height="1077" alt="Screenshot 2026-10-29 173313" src="https://github.com/user-attachments/assets/a3dc662b-28fd-4b64-8014-213aa738ae01" />




## RESULT:
The program is executed successfully
