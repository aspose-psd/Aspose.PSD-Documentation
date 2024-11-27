---
title: Catatan Rilis Aspose.PSD untuk .NET 22.4
type: docs
weight: 90
url: /id/net/aspose-psd-untuk-net-22-4-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Kunci** | **Ringkasan** | **Kategori** |
| :- | :- | :- |
|PSDNET-261|Rendering Efek Lapisan Dalam Cahaya Kilap|Fitur|
|PSDNET-1123|Menambahkan Dukungan Lisensi Sha256|Peningkatan|
|PSDNET-1107|Penempatan teks multi-baris tidak sesuai dengan hasil di Photoshop|Bug|
|PSDNET-1113|Isu dengan memuat file PSD pada penguraian data sumber teks|Bug|
|PSDNET-1129|Posisi kustom pola yang salah setelah disimpan sebagai PSD|Bug|


## **Perubahan API Publik**
# **API yang Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Kiri
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Kanan
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Tengah
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.WarnaIsi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.ModoCampuran
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Tampak
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Keburaman
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensitas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Aliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Sepread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Ukuran
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Kebisingan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.CampuranLembut
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Jarak


# **API yang Dihapus:**
- Tidak Ada


## **Contoh Penggunaan:**

**PSDNET-261. Rendering Efek Lapisan Dalam Cahaya Kilap**
{{< highlight csharp >}}
string src = "LapisanHijau.psd";
string output = "output261.png";

using (var image = (PsdImage)Image.Load(src))
{
    OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
    effect.Range = 10;
    effect.Spread = 10;
    ((IColorFillSettings)effect.FillColor).Color = Color.Merah;
    effect.Opacity = 128;
    effect.BlendMode = BlendMode.Normal;

    image.Save(output, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1107. Penempatan teks multi-baris tidak sesuai dengan hasil di Photoshop**

{{< highlight csharp >}}
string src = "sumber1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Baris Teks1\rBaris Teks2\rBaris Teks3", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Kiri;
   portions[1].Paragraph.Justification = JustificationMode.Kanan;
   portions[2].Paragraph.Justification = JustificationMode.Tengah;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1113. Isu dengan memuat file PSD pada penguraian data sumber teks**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // Berhasil dimuat.
}
{{< /highlight >}}


**PSDNET-1129. Posisi kustom pola yang salah setelah disimpan sebagai PSD**

{{< highlight csharp >}}
string sourceFile = "input_1129.psd";
string outputPsd = "out_psdnet1129.psd";
string outputPng = "out_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
