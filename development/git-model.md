# Git Model

[Kaothom Thomkao](https://app.gitbook.com/u/qnHc3ighR5YNc27y3goLcvHnDnt1 "mention")

มี branch อยู่จำนวนทั้งหมด 2 branch

* Master  -> branch แม่แบบไว้สำหรับการ create feature branch
* Dev  ->  ไว้สำหรับ test feature ที่ทำมาก่อนจะนำขึ้น production จริง
* Stagging  -> ไว้สำหรับ test product ต่างๆบน server ว่าสามารถใช้งานได้ปกติหรือไม่
* Production  -> ไว้สำหรับ product on server จริง

การเพิ่ม Feature

* ในการทำ feature ใหม่จะทำการแตก branch ใหม่จาก master ก่อนเพื่อไม่ให้ code ที่ commit ขึ้นไปไม่ส่งผลกระทบต่อ production&#x20;
* เมื่อทำ feature เสร็จแล้วจะ cherry pick เข้า dev branch เพื่อทดสอบ feature ที่ทำมา
* เมื่อทุกอย่างโอเคแล้วจึงค่อย up to date to master แล้วจึง merge feature branch นั้นๆเข้า master



<figure><img src="../.gitbook/assets/Simplified-version-of-the-gitflow-branching-model-adapted-from-8.png" alt=""><figcaption></figcaption></figure>
