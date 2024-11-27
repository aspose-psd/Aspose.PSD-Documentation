---
title: رسم الصور باستخدام الرسومات
type: docs
weight: 20
url: /ar/net/drawing-images-using-graphics/
---

## **رسم الصور باستخدام الرسومات**
مع مكتبة Aspose.PSD يمكنك رسم أشكال بسيطة مثل خطوط ومستطيلات ودوائر، بالإضافة إلى أشكال معقدة مثل المضلعات والمنحنيات والأقواس والأشكال بيزير. تنشئ مكتبة Aspose.PSD هذه الأشكال باستخدام فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) التي توجد في مساحة أسماء Aspose.PSD. الكائنات الرسومية مسؤولة عن أداء عمليات رسم مختلفة على صورة، مما يغير سطح الصورة. تستخدم فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) مجموعة متنوعة من كائنات المساعدة لتحسين الأشكال:

- Pens، لرسم خطوط أو تحديد الأشكال أو رسم التمثيلات الهندسية الأخرى.
  
- Brushes، لتعريف كيفية ملء المناطق.

- Fonts، لتعريف شكل الحروف من النص.

### **الرسم باستخدام فئة الرسومات**
أدناه مثال على الشيفرة يوضح استخدام فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). تم تقسيم شيفرة المصدر إلى عدة أجزاء لتبقيها بسيطة وسهلة المتابعة. خطوة بخطوة، تظهر الأمثلة كيفية:

1. إنشاء صورة.
1. إنشاء وتهيئة كائن Graphics.
1. تنظيف السطح.
1. رسم قلب دائري.
1. رسم مضلع ملون وحفظ الصورة.

### **عينات البرمجة**
#### **إنشاء صورة**
ابدأ بإنشاء صورة باستخدام أي من الطرق الموصوفة في إنشاء الملفات.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}

#### **إنشاء وتهيئة كائن Graphics**
ثم قم بإنشاء وتهيئة كائن Graphics عن طريق تمرير كائن الصورة إلى مُنشئه.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}

#### **تنظيف السطح**
نظّف سطح الرسوميات عن طريق استدعاء طريقة Clear لفئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) وتمرير اللون كمعلمة. تملأ هذه الطريقة سطح الرسومات باللون الذي تم تمريره كوسيط.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

#### **رسم قلب دائري**
يمكنك ملاحظة أن فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) قد قامت بتعريض العديد من الطرق لرسم وملء الأشكال. ستجد القائمة الكاملة للطرق في مرجع API Aspose.PSD لـ .NET. تم عرض العديد من إصدارات طريقة DrawEllipse المعرضة بواسطة فئة Graphics. تقبل جميع هذه الطرق كائن Pen كمعلمة أولى. يتم تمرير المعلمات لاحقًا لتحديد المستطيل المحيط بالقلب الدائري. لأجل هذا المثال استخدم الإصدار الذي يقبل كائن Rectangle كمعلمة ثانية لرسم قلب دائري باستخدام كائن Pen باللون المرغوب.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}

#### **رسم مضلع ملون**
ثم رسم مضلع باستخدام LinearGradientBrush ومصفوفة نقاط. فئة Graphics قد عرضت العديد من الإصدارات المعرضة لطريقة FillPolygon(). تقبل كل هذه كائن Brush كمعلمة أولى، تعريف خصائص الملء. المعلمة الثانية هي مصفوفة من النقاط. يرجى ملاحظة أن كل نقطتين متتاليتين في المصفوفة تحددان جانبًا من المضلع.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

### **رسم الصور باستخدام الرسومات: المصدر الكامل**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

يتم إنشاء جميع الفئات التي تنفذ IDisposable والتي تصل إلى موارد غير قيّدة في عبارة Using للتأكد من التخلص منها بشكل صحيح.