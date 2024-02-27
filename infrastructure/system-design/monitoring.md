# Monitoring

[Baangkok Vanijyananda](https://app.gitbook.com/u/5XBQ6zvmsFdF62v6lDsQg7C7olW2 "mention")

## Prometheus

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

**Prometheus** เป็น software ที่ใช้สำหรับเก็บ metrics หรือ log ต่างๆที่เกิดจาก software อื่นๆที่เรารันอยู่ ตัว Prometheus Server จะ pull metrics จาก application / Kubernetes server / OS / ฯลฯ แล้วนำมาเก็บไว้ใน database ประเภท time series

***

**Prometheus** is a software used for recording metrics, logs, etc. The central Prometheus server will pull metrics from applications, or the Kubernetes server, or the OS, etc., and store them in a time series database.

## Grafana

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

**Grafana** เป็น data visualization tool ซึ่งจะ query ข้อมูล time series จาก database ของ Prometheus แล้วนำมาพลอตเป็น graph, gauge, และอื่นๆ เป็น dashboard นอกจากนี้ Grafana ยังสามารถส่ง alert ได้เมื่อ metrics ที่เรากำหนดขึ้นสูงเกิดค่าที่เรากำหนด

***

**Grafana** is a data visualization tool. Grafana queries time series data from Prometheus's database and visualize them as graphs, gauges, etc. on Grafana dashboards. Additionally, Grafana can also send out alerts when certain threshold of certain metrics are reached.&#x20;

## Kibana / Elastic Search

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

**Kibana with Elastic Search** เป็น tools สำหรับการค้นหา log ซึ่งจะทำให้ developers สามารถหา log จาก containers, applications, clusters, ฯลฯ ได้อย่างรวดเร็ว

***

**Kibana with Elastic Search** is a log browsing tool. Kibana allows developers to quickly search for logs from containers, applications, clusters, etc.
