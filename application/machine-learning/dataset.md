# Dataset

{% embed url="https://www.kaggle.com/datasets/ayanwap7/rice-image-dataset-train-test-split" %}
ชุดข้อมูลที่ใช้ในการทำโมเดลและทดสอบโมเดล
{% endembed %}

จากชุดข้อมูลข้างต้น ประกอบด้วยรูปภาพทั้งหมด75,00 รูป สำหรับพันธุ์ข้าว5 ชนิด ดังนี้

* Arborio (ข้าวอาโบริโอ) 15,000 รูป
* Basmati (ข้าวบาสมาติ/ ข้าวอินเดีย) 15,000 รูป
* Ipsala (ข้าวอิปสาลา) 15,000 รูป
* Jasmine (ข้าวหอมมะลิ) 15,000 รูป
* Karacadag (ข้าวคารากาดาก) 15,000 รูป

ได้ทำการแบ่งข้อมูลเป็น3ส่วนสำหรับการทำโมเดลในอัตราส่วน&#x20;

&#x20;80%: 10% 10% (Train: Validate: Test) = (60,000 รูป: 7,500 รูป: 7,500 รูป)

โดยรูปภาพทั้งหมด อยู่ในรูปแบบ.jpg และเป็นภาพสีrgb

#### ตัวอย่างชุดข้อมูลที่ใช้ในการทำโมเดล

| รูป                                        | พันธุ์ข้าว |
| ------------------------------------------ | ---------- |
| ![](<../../.gitbook/assets/Arborio .jpg>)  | Arborio    |
| ![](<../../.gitbook/assets/Basmati .jpg>)  | Basmati    |
| ![](<../../.gitbook/assets/Ipsala 3.jpg>)  | Ipsala     |
| ![](<../../.gitbook/assets/Jasmine 4.jpg>) | Jasmine    |
| ![](../../.gitbook/assets/Karacadag.jpg)   | Karacadag  |

