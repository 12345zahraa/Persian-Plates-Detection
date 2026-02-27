# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle">
  <br>
  <img src="result.png" width="600">
</div>

---

<div dir="rtl">

## 📘 معرفی پروژه
این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** است که با مدل **YOLO11** پیاده‌سازی شده است.

* ✅ **دقت:** ۹۹٪ در تشخیص نویسه‌ها.
* ✅ **سرعت:** پردازش سریع روی GPU.

### 🛠 Usage
</div>

```python
from ultralytics import YOLO
model = YOLO('best.pt')
results = model.predict(source='result.png', save=True)
