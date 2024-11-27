---
title: Aspose.PSD pro .NET 21.10 - Poznámky k vydání
type: docs
weight: 30
url: /cs/net/aspose-psd-pro-net-21-10-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 21.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-128|Podpora mechanismu Smart Filters|Funkce|
|PSDNET-414|Podpora Fxid/FEidResource|Funkce|
|PSDNET-556|Chyba při načítání struktury Alias|Chyba|
|PSDNET-948|Změna písma a barvy pro textovou vrstvu PSD|Chyba|
|PSDNET-971|Přidání schopnosti vlastní tvorby vrstvy s vektorovou maskou|Vylepšení|

## **Změny ve veřejném API**
# **Přidána API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.SmartFilters
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Distribution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.AmountNoise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.IsMonochromatic
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Radius
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Uniform
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Gaussian
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.BlendMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Apply(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.ApplyToMask(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.OnLoad
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Clone
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.sourceDescriptor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.FilterId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsValidAtPosition
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskExtendWithWhite
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.Filters
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.UpdateResourceValues
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.#ctor(System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FilterEffectMasks
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FEidTypeToolKey
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FXidTypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.#ctor(System.String,Aspose.PSD.Rectangle,System.Int32,System.Int32,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation[],Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation,Aspose.PSD.Rectangle,Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.GUID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Rectangle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.PixelsDepth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaxChannels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Channels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.UserMask
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaskRectangle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.SheetMask
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.SaveData(Aspose.PSD.StreamContainer)

# **Odebrané API:**
- Žádné

## **Příklady použití:**

**PSDNET-128. Podpora mechanismu Smart Filters**

{{< highlight csharp >}}
            string sourceFilte = "r2_SmartFilters.psd";
            string outputPsd = "out_r2_SmartFilters.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Objekty nejsou stejné.");
                }
            }

            using (var image = (PsdImage)Image.Load(sourceFilte))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                // úprava chytrých filtrů
                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // kontrola hodnot filtru
                AssertAreEqual(3.1, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Dissolve, gaussianBlur.BlendMode);
                AssertAreEqual(90d, gaussianBlur.Opacity);
                AssertAreEqual(true, gaussianBlur.IsEnabled);

                // aktualizace hodnot filtru
                gaussianBlur.Radius = 1;
                gaussianBlur.BlendMode = BlendMode.Divide;
                gaussianBlur.Opacity = 75;
                gaussianBlur.IsEnabled = false;
                AddNoiseSmartFilter addNoise = (AddNoiseSmartFilter)smartObj.SmartFilters.Filters[1];
                addNoise.Distribution = NoiseDistribution.Uniform;

                // přidání nových položek filtrů
                var filters = new List<SmartFilter>(smartObj.SmartFilters.Filters);
                filters.Add(new GaussianBlurSmartFilter());
                filters.Add(new AddNoiseSmartFilter());
                smartObj.SmartFilters.Filters = filters.ToArray();

                // aplikování změn
                smartObj.SmartFilters.UpdateResourceValues();

                // Použití filtrů
                smartObj.SmartFilters.Filters[0].Apply(image.Layers[2]);
                smartObj.SmartFilters.Filters[4].ApplyToMask(image.Layers[2]);

                image.Save(outputPsd);
            }

            using (var image = (PsdImage)Image.Load(outputPsd))
            {
                SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)smartObj.SmartFilters.Filters[0];

                // kontrola hodnot filtru
                AssertAreEqual(1d, gaussianBlur.Radius);
                AssertAreEqual(BlendMode.Divide, gaussianBlur.BlendMode);
                AssertAreEqual(75d, gaussianBlur.Opacity);
                AssertAreEqual(false, gaussianBlur.IsEnabled);

                AssertAreEqual(true, smartObj.SmartFilters.Filters[5] is GaussianBlurSmartFilter);
                AssertAreEqual(true, smartObj.SmartFilters.Filters[6] is AddNoiseSmartFilter);
            }
{{< /highlight >}}

**PSDNET-414. Podpora Fxid/FEidResource**

{{< highlight csharp >}}
           // kód příkladu PSDNET-414
{{< /highlight >}}

**PSDNET-556. Chyba při načítání AliasStructure**

{{< highlight csharp >}}
           // kód příkladu PSDNET-556
{{< /highlight >}}

**PSDNET-948. Změna písma a barvy pro textovou vrstvu PSD**

{{< highlight csharp >}}
           // kód příkladu PSDNET-948
{{< /highlight >}}

**PSDNET-971. Přidání schopnosti vlastní tvorby vrstvy s vektorovou maskou**

{{< highlight csharp >}}
           // kód příkladu PSDNET-971
{{< /highlight >}}**PSDNET-414. Podpora Fxid/FEidResource**

{{< highlight csharp >}}
            string inputFilePath = "psdnet414_3.psd";
            string output = "out_psdnet414_3.psd";

            int resLength = 1144;
            int maskLength = 369;

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objekty nejsou stejné.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(inputFilePath))
            {
                FXidResource fXidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fXidResource.Length);
                foreach (var maskData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }

                psdImage.Save(output);
            }

            // kontrola po uložení
            using (var psdImage = (PsdImage)Image.Load(output))
            {
                FXidResource fXidResource = (FXidResource)psdImage.GlobalLayerResources[3];

                AssertAreEqual(resLength, fXidResource.Length);
                foreach (var maskData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskLength, maskData.Length);
                }
            }
{{< /highlight >}}

