
### Scenario 1: JWT Authentication Bypass via Unverified Signature

To begin with the practical side of JWT attacks, I started with PortSwigger’s lab on **JWT authentication bypass via unverified signature**. This lab demonstrates a common implementation flaw where the server accepts JWTs without validating their signature, allowing modified tokens to be trusted. The objective of the lab is to abuse this weakness, gain access to the admin panel

<img width="1153" height="831" alt="image" src="https://github.com/user-attachments/assets/8be55a3f-ea83-4027-b9c2-023e525206da" />


Click on ***Access THE LAB*** to start the lab

login to My account



<img width="1612" height="742" alt="image" src="https://github.com/user-attachments/assets/201969da-b2a0-4da4-9e7b-7f88e51319f6" />



***login to My account***

<img width="1668" height="558" alt="image" src="https://github.com/user-attachments/assets/e1519ee8-fe27-4f1b-88a9-bf2af9b76e8b" />


<img width="1616" height="565" alt="image" src="https://github.com/user-attachments/assets/1a21ba85-edd9-4cc5-b5e7-1e7742dd0f6a" />




<img width="1777" height="331" alt="image" src="https://github.com/user-attachments/assets/c67e9460-0a10-47f5-8019-768efd7ab5d4" />


We successfully logged in, now let’s refresh the page and intercept it using Burpsuite Interceptor& poxy tab

and request send to repeater

<img width="1397" height="726" alt="image" src="https://github.com/user-attachments/assets/52bd75bc-ef82-46b1-a592-97f96e8b79b4" />


If you observe carefully, every request contains a session token that is sent to the server and the token appears to be in JWT format


There are many tools to decode JWT tokens such as JWT Editor
<img width="1616" height="632" alt="image" src="https://github.com/user-attachments/assets/38da31be-4b76-4ea3-b931-1e1d12a2c274" />


<img width="1457" height="811" alt="image" src="https://github.com/user-attachments/assets/4a195cad-3121-4b6f-b635-7d341b60d0da" />



<img width="1386" height="668" alt="image" src="https://github.com/user-attachments/assets/40a1b2d8-5fbb-436e-9ea6-0d2ab831f734" />




<img width="1440" height="721" alt="image" src="https://github.com/user-attachments/assets/a5faa132-9876-41a0-8e6d-3c901e0aa359" />

<img width="1802" height="682" alt="image" src="https://github.com/user-attachments/assets/51b83421-ae9d-4774-a6f1-70b2e7f9d3b8" />


