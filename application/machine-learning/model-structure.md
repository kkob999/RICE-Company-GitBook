# Model Structure

เนื่องจาก RICE ของเรา มีการใช้Machine Learning ในส่วนของการค้นหาพันธ์ข้าวด้วยรูปภาพ โดยจะรับอินพุตเป็นรูปภาพและส่งผลลัพธ์เป็นพันธ์ุข้าวที่สอดคล้องหรือตรงกับรูปภาพ ดังนั้น เราจะมีโมเดลจำแนกพันธ์ุข้าว (**RICE Classification**)

### ResNet50

<figure><img src="../../.gitbook/assets/ResNet-50 Architecture.png" alt=""><figcaption><p>ResNet50 model architecture</p></figcaption></figure>

ResNet50 หรือ Deep Residual Network เป็นPre-trained model ที่ได้รับความนิยมในงานComputer Vision เช่น Image Classification, Object Detection, Image Recognition ResNet50ถูกพัฒนาขึ้นมาจากConvolutional Neural Network(CNN)&#x20;

ซึ่ง ResNet50 มีให้ใช้2 โครงสร้าง โดยสำหรับRICE นี้ ได้เลือกใช้ **ResNet50v2** เพราะเป็นที่นิยมใช้และใช้เวลาในการประมวลผลน้อย (ResNet50v2: [https://keras.io/api/applications/resnet/#resnet50v2-function](https://keras.io/api/applications/resnet/#resnet50v2-function))

<figure><img src="../../.gitbook/assets/ภาพถ่ายหน้าจอ 2567-02-23 เวลา 21.16.49.png" alt=""><figcaption><p>ตารางแสดงขนาด, จำนวนพารามิเตอร์ และเวลาในการประมวลผลของแต่ละโมเดล</p></figcaption></figure>

(ตารางเปรียบเทียบจำนวนพารามิเตอร์และเวลาในการประมวลผล: [https://keras.io/api/applications/](https://keras.io/api/applications/))

### Data Preprocessing

ทำการปรับขนาดรูปภาพ(resize)เป็น 256x256

<div>

<figure><img src="../../.gitbook/assets/RICEClassification (1).png" alt="" width="215"><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/RICEClassification.png" alt="" width="215"><figcaption></figcaption></figure>

</div>

### Model Architecture

โมเดล**RICE Classification** ถูกพัฒนามาจาก Resnet50v2 ในรูปแบบTransfer learning ที่มีการต่อlayerเพิ่มเติม

```python
base_model = tf.keras.applications.ResNet50V2(weights = 'imagenet' ,
                                             input_shape = (IM_SIZE,IM_SIZE,3) ,
                                             include_top = False)

flat = Flatten()(base_model.output)
dense = Dense(IM_SIZE, activation='relu')(flat)
dense = Dense(5, activation='softmax')(dense)

```

* Total parameters: 57,120,773
* Trainable: 57,075,333
* Non-trainable: 45,440
* Learning Rate: 0.0001
* Batch size: 80
* Image size: 256x256
* Loss function: Categorical Cross Entropy
* Optimizer: Adam

### Result

#### Test Accuracy & Loss

```
accuracy:  0.008280780166387558
loss:  0.9973333477973938
```

#### Confusion Matrix

<figure><img src="../../.gitbook/assets/RestNet50v2.png" alt=""><figcaption><p>Confusion Matrix</p></figcaption></figure>

### Tool

* ใช้ **Google Colaboratory** (Google Colab) ในการดำเนินการในส่วนของMachine Learning
* ใช้ **Python** และ **Tensorflow** ในการพัฒนาโมเดล

### Code

{% embed url="https://colab.research.google.com/drive/1hXz5J2HEkNDU-PLRs_VRoEEjYmEEgqxD?usp=sharing" %}
Code train model and prediction
{% endembed %}

*



##

