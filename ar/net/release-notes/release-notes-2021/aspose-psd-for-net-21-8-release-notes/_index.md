---
title: ملاحظات الإصدار لـ Aspose.PSD لـ .NET 21.8
type: docs
weight: 50
url: /ar/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-698|دعم طرق الضغط ZipWithPrediction|ميزة|
|PSDNET-663|تباعد غير صحيح للنص في PSD المُنشأ|خلل|
|PSDNET-685|استثناء عند حفظ PSD|خلل|
|PSDNET-927|تباعد غير صحيح بين الأسطر والرموز في Aspose.PSD عند استخدامها بدون ترخيص|خلل|

## **التغيرات العامة في واجهة برمجة التطبيقات**
# **الواجهات البرمجية المضافة:**
- لا شيء

# **الواجهات البرمجية المحذوفة:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDNET-663. تباعد غير صحيح للنص في PSD المُنشأ**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. استثناء عند حفظ PSD**

{{< highlight csharp >}}
            string sourceFileName = "File.psd";
            string outputFileName = "File2.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                var layer1 = (TextLayer)image.Layers[1];
                layer1.TextData.UpdateLayerData();

                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-698. دعم طرق الضغط ZipWithPrediction**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";

            string outputPng = "output.png";
            string outputRaw = "out_Raw.psd";
            string outputZip = "out_Zip.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(outputPng, new PngOptions());

                image.Save(outputRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                image.Save(outputZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. تباعد غير صحيح بين الأسطر والرموز في Aspose.PSD عند استخدامها بدون ترخيص**

{{< highlight csharp >}}
            bool[] licenseStates = new bool[] { false, true };
            for (int i = 0; i < licenseStates.Length; i++)
            {
                bool testLicense = licenseStates[i];
                if (testLicense)
                {
                    License license = new License();
                    license.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string sourceFile = "psdnetTest927.psd";
                string outputFile = "out_" + testLicense.ToString() + "_psdnetTest927.png";

                using (var image = (PsdImage)Image.Load(sourceFile))
                {
                    image.Save(outputFile, new PngOptions());
                }
            }
{{< /highlight >}}