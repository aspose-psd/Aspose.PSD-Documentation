---
title: Note sulla versione Aspose.PSD for .NET 19.6
type: docs
weight: 70
url: /it/net/aspose-psd-for-net-19-6-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD for .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-127|Possibilità di convertire file PSD in PSB e viceversa|Caratteristica|
|PSDNET-154|Porting delle sorgenti Aspose.Imaging 19.5 in Aspose.PSD|Miglioramento|
|PSDNET-155|Rimozione dell'API pubblica relativa ad Aspose.PSD|Miglioramento|
|PSDNET-159|Rimozione della proprietà IsLicensed|Miglioramento|
|PSDNET-102|La conversione di PSB in JPG si blocca|Baco|
|PSDNET-150|La posizione del nuovo layer di testo aggiunto si sposta durante la modifica in Photoshop|Baco|

## **Modifiche all'API pubblica**
# **API Aggiunte:**
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
# **API Rimosse:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapCoreHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeaderSizeV5
- T:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapCompression
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapImageSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapXPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapYPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsUsed
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsImportant
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.ExtraBitMasks
- T:Aspose.PSD.FileFormats.Bmp.BitmapV4Header
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.RedMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GreenMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.BlueMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.AlphaMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.CSType
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.Endpoints
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GammaRed
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GammaGreen
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GammaBlue
- T:Aspose.PSD.FileFormats.Bmp.BitmapV5Header
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.Intent
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.ProfileData
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.ProfileSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.Reserved
- T:Aspose.PSD.FileFormats.Bmp.BmpImage
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.String)

## **Esempi di utilizzo:**
**PSDNET-127. Possibilità di convertire file PSD in PSB e viceversa**

{{< highlight java >}}

 // Possibilità di convertire file PSD in PSB e viceversa

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

**PSDNET-102. Conversione PSB in JPG si blocca**

{{< highlight java >}}

  // Conversione PSB in JPG si blocca        

            string[] sourceFileNames = new string[] { 

                //File di test con layers

                "Little",

                "Simple",

                //File di test senza layers

                "psb",

                "psb3"

            };

            var options = new PsdLoadOptions();

            foreach (var fileName in sourceFileNames)

            {

                var sourceFileName = fileName + ".psb";

                using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

                {

                    // Tutti i file jpeg e psd devono essere leggibili

                    image.Save(fileName + "_output.jpg", new JpegOptions() { Quality = 95 });

                    image.Save(fileName + "_output.psb");

                }

            }             

{{< /highlight >}}

**PSDNET-150: La posizione del nuovo layer di testo aggiunto si sposta durante la modifica in Photoshop**

{{< highlight java >}}

             // La posizione del nuovo layer di testo aggiunto si sposta durante la modifica in Photoshop

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

            throw new Exception("È stato creato un layer di testo incorretto");

        }

        // Non possiamo testare la matrice di trasformazione con un'API pubblica,

        // ma se iniziamo a modificare il layer di testo in PSD dovremmo ottenere gli stessi limiti che abbiamo creato

        im.Save(exportPath);

    }

{{< /highlight >}}**PSDNET-155: Rimozione dell'API pubblica relativa ad Aspose.PSD**

{{< highlight java >}}

// Rimozione dell'API pubblica relativa ad Aspose.PSD

PsdImage image = (PsdImage)Image.Load("source.psd");

image.Compression = CompressionMethod.Jpeg;

var options = new JpegOptions();

image.Save("output.jpg", options);

image.Dispose();

{{< /highlight >}}

**PSDNET-159: Rimozione della proprietà IsLicensed**

{{< highlight java >}}

// Rimozione della proprietà IsLicensed

PsdImage image = (PsdImage)Image.Load("licensed.psd");

if (image.IsLicensed)

{

    Console.WriteLine("Il file è con licenza.");

}

else

{

    Console.WriteLine("Il file non è con licenza.");

}

image.Dispose();

{{< /highlight >}}

**Modifiche all'API pubblica:**

# **API Aggiunte:**

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

# **API Rimosse:**

- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapCoreHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderFullSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV2
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV3
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV4
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV5
- T:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapCompression
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapImageSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapXPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapYPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsUsed
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsImportant

Continua...