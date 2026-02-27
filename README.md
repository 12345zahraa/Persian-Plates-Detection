# Persian-Plates-Detection

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle">

  <br><br>

  <div style="width: 600px; height: 320px; overflow: hidden; border-radius: 12px; border: 1px solid #ddd;">
    <img src="result.png" style="width: 600px; margin-top: -50px;">
  </div>
</div>

<div dir="rtl" align="right">

## 📘 معرفی پروژه
این پروژه برای تشخیص هوشمند پلاک خودروهای ایرانی طراحی شده است.

### 🚀 ویژگی‌ها
* ✅ **دقت بالا:** mAP 99% روی دیتاست پلاک.
* ✅ **سرعت بالا:** بهینه برای T4 GPU.

</div>

---

## 🛠 Usage
```python
from ultralytics import YOLO
model = YOLO('best.pt')
results = model.predict(source='result.png', save=True)
