---
title: Poznámky k vydání Aspose.PSD pro .NET 19.8
type: docs
weight: 50
url: /cs/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání Aspose.PSD pro .NET 19.8

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-184|Načtení obrázkových souborů JPEG, PNG a dalších do objektu PsdImage ze streamu|Funkce|
|PSDNET-134|Implementace vykreslování vyplňové vrstvy: Přechod|Funkce|
|PSDNET-166|Uložení PSD do PDF neumožňuje vybírat text|Funkce|
|PSDNET-158|Podpora ukládání souborů PSB jako PDF|Funkce|
|PSDNET-189|Vysoká spotřeba paměti při načítání PSD s režimem pouze pro čtení|Vylepšení|
|PSDNET-171|Po vytvoření nové textové vrstvy se soubor PSD stal nečitelným pro PS|Chyba|
|PSDNET-156|Výjimka při načítání PSD|Chyba|

## **Změny ve veřejném API**
# **Přidaná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Odebraná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Příklady použití:**
**PSDNET-184. Načtení obrázkových souborů JPEG, PNG a dalších do objektu PsdImage ze streamu**

{{< highlight java >}}

    // Načtení obrázkových souborů JPEG, PNG a dalších do objektu PsdImage ze streamu

    string outputFilePath = "Vysledek.psd";

    var filesList = new string[]

    {

        "PrikladPsd.psd",

        "PrikladBmp.bmp",

        "PrikladGif.gif",

        "PrikladJpeg2000.jpf",

        "PrikladJpeg.jpg",

        "PrikladPng.png",

        "PrikladTiff.tif",

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

**PSDNET-134. Implementace vykreslení vyplňové vrstvy: Přechod**

{{< highlight java >}}

             // Implementace vykreslení vyplňové vrstvy: Přechod

            string fileName = "VrstvaPlniciPřechodem.psd";

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

