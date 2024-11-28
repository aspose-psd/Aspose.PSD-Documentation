---
title: Notatki do wydania Aspose.PSD dla .NET 20.5
type: dokumentacja
weight: 80
url: /pl/net/aspose-psd-for-net-20-5-release-notes/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-595|Wsparcie dla Maski Warstwy dla Grup Warstw|Funkcja|
|PSDNET-201|Wsparcie dla postępu konwersji dokumentu|Funkcja|
|PSDNET-275|Wsparcie zasobu Nvrt (Zasób Warstwy Regulacji Odwrócenia)|Funkcja|
|PSDNET-124|Wsparcie dla zapisywania obrazu PSD w trybie koloru odcieni szarości z 16 bitami na kanał|Funkcja|
|PSDNET-589|Refaktoryzacja przykładów na GitHubie|Udoskonalenie|
|PSDNET-587|Wyrównywanie tekstu za pomocą ITextPortion doesn't work for right-to-left languages. The output file is damaged.|Błąd|
|PSDNET-604|Wyjątek podczas próby otwarcia określonego pliku Psd z kolorem Lab i 8 bitów na kanał|Błąd|
|PSDNET-598|Naprawienie zapisywania obrazu PSD w trybie koloru odcieni szarości z 16 bitami na kanał do formatu PSD odcieni szarości 8 bitów na kanał|Błąd|
|PSDNET-599|Naprawienie zapisywania obrazu PSD w trybie koloru odcieni szarości z 16 bitami na kanał do formatu PSD RGB 16 bitów na kanał|Błąd|


## **Zmiany w API Publicznym**
# **Dodane API:**
- Brak
# **Usunięte API:**
- Brak

## **Przykłady użycia:**
**PSDNET-595. Wsparcie dla Maski Warstwy dla Grup Warstw**

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

**PSDNET-201. Wsparcie dla postępu konwersji dokumentu**

{{< highlight java >}}

 string sourceFilePath = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)

{

      string message = string.Format(

           "{0} {1}: {2} z {3}",

           progressInfo.Description,

           progressInfo.EventType,

           progressInfo.Value,

           progressInfo.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- Wczytywanie Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

      Console.WriteLine("---------- Zapisywanie Apple.psd w formacie PNG ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Zapisywanie Apple.psd w formacie PSD ----------");

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

**PSDNET-275. Wsparcie zasobu Nvrt (Zasób Warstwy Regulacji Odwrócenia)**

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

                           // Zasób Nvrt jest obsługiwany.

                           var resource = (NvrtResource)layerResource;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. Napraw zapisywanie obrazu PSD w trybie koloru odcieni szarości z 16 bitami na kanał do formatu PSD odcieni szarości 8 bitów na kanał**

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

        // Tutaj nie powinno być wyjątku.

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

**PSDNET-587. Wyrównywanie tekstu za pomocą ITextPortion nie działa dla języków od prawej do lewej. Plik wyjściowy jest uszkodzony.**

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

`     `**PSDNET-604. Wyjątek podczas próby otwarcia określonego pliku Psd z kolorem Lab i 8 bitów na kanał**

{{< highlight java >}}

 string srcFile = "Untitled-1.psd";

string outputFilePsd = "output.psd";

using (var psdImage = (PsdImage)Image.Load(srcFile))

{

    psdImage.Save(outputFilePsd);

}

// Plik LAB został wczytany i zapisany bez rzucenia wyjątków.

{{< /highlight >}}

**PSDNET-598. Napraw zapisywanie obrazu PSD w trybie koloru odcieni szarości z 16 bitami na kanał do formatu PSD odcieni szarości 8 bitów na kanał**

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

    // Tutaj nie powinno być wyjątku.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

**PSDNET-599. Fix zapisywania obrazu PSD w trybie koloru odcieni szarości z 16 bitami na kanał do formatu PSD RGB 16 bitów na kanał**

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

    // Tutaj nie powinno być wyjątku.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}
