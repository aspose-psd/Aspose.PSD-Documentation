---
title: Aspose.PSD dla .NET 19.10 - Informacje o wydaniu
type: docs
weight: 30
url: /pl/net/aspose-psd-dla-net-19-10-informacje-o-wydaniu/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki dotyczące wydania Aspose.PSD dla .NET 19.10

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-207|[Wsparcie dla warstwy regulacji balansu kolorów](/psd/pl/net/modyfikowanie-obrazow/#modyfikowanieobrazow-warstwareguacji-balansukolorow)|Funkcja|
|PSDNET-145|[Wsparcie dla warstwy odwrócenia](/psd/pl/net/modyfikowanie-obrazow/#modyfikowanieobrazow-odwrocenieodwrocenie)|Funkcja|
|PSDNET-139|[Wdrożenie interpolatora bicubic](/psd/pl/net/modyfikowanie-obrazow/#modyfikowanieobrazow-wdrozeniebicubicinterpolator)|Funkcja|
|PSDNET-169|[Dodanie obsługi eksportu PSD do PDF z maską przycięcia](/psd/pl/net/konwertowanie-psd-do-innych-formatow/#konwertowanielpsddoinnychformatow-psdnadpdfzmaska)|Funkcja|
|PSDNET-168|[Dodanie obsługi eksportu PSD do PDF z warstwami regulacji](/psd/pl/net/konwertowanie-psd-do-innych-formatow/#konwertowanielpsddoinnychformatow-psdnadpdfzwarstwaregu)|Funkcja|
|PSDNET-179|Problem z pobraniem efektu cienia warstwy|Usprawnienie|
|PSDNET-203|Gdy tekst jest aktualizowany ze znakami / (ukośnik), plik nie może być otwarty w programie Photoshop|Błąd|
|PSDNET-199|Plik PSD nie może być zapisany, gdy warstwa tekstowa zawiera jedynie złamanie wiersza|Błąd|
|PSDNET-185|Wyekstrahowano nieprawidłowy rozmiar czcionki|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
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
# **Usunięte API:**
- Brak

## **Przykłady użycia:**
**PSDNET-207. Wsparcie dla warstwy regulacji balansu kolorów**

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

**PSDNET-145. Wsparcie dla warstwy odwrócenia**

{{< highlight java >}}

            var filePath = "InvertStripes_before.psd";

            var outputPath = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-139. Wdrożenie interpolatora bicubic**

{{< highlight java >}}

             string sourceFile = "sample.psd";

            string destName = "ResamplerCubicConvolutionStripes_after.psd";

            // Wczytaj istniejący obraz do instancji klasy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCatmullRomStripes_after.psd";

            // Wczytaj istniejący obraz do instancji klasy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerMitchellStripes_after.psd";

            // Wczytaj istniejący obraz do instancji klasy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCubicBSplineStripes_after.psd";

            // Wczytaj istniejący obraz do instancji klasy PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerSinCStripes_after.psd";

            // Wczytaj istniejący obraz do instancji klasy PsdImage

            ...

{{< /highlight >}}

**PSDNET-169. Dodanie obsługi eksportu PSD do PDF z maską przycięcia**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-168. Dodanie obsługi eksportu PSD do PDF z warstwami regulacji**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("example.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Gdy tekst jest aktualizowany ze znakami / (ukośnik), plik nie może być otwarty w programie Photoshop**

{{< highlight java >}}

        ...

{{< /highlight >}}

**PSDNET-199. Plik PSD nie może być zapisany, gdy warstwa tekstowa zawiera jedynie złamanie wiersza**

{{< highlight java >}}

        ...

{{< /highlight >}}

**PSDNET-185. Wyekstrahowano nieprawidłowy rozmiar czcionki**

{{< highlight java >}}

             // Wyekstrahowano nieprawidłowy rozmiar czcionki 

            ...

{{< /highlight >}}

**PSDNET-179. Problem z pobraniem efektu cienia warstwy**

{{< highlight java >}}

       // Gdy właściwość DropShadowEffect.UseGlobalLight ma wartość 'true', obiekt DropShadowEffect używa wartości kąta z właściwości PsdImage.GlobalAngle.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}