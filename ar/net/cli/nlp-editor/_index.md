---
title: تطبيق محرر Aspose.PSD CLI NLP لـ .NET
type: docs
weight: 10
url: /ar/net/cli/nlp-editor/
is_root: false
keywords: أداة CLI لـ Photoshop, NLP, معالجة اللغة الطبيعية, PSD, وحدة التحكم, مكتبة C#, API PSD
description: تطبيق Aspose.PSD CLI NLP Editor القائم على Aspose.PSD لـ تنسيقات الملفات PSD, PSB, و AI. تأمين لعمليات CI/CD بدون كود. يدعم معالجة اللغة الطبيعية لتحرير ملفات PSD. فقط اكتب طلبك باللغة الطبيعية لتنفيذ مختلف العمليات مثل التحويل، التعديل، التغيير في الحجم، وأكثر من ذلك. لا يتطلب التطبيق تثبيت Adobe Photoshop أو Adobe Illustrator ويمكن تشغيله من الوحدة دون رمز إضافي.

---
**![شعار المنتج Aspose.PSD لـ .NET](home_1.png)**

**مرحبًا بك في تطبيق محرر Aspose.PSD NLP CLI لـ .NET**

تطبيق Aspose.PSD CLI NLP Editor هو أداة وحدة تحكم خفيفة لتحرير ملفات PSD باستخدام أوامر اللغة الطبيعية. سهلة الدمج في أنابيب CI/CD.

**إخلاء المسؤولية**

هذا تطبيق تجريبي. يُرجى تجربته وتقديم الملاحظات. أي تعليق يُقدر بشدة. نحن نريد أن نصل بالتطبيق بدون رمز إلى المستوى التالي. الدمج السهل في أي أنبوب بناء أو عملية تجارية هو هدفنا.

**الوظائف الرئيسية لتطبيق محرر Aspose.PSD NLP CLI لـ .NET**

1. تنفيذ عمليات على ملفات PSD, PSB, AI باستخدام أوامر اللغة الطبيعية.
2. يدعم مختلف العمليات مثل التحويل، التعديل، تغيير الحجم، وأكثر.
3. تأمين CI/CD بدون كود.
4. يدعم كتابة الطلبات باللغة الطبيعية لتحرير ملفات PSD.

## **الاستخدام من خط الأوامر:**

{{% alert color="primary" %}}
أولاً قم بتثبيت هذه الأداة dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

نوصي قبل الاستخدام الأول بتشغيل الأمر التالي:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
بعد هذا الأمر، ستتمكن من تشغيل التطبيق باسم مختصر هو nlp.cli بدلاً من Aspose.PSD.CLI.NLP.Editor. يمكنك تحديد اسم مختصر خاص بك.
{{% /alert %}}

**المعلمات المتاحة لـ تطبيق Aspose.PSD.CLI.Crop**

| **المعلمة** | **الوصف**                         |
|:-------------|:----------------------------------------|
| أي نص     | إلزامي. أمرك باللغة الطبيعية لتحديث ملف PSD أو PSB      |
| الترخيص      | مسار الترخيص.                    |
| مفصل      | عرض معلومات إضافية حول أمر محدد. |
| الإعداد        | إنشاء ملف bat في مجلد الأدوات لاستدعاء سريع من الوحدة. مثال: --setup psd.nlp. ثم يمكنك استدعاء الأداة بالأمر psd.nlp |

**أمثلة على الاستخدام**

1. سيحوّل هذا الأمر الملف الأول الذي تم العثور عليه (الذي يمكن فتحه بواسطة aspose.psd) من المجلد الحالي وسيحفظه بتنسيق png بشفافية. كما سيتم إعداد الترخيص. يجب عليك تحديد الترخيص مرة واحدة فقط. سيرتك القادمة ستُستخدم فيها الترخيص من المسار المحدد. سيعرض هذا الأمر سجل NLP المفصّل إذا كان متوفرًا.
{{< highlight bash >}}
  nlp.cli تحويل الملف من هذا المجلد إلى تنسيق png مع ألفا --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. سيجد هذا الأمر الملف بأقرب اسم إلى "smth.psd". ثم سيرفع التباين وسيحفظه إلى jpeg بأفضل جودة. سيُطبع اسم الملف الناتج. سيكون smth.jpg
{{< highlight bash >}}
ضبط التباين على 10% للطبقة ذات الاسم ellipse في الملف smth.psd وحفظه إلى output.jpg بأفضل جودة
{{< /highlight >}}

