# 🚗 Persian Car Plate & Digits Detection using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge" alt="YOLO11">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle" alt="Kaggle">
  
  <br><br>
  
  <img src="result.jpg" width="800">
</div>

---

## 📘 معرفی پروژه (Project Overview)
این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** و استخراج نویسه‌های آن (اعداد و حروف) است. با استفاده از معماری پیشرفته **YOLO11**، این مدل قادر است در شرایط نوری مختلف، پلاک را با دقت بسیار بالا شناسایی کند.

> 🔹 **هدف:** تبدیل تصاویر خودرو به داده‌های متنی پلاک با دقت ۹۹٪.

---

## 🚀 ویژگی‌های کلیدی (Key Features)
- ✅ **تشخیص پلاک:** مکان‌یابی دقیق مستطیل پلاک.
- ✅ **بازخوانی نویسه‌ها:** تشخیص تکی تمام اعداد و حروف فارسی پلاک.
- ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی پردازنده‌های گرافیکی (GPU).
- ✅ **دقت عالی:** آموزش دیده بر روی دیتاست تخصصی پلاک‌های ایرانی.

---

## 📊 نتایج آموزش (Training Results)

| Metric | Value |
| :--- | :--- |
| **mAP50** | ~0.99 (99%) |
| **Precision** | Very High |
| **Recall** | Stable |

---

## 📂 ساختار فایل‌ها (File Structure)
- `Persian_Plate_Detection.ipynb`: کد کامل آموزش در محیط کگل.
- `best.pt`: فایل نهایی وزن‌های مدل.
- `result.jpg`: تصویر خروجی مدل.

---

## 🛠 نحوه استفاده (Usage)

```python
from ultralytics import YOLO

# بارگذاری مدل
model = YOLO('best.pt')

# پیش‌بینی روی عکس جدید
results = model.predict(source='result.jpg', save=True)
