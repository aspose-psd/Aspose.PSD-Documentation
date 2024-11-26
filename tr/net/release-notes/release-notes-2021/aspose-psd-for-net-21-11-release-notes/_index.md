---
title: Aspose.PSD for .NET 21.11 - Yayın Notları
type: docs
weight: 20
url: /tr/net/aspose-psd-for-net-21-11-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/) için yayın notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-767|Varolan metin katmanını katman grubuna eklerken hata alınması|Hata|
|PSDNET-988|TextLayer.UpdateText'te IndexOutOfRangeException alınması|Hata|
|PSDNET-989|Dışa aktarılan şekillerin sonuç dosyasındaki yanlış koordinatlara sahip olması|Hata|
|PSDNET-1002|Klasör dışa aktarımında vektör şeklinin yanlış şekilde dışa aktarılması|Hata|

## **Halka Açık API Değişiklikleri**
# **Eklenen API'ler:**
- Yok

# **Kaldırılan API'ler:**
- Yok

## **Kullanım örnekleri:**

**PSDNET-767. Varolan metin katmanını katman grubuna eklerken hata alınması**

{{< highlight csharp >}}
     string outputPsd = "out_dummy_group.psd";

     var psdOptions = new PsdOptions()
     {
         Kaynak = new StreamSource(new MemoryStream(), true),
         RenkModu = ColorModes.Rgb,
         KanallarSayısı = 4,
         KanalBitSayısı = 8,
         SıkıştırmaYöntemi = CompressionMethod.RLE
     };
     kullanarak (PsdImage image = (PsdImage)Image.Create(psdOptions, 10, 15))
     {
         var group = image.AddLayerGroup("TestGroup", 0, true);
         var layer = image.AddTextLayer("Metin", Rectangle.FromLeftTopRightBottom(-2, 3, 14, 17));
         group.AddLayer(layer);

         image.Save(outputPsd);
     }
{{< /highlight >}}

**PSDNET-988. TextLayer.UpdateText'te IndexOutOfRangeException alınması**

{{< highlight csharp >}}
       string srcFile = "M1TTTT16062021001.psd";
       string fontsFolder = "Yazı Tipleri";
       string outputPng = "out_M1TTTT16062021001.png";

       FontSettings.SetFontsFolder(fontsFolder);
       FontSettings.UpdateFonts();

       string[] words = new[] { "Anne", "Stacy" };
       string[] fonts = new[] { "Caveat", "Gochi Hand", "Lobster", "Satisfy" };

       kullanarak (var image = (PsdImage)Image.Load(srcFile))
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

**PSDNET-989. Dışa aktarılan şekillerin sonuç dosyasındaki yanlış koordinatlara sahip olması**

{{< highlight csharp >}}
        kamu void CreatingVectorPathExample()
        {
            string outputPsd = "outputPsd.psd";

            kullanarak (var psdImage = (PsdImage)Image.Create(new PsdOptions() { Source = new Sources.StreamSource(new MemoryStream()), }, 500, 500))
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
{{< /highlight >}}

**PSDNET-1002. Klasör dışa aktarımında vektör şeklinin yanlış şekilde dışa aktarılması**

{{< highlight csharp >}}
       string srcFile = "psdnet1002.psd";
       string outputPng = "output.png";

       kullanarak (var image = (PsdImage)Image.Load(srcFile))
       {
           image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
       }
{{< /highlight >}}