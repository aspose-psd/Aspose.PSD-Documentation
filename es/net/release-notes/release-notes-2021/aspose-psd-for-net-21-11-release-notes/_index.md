---
title: Notas de la versión de Aspose.PSD para .NET 21.11
type: docs
weight: 20
url: /es/net/aspose-psd-para-net-21-11-notas-de-lanzamiento/
---

{{% alert color="primary" %}} 

Esta página contiene las notas de lanzamiento de [Aspose.PSD para .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-767|Excepción al agregar la capa de texto existente a un grupo de capas|Error|
|PSDNET-988|IndexOutOfRangeException en TextLayer.UpdateText|Error|
|PSDNET-989|Las formas exportadas tienen coordenadas incorrectas en el archivo de resultado|Error|
|PSDNET-1002|Exportación incorrecta de la forma vectorial en la exportación de carpetas|Error|

## **Cambios en la API pública**
# **APIs agregadas:**
- Ninguna

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-767. Excepción al agregar la capa de texto existente a un grupo de capas**

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

**PSDNET-988. IndexOutOfRangeException en TextLayer.UpdateText**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Fuentes";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] words = new[] { "Mamá", "Stacy" };
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

**PSDNET-989. Las formas exportadas tienen coordenadas incorrectas en el archivo de resultado**

{{< highlight csharp >}}
        public void EjemploCrearRutaVector()
        {
            string outputPsd = "outputPsd.psd";

            using (var psdImage = (PsdImage)Image.Create(new PsdOptions() { Source = new Sources.StreamSource(new MemoryStream()), }, 500, 500))
            {
                FillLayer capa = FillLayer.CreateInstance(PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                psdImage.AddLayer(capa);

                VectorPath rutaVector = VectorDataProvider.CreateVectorPathForLayer(capa);
                rutaVector.FillColor = Color.IndianRed;
                PathShape forma = new PathShape();
                forma.Points.Add(new BezierKnot(new PointF(50, 150), true));
                forma.Points.Add(new BezierKnot(new PointF(100, 200), true));
                forma.Points.Add(new BezierKnot(new PointF(0, 200), true));
                rutaVector.Shapes.Add(forma);
                VectorDataProvider.UpdateLayerFromVectorPath(capa, rutaVector, true);

                psdImage.Save(outputPsd);
            }
        }
{{< /highlight >}}

**PSDNET-1002. Exportación incorrecta de la forma vectorial en la exportación de carpetas**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}