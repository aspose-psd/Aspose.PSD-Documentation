---
title: Catatan Rilis Aspose.PSD untuk .NET 21.1
type: docs
weight: 120
url: /id/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Exception saat mencoba mengonversi file Psd tertentu ke png|Bug|
|PSDNET-792|Exception saat menyimpan PSD dengan smart object ke PNG|Bug|

## **Perubahan API Publik**
# **API yang Ditambahkan:**
- Tidak ada

# **API yang Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**
**PSDNET-766. Aspose.PSD 20.10: Exception saat mencoba mengonversi file Psd tertentu ke png**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Exception saat menyimpan PSD dengan smart object ke PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Mencari Smart Object
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Kami sedang memuat Lapisan Smart Object dari Memori Stream,
                        // Tetapi kami bisa menggunakan smart smart.ExportContents(somePath) untuk mengekspor smart object ke file
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
                                        // Kami bisa menggunakan UpdateText sederhana, tetapi cara ini memberikan kemampuan kepada kami untuk mengedit teks secara berurutan
                                        // Buat lapisan teks multiline dan fitur pengeditan teks dan paragraf lainnya
                                        // Harap berhati-hati. Jika Konten Smart Object bukan PSD, Anda tidak dapat menggunakan cara ini untuk mengedit teks
                                        // Dalam hal tersebut, Anda harus menggunakan API Grafis: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Terbaik";

                                        // Anda harus mengubah ukuran teks jika Anda ingin membuat gambar terlihat baik.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Lebih baik menggunakan ReplaceContents. Ini akan secara otomatis membuat ulang Smart Object
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Dengan cara ini kami menyimpan File PSD yang telah diubah
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}  
