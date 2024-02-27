# Order service

## Overview

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Database for order service</p></figcaption></figure>

Database นี้นั้นจะเก็บข้อมูลของสินค้าที่มีการสั่งซื้อเกิดขึ้นของแต่ user แต่ละคนที่อยู่ในกลุ่มของ customer

## order

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption><p>order table</p></figcaption></figure>

เป็นตารางหลักที่เอาไว้เก็บข้อมูลการสั่งซื้อของสินค้า เช่น สถานะของสินค้า, ที่อยู่ที่ใช้ในการจัดส่ง

### foreign key from others database

* user\_id: เป็น foreign key ที่มาจากตาราง user ซึ่งถูกเก็บอยู่ภายใน user database โดยจะเป็นสิ่งที่บอกว่า order นั้นเป็นของ user ใดที่อยู่ในกลุ่ม buyer
* sub\_district\_id: เป็น foreign key ที่มาจากตาราง  sub\_district  ซึ่งถูกเก็บอยู่ภายใน district database ซึ่งจะเป็นสิ่งที่บอก ตำบล, อำเภอ และรหัสไปรษณีย์ของที่อยู่

## order\_detail

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption><p>order_detail table</p></figcaption></figure>

เป็นตารางที่เอาเก็บข้อมูลของสินค้าที่มีการสั่งซื้อ คือ ราคา, จำนวนที่ซื้อ

### foreign key from others database

* product\_id: เป็น foreign key ที่มาจากตาราง product ซึ่งถูกเก็บอยู่ภายใน product database โดยเป็นสิ่งที่จะช่วยในการดึงข้อมูลต่าง ๆ ของตัวสินค้า เช่น ร้านที่ขาย, ประเภทของข้าว เป็นต้น

## payment\_detail

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption><p>payment_detail table</p></figcaption></figure>

เป็นตารางที่เก็บข้อมูลเกี่ยวกับการชำระเงินของสินค้าที่ซื้อ

## payment\_type

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption><p>payment_type table</p></figcaption></figure>

เป็นตารางที่เก็บประเภทที่ใช้ในการชำระเงิน เช่น เงินสด, บัตรเครดิต เป็นต้น

## order\_status

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

เป็นตารางที่เก็บสถานะต่าง ๆ ของ order เช่น รอชำระเงิน, เตรียมจัดส่ง, กำลังจัดส่ง เป็นต้น

## shipping\_provider

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption><p>shipping_provider table</p></figcaption></figure>

เป็นตารางที่เก็บผู้ที่ทำการจัดส่งสินค้า เช่น Kerry, ไปรษณีย์ไทย,  Flash Express เป็นต้น
