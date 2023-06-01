# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

### DATE : 26-04-2023

### AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

### ALGORITHM :
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module
in server.
4. Send and receive the message using the send function in socket.

### PROGRAM :
### Client:
```
# Developed by: Gowrisankar.p
# Register No: 212222230041
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
msg=input("Client > ")
s.send(msg.encode())
print("Server > ",s.recv(1024).decode())
```
### Server:
```
# Developed by: Gowrisankar.p
# Register No: 212222230041
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
ClientMessage=c.recv(1024).decode()
c.send(ClientMessage.encode())
```
### OUTPUT :
### Client:
![image](https://github.com/gowrisankarponnusamy/EX-8/assets/119393123/c27a3b96-d946-4d02-9605-55181df8898d)
### Server:
![image](https://github.com/gowrisankarponnusamy/EX-8/assets/119393123/220ea5b9-1ff3-4727-adc7-c6adf49403d0)
### RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
