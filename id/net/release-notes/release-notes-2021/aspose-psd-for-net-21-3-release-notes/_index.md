---
title: Catatan Rilis Aspose.PSD untuk .NET 21.3
type: docs
weight: 100
url: /id/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-823|Menambahkan SectionDividerLayer untuk meningkatkan pengalaman dengan grup lapisan|Peningkatan|
|PSDNET-694|Ketika membaca PattResource, lebar dan tinggi tertukar|Bug|
|PSDNET-789|Penggabungan yang Tidak Tepat dari Lebih dari Satu Efek Lapisan|Bug|
|PSDNET-805|Urutan dan logika Penggabungan yang Tidak Tepat ketika terdapat lebih dari satu Efek Lapisan|Bug|
|PSDNET-842|Properti efek Stroke tidak disimpan ke file PSD|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

**PSDNET-694. Ketika membaca PattResource, lebar dan tinggi tertukar**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // memanggil rendering pola

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Penggabungan yang Tidak Tepat dari Lebih dari Satu Efek Lapisan**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // Mencari Lapisan Teks
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Terbaik";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // Dengan cara ini kita menyimpan File PSD yang diubah
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Urutan dan logika Penggabungan yang Tidak Tepat ketika terdapat lebih dari satu Efek Lapisan**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Nomor1Terbaik.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                //Dengan cara ini kita menyimpan File PSD yang diubah
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Menambahkan SectionDividerLayer untuk meningkatkan pengalaman dengan grup lapisan**

{{< highlight csharp >}}
            // Kode berikut menunjukkan lapisan SectionDividerLayer dan cara mendapatkan LayerGroup yang terkait dengannya.

            // Hierarchy lapisan
            //    [0]: '</Layer group>' SectionDividerLayer untuk Grup 1
            //    [1]: 'Layer 1' Lapisan Biasa
            //    [2]: '</Layer group>' SectionDividerLayer untuk Grup 2
            //    [3]: '</Layer group>' SectionDividerLayer untuk Grup 3
            //    [4]: 'Grup 3' GroupLayer
            //    [5]: 'Grup 2' GroupLayer
            //    [6]: 'Grup 1' GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objek tidak sama.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Membuat hirarki lapisan
                // Menambahkan LayerGroup 'Grup 1'
                LayerGroup group1 = image.AddLayerGroup("Grup 1", 0, true);
                // Menambahkan lapisan biasa
                Layer layer1 = new Layer();
                layer1.DisplayName = "Lapisan 1";
                group1.AddLayer(layer1);
                // Menambahkan LayerGroup 'Grup 2'
                LayerGroup group2 = group1.AddLayerGroup("Grup 2", 1);
                // Menambahkan LayerGroup 'Grup 3'
                LayerGroup group3 = group2.AddLayerGroup("Grup 3", 0);

                // Mendapatkan SectionDividerLayer's
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // menggunakan metode SectionDividerLayer.GetRelatedLayerGroup(), mendapatkan instance LayerGroup terkait.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // LayerGroup yang sama
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // LayerGroup yang sama
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // LayerGroup yang sama

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Grup 1' berisi 5 lapisan
            }
{{< /highlight >}}

**PSDNET-842. Properti efek Stroke tidak disimpan ke file PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objek tidak sama.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Tidak akan menimbulkan ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Memeriksa nilai yang disimpan
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
