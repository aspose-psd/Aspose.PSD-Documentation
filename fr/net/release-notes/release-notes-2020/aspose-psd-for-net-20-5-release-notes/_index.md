---
title: Aspose.PSD pour .NET 20.5 - Notes de publication
type: docs
weight: 80
url: /fr/net/aspose-psd-pour-net-20-5-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-595|Prise en charge des masques de calque pour les groupes de calques|Fonctionnalité|
|PSDNET-201|Prise en charge de la progression de conversion de document|Fonctionnalité|
|PSDNET-275|Prise en charge de la ressource Nvrt (Ressource de calque d'ajustement inversée)|Fonctionnalité|
|PSDNET-124|Prise en charge de l'enregistrement d'image PSD en mode couleur niveau de gris avec 16 bits par canal|Fonctionnalité|
|PSDNET-589|Refactorisation des exemples sur GitHub|Améliorations|
|PSDNET-587|L'alignement du texte via ITextPortion ne fonctionne pas pour les langues de droite à gauche. Le fichier de sortie est endommagé.|Erreur|
|PSDNET-604|Exception lors de la tentative d'ouverture d'un fichier Psd particulier avec Lab Color et 8 bits/chaîne|Erreur|
|PSDNET-598|Correction de l'enregistrement d'une image PSD en mode couleur niveau de gris 16 bits par canal en mode PSD niveau de gris 8 bits par canal|Erreur|
|PSDNET-599|Correction de l'enregistrement d'une image PSD en mode couleur niveau de gris 16 bits par canal en format PSD RVB 16 bits par canal|Erreur|

## **Changements d'API publique**
# **APIs ajoutées :**
- Aucune
# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**
**PSDNET-595. Prise en charge des masques de calque pour les groupes de calques**

{{< highlight java >}}

 string srcFile = "psdnet595.psd";

string outputPng = "output.png";

string outputPsd = "output.psd";

using (var input = (PsdImage)Image.Load(srcFile))

{

     input.Save(outputPng, new PngOptions());

     input.Save(outputPsd);

}

{{< /highlight >}}

**PSDNET-201. Prise en charge de la progression de conversion de document**

{{< highlight java >}}

 string sourceFilePath = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)

{

      string message = string.Format(

           "{0} {1}: {2} sur {3}",

           progressInfo.Description,

           progressInfo.EventType,

           progressInfo.Value,

           progressInfo.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- Chargement de Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

      Console.WriteLine("---------- Enregistrement de Apple.psd au format PNG ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Enregistrement de Apple.psd au format PSD ----------");

      image.Save(

           outputStream,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = localProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-275. Prise en charge de la ressource Nvrt (Ressource de calque d'ajustement inversée)**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load("InvertAdjustmentLayer.psd"))

{

      foreach (var layer in psdImage.Layers)

      {

           if (layer is InvertAdjustmentLayer)

           {

                 foreach (var layerResource in layer.Resources)

                 {

                      if (layerResource is NvrtResource)

                      {

                           // La ressource Nvrt est prise en charge.

                           var resource = (NvrtResource)layerResource;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. Correction de l'enregistrement d'une image PSD en mode couleur niveau de gris 16 bits par canal en mode PSD niveau de gris 8 bits par canal**

{{< highlight java >}}

 void SaveToPsdThenLoadAndSaveToPng(

    string file,

    ColorModes colorMode,

    short channelBitsCount,

    short channelsCount,

    CompressionMethod compression,

    int layerNumber)

{

    string filePath = file + ".psd";

    string postfix = colorMode.ToString() + channelBitsCount + "_" + channelsCount + "_" + compression;

    string exportPath = @"Output\" + file + postfix + ".psd";

    PsdOptions psdOptions = new PsdOptions()

    {

        ColorMode = colorMode,

        ChannelBitsCount = channelBitsCount,

        ChannelsCount = channelsCount,

        CompressionMethod = compression

    };

    using (PsdImage image = (PsdImage)Image.Load(filePath))

    {

        RasterCachedImage raster = layerNumber >= 0 ? (RasterCachedImage)image.Layers[layerNumber] : image;

        Aspose.PSD.Graphics graphics = new Graphics(raster);

        int width = raster.Width;

        int height = raster.Height;

        Rectangle rect = new Rectangle(

            width / 3,

            height / 3,

            width - (2 * (width / 3)) - 1,

            height - (2 * (height / 3)) - 1);

        graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

        image.Save(exportPath, psdOptions);

    }

    string pngExportPath = Path.ChangeExtension(exportPath, "png");

    using (PsdImage image = (PsdImage)Image.Load(exportPath))

    {

        // Il ne devrait y avoir aucune exception.

        image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

    }

}

SaveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, 16, 5, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SaveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SaveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDNET-587. L'alignement du texte via ITextPortion ne fonctionne pas pour les langues de droite à gauche. Le fichier de sortie est endommagé.**

{{< highlight java >}}

 string sourceFileName = "bidi.psd";

string outputFileName = "bidiOutput.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    var layer = (TextLayer)image.Layers[2];

    var portions = layer.TextData.Items;

    portions[0].Paragraph.Justification = 2;

    layer.TextData.UpdateLayerData();

    image.Save(outputFileName);

}

{{< /highlight >}}

` `**PSDNET-604. Exception lors de la tentative d'ouverture d'un fichier Psd particulier avec Lab Color et 8 bits/chaîne**

{{< highlight java >}}

 string srcFile = "Untitled-1.psd";

string outputFilePsd = "output.psd";

using (var psdImage = (PsdImage)Image.Load(srcFile))

{

    psdImage.Save(outputFilePsd);

}

// Le fichier LAB est chargé et enregistré sans lever d'exceptions.

{{< /highlight >}}

**PSDNET-598. Correction de l'enregistrement d'une image PSD en mode couleur niveau de gris 16 bits par canal en mode PSD niveau de gris 8 bits par canal**

{{< highlight java >}}

 string sourceFileName = "grayscale16bit.psd";

string exportFileName = "grayscale16bit_output.psd";

PsdOptions psdOptions = new PsdOptions()

{

    ColorMode = ColorModes.Grayscale,

    ChannelBitsCount = 8,

    ChannelsCount = 2

};

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    RasterCachedImage raster = image.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int width = raster.Width;

    int height = raster.Height;

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

    image.Save(exportFileName, psdOptions);

}

string pngExportPath = Path.ChangeExtension(exportFileName, "png");

using (PsdImage image = (PsdImage)Image.Load(exportFileName))

{

    // Il ne devrait y avoir aucune exception.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

**PSDNET-599. Correction de l'enregistrement d'une image PSD en mode couleur niveau de gris 16 bits par canal en format PSD RVB 16 bits par canal**

{{< highlight java >}}

 string sourceFileName = "grayscale16bit.psd";

string exportFileName = "grayscale16bit_output.psd";

PsdOptions psdOptions = new PsdOptions()

{

    ColorMode = ColorModes.Rgb,

    ChannelBitsCount = 8,

    ChannelsCount = 4

};

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    RasterCachedImage raster = image.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int width = raster.Width;

    int height = raster.Height;

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

    image.Save(exportFileName, psdOptions);

}

string pngExportPath = Path.ChangeExtension(exportFileName, "png");

using (PsdImage image = (PsdImage)Image.Load(exportFileName))

{

    // Il ne devrait y avoir aucune exception.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}
