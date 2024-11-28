---
title: Aspose.PSD für .NET 22.7 - Versionshinweise
type: docs
weight: 60
url: /de/net/aspose-psd-für-net-22-7-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-482|Unterstützung von Bildbereichsressource #4000-4999 Plug-In-Ressource(n)|Feature|
|PSDNET-875|Eine unbehandelte Ausnahme des Typs "System.OutOfMemoryException" tritt in Aspose.PSD.dll auf|Fehler|
|PSDNET-1050|Nach dem Exportieren der PSD-Datei ist das Ergebnis viel größer als die Quelldatei|Fehler|
|PSDNET-1083|Fehlerhafte Datenanalyse für XmpResource|Fehler|
|PSDNET-1205|Nach dem Exportieren hat sich die Größe von PSD-Dateien mit Unterordnern erhöht|Fehler|


## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
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


# **Entfernte APIs:**
- Keine


## **Beispiele für die Verwendung:**

**PSDNET-482. Unterstützung von Bildbereichsressource #4000-4999 Plug-In-Ressource(n)**

{{< highlight csharp >}}
// Der folgende Code zeigt, wie die Verzögerungszeit im Zeitrahmen des animierten Datensatzes festgelegt/aktualisiert wird.
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

            // Erstellt den Rahmenverzögerungseintrag mit dem Wert 100 Hundertstel-Sekunde, was 1 Sekunde entspricht.
            var frameDelay = new IntegerStructure(new ClassID("FrDl"));
            frameDelay.Value = 100; // Zeit in Hundertstel-Sekunden festlegen.

            frame1.Structures = AddOrReplaceStructure(frame1.Structures, frameDelay);

            break;
        }
    }

    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-875. Eine unbehandelte Ausnahme des Typs "System.OutOfMemoryException" tritt in Aspose.PSD.dll auf**

{{< highlight csharp >}}
string srcFile = "001-.psd";
string jpgFilePath = "T_0003.jpg";
string outputFilePath = "output_newPsd.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    using (FileStream fs = new FileStream(jpgFilePath, FileMode.Open))
    {
        var newLayer = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        newLayer.DisplayName = "NeueEbene";

        im.AddLayer(newLayer);

        im.Save(outputFilePath, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Nach dem Exportieren der PSD-Datei ist das Ergebnis viel größer als die Quelldatei**

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
    throw new Exception("Die Ausgabedatei ist größer als sie sollte.");
}
{{< /highlight >}}

**PSDNET-1083. Fehlerhafte Datenanalyse für XmpResource**

{{< highlight csharp >}}
string inputPsdImagePath = @"input.psd";
string savedPsdImagePath = @"saved.psd";

bool isOriginalContain = false;
bool isSavedContain = false;

// Sub-XMP-Schlüssel in Eingabedatei finden
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

// Sub-XMP-Schlüssel in gespeicherter Datei finden
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
    // Alles ist in Ordnung!
}
else
{
    throw new Exception("Es funktioniert nicht");
}
{{< /highlight >}}

**PSDNET-1205. Nach dem Exportieren hat sich die Größe von PSD-Dateien mit Unterordnern erhöht**

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
        throw new Exception("Die Ausgabedatei ist größer als sie sollte.");
    }
}
{{< /highlight >}}
