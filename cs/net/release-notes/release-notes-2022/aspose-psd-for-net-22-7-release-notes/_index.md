---
title: Aspose.PSD pro .NET 22.7 - Poznámky k vydání
type: docs
weight: 60
url: /cs/net/aspose-psd-pro-net-22-7-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-482|Podpora pro sekci zdroje obrazu #4000-4999 Plug-In resource(s)|Funkce|
|PSDNET-875|Nerušená výjimka "System.OutOfMemoryException" typu se objevuje v Aspose.PSD.dll|Chyba|
|PSDNET-1050|Po exportu souboru PSD je výsledek mnohem větší než zdrojový soubor|Chyba|
|PSDNET-1083|Nesprávný rozbor dat pro XmpResource|Chyba|
|PSDNET-1205|Po exportu se zvětšil rozměr souborů PSD se složkami|Chyba|


## **Změny ve veřejné API**
# **Přidaná API:**
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


# **Odebraná API:**
- Žádné


## **Příklady použití:**

**PSDNET-482. Podpora pro sekci zdroje obrazu #4000-4999 Plug-In resource(s)**

{{< highlight csharp >}}
// Následující kód demonstruje, jak nastavit/aktualizovat dobu zpoždění v rámci časové osy snímku animovaných dat.
string sourceFile = "3_animated.psd";
string outputPsd = "output_3_animated.psd";

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

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    foreach (var imageResource in image.ImageResources)
    {
        if (imageResource is AnimatedDataSectionResource)
        {
            var animatedData =
            (AnimatedDataSectionStructure) (imageResource as AnimatedDataSectionResource).AnimatedDataSection;
            var framesList = FindStructure<ListStructure>(animatedData.Items, "FrIn");

            var frame1 = (DescriptorStructure)framesList.Types[1];

            // Vytvoří záznam o zpoždění snímku s hodnotou 100 centi-sekund, což je rovno 1 sekundě.
            var frameDelay = new IntegerStructure(new ClassID("FrDl"));
            frameDelay.Value = 100; // nastaví čas v centi-sekundách.

            frame1.Structures = AddOrReplaceStructure(frame1.Structures, frameDelay);

            break;
        }
    }

    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-875. Nerušená výjimka "System.OutOfMemoryException" typu se objevuje v Aspose.PSD.dll**

{{< highlight csharp >}}
string srcFile = "001-.psd";
string jpgFilePath = "T_0003.jpg";
string outputFilePath = "output_newPsd.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    using (FileStream fs = new FileStream(jpgFilePath, FileMode.Open))
    {
        var newLayer = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        newLayer.DisplayName = "Nová vrstva";

        im.AddLayer(newLayer);

        im.Save(outputFilePath, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Po exportu souboru PSD je výsledek mnohem větší než zdrojový soubor**

{{< highlight csharp >}}
string src = "ShimadzuLetterhead100.psd";
string output = "output.psd";
using (var img = (PsdImage)Image.Load(src))
{
    img.Save(output);
}

double outputSizeMb = new FileInfo(output).Length / 1024d / 1024d;
if (outputSizeMb > 6)
{
    throw new Exception("Výstupní soubor je větší, než by měl být.");
}
{{< /highlight >}}

**PSDNET-1083. Nesprávný rozbor dat pro XmpResource**

{{< highlight csharp >}}
string inputPsdImagePath = @"input.psd";
string savedPsdImagePath = @"saved.psd";

bool isOriginalContain = false;
bool isSavedContain = false;

// Najde podklíč XMP vstupního souboru
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
                    isOriginalContain = true;
                    break;
                }
            }
        }

        if (isOriginalContain)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

// Najde podklíč XMP v uloženém souboru
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
                    isSavedContain = true;
                    break;
                }
            }
        }

        if (isSavedContain)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

if (isOriginalContain && isSavedContain)
{
    // Vše je v pořádku!
}
else
{
    throw new Exception("To nefunguje");
}
{{< /highlight >}}

**PSDNET-1205. Po exportu se zvětšil rozměr souborů PSD se složkami**

{{< highlight csharp >}}
string[] sourceFiles = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var fileName in sourceFiles)
{
    string sourceFilePath = fileName;
    string outputFilePath = "output_" + fileName;

    using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
    {
        image.Save(outputFilePath);
    }

    double outputSizeMb = new FileInfo(outputFilePath).Length / 1024d / 1024d;
    if (outputSizeMb > 1.9)
    {
        throw new Exception("Výstupní soubor je větší, než by měl být.");
    }
}
{{< /highlight >}}
