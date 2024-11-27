---
title: Aspose.PSD pro .NET 21.11 - Poznámky k vydání
type: docs
weight: 20
url: /cs/net/aspose-psd-pro-net-21-11-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje informace o vydání pro [Aspose.PSD pro .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-767|Výjimka při přidávání existující textové vrstvy do skupiny vrstev|Chyba|
|PSDNET-988|IndexOutOfRangeException při aktualizaci textové vrstvy|Chyba|
|PSDNET-989|Exportované tvary mají špatné souřadnice ve výsledném souboru|Chyba|
|PSDNET-1002|Nesprávný export vektorového tvaru při exportu složky|Chyba|

## **Změny ve veřejném API**
# **Přidaná API:**
- Žádné

# **Odebrané API:**
- Žádné

## **Příklady použití:**

**PSDNET-767. Výjimka při přidávání existující textové vrstvy do skupiny vrstev**

{{< highlight csharp >}}
            string outputPsd = "out_dummy_group.psd";

            var psdOptions = new PsdOptions()
            {
                Source = new StreamSource(new MemoryStream(), true),
                ColorMode = ColorModes.Rgb,
                ChannelsCount = 4,
                ChannelBitsCount = 8,
                CompressionMethod = CompressionMethod.RLE
            };
            using (PsdImage image = (PsdImage)Image.Create(psdOptions, 10, 15))
            {
                var group = image.AddLayerGroup("TestGroup", 0, true);
                var layer = image.AddTextLayer("Text", Rectangle.FromLeftTopRightBottom(-2, 3, 14, 17));
                group.AddLayer(layer);

                image.Save(outputPsd);
            }
{{< /highlight >}}

**PSDNET-988. IndexOutOfRangeException při aktualizaci textové vrstvy**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Fonts";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] words = new[] { "Mom", "Stacy" };
            string[] fonts = new[] { "Caveat", "Gochi Hand", "Lobster", "Satisfy" };

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                foreach (var layer in image.Layers)
                {
                    var txtLayer = layer as TextLayer;
                    if (txtLayer != null)
                    {
                        for (int w = 0; w < words.Length; w++)
                        {
                            for (int f = 0; f < fonts.Length; f++)
                            {
                                txtLayer.UpdateText(words[w]);
                                foreach (var txtItem in txtLayer.TextData.Items)
                                {
                                    txtItem.Style.FontName = FontSettings.GetAdobeFontName(fonts[f]);
                                }

                                txtLayer.TextData.UpdateLayerData();
                            }
                        }
                    }
                }

                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}


