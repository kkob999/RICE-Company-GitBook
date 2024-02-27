# Cart service

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Database for cart service</p></figcaption></figure>

Database นี้นั้นจะเอาไว้เก็บข้อมูลของ user ที่อยู่ในหมวดของ buyer เพื่อเก็บข้อมูลของสินค้าที่ user นั้นได้เพิ่มเข้ามาในตะกร้าของตนเอง โดยมี foreign key ที่มาจากตาราง user ซึ่งถูกเก็บอยู่ภายใน user database ซึ่งจะเป็นสิ่งที่ทำให้รู้ว่าตะกร้านี้เป็นของ user ใด และมี foreign key ที่มาจากตาราง product ซึ่งถูกเก็บอยู่ใน product database ซึ่งเป็นเอาไว้ดึงข้อมูลของสินค้าที่อยู่ภายในตะกร้า
