---
title: Aspose.PSD voor .NET 23.10 - release-opmerkingen
type: docs
weight: 30
url: /nl/net/aspose-psd-for-net-23-10-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel**     | **Samenvatting**                                                                                                                | **Categorie** |
|:------------|:------------------------------------------------------------------------|:--------|
| PSDNET-692 | Ondersteuning van verticale tekstrichting | Functie |
| PSDNET-1402 | Gebruik instellingen voor lijn van vstk-bron in vormlijnrendering | Functie |
| PSDNET-1607 | Implementeer het renderen van het interne gebied van lijnfiguren | Functie |
| PSDNET-1644 | Herschilder de vormlaag niet als deze niet is gewijzigd | Functie |
| PSDNET-1696 | [AI-formaat] Ondersteuning toevoegen voor het lezen van koptekst uit op PDF gebaseerde AI-bestanden | Functie |
| PSDNET-1560 | Diverse manieren om Psd-bestandsresolutie in te stellen werken niet | Fout |
| PSDNET-1728 | FontSettings.SetFontsFolders werkt niet of Aspose.PSD gebruikt het verkeerde lettertype | Fout |
| PSDNET-1739 | Foutopsporing. Los een nulverwijzing op die optreedt bij PsdImage.Save wanneer er een vormlaag aanwezig is | Fout |


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment


# **Verwijderde API's:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **Voorbeelden van gebruik:**

**PSDNET-692. Ondersteuning van verticale tekstrichting**

{{< highlight csharp >}}
string bronBestand = "692_lt1.psd";
string uitvoerBestand = "692_output.png";
string lettertypeMap = "692_Lettertypen";

var lettertypeMappen = new List<string>(FontSettings.GetFontsFolders());
lettertypeMappen.Add(lettertypeMap);
FontSettings.SetFontsFolders(lettertypeMappen.ToArray(), true);

using (PsdImage psdAfbeelding = (PsdImage)Image.Load(bronBestand))
{
    psdAfbeelding.Save(uitvoerBestand, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1402. Gebruik instellingen voor lijn van vstk-bron in vormlijnrendering**

{{< highlight csharp >}}
string bronBestand = "StrokeShapeTest.psd";
string uitvoerBestandPsd = "StrokeShapeTest.out.psd";
string uitvoerBestandPng = "StrokeShapeTest.out.png";

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand))
{
    Layer laag = afbeelding.Layers[1];
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Layers[1];
    ColorFillSettings vulInstellingen = (ColorFillSettings)vormLaag.Fill;
    vulInstellingen.Color = Color.GreenYellow;
    vormLaag.Update();

    ShapeLayer vormLaag2 = (ShapeLayer)afbeelding.Layers[3];
    GradientFillSettings verloopInstellingen = (GradientFillSettings)vormLaag2.Fill;
    verloopInstellingen.Dither = true;
    verloopInstellingen.Reverse = true;
    verloopInstellingen.AlignWithLayer = false;
    verloopInstellingen.Angle = 20;
    verloopInstellingen.Scale = 50;
    verloopInstellingen.ColorPoints[0].Location = 100;
    verloopInstellingen.ColorPoints[1].Location = 4000;
    verloopInstellingen.TransparencyPoints[0].Location = 200;
    verloopInstellingen.TransparencyPoints[1].Location = 3800;
    verloopInstellingen.TransparencyPoints[0].Opacity = 90;
    verloopInstellingen.TransparencyPoints[1].Opacity = 10;
    vormLaag2.Update();

    ShapeLayer vormLaag3 = (ShapeLayer)afbeelding.Layers[5];
    StrokeSettings lijnInstellingen = (StrokeSettings)vormLaag3.Stroke;
    lijnInstellingen.Size = 15;
    ColorFillSettings lijnVulInstellingen = (ColorFillSettings)lijnInstellingen.Fill;
    lijnVulInstellingen.Color = Color.GreenYellow;
    vormLaag3.Update();

    afbeelding.Save(uitvoerBestandPsd);
    afbeelding.Save(uitvoerBestandPng, new PngOptions());
}

