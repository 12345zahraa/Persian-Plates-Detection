# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<!-- Badges -->
<div align="center"
     style="display:flex;
            justify-content:center;
            align-items:center;
            gap:0;
            margin:-12px 0 -12px 0;
            padding:0;">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python"
       style="margin:0; padding:0; display:block;">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge"
       style="margin:0; padding:0; display:block;">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle"
       style="margin:0; padding:0; display:block;">
</div>

<!-- Result Image -->
<div align="center"
     style="display:flex;
            justify-content:center;
            align-items:center;
            margin:-20px 0 -20px 0;
            padding:0;">
  <img src="result.png"
       width="800"
       style="margin:0; padding:0; display:block;">
</div>

<!-- RTL Section -->
<div dir="rtl"
     style="margin:-10px 0 0 0; padding:0;">

## 🚗 تشخیص پلاک و نویسه‌های ایرانی با YOLO11

این پروژه یک سیستم هوشمند برای تشخیص پلاک خودروهای ایرانی و استخراج نویسه‌های آن (اعداد و حروف) است.  
با استفاده از معماری پیشرفته YOLO11، این مدل قادر است در شرایط نوری مختلف، پلاک را با دقت بسیار بالا شناسایی کند.

### 🚀 ویژگی‌های کلیدی
- ✅ تشخیص پلاک: مکان‌یابی دقیق مستطیل پلاک
- ✅ بازخوانی نویسه‌ها: تشخیص تمام اعداد و حروف فارسی
- ✅ سرعت بالا: بهینه‌شده برای اجرا روی GPU (Kaggle T4)

### 📂 ساختار فایل‌ها
- best.pt: فایل نهایی وزن‌های مدل (۵.۳ مگابایت)
- result.png: تصویر نمونه از خروجی تشخیص پلاک

</div>

---

## 🛠 Usage

`python
from ultralytics import YOLO

# Load the model
model = YOLO('best.pt')

# Predict on an image
results = model.predict(source='result.png', save=True)
