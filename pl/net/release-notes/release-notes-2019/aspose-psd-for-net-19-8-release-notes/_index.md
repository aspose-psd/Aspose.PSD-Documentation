---
title: Notatki dotyczące wydania Aspose.PSD dla .NET 19.8
type: docs
weight: 50
url: /pl/net/aspose-psd-dla-net-19-8-notatki-o-wydaniu/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania Aspose.PSD dla .NET 19.8

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-184|Wczytywanie plików obrazów JPEG, PNG i innych do PsdImage ze strumienia|Funkcja|
|PSDNET-134|Implementacja renderowania warstwy wypełnienia: Gradient|Funkcja|
|PSDNET-166|Zapisywanie plików PSD jako PDF nie zapewnia możliwości zaznaczania tekstu|Funkcja|
|PSDNET-158|Wsparcie dla zapisywania PSB jako PDF|Funkcja|
|PSDNET-189|Wysokie zużycie pamięci podczas wczytywania pliku PSD w trybie tylko do odczytu|Usprawnienie|
|PSDNET-171|Po utworzeniu nowej warstwy tekstowej, plik PSD staje się nieczytelny dla PS|Błąd|
|PSDNET-156|Wyjątek podczas wczytywania pliku PSD|Błąd|

## **Zmiany w interfejsie publicznym**
# **Dodane interfejsy:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Usunięte interfejsy:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Przykłady użycia:**
**PSDNET-184. Wczytywanie plików obrazów JPEG, PNG i innych do PsdImage ze strumienia**

{{< highlight java >}}

    // wczytywanie plików obrazów JPEG, PNG i innych do PsdImage ze strumienia

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. Implementacja renderowania warstwy wypełnienia: Gradient**

{{< highlight java >}}

             // Implementacja renderowania warstwy wypełnienia: Gradient

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. Zapisywanie plików PSD jako PDF nie zapewnia możliwości zaznaczania tekstu**

{{< highlight java >}}

  // Zapisywanie plików PSD jako PDF nie zapewnia możliwości zaznaczania tekstu

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Po utworzeniu nowej warstwy tekstowej, plik PSD staje się nieczytelny dla PS**

{{< highlight java >}}

 // Po utworzeniu nowej warstwy tekstowej na serwerze kompilacji, plik PSD staje się nieczytelny dla PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Jakiś tekst", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. Wyjątek podczas wczytywania pliku PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Wysokie zużycie pamięci podczas wczytywania pliku PSD w trybie tylko do odczytu**

{{< highlight java >}}

 // Wysokie zużycie pamięci Aspose.PSD podczas wczytywania pliku PSD w trybie tylko do odczytu

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Zużycie pamięci musi być mniejsze niż 100 MB dla tych przykładów

            if (memoryUsed > 100)

            {

                throw new Exception("Zużycie pamięci jest zbyt duże");

            }

{{< /highlight >}}

**PSDNET-158. Wsparcie dla zapisywania PSB jako PDF**

{{< highlight java >}}

 // Wsparcie dla zapisywania PSB jako PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
