# Product service

## Overview

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption><p>Database for Product service</p></figcaption></figure>

Database นี้นั้นจะเก็บข้อมูลของสินค้าที่มีอยู่ภายในระบบ

## product

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption><p>product table</p></figcaption></figure>

เป็นตารางหลักที่เอาไว้เก็บข้อมูลหลักของสินค้า เช่น ชื่อ, คำอธิบาย, ราคา

### foreign key from others database

* shop\_id: เป็น foreign key ที่มาจากตาราง shop ซึ่งถูกเก็บอยู่ภายใน shop database โดยจะเป็นสิ่งที่บอกว่าสินค้านั้นเป็นของร้านใด

## review

<figure><img src="../../../.gitbook/assets/image (38).png" alt=""><figcaption><p>review table</p></figcaption></figure>

เป็นตารางที่เอาไว้เก็บข้อมูลการรีวิวของสินค้า

### foreign key from others database

* order\_id: เป็น foreign key ที่มาจากตาราง order ซึ่งถูกเก็บอยู่ภายใน order database โดยจะเป็นสิ่งที่บอกว่าการรีวิวนั้นมาจาก order ใด
* user\_id: เป็น foreign key ที่มาจากตาราง user ซึ่งถูกเก็บอยู่ภายใน user database โดยจะเป็นสิ่งที่บอกว่ารีวิวนั้นมาจาก user ใด

## review\_file

<figure><img src="../../../.gitbook/assets/image (39).png" alt=""><figcaption><p>review_file table</p></figcaption></figure>

เป็นตารางที่เอาไว้เก็บ attachment ของรีวิว เช่น รูปภาพ, วิดีโอ เป็นต้น

## rice\_type

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

เป็นตารางที่เก็บประเภทของข้าว เช่น ข้าวกล้อง, ข้าวสาร เป็นต้น

## rice\_species

<figure><img src="../../../.gitbook/assets/image (41).png" alt=""><figcaption><p>rice_species table</p></figcaption></figure>

เป็นตารางที่เก็บสายพันธุ์ของข้าว เช่น ข้าวหอมมะลิ,  ข้าวเหนียวเขาวง เป็นต้น

## milling\_grade

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption><p>milling_grade table</p></figcaption></figure>

เป็นตารางที่เก็บคุณภาพของการสีข้าว เช่น สีดีพิเศษ, สีดี, สีปานกลาง เป็นต้น

## rice\_class

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption><p>rice_class table</p></figcaption></figure>

เป็นตารางที่เก็บชั้นของเมล็ดข้าว โดยการแบ่งนั้นจะแบ่งตามความยาว

## product\_file

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption><p>product_file tables</p></figcaption></figure>

เป็นตารางที่เก็บ attachment ของตัวสินค้า เช่น รูปภาพ, วิดีโอ เป็นต้น
