---
title: تجنب تدهور الأداء عند رسم صور مضغوطة
type: docs
weight: 10
url: /ar/net/تجنب-تدهور-الأداء-عند-رسم-صور-مضغوطة/
---

## **تجنب تدهور الأداء عند رسم صور مضغوطة**
هناك أوقات عندما ترغب في إجراء عمليات رسومية شديدة التعقيد على صورة مضغوطة. عندما يضطر Aspose.PSD إلى ضغط وفك ضغط الصور على الطاير، قد يحدث تدهور في الأداء. قد تنطوي رسم صور مضغوطة أيضًا على عقوبة في الأداء.
### **الحل**
لتجنب تدهور الأداء، نوصي بتحويل الصورة إلى شكل غير مضغوط، أو على النحو الخام، قبل إجراء عمليات رسومية.
### **استخدام مسار الملف**
في المثال التالي، يتم تحويل صورة PSD إلى شكل خام (بدون ضغط) وحفظها على القرص. يتم تحميل الصورة غير المضغوطة مرة أخرى قبل إجراء عمليات رسومية عليها. نفس التقنية تنطبق على ملفات BMP و GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **استخدام كائن Stream**
يظهر شظايا الكود التالي كيفية تحويل صورة PSD إلى شكل خام (بدون ضغط) وحفظها على القرص باستخدام MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}