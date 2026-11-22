# ساخت APK بازی «ماریو با آریا» (بدون Android Studio)

1. در github.com یک حساب بساز (رایگان) و یک ریپوی جدید (Repository) بساز.
2. محتوای همین پوشه را داخل ریپو آپلود کن (Add file → Upload files).
   حتماً پوشه مخفی `.github` هم آپلود شود.
3. به تب **Actions** برو، روی «Build APK» کلیک کن و **Run workflow** را بزن.
4. حدود ۵ تا ۸ دقیقه صبر کن. بعد از تمام شدن، روی اجرا کلیک کن و
   فایل `mario-with-aria-apk` را از بخش **Artifacts** دانلود کن (داخلش `app-debug.apk` است).
5. APK را روی گوشی اندروید بریز و نصب کن
   (اگر خواست، «Install unknown apps / نصب از منبع ناشناس» را برای مرورگر یا فایل‌منیجر فعال کن).

## ساخت روی کامپیوتر (اختیاری)
Node.js 18+ ، Java 17 و Android SDK لازم است:
    npm install
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug
خروجی: android/app/build/outputs/apk/debug/app-debug.apk

## نکته‌ها
- بازی کاملاً آفلاین کار می‌کند و سکه‌ها و خریدها روی گوشی ذخیره می‌مانند.
- برنامه به‌صورت افقی (landscape) باز می‌شود.
- این APK با کلید debug ساخته می‌شود و برای نصب شخصی مناسب است، نه انتشار در Google Play.
