# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge" alt="YOLO11">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle" alt="Kaggle">
</div>

---

<div dir="rtl">

## 📘 معرفی پروژه
این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** و استخراج نویسه‌های آن (اعداد و حروف) است. با استفاده از معماری پیشرفته **YOLO11**، این مدل قادر است در شرایط نوری مختلف، پلاک را با دقت بسیار بالا شناسایی کند.

> 🔹 **هدف:** تبدیل تصاویر خودرو به داده‌های متنی پلاک با دقت بالا.

### 🚀 ویژگی‌های کلیدی
- ✅ **تشخیص پلاک:** مکان‌یابی دقیق مستطیل پلاک.
- ✅ **بازخوانی نویسه‌ها:** تشخیص تکی تمام اعداد و حروف فارسی پلاک.
- ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی GPU (Kaggle T4).

### 📊 نتایج آموزش
مدل بر روی پلاک و نویسه‌ها آموزش دیده و به دقت **mAP50: 99%** دست یافته است.

### 📂 ساختار فایل‌ها
- `best.pt`: فایل نهایی وزن‌های مدل (۵.۳ مگابایت).
- `result.png`: تصویر نمونه خروجی تشخیص پلاک.

</div>

---

## 🛠 Usage
```python
from ultralytics import YOLO

# Load the trained model
model = YOLO('best.pt')

# Predict on a new image
results = model.predict(source='result.png', save=True)