**PSDNET-989. Exportované tvary mají špatné souřadnice ve výsledném souboru**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string outputPsd = "outputPsd.psd";

            using (var psdImage = (PsdImage)Image.Create(new PsdOptions() { Source = new Sources.StreamSource(new MemoryStream()), }, 500, 500))
            {
                FillLayer layer = FillLayer.CreateInstance(PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                psdImage.AddLayer(layer);

                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(layer);
                vectorPath.FillColor = Color.IndianRed;
                PathShape shape = new PathShape();
                shape.Points.Add(new BezierKnot(new PointF(50, 150), true));
                shape.Points.Add(new BezierKnot(new PointF(100, 200), true));
                shape.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath.Shapes.Add(shape);
                VectorDataProvider.UpdateLayerFromVectorPath(layer, vectorPath, true);

                psdImage.Save(outputPsd);
            }
        }


    #region Editor vektorové cesty (Zde jsou umístěny třídy pro úpravy vektorových cest).

    /// <summary>
    /// Třída, která poskytuje práci mezi vrstvou <see cref="Layer"/> a <see cref="VectorPath"/>.
    /// </summary>
    public static class VectorDataProvider
    {
        /// <summary>
        /// Vytvoří instanci <see cref="VectorPath"/> na základě prostředků z vstupní vrstvy.
        /// </summary>
        /// <param name="psdLayer">Vrstva PSD.</param>
        /// <returns>Instance <see cref="VectorPath"/> na základě prostředků z vstupní vrstvy.</returns>
        public static VectorPath CreateVectorPathForLayer(Layer psdLayer)
        {
            ValidateLayer(psdLayer);

            Size imageSize = psdLayer.Container.Size;

            VectorPathDataResource pathResource = FindVectorPathDataResource(psdLayer, true);
            SoCoResource socoResource = FindSoCoResource(psdLayer, true);
            VectorPath vectorPath = new VectorPath(pathResource, imageSize);
            if (socoResource != null)
            {
                vectorPath.FillColor = socoResource.Color;
            }

            return vectorPath;
        }

        /// <summary>
        /// Aktualizuje prostředky vstupní vrstvy z instance <see cref="VectorPath"/> nebo nahradí novým zdrojem cesty a aktualizuje.
        /// </summary>
        /// <param name="psdLayer">Vrstva PSD.</param>
        /// <param name="vectorPath">Vektorová cesta.</param>
        /// <param name="imageSize">Velikost obrázku pro správné korekce souřadnic bodů.</param>
        public static void UpdateLayerFromVectorPath(Layer psdLayer, VectorPath vectorPath, bool createIfNotExist = false)
        {
            ValidateLayer(psdLayer);

            VectorPathDataResource pathResource = FindVectorPathDataResource(psdLayer, createIfNotExist);
            VogkResource vogkResource = FindVogkResource(psdLayer, createIfNotExist);
            SoCoResource socoResource = FindSoCoResource(psdLayer, createIfNotExist);

            Size imageSize = psdLayer.Container.Size;
            UpdateResources(pathResource, vogkResource, socoResource, vectorPath, imageSize);

            ReplaceVectorPathDataResourceInLayer(psdLayer, pathResource, vogkResource, socoResource);
        }

        // Zde jsou další metody třídy VectorDataProvider

        /// <summary>
        /// Odebere data vektorové cesty z vstupní vrstvy.
        /// </summary>
        /// <param name="psdLayer">Vrstva PSD.</param>
        public static void RemoveVectorPathDataFromLayer(Layer psdLayer)
        {
            // ...
        }

        // Další metody třídy VectorDataProvider

        /// <summary>
        /// Aktualizuje zdroje dat z instance <see cref="VectorPath"/>.
        /// </summary>
        /// <param name="pathResource">Prostředek cesty.</param>
        /// <param name="vogkResource">Prostředek původu vektorových dat.</param>
        /// <param name="socoResource">Prostředek jednotné barvy.</param>
        /// <param name="vectorPath">Vektorová cesta.</param>
        /// <param name="imageSize">Velikost obrázku pro správné korekce souřadnic bodů.</param>
        private static void UpdateResources(VectorPathDataResource pathResource, VogkResource vogkResource, SoCoResource socoResource, VectorPath vectorPath, Size imageSize)
        {
            // Metoda pro aktualizaci prostředků
        }

        // Další metody třídy VectorDataProvider

        /// <summary>
        /// Najde prostředek <see cref="VectorPathDataResource"/> v zdrojích vstupní vrstvy.
        /// </summary>
        /// <param name="psdLayer">Vrstva PSD.</param>
        /// <param name="createIfNotExist">Pokud prostředek neexistuje, pro hodnotu <see cref="true"/> vytvoří nový prostředek, jinak vrátí <see cref="null"/>.</param>
        /// <returns>Prostředek <see cref="VectorPathDataResource"/>.</returns>
        private static VectorPathDataResource FindVectorPathDataResource(Layer psdLayer, bool createIfNotExist = false)
        {
            // ...
        }

        // Další metody třídy VectorDataProvider
    }

    // Další třídy a metody

{{< /highlight >}}

**PSDNET-1002. Nesprávný export vektorového tvaru při exportu složky**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}