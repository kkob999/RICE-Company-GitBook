# Server Operating System and Virtualization

## Red Hat Enterprise Linux (RHEL)

<figure><img src="https://blog.desdelinux.net/wp-content/uploads/2022/05/RHEL9.jpg" alt="" width="563"><figcaption></figcaption></figure>

เป็นระบบปฏิบัติการ Linux ระดับองค์กรชั้นนำที่พัฒนาโดย Red Hat, Inc. มันถูกออกแบบมาใช้ในสภาพแวดล้อมธุรกิจที่สำคัญและมีความเสถียรและปลอดภัยและสามารถปรับขนาดได้

คุณลักษณะหลักของ RHEL:

1. **Stability**: RHEL มีความเสถียรและเชื่อถือได้ ทำให้เหมาะสำหรับ workload และแอปพลิเคชันที่จำเป็นต้องใช้งานอย่างต่อเนื่อง
2. **Security**: RHEL มีคุณสมบัติด้านความปลอดภัยที่แข็งแกร่ง เช่น SELinux (Security-Enhanced Linux) สำหรับควบคุมการเข้าถึงและการป้องกันระบบ รวมถึงการอัปเดตและซ่อมแซมความปลอดภัยเป็นประจำ
3. **Scalability**: RHEL ออกแบบมาเพื่อขยายขนาดได้ตั้งแต่การติดตั้งบนเซิร์ฟเวอร์เดียว จนถึงคลัสเตอร์หลายโหนด ซึ่งช่วยให้องค์กรสามารถขยายพื้นที่พื้นที่พื้นที่ตามความต้องการได้
4. **Support**: Red Hat ให้บริการสนับสนุนอย่างครอบคลุมสำหรับ RHEL รวมถึงการสนับสนุนทางเทคนิค การอัปเดตและการบำรุงรักษาอย่างสม่ำเสมอ เพื่อให้ลูกค้าขององค์กรมีการเข้าถึงช่วยเหลือเมื่อจำเป็น
5. **Compatibility**: RHEL เข้ากันได้กับหลายสถาปัตยกรรมฮาร์ดแวร์และแอปพลิเคชันซอฟต์แวร์ ทำให้มีความยืดหยุ่นสำหรับสภาพแวดล้อม IT ที่หลากหลาย



## Server Virtualization

เป็นเทคโนโลยีการจำลองเซิร์ฟเวอร์เครื่องจริง (Physical Server) 1 เครื่อง ให้เป็นเซิร์ฟเวอร์เสมือน (Virtual Server เรียกย่อว่า VM) หลายๆ เครื่องโดยแต่ละเครื่องสามารถลงระบบปฏิบัติการ (OS) และแอพพลิเคชั่นต่างกันได้ โดย VM แต่ละเครื่องมีอิสระต่อกัน หาก VM ตัวใดตัวหนึ่งเสียหายหรือแฮงค์ VM ตัวอื่นสามารถทำงานได้อย่างปกติ

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20200813134720/servervirtualizationcloudcomputing.png" alt=""><figcaption></figcaption></figure>

**ประโยชน์ของการทำ Server Virtualization**

1. ลดต้นทุนและค่าใช้จ่ายในการดำเนินงาน
2. Downtime ต่ำหรือลดปัญหาการ Downtime
3. เพิ่มประสิทธิผลทางด้าน IT และการตอบสนองที่รวดเร็ว
4. Provisioning ได้รวดเร็ว ไม่ว่าจะเป็นการ Setup และเพิ่มลดทรัพยากร
5. เพิ่มความสามารถในการ Backup และ Restore
6. จัดการได้ผ่านศูนย์กลาง ง่ายต่อการบริหารจัดการ
7. เพิ่มความสามารถในการทำ High Availability
8. เพิ่มความสามารถในการทำ Disaster Recovery
9. ลดระยะเวลาการดูแลรักษา

## VMware vSphere

<figure><img src="https://www.globenetcorp.com/wp-content/uploads/2020/05/vmware_vsphere.png" alt="" width="563"><figcaption></figcaption></figure>

VMware vSphere คือ แพลตฟอร์มการจำลองเสมือนของวีเอ็มแวร์ มี 2 ส่วนประกอบหลักของ vSphere คือ&#x20;

* ESXi: เป็นแพลตฟอร์มการจำลองเสมือนที่คุณสร้าง และเรียกใช้เครื่องเสมือน (อุปกรณ์เสมือน vCenter Server เป็นบริการที่จัดการโฮสต์หลายโฮสต์ที่เชื่อมต่อในเครือข่าย และ pool host resources) นอกจากนี้ยังสามารถเปิดใช้งานคุณลักษณะต่างๆ เช่น vSphere Distributed Resource Scheduler (DRS), vSphere High Availability (HA), vSphere vMotion และ vSphere Storage vMotion
* VMware vCenter Server: เป็นชุดซอฟต์แวร์ที่จัดการโครงสร้างพื้นฐานการจำลองเสมือนของ VMware ทั้งหมด โดยทำหน้าที่เป็นหน้าต่างเดียว จากนั้นการกำหนด VM ให้กับโฮสต์จะได้รับการจัดการ เช่นเดียวกับการกำหนดทรัพยากรให้กับงาน ตามนโยบายที่กำหนดโดยผู้ดูแลระบบ vCenter อินสแตนซ์ (instances) เดียวสามารถจัดการโฮสต์ได้มากถึง 1,000 โฮสต์ในแต่ละครั้งใน VM ที่ใช้งานอยู่มากถึง 10,000 VM หรือ VM ที่ลงทะเบียน 15,000 ตัว

<figure><img src="https://kirz.com/upload-img/Theme/Blog/GUID-VMware_vSphere_.png" alt=""><figcaption></figcaption></figure>
