یک اپلیکیشن اندرویدی بساز که بتواند ماکروهای لمسی روی صفحه را اجرا کند. 

ویژگی‌ها:
- پلتفرم اندروید (Kotlin، minSdk 24).
- استفاده از AccessibilityService و dispatchGesture برای شبیه‌سازی لمس.
- پشتیبانی از Tap، Long-Press، Swipe و Multi-Touch (۲ تا ۴ انگشت).
- امکان زمان‌بندی دقیق (Delay و Hold به میلی‌ثانیه).
- قابلیت اجرای همزمان یا پشت‌سرهم رویدادها.
- ذخیره و بارگذاری ماکروها به صورت JSON.
- اجرای ماکرو از طریق دکمه‌های شناور (Overlay) و امکان توقف فوری.
- مثال JSON برای یک ماکرو:
  ```json
  {
    "name": "test_macro",
    "steps": [
      {"type": "tap", "point": {"x": 0.5, "y": 0.5}, "holdMs": 100},
      {"type": "delay", "ms": 200},
      {"type": "swipe", "from": {"x": 0.4, "y": 0.7}, "to": {"x": 0.6, "y": 0.7}, "durationMs": 150}
    ],
    "repeat": 1
  }
