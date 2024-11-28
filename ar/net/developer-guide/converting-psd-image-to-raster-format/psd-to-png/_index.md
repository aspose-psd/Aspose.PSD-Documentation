---
title: تحويل PSD إلى PNG باستخدام C#
linktitle: PSD إلى PNG
type: docs
weight: 30
url: /ar/net/psd-to-png/
description: يمكن لـ C# .NET Photoshop Manipulation API تحويل من تنسيق PSD إلى تنسيق PNG باستخدام الرمز المقدم في هذه المقالة.
---

Aspose.PSD هو SDK لتنسيق PSD وواجهة برمجة التطبيقات لـ C# .NET Photoshop Manipulation API، الذي يمكنه التحويل من تنسيق PSD إلى تنسيق PNG.

لهذا التحويل من PSD يجب عليك استخدام الكود التالي بلغة C#:

الكود المعروض أدناه يوضح كيفية تحويل PSD إلى Png:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ConvertPsdToPng-ConvertPsdToPng.cs" >}}

يمكنك تحديد مستوى ضغط تنسيق Png من 0 إلى 9، حيث 9 هو أعلى درجة ضغط. يمكنك استخدام ضغط Png التدريجي وتغيير نوع الألوان لملف Png. [Png Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions) لديها خصائص مختلفة لأي حالة من حالات تصدير PSD.

استخدام ملف PNG شبه شفاف مع قناة ألفا لموقعك أو عملك هو حلا جيدًا. يمكن تصدير ملف Adobe Photoshop بشكل دقيق جدًا مع [وضع للقراءة فقط](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/readonlymode).

هنا مثال على ملف PSD المصدر الذي تم تصديره بـ [قناع مُطبَّق](https://docs.aspose.com/display/psdjava/Apply+Masking)، [طبقة بنص](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)، و [طبقة لون ملء شفافة](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.filllayers/filllayer) (Aspose.PSD تدعم جميع أنواع [طبقات ملء Adobe Photoshop](https://docs.aspose.com/display/psdjava/Support+of+Fill+Layers)). كما يمكنك رؤية [تأثير الظل](/ar/net/shadow-effects-in-psd-file/) على طبقة شكل PSD.

![todo:image_alt_text](psd-to-png_1.png)