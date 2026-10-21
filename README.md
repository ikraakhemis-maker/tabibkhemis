# طبيب خميس مليانة — تطبيق أندرويد

تطبيق أندرويد (WebView) يفتح «دليل أطباء خميس مليانة وضواحيها» من:
https://ikraakhemis-maker.github.io/tabibkhemis/

## الميزات
- أيقونة تكيفية (Adaptive) تدعم أيقونات Android 13+ المتناسقة، وشاشة بداية باسم التطبيق
- سحب للأسفل للتحديث، شريط تحميل، وشاشة «لا يوجد اتصال» مع إعادة المحاولة
- أزرار الاتصال الهاتفي (tel:) وواتساب والروابط الخارجية تُفتح في تطبيقاتها
- زر الرجوع يتنقل داخل الموقع
- تنبيه إذا كان Android System WebView قديماً

## الحصول على APK
1. أنشئ مستودعاً جديداً على GitHub وارفع كل الملفات إليه (فرع `main`).
2. تبويب **Actions** ← **Build Android APK** ← انتظر الاكتمال.
3. نزّل `Tabib-Khemis-APK` من **Artifacts**، فك الضغط، وثبّت `app-debug.apk`
   (فعّل «السماح بالتثبيت من مصادر غير معروفة»).

## التخصيص
- رابط الموقع: `TARGET_URL` و`HOST` في `app/src/main/java/com/tabibkhemis/app/MainActivity.java`
- الاسم: `app/src/main/res/values/strings.xml`
- الأيقونة: `app/src/main/res/drawable/ic_launcher_*.xml`، وأيقونة المتجر 512×512 في `store/icon-512.png`
- معرّف الحزمة: `com.tabibkhemis.app` في `app/build.gradle`

## للنشر على Google Play
نسخة `debug` للتجربة فقط. للنشر تحتاج بناء نسخة `release` موقّعة (AAB) بمفتاح توقيع خاص بك.
