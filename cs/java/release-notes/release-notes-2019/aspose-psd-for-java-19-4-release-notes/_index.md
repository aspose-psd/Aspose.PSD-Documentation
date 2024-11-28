---
title: Aspose.PSD pro Java 19.4 - Poznámky k vydání
type: docs
weight: 20
url: /cs/aspose-psd-pro-java-19-4-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro Aspose.PSD pro Java 19.4.

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-1|Přidání funkce načítání souborů s obrazy ve formátu JPEG/PNG apod. do třídy PsdImage bez přímého načítání (což není podporované v Aspose.PSD)|Funkce|
|PSDJAVA-2|Podpora režimu RGB Color s 16 bity/kanál (64 bity na barvu)|Funkce|
|PSDJAVA-3|Podpora vrstevních vektorových masek a možnosti otáčení textové vrstvy|Funkce|
|PSDJAVA-4|Všechny asijské znaky nejsou správně zobrazovány|Chyba|
|PSDJAVA-5|Symboly \r\n jsou interpretovány jako dvojitý odstavec, což je chybné|Chyba|
|PSDJAVA-6|Pokud je textová vrstva aktualizována řetězcem obsahujícím konec řádku, soubor PSD se stane nečitelným|Chyba|
|PSDJAVA-7|Pokud je textová vrstva aktualizována řetězcem obsahujícím zarážky, zpracování selže s výjimkou|Chyba|
# **Změny ve veřejném API**
# **Přidaná API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **Odstraněná API:**
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
# **Příklady použití:**

**PSDJAVA-1. Funkce načtení souborů s obrazy ve formátech JPEG/PNG apod. do třídy PsdImage bez přímého načítání (což není podporované v Aspose.PSD)**

{{< highlight java >}}

 String filePath = "PsdExample.psd";

    String outputFilePath = "PsdResult.psd";

    PsdImage image = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(filePath);

         try 

         {

              Layer layer = null;

              try

              {

                  layer = new Layer((RasterImage)im);

                  image.addLayer(layer);

                  image.save(outputFilePath);

              }

              catch

              {

                  if (layer != null)

                  {

                       layer.dispose();

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

         image.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. Podpora režimu RGB Color s 16 bity/kanál (64 bity na barvu)**

{{< highlight java >}}

  // Podpora režimu RGB Color s 16 bity/kanál (64 bity na barvu)

        String sourceFileName = "inRgb16.psd.psd";

        String outputFilePathJpg = "outRgb16.jpg";

        String outputFilePathPsd = "outRgb16.psd";

        PsdLoadOptions options = new PsdLoadOptions();

        PsdImage image = (PsdImage)Image.load(sourceFileName, options);

        try

        {

            PsdOptions psdOpt = new PsdOptions(image);

            image.save(outputFilePathPsd, psdOpt);
    


            JpegOptions jpegOpt = new JpegOptions();

            jpegOpt.setQuality(100);

            image.save(outputFilePathJpg);

        }

        finally 

        {

             image.dispose();

        }

    // Soubory musí být otevřeny bez výjimky a musí být čitelné pro Photoshop    

   image = Image.load(outputFilePathPsd));

   image.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Podpora vrstevních vektorových masek a možnosti otáčení textové vrstvy**

{{< highlight java >}}

 // Operace RotateFlip nefunguje jak by měla s PSD

    String sourceFile = "1.psd";

    String pngPath = "RotateFlipTest2617.png";

    String psdPath = "RotateFlipTest2617.psd";

    int flipType = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(sourceFile));



    try

    {

        im.rotateFlip(flipType);

        PngOptions options = new PngOptions();

        options.setColorType(PngColorType.TruecolorWithAlpha);

        im.save(pngPath, options);

        im.save(psdPath);

    }

    finally 

    {

        im.dispose();

    }

{{< /highlight >}}

**PSDJAVA-4. Všechny asijské znaky nejsou správně zobrazovány**

[**Prosím, zkontrolujte připojený příklad**](attachments/92602686/92766213.java)

**PSDJAVA-5. Symboly \r\n jsou interpretovány jako dvojitý odstavec, což je chybné**

{{< highlight java >}}

 // Symboly \r\n jsou interpretovány jako dvojitý odstavec, což není správné

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";
    


            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("První odstavec\r\nDruhý odstavec\r\nTřetí odstavec\nČtvrtý odstavec");

                image.save(exportPath, imageOptions);

                // Vytvořený obrázek musí být čitelný pomocí Aspose.PSD/Aspose.Imaging a Photoshopu

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();

            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}



**PSDJAVA-6. Pokud je textová vrstva aktualizována řetězcem obsahujícím konec řádku, soubor PSD se stane nečitelným**

{{< highlight java >}}

 // Pokud je textová vrstva aktualizována řetězcem obsahujícím konec řádku, soubor PSD se stane nečitelným.

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";
    


            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("První odstavec\r\nDruhý odstavec\r\nTřetí odstavec\r\nČtvrtý odstavec");

                image.save(exportPath, imageOptions);

                // Vytvořený obrázek musí být čitelný pomocí Aspose.PSD/Aspose.Imaging a Photoshop