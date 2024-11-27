---
title: Catatan Rilis Aspose.PSD for .NET 19.9
type: docs
weight: 40
url: /id/net/aspose-psd-for-net-19-9-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD for .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-160|Nama lapisan yang salah diekstrak|Fitur|
|PSDNET-175|Mendapatkan properti teks dari bagian teks yang berbeda di dalam Lapisan Teks PSD|Fitur|
|PSDNET-190|Dukungan untuk Menambahkan grup lapisan|Fitur|
|PSDNET-192|Dukungan untuk Properti Skala untuk Lapisan Isian Gradien|Fitur|
|PSDNET-162|Menyesuaikan Kecerahan|Peningkatan|
|PSDNET-174|IndexOutOfRangeException saat menyimpan gambar PSD sebagai JPEG|Bug|
|PSDNET-180|Memperbarui teks lapisan teks memunculkan pengecualian|Bug|
|PSDNET-182|Menyimpan gambar PSD setelah operasi RotateFlip menghasilkan file yang rusak yang tidak dapat dibuka|Bug|

## **Perubahan API Publik**
# **API ditambahkan:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**
**PSDNET-160. Nama lapisan yang salah diekstrak**

Untuk menampilkan nama lapisan dengan benar, gunakan properti **DisplayName**. Saat ini telah ditambahkan setter untuk properti ini dan properti tersebut dapat diubah. Ketika Photoshop menyimpan nama lapisan menggunakan properti Name, karakter Korea disimpan sebagai byte 63'?' dalam ASCII. Gunakan properti **DisplayName** karena properti Name tidak mendukung karakter Korea.

