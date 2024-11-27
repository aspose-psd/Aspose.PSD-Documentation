---
title: Aspose.PSD für Java 19.4 - Versionshinweise
type: docs
weight: 20
url: /de/java/aspose-psd-fur-java-19-4-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für Aspose.PSD für Java 19.4

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-1|Möglichkeit, JPEG/PNG/etc. Bilddateien zu PsdImage ohne direktes Laden zu laden (was in Aspose.PSD nicht unterstützt wird)|Funktion|
|PSDJAVA-2|Unterstützung des RGB-Farbmodus mit 16 Bits/Kanal (64 Bits pro Farbe)|Funktion|
|PSDJAVA-3|Unterstützung von Ebenen-Vektormasken und benutzerdefinierte FlipRotate-Textebene|Funktion|
|PSDJAVA-4|Alle asiatischen Zeichen werden nicht korrekt gerendert|Fehler|
|PSDJAVA-5|\r\n-Symbole werden als doppelte Zeilenumbrüche interpretiert, was falsch ist|Fehler|
|PSDJAVA-6|Wenn eine Textebene mit einem String aktualisiert wird, der Zeilenumbrüche enthält, wird die PSD-Datei unlesbar|Fehler|
|PSDJAVA-7|Wenn eine Textebene mit einem String aktualisiert wird, der Tabulatoren enthält, schlägt die Verarbeitung mit einer Ausnahme fehl|Fehler|
# **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **Entfernte APIs:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTrailer
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsPaletteSorted
- P:Aspose.PSD.FileFormats.Gif.GifImage.PaletteColorResolutionBits
- P:Aspose.PSD.FileFormats.Gif.GifImage.Width
- P:Aspose.PSD.FileFormats.Gif.GifImage.Height
- P:Aspose.PSD.FileFormats.Gif.GifImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.GifImage.Blocks
- P:Aspose.PSD.FileFormats.Gif.GifImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColorIndex
- P:Aspose.PSD.FileFormats.Gif.GifImage.PixelAspectRatio
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsCached
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.TransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasBackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.ImageOpacity
- M:Aspose.PSD.FileFormats.Gif.GifImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.CacheData
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.OrderBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.ClearBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.InsertBlock(System.Int32,Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AddBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RemoveBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Grayscale
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceNonTransparentColors(System.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double,System.Int32)
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasAlpha
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.FileFormat
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.PremultiplyComponents
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ByteOrder
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HorizontalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.VerticalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Frames
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Height
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Width
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.IsCached
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ExifData
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ImageOpacity
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.XmpData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AlignResolutions
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.SetResolution(System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.CacheData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Add(Aspose.PSD.FileFormats.Tiff.TiffImage)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrames(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.InsertFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeWidthProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeHeightProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Grayscale
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
# **Beispiel für die Verwendung:**

**PSDJAVA-1. Funktion zum Laden von JPEG/PNG/etc-Bilddateien in PsdImage ohne direktes Laden (nicht unterstützt in Aspose.PSD)**

{{< highlight java >}}

 String dateipfad = "PsdBeispiel.psd";

    String ausgabedateipfad = "PsdErgebnis.psd";

    PsdImage bild = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(dateipfad);

         try 

         {

              Layer ebene = null;

              try

              {

                  ebene = new Layer((RasterImage)im);

                  bild.addLayer(ebene);

                  bild.save(ausgabedateipfad);

              }

              catch

              {

                  if (ebene != null)

                  {

                       ebene.dispose();

                  }

                  throw;

              }

         }    

         finally 
         {
              im.dispose(); 
         }
    }

    finally

    {

         bild.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. Unterstützung des RGB-Farbmodus mit 16 Bits/Kanal (64 Bits pro Farbe)**

{{< highlight java >}}

  // Unterstützung des RGB-Farbmodus mit 16 Bits/Kanal (64 Bits pro Farbe)

        String quelleDateiName = "inRgb16.psd.psd";

        String ausgabedateipfadJpg = "outRgb16.jpg";

        String ausgabedateipfadPsd = "outRgb16.psd";

        PsdLoadOptions optionen = new PsdLoadOptions();

        PsdImage bild = (PsdImage)Image.load(quelleDateiName, optionen);

        try

        {

            PsdOptions psdOpt = new PsdOptions(bild);

            bild.save(ausgabedateipfadPsd, psdOpt);



            JpegOptions jpegOpt = new JpegOptions();

            jpegOpt.setQuality(100);

            bild.save(ausgabedateipfadJpg);

        }

        finally 

        {

             bild.dispose();

        }

    // Dateien müssen ohne Ausnahme geöffnet werden und für Photoshop lesbar sein    

   bild = Image.load(ausgabedateipfadPsd));

   bild.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Unterstützung von Ebenen-Vektormasken und benutzerdefinierte FlipRotate-Textebene**

{{< highlight java >}}

 // Die RotateFlip-Operation funktioniert nicht wie erwartet mit PSD

    String quelleDatei = "1.psd";

    String pngPfad = "RotateFlipTest2617.png";

    String psdPfad = "RotateFlipTest2617.psd";

    int flipTyp = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(quelleDatei));



    try

    {

        im.rotateFlip(flipTyp);

        PngOptions optionen = new PngOptions();

        optionen.setColorType(PngColorType.TruecolorWithAlpha);

        im.save(pngPfad, optionen);

        im.save(psdPfad);

    }

    finally 

    {

        im.dispose();

    }

{{< /highlight >}}

**PSDJAVA-4. Alle asiatischen Zeichen werden nicht korrekt gerendert**

[**Bitte überprüfen Sie das angehängte Beispiel**](attachments/92602686/92766213.java)

**PSDJAVA-5. \r\n-Symbole werden als doppelte Zeilenumbrüche interpretiert, was falsch ist**

{{< highlight java >}}

 // \r\n-Symbole werden als doppelte Zeilenumbrüche interpretiert, was falsch ist

            String dateiName = "TextTest.psd";

            String exportPfad = "Ergebnis.psd";



            PsdImage bild = (PsdImage)Image.load(dateiName);

            TextLayer ebene = (TextLayer)bild.getLayers()[0];

            PsdOptions bildOptionen = new PsdOptions(bild);

            try

            {

                ebene.updateText("Erster Absatz\r\nZweiter Absatz\rDritter Absatz\nVierter Absatz");

                bild.save(exportPfad, bildOptionen);

                // Das erstellte Bild muss von Aspose.PSD/Aspose.Imaging und von Photoshop lesbar sein

                PsdImage erstelltesBild = (PsdImage)Image.load(exportPfad);

                erstelltesBild.dispose();

            }

            finally

            {

                bild.dispose();

            }

{{< /highlight >}}



**PSDJAVA-6. Wenn eine Textebene mit einem String aktualisiert wird, der Zeilenumbrüche enthält, wird die PSD-Datei unlesbar**

{{< highlight java >}}

 // Wenn eine Textebene mit einem String aktualisiert wird, der Zeilenumbrüche enthält, wird die PSD-Datei unlesbar.

            String dateiname = "TextTest.psd";

            String exportpfad = "Ergebnis.psd";



            PsdImage bild = (PsdImage)Image.load(dateiname);

            TextLayer ebene = (TextLayer)bild.getLayers()[0];

            PsdOptions bildOptionen = new PsdOptions(bild);

            try

            {

                ebene.updateText("Erster Absatz\r\nZweiter Absatz\r\nDritter Absatz\r\nVierter Absatz");

                bild.save(exportpfad, bildOptionen);

                // Das erstellte Bild muss von Aspose.PSD/Aspose.Imaging und von Photoshop lesbar sein

                PsdImage erstelltesBild = (PsdImage)Image.load(exportpfad);

                erstelltesBild.dispose();



            }

            finally

            {

                bild.dispose();

            }

{{< /highlight >}}



**PSDJAVA-7. Wenn eine Textebene mit einem String aktualisiert wird, der Tabulatoren enthält, schlägt die Verarbeitung mit einer Ausnahme fehl**

{{< highlight java >}}

 //