**PSDNET-556. Chyba při načítání AliasStructure**

{{< highlight csharp >}}
            string srcFile = "Aspose.psd";
            string outputPsd = "out_Aspose.psd";
            string outputPng = "out_Aspose.png";

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objekty nejsou stejné.");
                }
            }

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                LnkeResource lnkeResource = (LnkeResource)image.GlobalLayerResources[3];
                LiFeDataSource dataSource = (LiFeDataSource)lnkeResource[0];
                AssertAreEqual(2484L, dataSource.Length);

                foreach (var layer in image.Layers)
                {
                    if (layer is TextLayer)
                    {
                        TextLayer textLayer = layer as TextLayer;
                        textLayer.UpdateText("Test", Aspose.PSD.Color.Black);
                    }
                }

                image.Save(outputPsd);
                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
            }
{{< /highlight >}}

**PSDNET-948. Změna písma a barvy pro textovou vrstvu PSD**

{{< highlight csharp >}}
            string sourceFileName = "fontExamples948.psd";
            string testFontsFoler = "Fonts";
            string outputPng = "output.png";

            FontSettings.SetFontsFolder(testFontsFoler);

            using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFileName))
            {
                foreach (var layer in image.Layers)
                {
                    var textLayer = layer as TextLayer;
                    if (textLayer != null)
                    {
                        ITextPortion textPortion = textLayer.TextData.Items[0];
                        textPortion.Style.FillColor = Color.BlueViolet;

                        textLayer.TextData.UpdateLayerData();
                    }
                }

                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-971. Přidání schopnosti vlastní tvorby vrstvy s vektorovou maskou**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string fileName = "PathExample2.psd";

            string outputPsd = "out_CreatingVectorPathExampleTest.psd";
            string outputPng = "out_CreatingVectorPathExampleTest.png";

            using (var psdImage = (PsdImage)Image.Load(fileName))
            {
                VectorDataProvider.RemoveVectorPathDataFromLayer(psdImage.Layers[2]);

                // vytváření objektu VectorPath pro existující vrstvu bez dat vektorové cesty
                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(psdImage.Layers[1]);

                // Nastavení barvy výplně vektorové cesty
                vectorPath.FillColor = Color.MediumPurple;

                // přidání nového tvaru
                PathShape newShape = new PathShape();
                newShape.Points.Add(new BezierKnot(new PointF(65, 175), true));
                newShape.Points.Add(new BezierKnot(new PointF(65, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 210), true));
                newShape.Points.Add(new BezierKnot(new PointF(190, 175), true));
                vectorPath.Shapes.Add(newShape);

                // aktualizace dat cesty ve vrstvě
                VectorDataProvider.UpdateLayerFromVectorPath(psdImage.Layers[1], vectorPath, true);


                // vytváření objektu VectorPath pro novou vrstvu
                FillLayer layer2 = FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                layer2.DisplayName = "Layer 2";
                psdImage.AddLayer(layer2);
                VectorPath vectorPath2 = VectorDataProvider.CreateVectorPathForLayer(layer2);

                // Nastavení barvy výplně vektorové cesty
                vectorPath2.FillColor = Color.IndianRed;

                // přidání nového tvaru
                PathShape newShape2 = new PathShape();
                newShape2.Points.Add(new BezierKnot(new PointF(50, 150), true));
                newShape2.Points.Add(new BezierKnot(new PointF(100, 200), true));
                newShape2.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath2.Shapes.Add(newShape2);

                // aktualizace dat cesty ve vrstvě
                VectorDataProvider.UpdateLayerFromVectorPath(layer2, vectorPath2, true);

                psdImage.Save(outputPsd);
                psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
            }
        }
{{< /highlight >}}

# **Editor cest vektorů (Zde umístěné třídy pro editaci vektorových cest).**

```csharp
    /// <summary>
    /// Třída poskytující práci mezi <see cref="Layer"/> a <see cref="VectorPath"/>.
    /// </summary>
    public static class VectorDataProvider
    {
        // Implementace metod pro práci s daty vektorových cest ve vrstvách
    }
```

```csharp
    /// <summary>
    /// Beziérový klička, obsahuje jeden kotouč a dva ovládací body.
    /// </summary>
    public class BezierKnot
    {
        // Implementace třídy BezierKnot pro reprezentaci ovládacích bodů v kličce Bezierovy křivky
    }
```

```csharp
    /// <summary>
    /// Obrys z kotoučů Bezierovy křivky.
    /// </summary>
    public class PathShape
    {
        // Implementace třídy PathShape pro reprezentaci obrysu z kotoučů Bezierovy křivky
    }
```

```csharp
    /// <summary>
    /// Třída obsahující vektorové cesty.
    /// </summary>
    public class VectorPath
    {
        // Implementace třídy VectorPath pro manipulaci s vektorovými cestami
    }
```

```csharp
    // Další třídy a metody
```