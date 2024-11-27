---
title: Catatan Rilis Aspose.PSD untuk .NET 21.8
type: docs
weight: 50
url: /id/net/aspose-psd-untuk-net-21-8-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-698|Dukungan untuk Metode Kompresi ZipWithPrediction|Fitur|
|PSDNET-663|Jarak teks tidak benar dalam PSD yang dibuat|Bug|
|PSDNET-685|Pengecualian saat menyimpan PSD|Bug|
|PSDNET-927|Jarak yang tidak benar antara baris dan simbol di Aspose.PSD ketika kita menggunakannya tanpa lisensi|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

**PSDNET-663. Jarak teks tidak benar dalam PSD yang dibuat**

{{< highlight csharp >}}
            string namaFileSumber = "sumber.psd";
            string namaFileKeluaran = "keluaran.png";

            menggunakan (PsdImage gambar = (PsdImage)Image.Load(namaFileSumber))
            {
                gambar.Save(namaFileKeluaran, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Pengecualian saat menyimpan PSD**

{{< highlight csharp >}}
            string namaFileSumber = "File.psd";
            string namaFileKeluaran = "File2.psd";

            menggunakan (PsdImage gambar = (PsdImage)Image.Load(namaFileSumber))
            {
                var layer1 = (TextLayer)gambar.Layers[1];
                layer1.TextData.UpdateLayerData();

                gambar.Save(namaFileKeluaran);
            }
{{< /highlight >}}

**PSDNET-698. Dukungan untuk Metode Kompresi ZipWithPrediction**

{{< highlight csharp >}}
            string jalurBerkasMasukan = "zipTest698.psd";

            string keluaranPng = "keluaran.png";
            string keluaranRaw = "out_Raw.psd";
            string keluaranZip = "out_Zip.psd";

            menggunakan (Image gambar = Image.Load(jalurBerkasMasukan))
            {
                image.Save(outputPng, new PngOptions());

                image.Save(outputRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                image.Save(outputZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Jarak yang tidak benar antara baris dan simbol di Aspose.PSD ketika kita menggunakannya tanpa lisensi**

{{< highlight csharp >}}
            bool[] statusLisensi = new bool[] { false, true };
            untuk (int i = 0; i < statusLisensi.Length; i++)
            {
                boolean ujiLisensi = statusLisensi[i];
                jika (ujiLisensi)
                {
                    Lisensi lisensi = new Lisensi();
                    license.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string berkasSumber = "psdnetTest927.psd";
                string berkasKeluaran = "keluar_" + testLicense.ToString() + "_psdnetTest927.png";

                menggunakan (var gambar = (PsdImage)Image.Load(berkasSumber))
                {
                    image.Save(berkasKeluaran, new PngOptions());
                }
            }
{{< /highlight >}}
