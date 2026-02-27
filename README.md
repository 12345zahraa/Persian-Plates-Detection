# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge" alt="YOLO11">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle" alt="Kaggle">
</div>

---

<div align="center">
  <img src="result.png" width="800">
</div>

---

<div dir="rtl">

# 🚗 تشخیص پلاک و نویسه‌های ایرانی با YOLO11

این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** و استخراج نویسه‌های آن (اعداد و حروف) است. با استفاده از معماری پیشرفته **YOLO11**، این مدل قادر است در شرایط نوری مختلف، پلاک را با دقت بسیار بالا شناسایی کند.

## 🚀 ویژگی‌های کلیدی
- ✅ **تشخیص پلاک:** مکان‌یابی دقیق مستطیل پلاک.
- ✅ **بازخوانی نویسه‌ها:** تشخیص تمام اعداد و حروف فارسی.
- ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی GPU.

## 📂 ساختار فایل‌ها
- `best.pt`: فایل نهایی وزن‌های مدل (۵.۳ مگابایت).
- `result.png`: تصویر نمونه از خروجی تشخیص پلاک.
- `README.md`: توضیحات و راهنمای پروژه.

---

## 🛠 نحوه استفاده (Usage)
</div>

```python
from ultralytics import YOLO

# بارگذاری مدل آموزش‌دیده
model = YOLO('best.pt')

# پیش‌بینی روی عکس جدید
results = model.predict(source='your_image.jpg', save=True)
