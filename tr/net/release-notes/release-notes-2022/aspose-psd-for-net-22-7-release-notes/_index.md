---
title: Aspose.PSD for .NET 22.7 - Sürüm Notları
type: docs
weight: 60
url: /tr/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Bu sayfada [Aspose.PSD for .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notları bulunmaktadır.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-482|Resim Bölüm Kaynağı #4000-4999 Eklentisi destekleme|Özellik|
|PSDNET-875|Aspose.PSD.dll'de "System.OutOfMemoryException" türünde ele alınmayan bir istisna oluşur|Hata|
|PSDNET-1050|PSD dosyasını dışa aktardıktan sonra sonuç kaynak dosyadan çok daha büyüktür|Hata|
|PSDNET-1083|XmpResource için verinin yanlış ayrıştırılması|Hata|
|PSDNET-1205|Dışa aktarıldıktan sonra alt klasörleri olan PSD dosyalarının boyutu artmıştır|Hata|

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
- Hiçbiri

## **Kullanım Örnekleri:**

**PSDNET-482. Resim Bölüm Kaynağı #4000-4999 Eklentisi destekleme**

{{< highlight csharp >}}
// Aşağıdaki kod, animasyonlu verilerin zaman çizelgesindeki gecikme süresini nasıl ayarlayacağını veya güncelleyeceğini göstermektedir.
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
    List<OSTypeStructure> listOfStructures = new List<OSTypeStructure>(structures);

    for (int i = 0; i < listOfStructures.Count; i++)
    {
        OSTypeStructure structure = listOfStructures[i];
        if (structure.KeyName.ClassName == newStructure.KeyName.ClassName)
        {
            listOfStructures.RemoveAt(i);
            break;
        }
    }

    listOfStructures.Add(newStructure);

    return listOfStructures.ToArray();
}

using (PsdImage image = (PsdImage)Image.Load(kaynakDosya))
{
    foreach (var imageResource in image.ImageResources)
    {
        if (imageResource is AnimatedDataSectionResource)
        {
            var animatedData = (AnimatedDataSectionStructure)(imageResource as AnimatedDataSectionResource).AnimatedDataSection;
            var framesList = FindStructure<ListStructure>(animatedData.Items, "FrIn");

            var frame1 = (DescriptorStructure)framesList.Types[1];

            // 100 centi-saniye değerine eşit olan 1 saniyelik bir çerçeve gecikme kaydı oluşturur.
            var frameDelay = new IntegerStructure(new ClassID("FrDl"));
            frameDelay.Value = 100; // centi-saniye cinsinden zaman ayarlayın.

            frame1.Structures = AddOrReplaceStructure(frame1.Structures, frameDelay);

            break;
        }
    }

    image.Save(ciktiPsd);
}
{{< /highlight >}}

**PSDNET-875. Aspose.PSD.dll'de "System.OutOfMemoryException" türünde ele alınmayan bir istisna oluşur**

{{< highlight csharp >}}
string srcFile = "001-.psd";
string jpgFilePath = "T_0003.jpg";
string outputFilePath = "output_newPsd.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    using (FileStream fs = new FileStream(jpgFilePath, FileMode.Open))
    {
        var newLayer = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        newLayer.DisplayName = "YeniKatman";

        im.AddLayer(newLayer);

        im.Save(outputFilePath, true);   
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

double ciktiBoyutuMb = new FileInfo(cikti).Length / 1024d / 1024d;
if (ciktiBoyutuMb > 6)
{
    throw new Exception("Çıktı dosyası beklenenden daha büyüktür.");
}
{{< /highlight >}}

**PSDNET-1083. XmpResource için verinin yanlış ayrıştırılması**

{{< highlight csharp >}}
string inputPsdImagePath = @"input.psd";
string savedPsdImagePath = @"saved.psd";

bool orijinalİçerir = false;
bool kaydedilmişİçerir = false;

// Giriş dosyasındaki alt XMP anahtarını bul
using (PsdImage img = (PsdImage)Image.Load(inputPsdImagePath))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string xmlValue = xmpArray.GetXmlValue();

                if (xmlValue.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    orijinalİçerir = true;
                    break;
                }
            }
        }

        if (orijinalİçerir)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

// Kaydedilmiş dosyadaki alt XMP anahtarını bul
using (PsdImage img = (PsdImage)Image.Load(savedPsdImagePath))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string xmlValue = xmpArray.GetXmlValue();

                if (xmlValue.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    kaydedilmişİçerir = true;
                    break;
                }
            }
        }

        if (kaydedilmişİçerir)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

if (orijinalİçerir && kaydedilmişİçerir)
{
    // Her şey yolunda!
}
else
{
    throw new Exception("Çalışmıyor");
}
{{< /highlight >}}

**PSDNET-1205. Dışa aktarıldıktan sonra alt klasörleri olan PSD dosyalarının boyutu artmıştır**

{{< highlight csharp >}}
string[] kaynakDosyalar = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var dosyaAdı in kaynakDosyalar)
{
    string kaynakDosyaYolu = dosyaAdı;
    string ciktiDosyaYolu = "cikti_" + dosyaAdı;

    using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaYolu))
    {
        image.Save(ciktiDosyaYolu);
    }

    double ciktiBoyutuMb = new FileInfo(ciktiDosyaYolu).Length / 1024d / 1024d;
    if (ciktiBoyutuMb > 1.9)
    {
        throw new Exception("Çıktı dosyası beklenenden daha büyüktür.");
    }
}
{{< /highlight >}}
