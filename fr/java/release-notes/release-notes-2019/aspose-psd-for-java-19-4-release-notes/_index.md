---
title: Notes de publication d'Aspose.PSD pour Java 19.4
type: docs
weight: 20
url: /fr/java/aspose-psd-pour-java-19-4-notes-de-release/
---

{{% alert color="primary" %}} 

Cette page contient les notes de publication pour Aspose.PSD pour Java 19.4

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-1|Créer une fonctionnalité pour charger des fichiers d'images JPEG/PNG/etc dans PsdImage sans chargement direct (ce qui n'est pas pris en charge par Aspose.PSD)|Fonctionnalité|
|PSDJAVA-2|Prise en charge du mode couleur RVB avec 16 bits/canal (64 bits par couleur)|Fonctionnalité|
|PSDJAVA-3|Prise en charge des masques vectoriels de calque et de la rotation personnalisée de calque de texte|Fonctionnalité|
|PSDJAVA-4|Tous les caractères asiatiques ne sont pas rendus correctement|Bogue|
|PSDJAVA-5|Les symboles \r\n sont interprétés comme un double saut de ligne, ce qui est incorrect|Bogue|
|PSDJAVA-6|Si un calque de texte est mis à jour avec une chaîne contenant des sauts de ligne, le fichier PSD devient illisible|Bogue|
|PSDJAVA-7|Si un calque de texte est mis à jour avec une chaîne contenant des symboles de tabulation, le traitement échoue avec une exception|Bogue|
# **Modifications de l'API publique**
# **APIs ajoutées:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **APIs supprimées:**
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
# **Exemples d'utilisation :**

**PSDJAVA-1. Créer une fonctionnalité pour charger des fichiers d'images JPEG/PNG/etc dans PsdImage sans chargement direct (ce qui n'est pas pris en charge par Aspose.PSD)**

{{< highlight java >}}

 String cheminFichier = "ExemplePsd.psd";

    String cheminFichierSortie = "ResultatPsd.psd";

    PsdImage image = new PsdImage(200, 200);

    try 

    {
         PsdImage im = Image.load(cheminFichier);

         try 

         {
              Calque calque = null;

              try
              {
                  calque = new Calque((RasterImage)im);
                  image.addLayer(calque);
                  image.save(cheminFichierSortie);
              }
              catch
              {
                  if (calque != null)
                  {
                       calque.dispose();
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


**PSDJAVA-2. Prise en charge du mode couleur RVB avec 16 bits/canal (64 bits par couleur)**

{{< highlight java >}}

  // Prise en charge du mode couleur RVB avec 16 bits/canal (64 bits par couleur)

        String nomFichierSource = "inRgb16.psd.psd";

        String cheminFichierSortieJpg = "outRgb16.jpg";

        String cheminFichierSortiePsd = "outRgb16.psd";

        PsdLoadOptions options = new PsdLoadOptions();

        PsdImage image = (PsdImage)Image.load(nomFichierSource, options);

        try
        {
            PsdOptions psdOpt = new PsdOptions(image);
            image.save(cheminFichierSortiePsd, psdOpt);
            
            JpegOptions jpegOpt = new JpegOptions();
            jpegOpt.setQuality(100);
            image.save(cheminFichierSortieJpg);
        }
        finally 
        {
             image.dispose();
        }

    // Les fichiers doivent être ouverts sans exception et lisibles dans Photoshop    

   image = Image.load(cheminFichierSortiePsd));
   image.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Prise en charge des masques vectoriels de calque et de la rotation personnalisée de calque de texte**

{{< highlight java >}}

 // L'opération de rotation inclinée ne fonctionne pas comme prévu avec PSD

    String fichierSource = "1.psd";

    String cheminPng = "TestRotationInclinee2617.png";

    String cheminPsd = "TestRotationInclinee2617.psd";

    int typeInclinaison = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(fichierSource));

    try
    {
        im.rotateFlip(typeInclinaison);

        PngOptions options = new PngOptions();
        options.setColorType(PngColorType.TruecolorWithAlpha);
        im.save(cheminPng, options);
        im.save(cheminPsd);
    }
    finally 
    {
        im.dispose();
    }

{{< /highlight >}}

**PSDJava-4. Tous les caractères asiatiques ne sont pas rendus correctement**

[**Veuillez vérifier l'exemple joint**](attachments/92602686/92766213.java)

**PSDJAVA-5. Les symboles \r\n sont interprétés comme un double saut de ligne, ce qui est incorrect**

{{< highlight java >}}

 // Les symboles \r\n sont interprétés comme un double saut de ligne, ce qui est incorrect
            String nomFichierSource = "TestTexte.psd";
            String cheminExportation = "Resultat.psd";

            PsdImage image = (PsdImage)Image.load(nomFichierSource);            
            CalqueTexte calque = (CalqueTexte)image.getLayers()[0];            
            PsdOptions optionsImage = new PsdOptions(image);

            try
            {
                calque.updateTexte("Premier paragraphe\r\nDeuxième paragraphe\rTroisième paragraphe\nQuatrième paragraphe");
                image.save(cheminExportation, optionsImage);
                PsdImage imageCreee = (PsdImage)Image.load(cheminExportation);
                imageCreee.dispose();
            }
            finally
            {
                image.dispose();
            }

{{< /highlight >}}


**PSDJAVA-6. Si un calque de texte est mis à jour avec une chaîne contenant des sauts de ligne, le fichier PSD devient illisible**

{{< highlight java >}}

 // Si un calque de texte est mis à jour avec une chaîne contenant des sauts de ligne, le fichier PSD devient illisible.

            String nomFichierSource = "TestTexte.psd";
            String cheminExportation = "Resultat.psd";

            PsdImage image = (PsdImage)Image.load(nomFichierSource);
            CalqueTexte calque = (CalqueTexte)image.getLayers()[0];
            PsdOptions optionsImage = new PsdOptions(image);
            
            try
            {
                calque.updateTexte("Premier paragraphe\r\nDeuxième paragraphe\r\nTroisième paragraphe\r\nQuatrième paragraphe");
                image.save(cheminExportation, optionsImage);
                PsdImage imageCreee = (PsdImage)Image.load(cheminExportation);
                imageCreee.dispose();
            }
            finally
            {
                image.dispose();
            }

{{< /highlight >}}


**PSDJAVA-7. Si un calque de texte est mis à jour avec une chaîne contenant des symboles de tabulation, le traitement échoue avec une exception**

{{< highlight java >}}

 // Si un calque de texte est mis à jour avec une chaîne contenant des symboles de tabulation, le traitement échoue