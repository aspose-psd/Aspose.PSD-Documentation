---
title: Aspose.PSD для .NET 21.8 - Примечания к выпуску
type: docs
weight: 50
url: /ru/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания о выпуске [Aspose.PSD для .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-698|Поддержка методов сжатия ZipWithPrediction|Функциональность|
|PSDNET-663|Некорректный интервал между текстом в созданном PSD файле|Ошибка|
|PSDNET-685|Исключение при сохранении PSD|Ошибка|
|PSDNET-927|Некорректное расстояние между строками и символами в Aspose.PSD при использовании без лицензии|Ошибка|

## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

## **Примеры использования:**

**PSDNET-663. Некорректный интервал между текстом в созданном PSD файле**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Исключение при сохранении PSD**

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

**PSDNET-698. Поддержка методов сжатия ZipWithPrediction**

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

**PSDNET-927. Некорректное расстояние между строками и символами в Aspose.PSD при использовании без лицензии**

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
