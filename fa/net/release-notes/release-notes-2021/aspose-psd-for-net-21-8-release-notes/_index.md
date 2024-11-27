---
title: یادداشت های نسخه Aspose.PSD برای .NET 21.8
type: docs
weight: 50
url: /fa/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت های نسخه [Aspose.PSD برای .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/) می باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-698|پشتیبانی از روش های فشرده سازی ZipWithPrediction|ویژگی|
|PSDNET-663|فاصله متن نادرست در PSD تولید شده می باشد|خطا|
|PSDNET-685|استثنا در هنگام ذخیره سازی PSD|خطا|
|PSDNET-927|فاصله نادرست بین خطوط و نمادها در Aspose.PSD زمان استفاده از آن بدون لایسنس|خطا|

## **تغییرات در API عمومی**
# **API های اضافه شده:**
- هیچ

# **API های حذف شده:**
- هیچ

## **مثال های استفاده:**

**PSDNET-663. فاصله متن نادرست در PSD تولید شده می باشد**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. استثنا در هنگام ذخیره سازی PSD**

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

**PSDNET-698. پشتیبانی از روش های فشرده سازی ZipWithPrediction**

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

**PSDNET-927. فاصله نادرست بین خطوط و نمادها در Aspose.PSD زمان استفاده از آن بدون لایسنس**

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
