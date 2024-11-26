---
title: Aspose.PSD for .NET 22.7 - Sürüm Notları
type: docs
weight: 60
url: /tr/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-482|Resim Bölüm Kaynağı #4000-4999 Eklenti kaynağını destekle|#Özellik|
|PSDNET-875|Aspose.PSD.dll içinde "System.OutOfMemoryException" türünde ele alınmamış bir istisna oluşur|Hata|
|PSDNET-1050|PSD dosyasını dışa aktardıktan sonra sonuç kaynak dosyadan çok daha büyüktür|Hata|
|PSDNET-1083|XmpResource için veri ayrıştırması yanlış|Hata|
|PSDNET-1205|Dışa aktardıktan sonra alt klasörlere sahip PSD dosyalarının boyutu artmıştır|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.SaveData(Aspose.PSD.StreamContainer)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.KeyName
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.AnimatedDataSection
- M:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.SaveData(Aspose.PSD.StreamContainer)


# **Kaldırılan API'lar:**
- Yok


## **Kullanım Örnekleri:**

**PSDNET-482. Resim Bölüm Kaynağı #4000-4999 Eklenti kaynağını destekle**

{{< highlight csharp >}}
// Aşağıdaki kod, animasyonlu verinin zaman çizelgesinde gecikme süresinin nasıl ayarlanacağını/güncelleneceğini gösterir.
string kaynakDosya = "3_animated.psd";
string ciktiPsd = "cikti_3_animated.psd";

T FindStructure<T>(IEnumerable<OSTypeStructure> structures, string keyName) where T : OSTypeStructure
{
    foreach (var structure in structures)
    {
        if (structure.KeyName.ClassName == keyName)
        {
            return structure as T;
        }
    }

    return null;
}

OSTypeStructure[] AddOrReplaceStructure(IEnumerable<OSTypeStructure> structures, OSTypeStructure newStructure)
{
    List<OSTypeStructure> structureListesi = new List<OSTypeStructure>(structures);

    for (int i = 0; i < structureListesi.Count; i++)
    {
        OSTypeStructure structure = structureListesi[i];
        if (structure.KeyName.ClassName == newStructure.KeyName.ClassName)
        {
            structureListesi.RemoveAt(i);
            break;
        }
    }

    structureListesi.Add(newStructure);

    return structureListesi.ToArray();
}

using (PsdImage resim = (PsdImage)Image.Load(kaynakDosya))
{
    foreach (var resimKaynagi in resim.ImageResources)
    {
        if (resimKaynagi is AnimatedDataSectionResource)
        {
            var animasyonluVeri =
            (AnimatedDataSectionStructure) (resimKaynagi as AnimatedDataSectionResource).AnimatedDataSection;
            var framesList = FindStructure<ListStructure>(animasyonluVeri.Items, "FrIn");

            var frame1 = (DescriptorStructure)framesList.Types[1];

            // Değer 1 saniyeye eşit olan 100 santisaniye olarak belirtilmiş olan çerçeve gecikme kaydı oluşturur.
            var frameGecikme = new IntegerStructure(new ClassID("FrDl"));
            frameGecikme.Value = 100; // santisaniye cinsinden zamanı ayarlar.

            frame1.Structures = AddOrReplaceStructure(frame1.Structures, frameGecikme);

            break;
        }
    }

    resim.Save(ciktiPsd);
}
{{< /highlight >}}

**PSDNET-875. Aspose.PSD.dll içinde "System.OutOfMemoryException" türünde ele alınmamış bir istisna oluşur**

{{< highlight csharp >}}
string kaynakDosya = "001-.psd";
string jpgDosyaYolu = "T_0003.jpg";
string ciktiDosyaYolu = "cikti_yeniPsd.psd";

using (var im = (PsdImage)Image.Load(kaynakDosya))
{
    using (FileStream fs = new FileStream(jpgDosyaYolu, FileMode.Open))
    {
        var yeniKatman = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        yeniKatman.DisplayName = "YeniKatman";

        im.AddLayer(yeniKatman);

        im.Save(ciktiDosyaYolu, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. PSD dosyasını dışa aktardıktan sonra sonuç kaynak dosyadan çok daha büyüktür**

{{< highlight csharp >}}
string kaynak = "ShimadzuLetterhead100.psd";
string cikti = "cikti.psd";
using (var img = (PsdImage)Image.Load(kaynak))
{
    img.Save(cikti);
}

double ciktiBoyutMb = new FileInfo(cikti).Length / 1024d / 1024d;
if (ciktiBoyutMb > 6)
{
    throw new Exception("Çıktı dosyası beklenenden daha büyüktür.");
}
{{< /highlight >}}

**PSDNET-1083. XmpResource için veri ayrıştırması yanlış**

{{< highlight csharp >}}
string girdiPsdResimYolu = @"girdi.psd";
string kaydedilmisPsdResimYolu = @"kaydedilmis.psd";

bool orijinalIcerir = false;
bool kaydedilenIcerir = false;

// Giriş dosyasında alt XMP anahtarını bul
using (PsdImage img = (PsdImage)Image.Load(girdiPsdResimYolu))
{
    foreach (var paket in img.XmpData.Packages)
    {
        foreach (var pak in paket)
        {
            if (pak.Value is XmpArray)
            {
                XmpArray xmpDizisi = (XmpArray)pak.Value;

                string xmlDeger = xmpDizisi.GetXmlValue();

                if (xmlDeger.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    orijinalIcerir = true;
                    break;
                }
            }
        }

        if (orijinalIcerir)
        {
            break;
        }
    }
    img.Save(kaydedilmisPsdResimYolu);
}

// Kaydedilen dosyada alt XMP anahtarını bul
using (PsdImage img = (PsdImage)Image.Load(kaydedilmisPsdResimYolu))
{
    foreach (var paket in img.XmpData.Packages)
    {
        foreach (var pak in paket)
        {
            if (pak.Value is XmpArray)
            {
                XmpArray xmpDizisi = (XmpArray)pak.Value;

                string xmlDeger = xmpDizisi.GetXmlValue();

                if (xmlDeger.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    kaydedilenIcerir = true;
                    break;
                }
            }
        }

        if (kaydedilenIcerir)
        {
            break;
        }
    }
    img.Save(kaydedilmisPsdResimYolu);
}

if (orijinalIcerir && kaydedilenIcerir)
{
    // Her şey yolunda!
}
else
{
    throw new Exception("İşe yaramaz");
}
{{< /highlight >}}

**PSDNET-1205. Dışa aktardıktan sonra alt klasörlere sahip PSD dosyalarının boyutu artmıştır**

{{< highlight csharp >}}
string[] kaynakDosyalar = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var dosyaAdı in kaynakDosyalar)
{
    string kaynakDosyaYolu = dosyaAdı;
    string ciktiDosyaYolu = "cikti_" + dosyaAdı;

    using (PsdImage resim = (PsdImage)Image.Load(kaynakDosyaYolu))
    {
        resim.Save(ciktiDosyaYolu);
    }

    double ciktiBoyutMb = new FileInfo(ciktiDosyaYolu).Length / 1024d / 1024d;
    if (ciktiBoyutMb > 1.9)
    {
        throw new Exception("Çıktı dosyası beklenenden daha büyüktür.");
    }
}
{{< /highlight >}}
