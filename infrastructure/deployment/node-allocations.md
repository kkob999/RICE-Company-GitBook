# Node Allocations

## EC2 Instances

เราจะใช้ EC2 instances ที่ใหญ่เป็น host สำหรับ pods (nodes) นั่นก็เพราะว่า instance ที่ใหญ่กว่ามี pod-count-per-instance ที่มากกว่าเมื่อเทียบกว่า instance ที่เล็กกว่านั่นเอง

มี instance 3 ชนิดที่เราจะใช้:

* 4x **t4g.small** (2 vCPUs / 2GiB RAM / 11 pods) เป็น control plane
* 12x **c7g.large** (2 vCPUs / 4 GiB RAM / 29 pods) เป็น worker node ทั่วไป
* 2x **c7g.2xlarge** (8 vCPUs / 16 GiB RAM / 58 pods) เป็น worker node ที่ต้องใช้แรงประมวลผลสูง&#x20;

***

We will use fewer but more powerful EC2 instances as nodes to host our pods. This is because larger EC2 instances offer better pod-count-per-instance ratio compared to smaller EC2 instances.

There are 3 types of instances that we will use:

* 4x **t4g.small** (2 vCPUs / 2GiB RAM / 11 pods) for control plane
* 12x **c7g.large** (2 vCPUs / 4 GiB RAM / 29 pods) for general workers
* 2x **c7g.2xlarge** (8 vCPUs / 16 GiB RAM / 58 pods) for compute-heavy workers

## Node Groups

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

เราแบ่ง nodes ออกเป็น 4 กลุ่ม:

* **master** สำหรับ control plane
* **worker-general** สำหรับ service ที่ใช้แรงประมวลผลน้อยกว่าเช่น order, shipping, etc. รวมไปถึง cronjobs  และอื่นๆ
* **worker-compute** สำหรับ service ที่ใช้แรงประมวลผลน้อยกว่าเช่น user, shop, product, etc. รวมไปถึง message queues และอื่นๆ
* **general-internal** เหมือนกับ worker-general แต่ใช้สำหรับ internal services เช่น monitoring, build instance

***

We separate the nodes into 4 node groups:

* **master** for the control plane
* **worker-general** for less CPU intensive services such as order, shipping, etc. as well as cronjobs and other services
* **worker-compute** for more CPU intensive services such as user, shop, product, etc. as well as message queues and other services
* **general-internal** are the same as worker-general but for other internal services such as monitoring, build instance
