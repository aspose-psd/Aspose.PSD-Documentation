---
title: Aspose.PSD for .NET 19.10 - Release Notes
type: docs
weight: 30
url: /nl/net/aspose-psd-for-net-19-10-release-notes/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor Aspose.PSD voor .NET 19.10.

{{% /alert %}} 

|**Belangrijkste**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-207|[Ondersteuning van Color Balance Adjustment Layer](/psd/nl/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|Functie|
|PSDNET-145|[Ondersteuning van Invert Adjustment Layer](/psd/nl/net/modifying-images/#modifyingimages-invertadjustmentlayer)|Functie|
|PSDNET-139|[Bicubische Resampler implementeren](/psd/nl/net/modifying-images/#modifyingimages-implementbicubicresampling)|Functie|
|PSDNET-169|[Toevoegen van ondersteuning voor PSD-export naar PDF met Clipping Masker](/psd/nl/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|Functie|
|PSDNET-168|[Toevoegen van ondersteuning voor PSD-export naar PDF met Aanpassingslagen](/psd/nl/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|Functie|
|PSDNET-179|Probleem met het verkrijgen van Layer DropShadowEffect|Verbetering|
|PSDNET-203|Wanneer tekst wordt bijgewerkt met (voorwaartse schuine streep) tekens, kan het bestand niet worden geopend in Photoshop|Fout|
|PSDNET-199|PSD-bestand kan niet worden opgeslagen wanneer de tekstlaag alleen een regeleinde bevat|Fout|
|PSDNET-185|Verkeerde lettergrootte geëxtraheerd|Fout|

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-207. Ondersteuning van Color Balance Adjustment Layer**

{{< highlight java >}}

            var filePath = "ColorBalance.psd";

            var outputPath = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                foreach (var layer in im.Layers)

                {

                    var cbLayer = layer as ColorBalanceAdjustmentLayer;

                    if (cbLayer != null)

                    {

                        cbLayer.ShadowsCyanRedBalance = 30;

                        cbLayer.ShadowsMagentaGreenBalance = -15;

                        cbLayer.ShadowsYellowBlueBalance = 40;

                        cbLayer.MidtonesCyanRedBalance = -90;

                        cbLayer.MidtonesMagentaGreenBalance = -25;

                        cbLayer.MidtonesYellowBlueBalance = 20;

                        cbLayer.HighlightsCyanRedBalance = -30;

                        cbLayer.HighlightsMagentaGreenBalance = 67;

                        cbLayer.HighlightsYellowBlueBalance = -95;

                        cbLayer.PreserveLuminosity = true;

                    }

                }

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-145. Ondersteuning van Invert Adjustment Layer**

{{< highlight java >}}

            var filePath = "InvertStripes_before.psd";

            var outputPath = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-139. Implementeer bicubische Resampler**

{{< highlight java >}}

             string sourceFile = "sample.psd";

            string destName = "ResamplerCubicConvolutionStripes_after.psd";

            // Laad een bestaande afbeelding in een instantie van de klasse PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCatmullRomStripes_after.psd";

            // Laad een bestaande afbeelding in een instantie van de klasse PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerMitchellStripes_after.psd";

            // Laad een bestaande afbeelding in een instantie van de klasse PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCubicBSplineStripes_after.psd";

            // Laad een bestaande afbeelding in een instantie van de klasse PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerSinCStripes_after.psd";

            // Laad een bestaande afbeelding in een instantie van de klasse PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.SinC);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerBellStripes_after.psd";

            // Laad een bestaande afbeelding in een instantie van de klasse PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Bell);

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-169. Toevoegen van ondersteuning voor PSD-export naar PDF met Clipping Masker**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}



**PSDNET-168. Toevoegen van ondersteuning voor PSD-export naar PDF met Aanpassingslagen**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("example.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Wanneer tekst wordt bijgewerkt met / (voorwaartse schuine streep) tekens, kan het bestand niet worden geopend in Photoshop**

{{< highlight java >}}

         var psdImage = (PsdImage)image;

        var layers = psdImage.Layers;

        for (var index = layers.Length - 1; index >= 0; index--)

        {

            var layer = layers[index];

            if (!(layer is TextLayer)) continue;

            var textLayer = (TextLayer)layer;

            textLayer.UpdateText("/");

        }

        var imageOptions = new PsdOptions(psdImage);

        var fileName = Path.GetFileName(filePath);

        var outputFilePath = Path.GetDirectoryName(filePath) + "\\target_" + fileName;

        psdImage.Save(outputFilePath, imageOptions);



{{< /highlight >}}

**PSDNET-199. PSD-bestand kan niet worden opgeslagen wanneer de tekstlaag alleen een regeleinde bevat**

{{< highlight java >}}

 string filePath = "testLineBreaks2.psd";

string outputPath = "testLineBreaks2_changed.psd";

var newText = "\r";

        using (var image = Image.Load(filePath))

        {

            var psdImage = image as PsdImage;

            if (image == null)

            {

                return;

            }

            var layers = psdImage.Layers;

            for (var index = layers.Length - 1; index >= 0; index--)

            {

                var layer = layers[index] as TextLayer;

                if (layer == null)

                {

                    continue;

                }

                layer.UpdateText(newText);

            }

            var imageOptions = new PsdOptions(psdImage);

            psdImage.Save(outputPath, imageOptions);

        }

{{< /highlight >}}

**PSDNET-185. Verkeerde lettergrootte geëxtraheerd**

{{< highlight java >}}

             // Verkeerde lettergrootte geëxtraheerd

            string filePath = "直播+电商.psd";

            var tolerantie = 0.001;

            using (var image = Image.Load(filePath))

            {

                int layerIndex = 22;

                // Oude API (Gebruik van de lettergrootte van de eerste alinea)

                PsdImage psdImage = image as PsdImage;

                double[] matrix = ((TextLayer)psdImage.Layers[layerIndex]).TransformMatrix;

                double basisLettergrootte = ((TextLayer)psdImage.Layers[layerIndex]).Font.Size;

                double lettergrootte = matrix[0] * basisLettergrootte;

                // Controleer de basis lettergrootte

                if (Math.Abs(100.0 - basisLettergrootte) > tolerantie)

                {

                    throw new Exception("Lettergrootte is onjuist gelezen");

                }

                // Controleer de werkelijke lettergrootte

                if (Math.Abs(88.425 - lettergrootte) > tolerantie)

                {

                    throw new Exception("TransformMatrix is onjuist gelezen");

                }

                // Nieuwe API (Eén tekstlaag kan elke hoeveelheid lettergroottes bevatten)

                ITextPortion[] gedeeltes = ((TextLayer)psdImage.Layers[layerIndex]).TextData.Items;

                ITextStyle stijl = gedeeltes[0].Style;

                double lettergrootteVanGedeelte = matrix[0] * stijl.FontSize;

                // Controleer de basis lettergrootte van het gedeelte

                if (Math.Abs(100.0 - stijl.FontSize) > tolerantie)

                {

                    throw new Exception("Lettergrootte is onjuist gelezen");

                }

                // Controleer de werkelijke lettergrootte van het gedeelte

                if (Math.Abs(88.425 - lettergrootteVanGedeelte) > tolerantie)

                {

                    throw new Exception("TransformMatrix is onjuist gelezen");

                }

            }

{{< /highlight >}}

**PSDNET-179. Probleem met het verkrijgen van Layer DropShadowEffect**

{{< highlight java >}}

       // Wanneer DropShadowEffect.UseGlobalLight eigenschap 'true' is, gebruikt DropShadowEffect-object de hoekwaarde van PsdImage.GlobalAngle-eigenschap.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}