---
title: محرر Aspose.PSD لسطر الأوامر NLP لـ .NET 24.6 - ملاحظات الإصدار
type: docs
weight: 90
url: /ar/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD محرر سطر الأوامر NLP لـ .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **المفتاح** | **الملخص**                                                                                 | **الفئة**   |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | الإصدار الأولي لتطبيقات Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor |  تحسينات   |


## **أمثلة الاستخدام:**

**PSDNET-2110. الإصدار الأولي لتطبيق محرر Aspose.PSD CLI NLP**

## **الاستخدام من سطر الأوامر:**

{{% alert color="primary" %}}
قم أولاً بتثبيت هذه الأداة من dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

نوصي بتشغيل الأمر التالي قبل الاستخدام الأول:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
بعد تشغيل هذا الأمر، ستتمكن من تشغيل هذا التطبيق باستخدام الاسم القصير nlp.cli بدلاً من Aspose.PSD.CLI.NLP.Editor. يمكنك تحديد اسم قصير خاص بك.
{{% /alert %}}

**أمثلة على الاستخدام**

1. هذا الأمر سيقوم بتحويل الملف الأول الموجود (الذي يمكن فتحه باستخدام aspose.psd) من المجلد الحالي وسيحفظه بتنسيق png مع شفافية. كما سيتم تعيين الترخيص. تحتاج إلى تحديد الترخيص مرة واحدة فقط. سيتم استخدام الترخيص في التشغيلات القادمة من المسار المحدد. سيعرض هذا الأمر سجل الواضح لمعالجة NLP إذا كان متاحًا.
{{< highlight bash >}}nlp.cli تحويل الملف من هذا المجلد إلى تنسيق png بألفا --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. هذا الأمر سيجد الملف بأقرب اسم مماثل لـ "smth.psd". ثم سيعدل التباين وسيحفظه كملف jpeg بأفضل جودة. سيتم طباعة اسم ملف الإخراج. سيكون smth.jpg
{{< highlight bash >}}تعديل التباين بنسبة 10 على الطبقة رقم 10 بالاسم ellipse في الملف smth.psd وحفظه في output.jpg بأفضل جودة{{< /highlight >}}

3. هذا الأمر سيقوم بفتح ملف على المسار المحدد، وسيقلل حجمه إلى 25%. سيتم طباعة الملف الناتج. سيتم حفظه في المجلد الحالي من الوحدة النقطية.
{{< highlight bash >}}تغيير حجم الملف C:\Users\someuser\Desktop\input.psd إلى 25%{{< /highlight >}}

4. هذا الأمر سيجد ملف input.psd في C:\Users\someuser\Desktop\ . ثم سيجد الطبقة بفهرس 3 وسيقوم بتغيير حجمها إلى عرض 50 بكسل وارتفاع 100 بكسل. بعد ذلك سيتم حفظ هذه الطبقة كملف PDF في C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}تغيير حجم الطبقة بفهرس 3 من C:\Users\someuser\Desktop\input.psd إلى عرض 50 وارتفاع 100 وحفظه في C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. هذا الأمر سيفتح smth.psd في المجلد الحالي، لكن جميع التأثيرات ستكون معطلة. ثم سيتم تحويل هذا الملف إلى تنسيق BMP وكملف output.bmp في المجلد الحالي.
{{< highlight bash >}}فتح smth.psd بدون تأثيرات وحفظه كمخرج output.bmp{{< /highlight >}}

**تنويه**

هذا تطبيق تجريبي. يرجى تجربته وترك ملاحظاتك. أي تعليق يُقدر بشدة. نريد أن نأخذ تطبيق عدم التشفير إلى المستوى التالي. هدفنا هو التكامل السهل مع أي خط أنابيب بناء أو عملية تجارية.