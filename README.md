# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge" alt="YOLO11">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle" alt="Kaggle">
</div>

<div align="center">
  <img src="result.png" width="800">
</div>

<div dir="rtl">

# 🚗 تشخیص پلاک و نویسه‌های ایرانی با YOLO11

این پروژه یک سیستم هوشمند برای تشخیص پلاک خودروهای ایرانی و استخراج نویسه‌های آن (اعداد و حروف) است.  
با استفاده از معماری پیشرفته **YOLO11**، این مدل قادر است در شرایط نوری مختلف، پلاک را با دقت بسیار بالا شناسایی کند.

### 🚀 ویژگی‌های کلیدی
- ✅ **تشخیص پلاک:** مکان‌یابی دقیق مستطیل پلاک
- ✅ **بازخوانی نویسه‌ها:** تشخیص تمام اعداد و حروف فارسی
- ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی GPU (Kaggle T4)

### 📂 ساختار فایل‌ها
- `best.pt`: فایل نهایی وزن‌های مدل (۵.۳ مگابایت)
- `result.png`: تصویر نمونه از خروجی تشخیص پلاک

</div>

---
## 📊 دیتاست‌های مورد استفاده (Datasets)
این پروژه با ترکیب دو دیتاست جامع از پلتفرم **Kaggle** آموزش دیده است تا بیشترین دقت را در تشخیص پلاک‌های ملی داشته باشد:

* 📂 **[Car Plate Detection - YOLOv11](https://www.kaggle.com/datasets/zahramollaey/car-plate-detection-yolov11):** دیتاست تخصصی برای آموزش مدل YOLOv11 جهت مکان‌یابی دقیق مستطیل پلاک.
* 📂 **[Persian Car Plates Digits Detection - YOLO](https://www.kaggle.com/datasets/zahramollaey/persian-car-plates-digits-detection-yolo):** دیتاست بهینه‌شده برای شناسایی و تفکیک نویسه‌ها (اعداد و حروف) پلاک‌های ایرانی.

> [!TIP]
> هر دو دیتاست با فرمت استاندارد **YOLO** برچسب‌گذاری شده‌اند.
---
## 🛠 Usage

```python
from ultralytics import YOLO

# Load the model
model = YOLO('best.pt')

# Predict on an image
results = model.predict(source='result.png', save=True)