3. سيرفع هذا الأمر ملفًا في المسار المحدد، وسيقلل حجمه بنسبة 25%. سيُطبع الملف الناتج. سيتم حفظه في المجلد الحالي للوحة التحكم.
{{< highlight bash >}}
تحديد حجم ملف C:\Users\someuser\Desktop\input.psd بنسبة 25%
{{< /highlight >}}

4. سيجد هذا الأمر الملف input.psd في C:\Users\someuser\Desktop\. ثم سيجد طبقة بفهرس 3 وسيغير حجمها إلى عرض 50 بكسل وطول 100 بكسل. سيتم حفظ هذه الطبقة باسم PDF في C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
ضبط حجم الطبقة ذات الفهرس 3 من C:\Users\someuser\Desktop\input.psd إلى عرض 50 وطول 100 وحفظها إلى C:\Users\someuser\Desktop\output.pdf
{{< /highlight >}}

5. سيفتح هذا الأمر ملف smth.psd في المجلد الحالي، ولكن ستتم تعطيل جميع التأثيرات. ثم سيتم تحويل هذا الملف إلى تنسيق BMP وكملف output.bmp في المجلد الحالي.
{{< highlight bash >}}
فتح smth.psd بدون تأثيرات وحفظه بتنسيق output.bmp
{{< /highlight >}}

**يرجى التحقق من تطبيقات [Aspose.PSD CLI](https://docs.aspose.com/psd/net/cli) لـ .NET الأخرى إذا كنت بحاجة إلى إضافة دعم لتنسيقات PSD, PSB, و AI إلى سير عملك**

1. [Aspose.PSD CLI تحويل](/psd/ar/net/cli/convert)
2. [Aspose.PSD CLI قص](/psd/ar/net/cli/crop)
3. [Aspose.PSD CLI تغيير الحجم](/psd/ar/net/cli/resize)
4. [Aspose.PSD CLI تصدير](/psd/ar/net/cli/export)
5. [Aspose.PSD CLI محرر NLP](/psd/ar/net/cli/nlp-editor)

**يرجى التحقق من Aspose.PSD لـ .NET أو [المنصات الأخرى]**

تطبيقات Aspose.PSD CLI هي حلاً جاهزًا للعمليات الشائعة. إذا كنت بحاجة إلى حلاً مرنًا، يرجى التحقق من الإصدار الكامل لـ Aspose.PSD

1. [Aspose.PSD لـ .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD لـ Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD لـ Python via .NET](https://releases.aspose.com/psd/python-net/)

## **موارد Aspose.PSD لـ .NET**

فيما يلي روابط لبعض الموارد المفيدة التي قد تحتاجها لإتمام مهامك.

- [توثيق الإصدارات الجديدة عبر الإنترنت لـ Aspose.PSD CLI لـ .NET](/psd/ar/net/cli/conversion)
- [ملاحظات الإصدار لتطبيقات Aspose.PSD CLI لـ .NET](/psd/ar/net/cli/conversion/release-notes/)
- [صفحة المنتج لـ Aspose.PSD لـ تطبيقات Aspose.PSD CLI لـ .NET](https://products.aspose.com/psd/net/cli)
- [دليل مرجعي لـ Aspose.PSD لـ .NET API](https://reference.aspose.com/net/psd)
- [تحميل أمثلة من مستودع GitHub](https://github.com/aspose-psd/CLI-Applications)
- [منتدى الدعم المجاني لـ Aspose.PSD لـ .NET](https://forum.aspose.com/c/psd)
- [مكتب المساعدة للدعم المدفوع لـ Aspose.PSD لـ .NET](https://helpdesk.aspose.com/)

