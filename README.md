# APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

# EXP: 9

# DATE:03-05-2023

# AIM:
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM:
# Client:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
server
4. Send and receive the message using the send function in socket.
# PROGRAM:
# CLIENT:
```python3
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
  ```
# SERVER:
```python3
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   print("Client > ",ClientMessage)
   msg=input("Server > ")
   c.send(msg.encode())
```
   
# CLIENT OUTPUT : 
![image](https://github.com/SudharsanamRK/EX-9/assets/115523484/99e374d6-1340-4373-8763-15abc9afc439)

# SERVER OUTPUT :
![image](https://github.com/SudharsanamRK/EX-9/assets/115523484/c95b5a97-cf96-4e90-9bd5-22fdc7b3aa3b)


# RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully
created and executed.
