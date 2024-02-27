# Security policies

## Access Control

* การเข้าถึง Data center จะถูกจำกัดไว้ให้สำหรับบุคลากรที่ได้รับอนุญาตแล้วเท่านั้นและมีการควบคุมที่เข้มงวดเพื่อจัดการระดับการเข้าถึง
* Access Control Measures:&#x20;
  * Biometric authentication:&#x20;
    * เป็นการยืนยันตัวตนด้วยข้อมูลทางชีวภาพ ที่มีลักษณะเฉพาะตัว และไม่ซ้ำใคร เช่น ลายนิ้วมือ รูม่านตา โครงสร้างใบหน้า เสียง โดยผสานเทคโนโลยีทางด้านชีวภาพ การแพทย์ และด้านคอมพิวเตอร์เข้าด้วยกัน รวบรวมข้อมูล จดจำ แล้วเก็บไว้เพื่อนำมาเปรียบเทียบ และประมวลผลการยืนยันตัวตนของบุคคลนั้นๆ นี่เป็นกลไกหลักที่สำคัญเลยนะเนี่ย แล้วมีกี่แบบกันนะ
  * Visitor Access:&#x20;
    * ผู้เยี่ยมชมจากภายนอกต้องได้รับการนำโดยบุคลากรที่ได้รับอนุญาตและต้องปฏิบัติตามกฏระเบียบอย่างเคร่งครัด

## Remote Access

* [Global Protect by PaloAltoNetwork](remote-working-and-isp-provider.md#remote-working-work-from-home)
* [ISP Provider by True GIGATEX SME FIXED IP](remote-working-and-isp-provider.md#isp-provider-branch-connection)

## Employee Training and Awareness

* กำหนดให้มีการฝึกอบรมการตระหนักรู้ด้านความปลอดภัย (Security Awareness Training) แก่พนักงานทุกคนในบริษัทเพื่อให้ความรู้เกี่ยวกับความเสี่ยงด้านความปลอดภัยและให้รู้ถึงแนวทางการปฏิบัติที่ดีที่สุด
* ส่งเสริมวัฒนธรรมการตระหนักรู้ด้านความปลอดภัย และส่งเสริมให้พนักงานหมั่นรายงานเกี่ยวกับกิจกรรมที่น่าสงสัยที่เกิดขึ้น

## Environment Controls

* Temperature and Humidity Management:&#x20;
  * ปฏิบัติตามมาตรฐาน ASHRAE (the American Society of Heating, Refrigerating and Air-Conditioning Engineers)&#x20;
    * อุณหภูมิของอุปกรณ์ server และ storage ต้องอยู่ในช่วงระหว่าง 18 ถึง 27 องศาเซลเซียส
* Airflow Management:
  * มีการจัดการทางเดินอากาศทั้งร้อนและเย็นที่เหมาะสม
* Fire Suppression System:&#x20;
  * FM-200 Fire Suppression System
    * เป็นระบบดับเพลิงอัตโนมัติด้วยก๊าซ โดยใช้สาร hydrofluorocarbon หรือ HFC สำหรับดับไฟและยับยั้งการแพร่กระจายของไฟ

## Backup and Recovery

* Backup storage: มีการเตรียมเครื่อง storage สำรอง เพื่อเก็บข้อมูลสำรองและเพื่อเตรียมพร้อมสำหรับเหตุการณ์ที่คาดไม่ถึง เช่น เครื่อง storage หลักใช้งานไม่ได้ ฯลฯ
* UPS (**Uninterruptible Power Supply)**: มีการใช้งานเครื่องสำรองไฟที่เหมาะสมสำหรับรับมือในเหตุการณ์ที่คาดไม่ถึงต่างๆ เช่น ไฟฟ้าดับ เกิดไฟกระชาก ฯลฯ

## Firewall Protection

* มีการใช้ FortiGate firewall license (FortiGuard service) ที่ได้มาพร้อมกับเครื่อง Firewall
  * บริการ 24/7 Unified Threat Protection (UTP) ประกอบไปด้วย
    * FortiGuard IPS Service
    * FortiGuard Anti-Malware Protection (AMP) —Antivirus, Mobile Malware, Botnet, CDR, Virus Outbreak Protection and FortiSandbox Cloud Service
    * FortiGuard Web Security — URL and web content, Video and Secure DNS Filtering
    * FortiGuard Anti-Spam
    * FortiCare Premium

## BYOD (Bring Your Own Device)

* บริษัทของเราเปิดโอกาสให้พนักงงานในบริษัทสามารถนำอุปกรณ์ส่วนตัวมาใช้ในการทำงานได้ โดยทางบริษัทจะมีการกำหนดแนวปฏิบัติสำหรับพนักงานที่ใช้อุปกรณ์ส่วนตัวในการเข้าถึงเครือข่ายและข้อมูลของบริษัท
* มีการจัดเตรียมบริการต่างๆให้กับพนักงานของบริษัท เช่น บริการการติดตั้งซอฟต์แวร์รักษาความปลอดภัย เช่น โปรแกรมป้องกันไวรัส โปรแกรมป้องกันมัลแวร์ บนอุปกรณ์ส่วนตัวของพนักงาน
