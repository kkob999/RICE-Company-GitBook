# Chat System

## Chat System

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

ความท้าทายของ chat system คือการแชทจะต้องเป็นแบบ real-time นั่นคือข้อความจะต้องปรากฎทันที เพื่อที่จะทำเช่นนั้น เราออกแบบระบบแชทที่ประกอบไปด้วย server และ micro service หลายตัว

***

The challenge of a chat system is that the chat must be real time, i.e., the messages must appear instantly. To achieve that, we designed a chat system consisting of multiple servers and micro-services.

### Service Discovery

ผู้ใช้จะต้อง authenticate ผ่าน API Gateway และ API ของ "Chat Participants" ที่เกี่ยวข้อง (User / Admin / Shop)

จากนั้น Service Discovery จะค้นหา Chat Server ที่ใกล้กับผู้ใช้ที่สุด และแจ้งให้ผู้ใช้เชื่อมต่อกับ Chat Server นี้

***

First, the client will authenticate via API Gateway and their corresponding "Chat Participants" API (User / Admin / Shop).

Then Service Discovery will find the Chat Server that is closest to the client and tell the client to connect to this Chat Server.

### Chat Server

ผู้ใช้ จะเชื่อมต่อกับ Chat Server ด้วย WebSocket protocol ซึ่งสามารถสื่อสาร 2 ทางได้ นั่นคือ Chat Server สามารถ "push" message ใหม่ไปสู่เครื่องของผู้ใช้ได้โดยตรงโดยที่ผู้ใช้ไม่ต้องคอย "poll" message ใหม่

เมื่อเชื่อมต่อกับ Chat Server แล้ว จะทำการ query ประวัตแชทจาก Chat Database

เมื่อจะส่ง message ตัว message จะถูกส่งไปที่ Message Queue จากนั้น Main Chat API จะ consume message นั้นเพื่อนำไปเก็บไว้ใน Chat Database และถ้า Chat Server ของผู้รับ message นั้น online อยู่ Chat Server นั้นจะ consume message แล้ว "push" message ไปที่ผู้รับซึ่งทำให้ข้อความใหม่ปรากฏขึ้นมาทันที

***

The Chat Server provides WebSocket connection to the client, which allows  2-way communication; the Chat Server can "push" new messages directly to the client without the client having to "poll" for new messages.

When connecting to the Chat Server, it will query the chat history from Chat Database.

When sending a message, the message gets sent to the Message Queue. The Main Chat API will then consume that message and store it in the Chat Database. If the Chat Server of the message receiver is online, the Chat Server will also consume that message and "push" it to the receiver client so the new message pops up immediately.

### Message Queue - Kafka

เราจะใช้ Kafka เป็น Message Queue ของ chat system ของเรา

Kafka คือ distributed message queue ที่สามารถจัดการข้อมูลในประมาณมากๆได้แบบ real-time มีความทนทานต่อการล่ม และสามารถ scale ได้ง่าย เราสามารถมีหลาย node มาช่วยกันรัน Kafka service เดียวได้

Kafka จะการันตีว่าไม่มี message ที่สูญหายระหว่างทางเมื่อ consumer ไม่สามารถ process message ได้ทัน

***

Kafka will be used as the Message Queue in the chat system.

Kafka is a distributed message queue which excels in handling high volumes of real-time data streams with fault tolerance and scalability. We can have multiple nodes running Kafka together as one service.&#x20;

Kafka will ensure no message is lost when consumers are not able to consume messages as fast as the producers can produce.

### Presence Server

เมื่อผู้ใช้เชื่อมต่อมายัง Chat Server ก็จะทำการเชื่อมต่อไปยัง Presence Server ด้วย Presence Server ทำหน้าที่เฝ้าดูว่าผู้ใช้กำลังเปิดหน้า chat อยู่ ณ ขณะนั้นหรือเปล่า ข้อมูลนี้จะถูกเก็บไว้ที่ Chat Database ด้วย

***

When client connects to a Chat Server, they will also be connected to a Presence Server. The Presence Server will determine if the client is actively have the chat page open or not. This information will also be stored in the Chat Database

### Main Chat API

Main Chat API มีหน้าที่เก็บข้อมูล message ไปยัง Chat Database และเรียก notification API ต่อในกรณีที่มีข้อความส่งมาแต่ผู้รับไม่ได้กำลังเปิดหน้า chat อยู่

***

The Main Chat API is responsible for storing the messages to the Chat Database and calling the notification API when a message is received but the receiver does not have the chat page open.

### Chat Database - ScyllaDB

ScyllaDB เป็น distributed database ที่ถูกดีไซน์ให้มีประสิทธิภาพสูง ใช้ resource กับ infrastructure น้อย (เมื่อเทียบกับ Cassandra ซึ่งเป็น distributed database คู่แข่ง) และสามารถ scale ได้ง่าย

การแชทอาจใช้ I/O มากขึ้นเมื่อมีผู้ใช้เพิ่มมากขึ้น เราจึงตัดสินใจใช้ database ที่ scale ได้ง่าย

***

ScyllaDB is a distributed database designed to have high performance, less infrastructure overhead, and high scalability.&#x20;

Chatting might require high I/O if there are multiple users so we decided on an easily scalable database.





