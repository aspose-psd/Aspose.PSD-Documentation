---
title: Notes de publication Aspose.PSD pour .NET 21.11
type: docs
weight: 20
url: /fr/net/aspose-psd-pour-net-21-11-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-767|Exception lors de l'ajout du calque de texte existant à un groupe de calques|Bogue|
|PSDNET-988|IndexOutOfRangeException lors de l'actualisation du texte de calque de texte|Bogue|
|PSDNET-989|Les formes exportées ont des coordonnées incorrectes dans le fichier résultant|Bogue|
|PSDNET-1002|Export incorrect de forme vectorielle lors de l'exportation du dossier|Bogue|

## **Changements de l'API publique**
# **APIs ajoutées :**
- Aucune

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-767. Exception lors de l'ajout du calque de texte existant à un groupe de calques**

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
                var group = image.AddLayerGroup("GroupeTest", 0, true);
                var layer = image.AddTextLayer("Texte", Rectangle.FromLeftTopRightBottom(-2, 3, 14, 17));
                group.AddLayer(layer);

                image.Save(outputPsd);
            }
{{< /highlight >}}

**PSDNET-988. IndexOutOfRangeException lors de l'actualisation du texte de calque de texte**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Polices";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] mots = new[] { "Maman", "Stacy" };
            string[] polices = new[] { "Caveat", "Gochi Hand", "Homard", "Satisfaire" };

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                foreach (var calque in image.Layers)
                {
                    var calqueTxt = calque as TextLayer;
                    if (calqueTxt != null)
                    {
                        for (int w = 0; w < mots.Length; w++)
                        {
                            for (int f = 0; f < polices.Length; f++)
                            {
                                calqueTxt.UpdateText(mots[w]);
                                foreach (var itemTxt in calqueTxt.TextData.Items)
                                {
                                    itemTxt.Style.FontName = FontSettings.GetAdobeFontName(polices[f]);
                                }

                                calqueTxt.TextData.UpdateLayerData();
                            }
                        }
                    }
                }

                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-989. Les formes exportées ont des coordonnées incorrectes dans le fichier résultant**

{{< highlight csharp >}}
        public void ExempleCréerCheminVectoriel()
        {
            string outputPsd = "outputPsd.psd";

            using (var psdImage = (PsdImage)Image.Create(new PsdOptions() { Source = new Sources.StreamSource(new MemoryStream()), }, 500, 500))
            {
                FillLayer calque = FillLayer.CreateInstance(PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                psdImage.AddLayer(calque);

                VectorPath cheminVectoriel = VectorDataProvider.CreateVectorPathForLayer(calque);
                cheminVectoriel.FillColor = Color.IndianRed;
                PathShape forme = new PathShape();
                forme.Points.Add(new BezierKnot(new PointF(50, 150), true));
                forme.Points.Add(new BezierKnot(new PointF(100, 200), true));
                forme.Points.Add(new BezierKnot(new PointF(0, 200), true));
                cheminVectoriel.Shapes.Add(forme);
                VectorDataProvider.UpdateLayerFromVectorPath(calque, cheminVectoriel, true);

                psdImage.Save(outputPsd);
            }
        }
{{< /highlight >}}

**PSDNET-1002. Export incorrect de forme vectorielle lors de l'exportation du dossier**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}