// Controleer gewijzigde gegevens.
using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerBestandPsd))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Layers[1];
    ColorFillSettings vulInstellingen = (ColorFillSettings)vormLaag.Fill;
    AssertAreEqual(Color.GreenYellow, vulInstellingen.Color);

    ShapeLayer vormLaag2 = (ShapeLayer)afbeelding.Layers[3];
    GradientFillSettings verloopInstellingen = (GradientFillSettings)vormLaag2.Fill;
    AssertAreEqual(true, verloopInstellingen.Dither);
    AssertAreEqual(true, verloopInstellingen.Reverse);
    AssertAreEqual(false, verloopInstellingen.AlignWithLayer);
    AssertAreEqual(20.0, verloopInstellingen.Angle);
    AssertAreEqual(50, verloopInstellingen.Scale);
    AssertAreEqual(100, verloopInstellingen.ColorPoints[0].Location);
    AssertAreEqual(4000, verloopInstellingen.ColorPoints[1].Location);
    AssertAreEqual(200, verloopInstellingen.TransparencyPoints[0].Location);
    AssertAreEqual(3800, verloopInstellingen.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, verloopInstellingen.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, verloopInstellingen.TransparencyPoints[1].Opacity);

    ShapeLayer vormLaag3 = (ShapeLayer)afbeelding.Layers[5];
    StrokeSettings lijnInstellingen = (StrokeSettings)vormLaag3.Stroke;
    ColorFillSettings lijnVulInstellingen = (ColorFillSettings)lijnInstellingen.Fill;
    AssertAreEqual(15.0, lijnInstellingen.Size);
    AssertAreEqual(Color.GreenYellow, lijnVulInstellingen.Color);
}

void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1607. Implementeer het renderen van het interne gebied van lijnfiguren**

{{< highlight csharp >}}
string bronBestand = "ShapeInternalGradient.psd";
string uitvoerBestand = "ShapeInternalGradient.out.psd";

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Layers[1];
    GradientFillSettings vulInstellingen = (GradientFillSettings)vormLaag.Fill;
    vulInstellingen.Dither = true;
    vulInstellingen.Reverse = true;
    vulInstellingen.AlignWithLayer = false;
    vulInstellingen.Angle = 20.0;
    vulInstellingen.Scale = 50;
    vulInstellingen.ColorPoints[0].Location = 100;
    vulInstellingen.ColorPoints[1].Location = 4000;
    vulInstellingen.TransparencyPoints[0].Location = 200;
    vulInstellingen.TransparencyPoints[1].Location = 3800;
    vulInstellingen.TransparencyPoints[0].Opacity = 90.0;
    vulInstellingen.TransparencyPoints[1].Opacity = 10.0;

    vormLaag.Update();

    afbeelding.Save(uitvoerBestand);
}

// Controleer gewijzigde gegevens.
using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Layers[1];
    GradientFillSettings vulInstellingen = (GradientFillSettings)vormLaag.Fill;

    AssertAreEqual(true, vulInstellingen.Dither);
    AssertAreEqual(true, vulInstellingen.Reverse);
    AssertAreEqual(false, vulInstellingen.AlignWithLayer);
    AssertAreEqual(20.0, vulInstellingen.Angle);
    AssertAreEqual(50, vulInstellingen.Scale);
    AssertAreEqual(100, vulInstellingen.ColorPoints[0].Location);
    AssertAreEqual(4000, vulInstellingen.ColorPoints[1].Location);
    AssertAreEqual(200, vulInstellingen.TransparencyPoints[0].Location);
    AssertAreEqual(3800, vulInstellingen.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, vulInstellingen.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, vulInstellingen.TransparencyPoints[1].Opacity);
}

void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1644. Herschilder de vormlaag niet als deze niet is gewijzigd**

