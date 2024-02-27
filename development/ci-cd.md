# CI/CD

Continuous Integration

* แตก branch มาจาก master
* เมื่อเขียน code เสร็จแล้วจึงสร้าง pull request ไปยัง master
* จะมีการ automate เช็คว่าสามารถ build deploy ได้หรือไม่
  * หากไม่สามารถ deploy ได้เจ้าของ branch นั้นๆจะต้องกลับไปแก้ไขให้สามารถ deploy ได้
* ต้องมีคนมา review และกด approve ให้อย่างน้อย 3 คนจึงจะสามารถ rebase และ merge เข้า master ได้

Continuous Deployment

* นำ master merge เข้ากับ stagging
* Test feature ทุกอย่างให้แน่ใจว่าสามารถทำงานได้ปกติ
  * หากไม่สามารถทำงานได้ปกติ จะต้องกับไปแก้ไข branch master ใหม่ตามขั้นตอน CI ข้างต้น
* เมื่อทุกอย่างผ่านการ test แล้วว่าสามารถทำงานได้ปกติ จึง deploy ขึ้น server จริง

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>
