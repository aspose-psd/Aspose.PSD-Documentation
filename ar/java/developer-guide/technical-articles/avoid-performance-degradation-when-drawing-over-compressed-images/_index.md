---
title: تجنب تدهور الأداء عند رسم صور مضغوطة
type: docs
weight: 40
url: /ar/java/%D8%AA%D8%AC%D9%86%D8%A8-%D8%AA%D8%AF%D9%87%D9%88%D8%B1-%D8%A7%D9%84%D8%A3%D8%AF%D8%A7%D8%A1-%D8%B9%D9%86%D8%AF-%D8%B1%D8%B3%D9%85-%D8%B5%D9%88%D8%B1-%D9%85%D8%B6%D8%BA%D9%88%D8%B7%D8%A9/
---

## **تجنب تدهور الأداء عند رسم صور مضغوطة**
هناك أوقات ترغب فيها في أداء عمليات رسومية شديدة التعقيد على صورة مضغوطة. عندما يحتاج Aspose.PSD إلى ضغط وفك ضغط الصور أثناء التشغيل، فقد تحدث تدهورًا في الأداء. قد يكون رسم الصور على الصور المضغوطة أيضًا يحمل عقوبة أداء.
### **الحل**
لتجنب تدهور الأداء، نوصي بتحويل الصورة إلى تنسيق غير مضغوط، أو عريض، قبل أداء العمليات الرسومية.
### **استخدام مسار الملف**
في المثال التالي، يتم تحويل صورة PSD إلى تنسيق عريض (بدون ضغط) وحفظها على القرص. يتم تحميل الصورة غير المضغوطة مرة أخرى قبل أداء العمليات الرسومية عليها. تنطبق نفس التقنية على ملفات BMP و GIF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **استخدام كائن التيار**
يظهر مقطع الكود التالي لك كيفية تحويل صورة PSD إلى تنسيق عريض (بدون ضغط) وحفظها على القرص باستخدام التيار.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}