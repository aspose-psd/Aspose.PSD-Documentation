---
title: Aspose.PSD עבור .NET 20.5 - דוח שחרור
type: docs
weight: 80
url: /he/net/aspose-psd-for-net-20-5-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל את דוחות השחרור עבור [Aspose.PSD עבור .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-595|תמיכה במסכות שכבה עבור קבוצות שכבות|תכונה|
|PSDNET-201|תמיכה בהתקדמות המרה של מסמך|תכונה|
|PSDNET-275|תמיכה במשאב Nvrt (רסור שכבת התאמה להפוך)|תכונה|
|PSDNET-124|תמיכה בשמירת תמונת מצב גווניות Grayscale PSD עם 16 ביט לערוץ|תכונה|
|PSDNET-589|ריפוי דוגמאות ב-GitHub|שיפור|
|PSDNET-587|יישום יישור טקסט דרך ITextPortion לא עובד לשפות מימין לשמאל. הקובץ המוצאים נפגמים.|באג|
|PSDNET-604|חריגה כאשר מנסים לפתוח קובץ Psd מסוים עם צבע Lab ו-8 ביט לערוץ|באג|
|PSDNET-598|תיקון שמירת תמונת PSD עם מצב גווניות Grayscale עם 16 ביט לערוץ לתבנית Grayscale 8 ביט לערוץ|באג|
|PSDNET-599|תיקון שמירת תמונת PSD עם מצב גווניות Grayscale עם 16 ביט לערוץ לתבנית RGB 16 ביט לערוץ|באג|

## **שינויים ב-API הציבוריים**
# **APIs שהתווספו:**
- אין
# **APIs שהוסרו:**
- אין

## **דוגמאות שימוש:**
**PSDNET-595. תמיכה במסכות שכבה עבור קבוצות שכבות**

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

**PSDNET-201. תמיכה בהתקדמות המרה של מסמך**

{{< highlight java >}}

 string sourceFilePath = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)

{

      string message = string.Format(

           "{0} {1}: {2} מתוך {3}",

           progressInfo.Description,

           progressInfo.EventType,

           progressInfo.Value,

           progressInfo.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- טוען את Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

      Console.WriteLine("---------- שומר את Apple.psd לתבנית PNG ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- שומר את Apple.psd לתבנית PSD ----------");

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

**PSDNET-275. תמיכה במשאב Nvrt (רסור שכבת התאמה להפוך)**

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

                           // המשאב Nvrt נתמך.

                           var resource = (NvrtResource)layerResource;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. תיקון שמירת תמונת PSD עם מצב גווניות Grayscale עם 16 ביט לערוץ לתבנית Grayscale 8 ביט לערוץ**

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

        // לא צריך להיות חריגה כאן.

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

**PSDNET-587. יישור טקסט דרך ITextPortion לא עובד לשפות מימין לשמאל. הקובץ המוצאים נפגמים.**

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

` `**PSDNET-604. חריגה כאשר מנסים לפתוח קובץ Psd מסוים עם צבע Lab ו-8 ביט לערוץ**

{{< highlight java >}}

 string srcFile = "Untitled-1.psd";

string outputFilePsd = "output.psd";

using (var psdImage = (PsdImage)Image.Load(srcFile))

{

    psdImage.Save(outputFilePsd);

}

// קובץ LAB נטען ושמור ללא הרצת חריגות.

{{< /highlight >}}

**PSDNET-598. תיקון שמירת תמונת PSD עם מצב גווניות Grayscale עם 16 ביט לערוץ לתבנית Grayscale 8 ביט לערוץ**

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

    // לא צריך להיות חריגה כאן.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

**PSDNET-599. תיקון שמירת תמונת PSD עם מצב גווניות Grayscale עם 16 ביט לערוץ לתבנית RGB 16 ביט לערוץ**

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

    // לא צריך להיות חריגה כאן.

    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}
