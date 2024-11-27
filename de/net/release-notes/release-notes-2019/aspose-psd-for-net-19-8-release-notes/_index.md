---
title: Aspose.PSD für .NET 19.8 - Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-psd-fur-net-19-8-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für Aspose.PSD für .NET 19.8

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-184|Laden Sie JPEG, PNG und andere Bilddateien in PsdImage aus dem Stream|Funktion|
|PSDNET-134|Umsetzung des Renderns der Füllebene: Gradient|Funktion|
|PSDNET-166|Beim Speichern von PSD in PDF wird kein auswählbarer Text bereitgestellt|Funktion|
|PSDNET-158|Unterstützung beim Speichern von PSB als PDF|Funktion|
|PSDNET-189|Hoher Speicherverbrauch beim Laden von PSD im Nur-Lese-Modus|Verbesserung|
|PSDNET-171|Nach dem Erstellen einer neuen Textebene wurde die PSD-Datei für PS unlesbar|Fehler|
|PSDNET-156|Ausnahme beim Laden von PSD|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Entfernte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Beispiele zur Verwendung:**
**PSDNET-184. Laden von JPEG, PNG und anderen Bilddateien in PsdImage aus dem Stream**

{{< highlight java >}}

    // JPEG-, PNG- und andere Bilddateien in PsdImage aus dem Stream laden

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

**PSDNET-134. Umsetzung des Renderns der Füllebene: Gradient**

{{< highlight java >}}

             // Umsetzung des Renderns der Füllebene: Gradient

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

**PSDNET-166. Beim Speichern von PSD in PDF wird kein auswählbarer Text bereitgestellt**

{{< highlight java >}}

  // Beim Speichern von PSD in PDF wird kein auswählbarer Text bereitgestellt

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Nach dem Erstellen einer neuen Textebene wurde die PSD-Datei für PS unlesbar**

{{< highlight java >}}

 // Nach dem Erstellen einer neuen Textebene auf dem Build-Server wurde die PSD-Datei für PS unlesbar

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Einige Text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. Ausnahme beim Laden von PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Hoher Speicherverbrauch beim Laden von PSD im Nur-Lese-Modus**

{{< highlight java >}}

 // Hoher Speicherverbrauch von Aspose.PSD beim Laden von PSD im Nur-Lese-Modus

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Der Speicherverbrauch muss für diese Beispiele weniger als 100 MB betragen

            if (memoryUsed > 100)

            {

                throw new Exception("Speicherbedarf ist zu hoch");

            }

{{< /highlight >}}

**PSDNET-158. Unterstützung beim Speichern von PSB als PDF**

{{< highlight java >}}

 // Unterstützung beim Speichern von PSB als PDF

    string sourceFileName = "Beispiel.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "Beispiel.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
