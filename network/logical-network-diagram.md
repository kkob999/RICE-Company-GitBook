# Logical Network Diagram

## Branch

<figure><img src="../.gitbook/assets/Branch Logical Topology.png" alt=""><figcaption></figcaption></figure>

### Egress Layer

Egress Layer เป็นชั้นที่มี Router จำนวน 1 ตัวที่คอยรับ-ส่งข้อมูลออกสู่โลก internet จาก topology ได้ทำการรับ internet  จาก 1 ISP Provider และ Firewall จำนวน 1 ตัว ที่คอยทำหน้าที่ในส่วนของกันป้องกันอันตรายจากอินเทอร์เน็ต&#x20;

### Access Layer

Access Layer เป็นชั้นที่เชื่อมต่อ end-device ซึ่งประกอบไปด้วย L3 Access Switch 1 ตัว เชื่อมต่อกับ Access Point  7 ตัว และ PC 1 เครื่อง ในห้อง Network Admin ไว้สำหรับการ Config หรือการ Maintenance ต่างๆ



***

## Headquater

<figure><img src="../.gitbook/assets/HQ Logical Topology.png" alt=""><figcaption></figcaption></figure>

### Egress Layer

Egress Layer เป็นชั้นที่มี Router จำนวน 1 ตัวที่คอยรับ-ส่งข้อมูลออกสู่โลก internet จาก topology ได้ทำการรับ internet  จาก 1 ISP Provider และ Firewall จำนวน 1 ตัว ที่คอยทำหน้าที่ในส่วนของกันป้องกันอันตรายจากอินเทอร์เน็ต

### Collapse Core Layer

Collapse Core Layer เป็นชั้นที่มี L3 Switch 2 ตัวที่ทำหน้าที่เป็นทั้ง Distribution Switch และ Core Switch ในตัวเดียวกัน คอยทำหน้าที่ routing รวบรวมข้อมูลที่มาจากชั้น Access Layers ไปยัง Egress Layer เชื่อมต่อกันเองเพื่อการ Redundance และเชื่อมต่อไปยัง L3 Access Switch อีก 2 ตัว&#x20;

### Access Layer

Access Layer เป็นชั้นที่เชื่อมต่อ end-device ซึ่งประกอบไปด้วย L3 Access Switch 1 ตัว เชื่อมต่อกับ Access Point  27 ตัว และ PC 1 เครื่อง ในห้อง Datacenter Admin ไว้สำหรับการ Config หรือการ Maintenance ต่างๆ

### DMZ

DMZ(DeMilitarized Zone) หรือ "เขตปลอดทหาร" เป็นมาตรการรักษาความปลอดภัยที่เราใช้เพื่อป้องกัน เครือข่ายภายใน ขององค์กรต่อภัยคุกคามภายนอก โดยที่จะมี L3 Switch เป็นตัวขั้นระหว่าง Mail Server กับ Firewall ที่ป้องกันเครือข่ายภายในองค์กร

### Datacenter

ในส่วนของ Datacenter สามารถเข้าไปดูได้ที่ [#datacenter-logical-topology](datacenter.md#datacenter-logical-topology "mention")



***

## All

<figure><img src="../.gitbook/assets/Logical Topology.png" alt=""><figcaption></figcaption></figure>

ในภาพนี้จะเป็นการนำ Logical Topology ของ [#branch](logical-network-diagram.md#branch "mention") และ [#headquater](logical-network-diagram.md#headquater "mention") มารวมกันครับ
