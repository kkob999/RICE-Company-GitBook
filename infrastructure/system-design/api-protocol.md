# API Protocol

[Baangkok Vanijyananda](https://app.gitbook.com/u/5XBQ6zvmsFdF62v6lDsQg7C7olW2 "mention")

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption><p>gRPC and REST usage</p></figcaption></figure>

## gRPC

**gRPC** เป็น **Remote Procedure Call (RPC) framework** ประสิทธิภาพสูงที่สามารถรันใน environment ไหนก็ได้ gRPC ใช้ **Protocol Buffer** ซึ่งทำให้ application ที่เขียนด้วยภาษาต่างกันสามารถสื่อสารกันได้ นอกจากนี้ RPC API ยังเร็วกว่า REST เนื่องจาก RPC request ทำงานเหมือนกับการเข้าไป call function ของ server โดยตรง

* gRPC จะถูกใช้ในการสื่อสารกันระหว่าง backend services ภายใน ทำให้เราสามารถใช้ภาษาที่เหมาะสมในการ implement service ต่างๆได้
* RPC เร็วกว่า REST นั่นคือ backend ที่สร้างด้วย RPC ถ้าโค้ดเหมือนกันแล้ว จะประสิทธิภาพเร็วกว่านั่นเอง

***

**gRPC** is a modern open source high performance **Remote Procedure Call (RPC)** framework that can run in any environment. gRPC uses **Protocol Buffer** which makes applications implemented using different languages be able to communicate with each other. An RPC API is also faster than REST  since an RPC request behaves like the client is directly calling the function from the server.

* gRPC will be used between our internal backend services. This allows applications to be implemented using the most suited language.
* &#x20;RPC is faster that REST; allowing better performance within our microservice systems.

## REST

**RESTful API** เป็นสถาปัตยกรรมการสร้าง API ชนิดหนึงซึ่งใช้ HTTP request ในการเข้าถึงข้อมูล

* REST จะถูกใช้ในการสื่อสารระหว่างผู้ใช้กับ backend server ของเรา

***

**RESTful API** is an architectural style for an application program interface (API) that uses HTTP requests to access and use data.&#x20;

* REST will be used when the frontend client is accessing our backend.
