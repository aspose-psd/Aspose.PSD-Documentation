---
title: Aspose.PSD pro .NET 19.10 - poznámky k vydání
type: docs
weight: 30
url: /cs/net/aspose-psd-pro-net-19-10-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro Aspose.PSD pro .NET 19.10

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-207|[Podpora vrstvy úpravy barevné rovnováhy](/psd/cs/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|Funkce|
|PSDNET-145|[Podpora vrstvy inverze](/psd/cs/net/modifying-images/#modifyingimages-invertadjustmentlayer)|Funkce|
|PSDNET-139|[Implementace bicubic Resampleru](/psd/cs/net/modifying-images/#modifyingimages-implementbicubicresampling)|Funkce|
|PSDNET-169|[Přidání podpory pro export PSD do PDF s Clipping Maskou](/psd/cs/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|Funkce|
|PSDNET-168|[Přidání podpory pro export PSD do PDF s úpravovými vrstvami](/psd/cs/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|Funkce|
|PSDNET-179|Problém s načtením vrstvy DropShadowEffect|Vylepšení|
|PSDNET-203|Když je text aktualizován s lomítkem /, soubor nelze otevřít v Photoshopu|Chyba|
|PSDNET-199|Soubor PSD nelze uložit, když textová vrstva obsahuje pouze konec řádku|Chyba|
|PSDNET-185|Extrahovaná nesprávná velikost písma|Chyba|

## **Změny ve veřejném API**
# **Přidaná API:**
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
# **Odstraněná API:**
- žádné

## **Příklady použití:**
**PSDNET-207. Podpora vrstvy úpravy barevné rovnováhy**

{{< highlight java >}}

            var soubor = "ColorBalance.psd";

            var vystup = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(soubor))

            {

                foreach (var vrstva in im.Layers)

                {

                    var vrstvaBarev = vrstva as ColorBalanceAdjustmentLayer;

                    if (vrstvaBarev != null)

                    {

                        vrstvaBarev.ShadowsCyanRedBalance = 30;

                        vrstvaBarev.ShadowsMagentaGreenBalance = -15;

                        vrstvaBarev.ShadowsYellowBlueBalance = 40;

                        vrstvaBarev.MidtonesCyanRedBalance = -90;

                        vrstvaBarev.MidtonesMagentaGreenBalance = -25;

                        vrstvaBarev.MidtonesYellowBlueBalance = 20;

                        vrstvaBarev.HighlightsCyanRedBalance = -30;

                        vrstvaBarev.HighlightsMagentaGreenBalance = 67;

                        vrstvaBarev.HighlightsYellowBlueBalance = -95;

                        vrstvaBarev.PreserveLuminosity = true;

                    }

                }

                im.Save(vystup);

            }

{{< /highlight >}}

**PSDNET-145. Podpora vrstvy inverze**

{{< highlight java >}}

            var soubor = "InvertStripes_before.psd";

            var vystup = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(soubor))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(vystup);

            }

{{< /highlight >}}

**PSDNET-139. Implementace bicubic Resampleru**

{{< highlight java >}}

             string sourceFile = "sample.psd";

            string destName = "ResamplerCubicConvolutionStripes_after.psd";

            // Načtení existujícího obrázku do instance třídy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCatmullRomStripes_after.psd";

            // Načtení existujícího obrázku do instance třídy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerMitchellStripes_after.psd";

            // Načtení existujícího obrázku do instance třídy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCubicBSplineStripes_after.psd";

            // Načtení existujícího obrázku do instance třídy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerSinCStripes_after.psd";

            // Načtení existujícího obrázku do instance třídy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.SinC);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerBellStripes_after.psd";

            // Načtení existujícího obrázku do instance třídy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Bell);

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-169. Přidání podpory pro export PSD do PDF s Clipping Maskou**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}



**PSDNET-168. Přidání podpory pro export PSD do PDF s úpravovými vrstvami**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("example.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Když je text aktualizován s lomítkem /, soubor nelze otevřít v Photoshopu**

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

**PSDNET-199. Soubor PSD nelze uložit, když textová vrstva obsahuje pouze konec řádku**

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

**PSDNET-185. Extrahovaná nesprávná velikost písma**

{{< highlight java >}}

             // Extrahovaná nesprávná velikost písma

            string filePath = "直播+电商.psd";

            var tolerance = 0.001;

            using (var image = Image.Load(filePath))

            {

                int layerIndex = 22;

                // Staré API (Použití velikosti písma prvního odstavce)

                PsdImage psdImage = image as PsdImage;

                double[] matrix = ((TextLayer)psdImage.Layers[layerIndex]).TransformMatrix;

                double baseFontSize = ((TextLayer)psdImage.Layers[layerIndex]).Font.Size;

                double fontSize = matrix[0] * baseFontSize;

                // Kontrola základní velikosti písma

                if (Math.Abs(100.0 - baseFontSize) > tolerance)

                {

                    throw new Exception("Velikost písma byla přečtena nesprávně");

                }

                // Kontrola skutečné velikosti písma

                if (Math.Abs(88.425 - fontSize) > tolerance)

                {

                    throw new Exception("Transformační matice byla přečtena nesprávně");

                }

                // Nové API (Jedna textová vrstva může obsahovat libovolné množství velikostí písma)

                ITextPortion[] portions = ((TextLayer)psdImage.Layers[layerIndex]).TextData.Items;

                ITextStyle style = portions[0].Style;

                double fontSizeOfPortion = matrix[0] * style.FontSize;

                // Kontrola základní velikosti písma části

                if (Math.Abs(100.0 - style.FontSize) > tolerance)

                {

                    throw new Exception("Velikost písma byla přečtena nesprávně");

                }

                // Kontrola skutečné velikosti písma části

                if (Math.Abs(88.425 - fontSizeOfPortion) > tolerance)

                {

                    throw new Exception("Transformační matice byla přečtena nesprávně");

                }

            }

{{< /highlight >}}

**PSDNET-179. Problém s načtením vrstvy DropShadowEffect**

{{< highlight java >}}

       // Když je vlastnost DropShadowEffect.UseGlobalLight nastavena na 'true', objekt DropShadowEffect používá hodnotu úhlu z vlastnosti PsdImage.GlobalAngle.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}