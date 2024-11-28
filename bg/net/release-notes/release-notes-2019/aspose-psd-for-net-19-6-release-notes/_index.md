---
title: Aspose.PSD за .NET 19.6 - Бележки за изданието
type: docs
weight: 70
url: /bg/net/aspose-psd-za-net-19-6-belejki-za-izdanieto/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-127|Възможност за преобразуване на PSD файл в PSB и обратно|Функционалност|
|PSDNET-154|Пренасяне на входни данни от Aspose.Imaging 19.5 в Aspose.PSD|Подобрение|
|PSDNET-155|Почистване на публичния API, свързан с Aspose.PSD|Подобрение|
|PSDNET-159|Премахване на свойството IsLicensed|Подобрение|
|PSDNET-102|Преобразуване на PSB в JPG се забавя|Проблем|
|PSDNET-150|Ново добавеният текстов слой се измества при редакция в Photoshop|Проблем|

## **Промени в публичното API**
# **Добавени API:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F:Aspose.PSD.FileFormat.Cdr
- F:Aspose.PSD.FileFormat.Cmx
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P:Aspose.PSD.Image.BufferSizeHint
- P:Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M:Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P:Aspose.PSD.LoadOptions.BufferSizeHint
- T:Aspose.PSD.MemoryManagement.Configuration
- P:Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T:Aspose.PSD.ResolutionUnit
- F:Aspose.PSD.ResolutionUnit.None
- F:Aspose.PSD.ResolutionUnit.Inch
- F:Aspose.PSD.ResolutionUnit.Cm
# **Премахнати API:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
,...
- M:Aspose.PSD.Matrix.op_Inequality(Aspose.PSD.Matrix,Aspose.PSD.Matrix)

## **Примери за използване:**
**PSDNET-127. Възможност за преобразуване на PSD файл в PSB и обратно**

{{< highlight java >}}

 // Възможност за преобразуване на PSD файл в PSB и обратно

            string sourceFilePathPsb = "2layers.psb";

            string outputFilePathPsd = "ConvertFromPsb.psd";

            using (Image img = Image.Load(sourceFilePathPsb))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psd };

                img.Save(outputFilePathPsd, options);

            }

            string sourceFilePathPsd = "2layers.psd";

            string outputFilePathPsb = "ConvertFromPsd.psb";

            using (Image img = Image.Load(sourceFilePathPsd))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psb };

                img.Save(outputFilePathPsb, options);

            }

{{< /highlight >}}

**PSDNET-102. Проблем при преобразуване на PSB в JPG**

{{< highlight java >}}

  // Проблем при преобразуване на PSB в JPG          

            string[] sourceFileNames = new string[] { 

                //Test files with layers

                "Little",

                "Simple",

                //Test files without layers

                "psb",

                "psb3"

            };

            var options = new PsdLoadOptions();

            foreach (var fileName in sourceFileNames)

            {

                var sourceFileName = fileName + ".psb";

                using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

                {

                    // All jpeg and psd files must be readable

                    image.Save(fileName + "_output.jpg", new JpegOptions() { Quality = 95 });

                    image.Save(fileName + "_output.psb");

                }

            }             

{{< /highlight >}}

**PSDNET-150: Ново добавеният текстов слой се измества при редакция в Photoshop**

{{< highlight java >}}

             // Ново добавеният текстов слой се измества при редакция в Photoshop

    string sourceFileName = "OneLayer.psd";

    string exportPath = "OneLayer_Edited.psd";

    int leftPos = 99;

    int topPos = 47;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        im.AddTextLayer("Some text", new Rectangle(leftPos, topPos, 99, 47));

        TextLayer textLayer = (TextLayer)im.Layers[1];

        if (textLayer.Left != leftPos || textLayer.Top != topPos) 

        {

            throw new Exception("Was created incorrect Text Layer");

        }

        // We can't test Transform Matrix with a public API,

        // but if we start edit text layer in PSD we should get the same bounds as we created

        im.Save(exportPath);

    }

{{< /highlight >}}**PSDNET-154. Пренасяне на входни данни от Aspose.Imaging 19.5 в Aspose.PSD**

{{< highlight java >}}

 // Пренасяне на входни данни от Aspose.Imaging 19.5 в Aspose.PSD

Console.WriteLine("Това е само пример.");

{{< /highlight >}}

**PSDNET-155. Почистване на публичния API, свързан с Aspose.PSD**

{{< highlight java >}}

 // Почистване на публичния API, свързан с Aspose.PSD

Console.WriteLine("Това е само пример.");

{{< /highlight >}}

**PSDNET-159. Премахване на свойството IsLicensed**

{{< highlight java >}}

 // Премахване на свойството IsLicensed

Console.WriteLine("Това е само пример.");

{{< /highlight >}}
