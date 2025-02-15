---
title: ​​مزيج الألوان المعتمدة وعمق البت في PSD
type: ​​docs
weight: 80
url: /ar/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **الوصف**
يدعم Aspose.PSD فتح ملفات PSD بأي مزيج من أوضاع الألوان وأعماق البت في ملفات Adobe Photoshop PSD. يمكنك فتح هذه الملفات واستخدام واجهة برمجة تطبيقات منخفضة المستوى لتعديل محتوى الملف. ولكن بالنسبة لبعض المزيجات غير المعروفة يمكن أن تظهر مشكلات محددة، وبعضها مرتبط بقيود أوضاع الألوان.

## **مزيج التصدير المدعوم من أوضاع الألوان وعمق البت في PSD في وضع القراءة فقط**

| |Bitmap|أدمغة رمادية|مفهرس|RGB|CMYK|قناة متعددة|الحبر الثنائي|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|العمق 1|نعم|-[رابط](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|
|العمق 8|-|نعم|نعم|نعم|نعم|لا Q3-Q4|لا Q3-Q4|[نعم](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|العمق 16|-|نعم|-|نعم|نعم|- [رابط](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|لا (Q3-Q4)|
|العمق 32|-|نعم*[رابط](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|نعم*|- [رابط](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|- [رابط](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* مشكلات طفيفة في بعض الحالات

## **مزيج التصدير المدعوم من أوضاع الألوان وعمق البت في PSD في وضع التعديل**

| |Bitmap|أدمغة رمادية|مفهرس|RGB|CMYK|قناة متعددة|الحبر الثنائي|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|العمق 1|نعم|-|-|-|-|-|-|-|
|العمق 8|-|نعم|لا|نعم|نعم|لا Q3-Q4|لا Q3-Q4|[نعم](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|العمق 16|-|نعم|-|نعم|نعم*|-|-|لا (Q3-Q4)|
|العمق 32|-|لا (Q3-Q4)|-|لا (Q3-Q4)|-|-|-|-|
\* مشكلات طفيفة في بعض الحالات

إذا كنت بحاجة إلى دعم محدد لمزيج أوضاع الألوان / عمق البت، يمكنك نشر طلبك على [منتديات Aspose](https://forum.aspose.com/c/psd)