{{< highlight java >}}

             // melakukan perubahan pada nama lapisan dan menyimpannya

            using (var image = (PsdImage)Image.Load("layers with names.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // set nilai baru ke properti DisplayName

                    layer.DisplayName += "_changed";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. Mendapatkan properti teks dari bagian teks yang berbeda di dalam Lapisan Teks PSD**

{{< highlight java >}}

            const double Toleransi = 0.0001;

            var filePath = "ThreeColorsParagraphs.psd";

            var outputPath = "ThreeColorsParagraph_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var layer = im.Layers[i] as TextLayer;

                    if (layer != null)

                    {

                        var portions = layer.TextData.Items;

                        if (portions.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Memeriksa teks dari setiap bagian

                        if (portions[0].Text != "Lama " ||

                            portions[1].Text != "warna" ||

                            portions[2].Text != " teks\r" ||

                            portions[3].Text != "Paragraf kedua\r")

                        {

                            throw new Exception();

                        }

                        // Memeriksa data paragraf

                        // Paragraf memiliki justifikasi yang berbeda

                        if (

                            portions[0].Paragraph.Justification != 0 ||

                            portions[1].Paragraph.Justification != 0 ||

                            portions[2].Paragraph.Justification != 0 ||

                            portions[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // Semua properti lain dari paragraf pertama dan kedua sama

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var paragraph = portions[j].Paragraph;

                            if (Math.Abs(paragraph.AutoLeading - 1.2) > Toleransi ||

                                paragraph.AutoHyphenate != false ||

                                paragraph.Burasagari != false ||

                                paragraph.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragraph.StartIndent) > Toleransi ||

                                Math.Abs(paragraph.EndIndent) > Toleransi ||

                                paragraph.EveryLineComposer != false ||

                                Math.Abs(paragraph.FirstLineIndent) > Toleransi ||

                                paragraph.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragraph.GlyphSpacing[0] - 1) > Toleransi ||

                                Math.Abs(paragraph.GlyphSpacing[1] - 1) > Toleransi ||

                                Math.Abs(paragraph.GlyphSpacing[2] - 1) > Toleransi ||

                                paragraph.Hanging != false ||

                                paragraph.HyphenatedWordSize != 6 ||

                                paragraph.KinsokuOrder != 0 ||

                                paragraph.LetterSpacing.Length != 3 ||

                                Math.Abs(paragraph.LetterSpacing[0]) > Toleransi ||

                                Math.Abs(paragraph.LetterSpacing[1]) > Toleransi ||

                                Math.Abs(paragraph.LetterSpacing[2]) > Toleransi ||

                                paragraph.LeadingType != LeadingMode.Auto ||

                                paragraph.PreHyphen != 2 ||

                                paragraph.PostHyphen != 2 ||

                                Math.Abs(paragraph.SpaceBefore) > Toleransi ||

                                Math.Abs(paragraph.SpaceAfter) > Toleransi ||

                                paragraph.WordSpacing.Length != 3 ||

                                Math.Abs(paragraph.WordSpacing[0] - 0.8) > Toleransi ||

                                Math.Abs(paragraph.WordSpacing[1] - 1.0) > Toleransi ||

                                Math.Abs(paragraph.WordSpacing[2] - 1.33) > Toleransi ||

                                Math.Abs(paragraph.Zone - 36.0) > Toleransi)

                            {

                                throw new Exception();

                            }

                        }

                        // Memeriksa data gaya

                        // Gaya memiliki warna dan ukuran font yang berbeda

                        if (Math.Abs(portions[0].Style.FontSize - 12) > Toleransi ||

                            Math.Abs(portions[1].Style.FontSize - 12) > Toleransi ||

                            Math.Abs(portions[2].Style.FontSize - 12) > Toleransi ||

                            Math.Abs(portions[3].Style.FontSize - 10) > Toleransi)

                        {

                            throw new Exception();

                        }

                        if (portions[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            portions[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            portions[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            portions[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var style = portions[j].Style;

                            if (style.AutoLeading != false ||

                                style.HindiNumbers != false ||

                                style.Kerning != 0 ||

                                style.Leading != 0 ||

                                style.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                style.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Contoh pengeditan teks

                        portions[0].Text = "Halo ";

                        portions[1].Text = "Dunia";

                        // Contoh menghapus bagian teks

                        layer.TextData.RemovePortion(3);

                        layer.TextData.RemovePortion(2);

                        // Contoh menambahkan bagian teks baru

                        var createdPortion = layer.TextData.ProducePortion();

                        createdPortion.Text = "!!!\r";

                        layer.TextData.AddPortion(createdPortion);

                        portions = layer.TextData.Items;

                        // Contoh pengeditan paragraf dan gaya untuk bagian teks

                        // Tetapkan justifikasi yang tepat

                        portions[0].Paragraph.Justification = 1;

                        portions[1].Paragraph.Justification = 1;

                        portions[2].Paragraph.Justification = 1;

                        // Warna yang berbeda untuk setiap gaya. Akan diubah, tetapi rendering tidak sepenuhnya didukung

                        portions[0].Style.FillColor = Color.Aquamarine;

                        portions[1].Style.FillColor = Color.Violet;

                        portions[2].Style.FillColor = Color.LightBlue;

                        // Font yang berbeda. Akan diubah, tetapi rendering tidak sepenuhnya didukung

                        portions[0].Style.FontSize = 6;

                        portions[1].Style.FontSize = 8;

                        portions[2].Style.FontSize = 10;

                        layer.TextData.UpdateLayerData();

                        im.Save(outputPath, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Dukungan untuk Menambahkan grup lapisan**

{{< highlight java >}}

             // -Grup 1

            // --Lapisan 1

            // --Grup 2

            // ---Lapisan 2

            // ---Lapisan 3

            // --Lapisan 4

            string dataDir = "psdnet190_test.psd";

            var createOptions = new PsdOptions();

            createOptions.Source = new FileCreateSource(dataDir, false);

            createOptions.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var psdImage = (PsdImage)Image.Create(createOptions, 500, 500))

            {

                LayerGroup group1 = psdImage.AddLayerGroup("Grup 1", 0, true);

                Layer lapisan1 = new Layer(psdImage);

                lapisan1.Name = "Lapisan 1";

                group1.AddLayer(lapisan1);

                LayerGroup group2 = group1.AddLayerGroup("Grup 2", 1);

                Layer lapisan2 = new Layer(psdImage);

                lapisan2.Name = "Lapisan 2";

                group2.AddLayer(lapisan2);

                Layer lapisan3 = new Layer(psdImage);

                lapisan3.Name = "Lapisan 3";

                group2.AddLayer(lapisan3);

                Layer lapisan4 = new Layer(psdImage);

                lapisan4.Name = "Lapisan 4";

                group1.AddLayer(lapisan4);

                psdImage.Save();

            }

{{< /highlight >}}

**PSDNET-192. Dukungan untuk Properti Skala untuk Lapisan Isian Gradien**

{{< highlight java >}}

            using (var image = (PsdImage)Image.Load("FillLayerGradient.psd"))

            {

                // mendapatkan lapisan isian

                FillLayer lapisanIsian = null;

                foreach (var layer in image.Layers)

                {

                    lapisanIsian = lapisan as FillLayer;

                    if (lapisanIsian != null)

                    {

                        break;

                    }

                }

                var pengaturan = lapisanIsian.FillSettings as IGradientFillSettings;

                // memperbarui nilai skala

                pengaturan.Scale = 200;

                lapisanIsian.Update(); // Memperbarui data piksel

                image.Save("scaledImage.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}



**PSDNET-174. IndexOutOfRangeException saat menyimpan gambar PSD sebagai JPEG**

{{< highlight java >}}

         using (var image = Aspose.PSD.Image.Load("SamplePSD.psd"))

        {

            image.Save("sampleJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}

**PSDNET-180. Memperbarui teks layer teks memunculkan pengecualian**

{{< highlight java >}}

           // Memperbarui teks layer teks memunculkan pengecualian

            string filePath = "FlipVertical.psd";

            string outputPath = "FlipVertical_changed.psd";

            var teksBaru = "Uji";

            using (var image = Image.Load(filePath))

            {

                var psdImage = image as PsdImage;

                if (image == null)

                {

                    return;

                }

                var lapisan = psdImage.Layers;

                for (var indeks = lapisan.Length - 1; indeks >= 0; indeks--)

                {

                    var layer = lapisan[indeks] as TextLayer;

