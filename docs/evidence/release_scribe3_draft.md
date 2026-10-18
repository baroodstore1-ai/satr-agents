# Satr v1.1.0

## English

### Highlights
- **Arabic subtitles for episode 12.** Episode 12 now ships with a complete Arabic subtitle file, so you can load it and play it without translating the episode yourself. (!1)

### Fixes
- **Space after Arabic punctuation.** When an Arabic comma (،), semicolon (؛) or question mark (؟) was followed directly by a letter, the words ran together on screen, as in "مرحباً،كيف". Satr now inserts the missing space, so the line reads "مرحباً، كيف". (!2)
- **RTL corrections in subtitles.** Right-to-left fixes were applied to the Arabic subtitle text so lines display in the correct order. This change went straight to `main` as a commit, so it has no MR number.

### Under the hood
- Added a regression test for the missing space after Arabic punctuation, so the bug can't return unnoticed. (!2)
- Updated the release evidence notes after MR !1 passed its checks again following a rebase. (!1)

<div dir="rtl" lang="ar">

## بالعربية

### أبرز ما الجديد
- **ترجمة عربية للحلقة 12.** أصبحت الحلقة 12 تأتي مع ملف ترجمة عربية كامل، فيمكنك تحميله وتشغيله مباشرةً دون الحاجة إلى ترجمة الحلقة بنفسك. (!1)

### الإصلاحات
- **مسافة بعد علامات الترقيم العربية.** كانت الكلمات تلتصق على الشاشة إذا جاء حرف مباشرةً بعد الفاصلة (،) أو الفاصلة المنقوطة (؛) أو علامة الاستفهام (؟)، مثل «مرحباً،كيف». صار Satr يضيف المسافة الناقصة تلقائياً، فيظهر السطر هكذا: «مرحباً، كيف». (!2)
- **تصحيحات اتجاه الكتابة من اليمين إلى اليسار.** طُبّقت إصلاحات على نص الترجمة العربية ليظهر ترتيب الكلمات في السطر على الوجه الصحيح. أُضيف هذا التعديل مباشرةً إلى الفرع الرئيسي `main` دون طلب دمج، ولذلك لا يحمل رقم MR.

### تحسينات داخلية
- أُضيف اختبار انحدار لمشكلة المسافة الناقصة بعد علامات الترقيم العربية، حتى لا تعود المشكلة دون أن يلاحظها أحد. (!2)
- حُدّثت ملاحظات أدلة الإصدار بعد أن اجتاز MR !1 الفحوصات من جديد عقب إعادة الدمج (rebase). (!1)

</div>