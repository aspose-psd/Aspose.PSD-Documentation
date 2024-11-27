---
title: Note di rilascio di Aspose.PSD per .NET 24.3
type: docs
weight: 100
url: /it/net/aspose-psd-per-net-24-3-note-di-rilascio/
---

{{% alert color="primary" %}}

Questa pagina contiene le note di rilascio per [Aspose.PSD per .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                              | **Categoria**  |
|:------------|:--------------------------------------------------------------------------|:--------------|
| PSDNET-1905 | [Formato AI] Riduzione del tempo di caricamento delle immagini AI multipagina grandi | Miglioramento |
| PSDNET-1906 | Il file PSD dopo la conversione da 8 bit a 32 bit è diventato illeggibile      | Bug          |
| PSDNET-1914 | [Formato AI] Risoluzione del rendering della curva corta nel file AI      | Bug          |

## **Modifiche alla API pubblica**
# **API aggiunte:**
- Nessuna

# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDNET-1905. Il file PSD dopo la conversione da 8 bit a 16 bit è diventato illeggibile**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "test_smart_layer.psd");
string fileOutput = Path.Combine(cartellaOutput, "export.psd");

using (var immaginePsd8 = (PsdImage)Image.Load(fileSorgente))
{
    var opzioniPsd16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    immaginePsd8.Save(fileOutput, opzioniPsd16);
}

using (var immaginePsd16 = (PsdImage)Image.Load(fileOutput))
{
    if (immaginePsd16.GlobalLayerResources[0] is Lr16Resource)
    {
        // è corretto
    }
    else
    {
        throw new Exception("Risorsa globale errata, la prima risorsa dovrebbe essere Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. Il file PSD dopo la conversione da 8 bit a 32 bit è diventato illeggibile**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "test_smart_layer.psd");
string fileOutput = Path.Combine(cartellaOutput, "export.psd");

using (var immaginePsd8 = (PsdImage)Image.Load(fileSorgente))
{
    var opzioniPsd32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    immaginePsd8.Save(fileOutput, opzioniPsd32);
}

using (var immaginePsd8 = (PsdImage)Image.Load(fileOutput))
{
    if (immaginePsd8.GlobalLayerResources[0] is Lr32Resource)
    {
        // è corretto
    }
    else
    {
        throw new Exception("Risorsa globale errata, la prima risorsa dovrebbe essere Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [Formato AI] Risoluzione del rendering della curva corta nel file AI**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "shortCurve.ai");
string percorsoOutput = Path.Combine(cartellaOutput, "shortCurve.png");

using (AiImage immagine = (AiImage)Image.Load(fileSorgente))
{
    immagine.Save(percorsoOutput, new PngOptions());
}
{{< /highlight >}}
