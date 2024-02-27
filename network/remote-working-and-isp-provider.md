# Remote Working & ISP Provider

## Remote working (Work-From-Home)

สำหรับการ Remote working พวกเราเลือกใช้ GlobalProtect by PaloAltoNetwork ในการจัดการเรื่องของการ Authentication VPN จากการ Work-From-Home เข้าไปสู่ Network ภายในของบริษัท

### GlobalProtect by PaloAltoNetwork

GlobalProtect คือ โซลูชันเครือข่ายส่วนตัวเสมือน (VPN) ที่พัฒนาโดย Palo Alto Networks เพื่อให้การเชื่อมต่อระยะไกลไปยังเครือข่ายขององค์กรเป็นเรื่องปลอดภัยสำหรับผู้ใช้ โดยไม่ว่าจะอยู่ที่ไหนก็ตาม GlobalProtect จะช่วยให้ผู้ใช้สามารถเชื่อมต่อกับเครือข่ายองค์กรได้อย่างปลอดภัย แม้ว่าจะอยู่นอกสำนักงานหรือทำงานจากระยะไกลก็ตาม&#x20;

&#x20;Global Protect จะมีองค์ประกอบอยู่ 3 ส่วน

* Global Protect Portal : เป็นหน่วยควบคุมหลักที่ให้บริการการตั้งค่าและการจัดการสำหรับผู้ใช้และอุปกรณ์ที่เชื่อมต่อผ่าน GlobalProtect VPN หรือบุคคลภายนอกที่มีการเข้าถึงระบบ
* Global Protect Gateway : เป็นเกตเวย์ที่ให้บริการการเชื่อมต่อ VPN และความปลอดภัยระหว่างอุปกรณ์ของผู้ใช้และเครือข่ายองค์กร
* Global Protect Agents : เป็นโปรแกรมซอฟต์แวร์ที่ติดตั้งบนอุปกรณ์ของผู้ใช้ เพื่อให้ผู้ใช้สามารถเชื่อมต่อกับ GlobalProtect Gateway และเครือข่ายขององค์กร

<figure><img src="../.gitbook/assets/GlobalProtect (1).png" alt=""><figcaption></figcaption></figure>

***

## ISP Provider (branch connection)

สำหรับการเชื่อมต่อ VPN จาก Branch ไปสู่ Headquater พวกเราเลือกใช้เป็น Site-To-Site VPN ที่มี ISP Provider เป็น TRUE ที่ทำการเชื่อมต่อด้วย Public Fixed IP เป็นผู้บริการ และทางตัวของ Headquater เอง ก็ใช้ TRUE เช่นกัน

### **TRUE GIGATEX SME FIXED IP**

เป็น Package สำหรับ ธุรกิจ SME เหมาะกับบริษัทเราที่เป็น Start up

* Public Fixed IP Address
* Speed 2,000/500 Mbps
* ราคา : 2,090 บาทต่อเดือน

[https://truebusiness.truecorp.co.th/th/smepack/internet/gigatex-sme-fixed-ip](https://truebusiness.truecorp.co.th/th/smepack/internet/gigatex-sme-fixed-ip)
