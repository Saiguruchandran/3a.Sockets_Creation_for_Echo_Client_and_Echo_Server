# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### NAME: SAIGURUCHANDRAN
### REG NO:212223240143
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
### CLIENT
```

import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUPUT
### CLIENT:
![WhatsApp Image 2024-05-08 at 10 36 49_1bad6760](https://github.com/Saiguruchandran/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870946/bdbc6916-dbf0-4d94-bb41-e87e5ce0db80)

### SERVER:
![WhatsApp Image 2024-05-08 at 10 37 08_f2eb7201](https://github.com/Saiguruchandran/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144870946/68720c61-65ea-4bd5-8fec-b44fc22fbfd1)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
