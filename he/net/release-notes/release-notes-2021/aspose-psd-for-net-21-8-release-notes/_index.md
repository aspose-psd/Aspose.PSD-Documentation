---
title: Aspose.PSD עבור .NET 21.8 - רשומות שחרור
type: docs
weight: 50
url: /he/net/aspose-psd-עבור-net-21-8-רשומות-שחרור/
---

{{% alert color="primary" %}} 

דף זה מכיל רשומות שחרור עבור [Aspose.PSD עבור .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**ראשי**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-698|תמיכה בשיטות דחיסה ZipWithPrediction|תכונה|
|PSDNET-663|הרווח בין הטקסט אינו נכון ב-PSD שנוצר|באג|
|PSDNET-685|חריגה בעת שמירת PSD|באג|
|PSDNET-927|מרחק שגוי בין שורות וסמלים ב-Aspose.PSD כאשר משתמשים בו בלי רישיון|באג|

## **שינויים ב-API הציבורי**
# **APIs שנוספו:**
- אף אחד

# **APIs שהוסרו:**
- אף אחד

## **דוגמאות שימוש:**

**PSDNET-663. הרווח בין הטקסט אינו נכון ב-PSD שנוצר**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. חריגה בעת שמירת PSD**

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

**PSDNET-698. תמיכה בשיטות דחיסה ZipWithPrediction**

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

**PSDNET-927. מרחק שגוי בין שורות וסמלים ב-Aspose.PSD כאשר משתמשים בו בלי רישיון**

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
