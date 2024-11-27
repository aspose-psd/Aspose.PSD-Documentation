---
title: Note di rilascio di Aspose.PSD for .NET 22.7
type: documentazione
weight: 60
url: /it/net/aspose-psd-for-net-22-7-note-di-rilascio/
---

{{% alert color="primary" %}}

Questa pagina contiene le note di rilascio per [Aspose.PSD for .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-482|Supporto delle Risorse della Sezione delle Immagini #4000-4999 Plug-In resource(s)|Funzionalità|
|PSDNET-875|Si verifica un'eccezione non gestita di tipo "System.OutOfMemoryException" in Aspose.PSD.dll|Bug|
|PSDNET-1050|Dopo l'esportazione del file PSD, il risultato è molto più grande del file sorgente|Bug|
|PSDNET-1083|Analisi errata dei dati per XmpResource|Bug|
|PSDNET-1205|Dopo l'esportazione, le dimensioni dei file PSD con sottocartelle sono aumentate|Bug|


## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
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


# **API rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-482. Supporto delle Risorse della Sezione delle Immagini #4000-4999 Plug-In resource(s)**

{{< highlight csharp >}}
// Il codice seguente dimostra come impostare/aggiornare il tempo di ritardo nell'immagine della cornice temporale dei dati animati.
string fileSorgente = "3_animated.psd";
string psdOutput = "output_3_animated.psd";

T TrovaStruttura<T>(IEnumerable<OSTypeStructure> strutture, string nomeChiave) where T : OSTypeStructure
{
    foreach (var struttura in strutture)
    {
        if (struttura.KeyName.ClassName == nomeChiave)
        {
            return struttura as T;
        }
    }

    return null;
}

OSTypeStructure[] AggiungiOAggiornaStruttura(IEnumerable<OSTypeStructure> strutture, OSTypeStructure nuovaStruttura)
{
    List<OSTypeStructure> listaStrutture = new List<OSTypeStructure>(strutture);

    for (int i = 0; i < listaStrutture.Count; i++)
    {
        OSTypeStructure struttura = listaStrutture[i];
        if (struttura.KeyName.ClassName == nuovaStruttura.KeyName.ClassName)
        {
            listaStrutture.RemoveAt(i);
            break;
        }
    }

    listaStrutture.Add(nuovaStruttura);

    return listaStrutture.ToArray();
}

using (PsdImage immagine = (PsdImage)Image.Load(fileSorgente))
{
    foreach (var risorsaImmagine in immagine.ImageResources)
    {
        if (risorsaImmagine is AnimatedDataSectionResource)
        {
            var datiAnimati =
            (AnimatedDataSectionStructure) (risorsaImmagine as AnimatedDataSectionResource).AnimatedDataSection;
            var listaFrames = TrovaStruttura<ListStructure>(datiAnimati.Items, "FrIn");

            var frame1 = (DescriptorStructure)listaFrames.Types[1];

            // Crea il record di ritardo dell'immagine con valore 100 centesimi di secondo che corrisponde a 1 secondo.
            var ritardoFrame = new IntegerStructure(new ClassID("FrDl"));
            ritardoFrame.Value = 100; // imposta il tempo in centesimi di secondo.

            frame1.Structures = AggiungiOAggiornaStruttura(frame1.Structures, ritardoFrame);

            break;
        }
    }

    immagine.Save(psdOutput);
}
{{< /highlight >}}

**PSDNET-875. Si verifica un'eccezione non gestita di tipo "System.OutOfMemoryException" in Aspose.PSD.dll**

{{< highlight csharp >}}
string fileSrc = "001-.psd";
string percorsoJpg = "T_0003.jpg";
string percorsoOutput = "output_newPsd.psd";

using (var im = (PsdImage)Image.Load(fileSrc))
{
    using (FileStream fs = new FileStream(percorsoJpg, FileMode.Open))
    {
        var nuovoLivello = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        nuovoLivello.DisplayName = "NuovoLivello";

        im.AddLayer(nuovoLivello);

        im.Save(percorsoOutput, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Dopo l'esportazione del file PSD, il risultato è molto più grande del file sorgente**

{{< highlight csharp >}}
string fileSrc = "ShimadzuLetterhead100.psd";
string output = "output.psd";
using (var img = (PsdImage)Image.Load(fileSrc))
{
    img.Save(output);
}

double dimensioneOutputMb = new FileInfo(output).Length / 1024d / 1024d;
if (dimensioneOutputMb > 6)
{
    throw new Exception("Il file di output è più grande di quanto dovrebbe essere.");
}
{{< /highlight >}}

**PSDNET-1083. Analisi errata dei dati per XmpResource**

{{< highlight csharp >}}
string percorsoImmaginePsdInput = @"input.psd";
string percorsoImmaginePsdSalvata = @"saved.psd";

bool contenutoOriginalePresente = false;
bool contenutoSalvatoPresente = false;

// Trova la chiave XMP secondaria nel file di input
using (PsdImage img = (PsdImage)Image.Load(percorsoImmaginePsdInput))
{
    foreach (var pacchetto in img.XmpData.Packages)
    {
        foreach (var pac in pacchetto)
        {
            if (pac.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pac.Value;

                string valoreXml = xmpArray.GetXmlValue();

                if (valoreXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    contenutoOriginalePresente = true;
                    break;
                }
            }
        }

        if (contenutoOriginalePresente)
        {
            break;
        }
    }
    img.Save(percorsoImmaginePsdSalvata);
}

// Trova la chiave XMP secondaria nel file salvato
using (PsdImage img = (PsdImage)Image.Load(percorsoImmaginePsdSalvata))
{
    foreach (var pacchetto in img.XmpData.Packages)
    {
        foreach (var pac in pacchetto)
        {
            if (pac.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pac.Value;

                string valoreXml = xmpArray.GetXmlValue();

                if (valoreXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    contenutoSalvatoPresente = true;
                    break;
                }
            }
        }

        if (contenutoSalvatoPresente)
        {
            break;
        }
    }
    img.Save(percorsoImmaginePsdSalvata);
}

if (contenutoOriginalePresente && contenutoSalvatoPresente)
{
    // Tutto ok!
}
else
{
    throw new Exception("Non funziona");
}
{{< /highlight >}}

**PSDNET-1205. Dopo l'esportazione, le dimensioni dei file PSD con sottocartelle sono aumentate**

{{< highlight csharp >}}
string[] fileSorgenti = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var fileName in fileSorgenti)
{
    string percorsoSorgente = fileName;
    string percorsoOutput = "output_" + fileName;

    using (PsdImage immagine = (PsdImage)Image.Load(percorsoSorgente))
    {
        immagine.Save(percorsoOutput);
    }

    double dimensioneOutputMb = new FileInfo(percorsoOutput).Length / 1024d / 1024d;
    if (dimensioneOutputMb > 1.9)
    {
        throw new Exception("Il file di output è più grande di quanto dovrebbe essere.");
    }
}
{{< /highlight >}}
