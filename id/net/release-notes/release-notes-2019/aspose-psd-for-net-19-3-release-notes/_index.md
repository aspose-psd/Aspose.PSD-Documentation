---
title: Catatan Rilis Aspose.PSD untuk .NET 19.3
type: docs
weight: 100
url: /id/net/aspose-psd-untuk-net-19-3-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk Aspose.PSD untuk .NET 19.3

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-104|Rendering dari Lapisan Teks yang Diputar oleh TransformMatrix|Fitur|
|PSDNET-96|Menerapkan rendering Efek Stroke dengan Isian Warna untuk ekspor|Fitur|
|PSDNET-112|Transformer InnerData merusak beberapa lapisan dengan masker vektor|Bug|
|PSDNET-113|Pembaruan lapisan teks untuk gambar PSD menghasilkan kesalahan saat dibuka di Photoshop|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada
# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**
**PSDNET-104. Rendering dari Lapisan Teks yang Diputar oleh TransformMatrix**

{{< highlight java >}}

 string namaFileSumber = "TransformedText.psd";

string jalurEkspor = "TransformedTextExport.psd";

string jalurEksporPng = "TransformedTextExport.png";

var im = (PsdImage) Image.Load(namaFileSumber);

using(im) {

 im.Save(jalurEkspor);

 im.Save(jalurEksporPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Menerapkan rendering Efek Stroke dengan Isian Warna untuk ekspor**

{{< highlight java >}}

  // Menerapkan rendering Efek Stroke dengan Isian Warna untuk ekspor

 string namaFileSumber = "StrokeComplex.psd";

 string jalurEkspor = "StrokeComplexRendering.psd";

 string jalurEksporPng = "StrokeComplexRendering.png";

 var opsiMuat = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(namaFileSumber, opsiMuat)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var efek = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var pengaturan = (ColorFillSettings) efek.FillSettings;

   pengaturan.Color = Color.DeepPink;

  }

  // Simpan psd

  im.Save(jalurEkspor, new PsdOptions());

  // Simpan png

  im.Save(jalurEksporPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Transformer InnerData merusak beberapa lapisan dengan masker vektor**

{{< highlight java >}}

 // Transformer InnerData merusak beberapa lapisan dengan masker vektor

var fileSumber = "1.psd";

var jalurPng = "RotateFlipTest2617.png";

var jalurPsd = "RotateFlipTest2617.psd";

var jenisFlip = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(fileSumber))) {

 im.RotateFlip(jenisFlip);

 im.Save(jalurPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(jalurPsd);

}

{{< /highlight >}}

**PSDNET-113. Memperbarui lapisan teks untuk gambar PSD menghasilkan kesalahan saat dibuka di Photoshop**

{{< highlight java >}}

 string namaFileSumber = "Test.psd";

string jalurEkspor = "Hasil.psd";

using(Image image = Image.Load(namaFileSumber)) {

 if (!(image is PsdImage)) {

  return;

 }

 PsdImage psdImage = (PsdImage) image;

 Layer[] layers = psdImage.Layers;

 for (int index = layers.Length - 1; index >= 0; index--) {

  Layer layer = layers[index];

  if (!(layer is TextLayer)) {

   continue;

  }

  TextLayer textLayer = (TextLayer) layer;

  textLayer.UpdateText("\\()");

 }

 PsdOptions opsiGambar = new PsdOptions(psdImage);

 psdImage.Save(jalurEkspor, opsiGambar);

}

// File harus dibuka tanpa pengecualian dan harus dapat dibaca oleh Photoshop

using(Image image = Image.Load(jalurEkspor)) {}

{{< /highlight >}}
