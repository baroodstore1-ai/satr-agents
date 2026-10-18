# Satr v1.1.0

## English

### Highlights
- **Arabic subtitles for episode 12.** Episode 12 now ships with a complete Arabic subtitle file, so you can load it and play it without translating the episode yourself. The file includes right-to-left corrections, so words and punctuation in each line appear in the correct order on screen. (!1)

### Fixes
- **Space after Arabic punctuation.** When an Arabic comma (،), semicolon (؛) or question mark (؟) was followed directly by a letter, the words ran together on screen, as in "مرحباً،كيف". Satr now inserts the missing space, so the line reads "مرحباً، كيف". (!2)

### Under the hood
- Added a regression test for the missing space after Arabic punctuation, so the bug can't return unnoticed. (!2)
- CI now runs the subtitle gate on subtitle-only changes, so a change that touches only subtitle files is checked automatically. This went straight to `main` as commit ad13a72, so it has no MR number.

<div dir="rtl" lang="ar">

## بالعربية

### أبرز ما الجديد
- **ترجمة عربية للحلقة 12.** أصبحت الحلقة 12 تأتي مع ملف ترجمة عربية كامل، فيمكنك تحميله وتشغيله مباشرةً دون الحاجة إلى ترجمة الحلقة بنفسك. ويتضمن الملف تصحيحات لاتجاه الكتابة من اليمين إلى اليسار، فتظهر الكلمات وعلامات الترقيم في كل سطر بالترتيب الصحيح على الشاشة. (!1)

### الإصلاحات
- **مسافة بعد علامات الترقيم العربية.** كانت الكلمات تلتصق على الشاشة إذا جاء حرف مباشرةً بعد الفاصلة (،) أو الفاصلة المنقوطة (؛) أو علامة الاستفهام (؟)، مثل «مرحباً،كيف». صار Satr يضيف المسافة الناقصة تلقائياً، فيظهر السطر هكذا: «مرحباً، كيف». (!2)

### تحسينات داخلية
- أُضيف اختبار انحدار لمشكلة المسافة الناقصة بعد علامات الترقيم العربية، حتى لا تعود المشكلة دون أن يلاحظها أحد. (!2)
- صار CI يشغّل فحص الترجمة (subtitle gate) تلقائياً عند التعديلات التي تمسّ ملفات الترجمة وحدها، فيُفحص كل تغيير من هذا النوع دون تدخل يدوي. أُضيف هذا التعديل مباشرةً إلى الفرع الرئيسي `main` في الإيداع ad13a72، ولذلك لا يحمل رقم MR.

</div>