{{< highlight csharp >}}
string bronBestand = "ShapeInternalSolid.psd";
string uitvoerBestand = "ShapeInternalSolid.out.psd";

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Layers[1];
    ColorFillSettings vulInstellingen = (ColorFillSettings)vormLaag.Fill;
    vulInstellingen.Color = Color.Red;

    // Geen update van vormlaag gebruiken vóór opslaan

    afbeelding.Save(uitvoerBestand);

    // Controleer weergave van opgeslagen bestand
}

// Controleer dat de gegevens van de vormlaag niet zijn gewijzigd.
using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Layers[1];
    ColorFillSettings vulInstellingen = (ColorFillSettings)vormLaag.Fill;

    AssertAreEqual(Color.FromArgb(45, 211, 31), vulInstellingen.Color);
}

void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1696. [AI-formaat] Ondersteuning toevoegen voor het lezen van koptekst uit op PDF gebaseerde AI-bestanden**

{{< highlight csharp >}}
string bronBestand = "ai_source.ai";

void AssertIsNotNull(object verwacht)
{
    if (verwacht == null)
    {
        throw new Exception("Object is null.");
    }
}

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand))
{
    AssertIsNotNull(afbeelding);
    AssertIsNotNull(afbeelding.Header);
    AssertIsNotNull(afbeelding.Header.BoundingBox);
}
{{< /highlight >}}

**PSDNET-1560. Diverse manieren om Psd-bestandsresolutie in te stellen werken niet**

{{< highlight csharp >}}
string uitvoer1 = "1560_1_output.psd";
string uitvoer2 = "1560_2_output.psd";
string uitvoer3 = "1560_3_output.psd";

using (PsdImage nieuwePsd = (PsdImage)new PsdImage(600, 400))
{
    nieuwePsd.ImageResources = new ResourceBlock[] { new ResolutionInfoResource() };
    nieuwePsd.VerticalResolution = 100;
    nieuwePsd.HorizontalResolution = 100;
    nieuwePsd.Save(uitvoer1);
}

using (PsdImage nieuwePsd = (PsdImage)new PsdImage(600, 400))
{
    nieuwePsd.SetResolution(200, 200);
    nieuwePsd.Save(uitvoer2);
}

using (PsdImage nieuwePsd = (PsdImage)new PsdImage(600, 400))
{
    PsdOptions psdOpties = new PsdOptions()
    {
        ResolutionSettings = new ResolutionSetting()
        {
            HorizontalResolution = 300,
            VerticalResolution = 300
        }
    };
    nieuwePsd.Save(uitvoer3, psdOpties);
}

using (var psdAfbeelding1 = (PsdImage)Image.Load(uitvoer1))
{
    var resHulpbron = psdAfbeelding1.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resHulpbron);
    AreEqual(100, resHulpbron.VDpi.Integer);
    AreEqual(100, resHulpbron.HDpi.Integer);
}

using (var psdAfbeelding2 = (PsdImage)Image.Load(uitvoer2))
{
    var resHulpbron = psdAfbeelding2.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resHulpbron);
    AreEqual(200, resHulpbron.VDpi.Integer);
    AreEqual(200, resHulpbron.HDpi.Integer);
}

using (var psdAfbeelding3 = (PsdImage)Image.Load(uitvoer3))
{
    var resHulpbron = psdAfbeelding3.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resHulpbron);
    AreEqual(300, resHulpbron.VDpi.Integer);
    AreEqual(300, resHulpbron.HDpi.Integer);
}

void IsNotNull(object obj)
{
    if (obj == null)
    {
        throw new NullReferenceException();
    }
}

void AreEqual(object verwacht, object werkelijk)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception("Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1728. FontSettings.SetFontsFolders werkt niet of Aspose.PSD gebruikt het verkeerde lettertype**

{{< highlight csharp >}}
string src = "1728_Untitled-1.psd";
string fontsDir = "Fonts";
string outputPng = "1728_output.png";

FontSettings.SetFontsFolders(new string[] { fontsDir }, true);
using (PsdImage psdAfbeelding = (PsdImage)Image.Load(src))
{
    foreach (var laag in psdAfbeelding.Layers)
    {
        if (