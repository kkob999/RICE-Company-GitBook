# Instance Allocations

## Legends

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

## Node Allocations

ส่วนนี้คือการประเมินจำนวน replica สำหรับแต่ละ service ใน production cluster

สำหรับ environment dev / test / staging แล้ว จำนวน replica ของแต่ละ service จะถูกลดลงมาตามอัตราส่วนเดิม แต่จะไม่น้อยไปกว่า 2 replicas&#x20;

***

Here are replica count estimation of each service for the production cluster.

For dev / test / staging environment, each services' replica count would be scaled down proportionally but will have at least 2 replicas.

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>
