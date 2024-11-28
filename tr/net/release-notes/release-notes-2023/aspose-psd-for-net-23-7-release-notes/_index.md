---
title: Aspose.PSD for .NET 23.7 - Sürüm Notları
type: docs
weight: 60
url: /tr/net/aspose-psd-for-net-23-7-sürüm-notları/
---

{{% alert color="primary" %}}

Bu sayfa [Aspose.PSD for .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
|:------------|:---------|:------------|
| PSDNET-802  | PSD Dosyasının Her Katmanını Animasyonlu Gif Dosyasına Dışa Aktarma Yeteneği Ekleme | Özellik |
| PSDNET-1441 | Şekil katmanının Doldurma özelliğini vscg kaynağından atama | Özellik |
| PSDNET-1534 | Yeni warp türlerini (ark ve yay) ekleme | Özellik |
| PSDNET-1543 | PSD Dosyasını Kaydeden Uygulamayı Değiştirme - UpdateMetadata özelliği true olarak ayarlandığında | Özellik |
| PSDNET-1567 | Deformasyon görüntüsünün hesaplama alanını artırma | Özellik |
| PSDNET-1471 | Siyah ve beyaz ayarlama katmanı, yarı şeffaflığı yanlış işleme | Hata |
| PSDNET-1505 | SmartObject ReplaceContents (AllowWarpRepaint seçeneği etkin olduğunda) 2 dakika sonunda işlemin düşmesi | Hata |
| PSDNET-1585 | Gerçek LayerGroup Sol ve üst konumunu alma yeteneği ekleme | Hata |
| PSDNET-1589 | Katmanın yeniden boyutlandırılması, psd dosyasının noktalı yapılarla VogkResource'a sahip olduğunda yanlış çalışıyor | Hata |
| PSDNET-1608 | TextBound beklenildiği gibi çalışmıyor | Hata |
| PSDNET-1612 | Varsayılan yapılandırıcı ile oluşturulan bir katmanı PSD görüntüsüne eklemek varsayılan kaynakları eklemiyor | Hata |
| PSDNET-1623 | Timeline.LoopesCount, animasyonlu GIF'e dışa aktarırken yoksayılıyor | Hata |

## **Genel API Değişiklikleri**

# **Eklenen API'ler:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill

# **Kaldırılan API'ler:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor

## **Kullanım Örnekleri:**

**PSDNET-802. PSD Dosyasının Her Katmanını Animasyonlu Gif Dosyasına Dışa Aktarma Yeteneği Ekleme**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Her katman için çerçeveler oluşturun.
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // Mevcut durumları güncelle
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Şekil katmanının Doldurma özelliğini vscg kaynağından atama**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// Kaydedilen değişiklikleri kontrol et
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Siyah ve beyaz ayarlama katmanı, yarı şeffaflığı yanlış işleme**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Kaydedilen değişiklikleri kontrol et
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("2. Katmanın BlackWhiteAdjustmentLayer olması gerekiyor");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1505. SmartObject ReplaceContents (AllowWarpRepaint seçeneği etkin olduğunda) 2 dakika sonunda işlemin düşmesi**

{{< highlight csharp >}}
string kaynakDosya = "mug 4.psd";
string degiştirmeDosya = "artwork for replace.png";
string çıktıDosyası = "export.png";

int yeniYükseklik = 300;

using (var psdImage = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer smartObjectLayer = (SmartObjectLayer)psdImage.Layers[3];

    var ölçek = (double)yeniYükseklik / smartObjectLayer.Height;
    var yeniGenişlik = (int)Math.Round(smartObjectLayer.Width * ölçek);

    PsdImage içGörüntü = new PsdImage(yeniGenişlik, yeniYükseklik);
    içGörüntü.SetResolution(72, 72);

    Stream içAkış = new FileStream(değiştirmeDosya, FileMode.Open);
    Layer katman = new Layer(içAkış) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        içGörüntü.AddLayer(katman);

        smartObjectLayer.ReplaceContents(içGörüntü);
        smartObjectLayer.UpdateModifiedContent();

        psdImage.Save(çıktıDosyası, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        içGörüntü.Dispose();
        içAkış.Dispose();
        katman.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Yeni warp türlerini (ark ve yay) ekleme**

{{< highlight csharp >}}
string sourceArcFile = "arc_warp.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_warp.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. PSD Dosyasını Kaydeden Uygulamayı Değiştirme - UpdateMetadata özelliği true olarak ayarlandığında**

{{< highlight csharp >}}
string yol = "output.psd";
using (var görüntü = new PsdImage(100, 100))
{
    // Oluşturucu aracın değiştirilmesini istiyorsanız - "UpdateMetadata" özelliğinin true olarak ayarlandığından emin olun. Varsayılan olarak true olarak ayarlanır.
    var psdSeçenekleri = new PsdOptions();
    psdSeçenekleri.UpdateMetadata = true;

    // Görüntüyü kaydetme. 
    görüntü.Save(yol, psdSeçenekleri);

    // Kod içinde oluşturucu aracı kontrol et.
    var xmpVeri = görüntü.XmpVeri;
    var temelPaket = görüntü.XmpVeri.GetPackage(Namespaces.XmpBasic);

    // Burada güncellenen oluşturucu araç bilgisi olacak.
    var mevcutOluşturucuAraç = (string)temelPaket[":OluşturucuAraç"];
}
{{< /highlight >}}

**PSDNET-1567. Deformasyon görüntüsünün hesaplama alanını artırma**

{{< highlight csharp >}}
string sourceFile = "mug4_warp.psd";
string outputFile = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. Gerçek LayerGroup Sol ve üst konumunu alma yeteneği ekleme**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object beklenen, object gerçek)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception("Nesneler eşit değil.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layers = image.Layers;

    for (int i = 0; i < layers.Length; i++)
    {
        var layer = layers[i];

        if (layer is LayerGroup)
        {
            // Katman Grubunu al
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // Gerçek Sol, Üst, Sağ ve Alt konumları hesapla
            foreach (var innerLayer in group.Layers)
            {
                if (innerLayer is AdjustmentLayer || innerLayer.Bounds.IsEmpty)
                {
                    continue;
                }

                expectedLeft = Math.Min(expectedLeft, innerLayer.Left);
                expectedTop = Math.Min(expectedTop, innerLayer.Top);
                expectedRight = Math.Max((expectedLeft + group.Width), (innerLayer.Left + innerLayer.Width));
                expectedBottom = Math.Max((expectedTop + group.Height), (innerLayer.Top + innerLayer.Height));
            }

            // LayerGroup Sol, Üst, Sağ ve Alt konumlarının doğru bir şekilde hesaplandığından emin ol
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Katmanın yeniden boyutlandırılması, psd dosyasının noktalı yapılarla VogkResource'a sahip olduğunda yanlış çalışıyor**

{{< highlight csharp >}}
string[] kaynakDosyalar = new string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

foreach (string kaynakDosya in kaynakDosyalar)
{
    using (PsdImage image = (PsdImage)Image.Load(kaynakDosya))
    {
        Layer katman = image.Layers[0];

        katman.Resize(50, 50);

        AssertAreEqual(katman.Height, 50);
        AssertAreEqual(katman.Width, 50);
    }
}

void AssertAreEqual(object beklenen, object gerçek, string mesaj = null)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception(mesaj ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound beklenildiği gibi çalışmıyor**

{{< highlight csharp >}}
string kaynakDosya = "input_Test_forTicket.psd";
string çıktıDosyası = "out_1608.psd";

Size yeniMetinKutusu = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(kaynakDosya))
{
    //Adım: Metni Değiştir
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Metin testi değiştirildi";

    //Adım: TextBoundBox'ı Güncelle
    textLayer.TextData.UpdateLayerData();
    yeniMetinKutusu = new Size((int)Math.Ceiling(textLayer.TextBoundBox.Width), textLayer.Height);

    textLayer.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, yeniMetinKutusu);
    textLayer.TextData.UpdateLayerData();

    psdImage.Save(çıktıDosyası);
}

// Değişiklikleri kontrol et
using (var psdImage = (PsdImage)Image.Load(çıktıDosyası))
{
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);

    string arama = "<< /0 << /1 << /0 ["; // TextBox değerini dosyada bulmak için belirli bir karakter seti

    int başlangıçIndex = textData.IndexOf(arama) + arama.Length;
    int endIndex = textData.IndexOf("]", başlangıçIndex);
    string boxItems = textData.Substring(başlangıçIndex, endIndex - başlangıçIndex);

    string height = yeniMetinKutusu.Height.ToString("0.0####").Replace(",", ".");
    string width = yeniMetinKutusu.Width.ToString("0.0####").Replace(",", ".");

    if (!boxItems.Contains(height) || !boxItems.Contains(width))
    {
        throw new Exception("TextBox güncellenmedi.");
    }
}
{{< /highlight >}}

**PSDNET-1612. Varsayılan yapılandırıcı ile oluşturulan bir katmanı PSD görüntüsüne eklemek varsayılan kaynakları eklemiyor**

{{< highlight csharp >}}
string output = "newLayer.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var layer = new Layer();
    psdImage.AddLayer(layer);

    LyidResource lyidResource = (LyidResource)FindResource(LyidResource.TypeToolKey, layer.Resources);

    int layerId = lyidResource.Value; // NullReferenceException oluştu

   