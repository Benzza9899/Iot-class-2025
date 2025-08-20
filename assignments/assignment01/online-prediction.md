# Online Prediction
1. online ML เชื่อมต่อไปที่ influxDB
2. Load Model
3. นำข้อมูล kafka มา Predict
<!-- Online Prection ทำงานอย่างไร  -->

## ปิดการใช้งานของ Batch ML ดังนี้

1. Kafka-to-Json
2. Train-from-data
3. Predict-then-influxdb


## เริ่มใช้งาน Online ML ดังนี้

1. docker compose down batch ML
2. เเก้ไฟล์.env ใน online-ml-predict
3. docker compose up Online ML

## ผลที่ได้จากการใช้ ML มีดังนี้
![alt text](<Screenshot 2025-08-06 150123.png>)
<!-- แนบรูป Grafana  พร้อมอธิบาย -->
