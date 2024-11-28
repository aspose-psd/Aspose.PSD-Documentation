---
title: Note sulla versione di Aspose.PSD per .NET 24.2
type: docs
weight: 110
url: /it/net/aspose-psd-for-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                         | **Categoria** |
|:-----------|:-------------------------------------------------------------------------------------|:------------|
| PSDNET-1503 | Gestisci la proprietà Angolo per Impostazioni Riempimento Modello                      |   Funzionalità   |
| PSDNET-1719 | Supporto della scala verticale e orizzontale per TextLayer                           |     Funzionalità     |
| PSDNET-1783 | [Formato AI] Implementare il rendering corretto dello sfondo nel Formato AI basato su PDF |     Funzionalità     |
| PSDNET-1611 | Modificare il meccanismo Distorsione in deformazione                                   |     Miglioramento     |
| PSDNET-1802 | Velocizza la deformazione                                                               |     Miglioramento     |
| PSDNET-995  | Eccezione "Caricamento immagine non riuscito" all'apertura del documento               |     Bug     |
| PSDNET-1491 | Risolvere il salvataggio dei file psd con modello di tratto                           |     Bug     |
| PSDNET-1642 | Lo stile del testo è scorretto in un oggetto intelligente quando si utilizza ReplaceContents |     Bug     |
| PSDNET-1884 | [Formato AI] Risolvere il rendering Cubic Bezier nel file AI                          |     Bug     |

## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **API rimosse:**
- Nessuna

## **Esempi d'uso:**

**PSDNET-1503. Gestisci la proprietà Angolo per Impostazioni Riempimento Modello**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(cartellaBase, "PatternFillLayerWide_0.psd");
string fileOutput = Path.Combine(cartellaOutput, "PatternFillLayerWide_0_output.psd");

using (PsdImage immagine = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer livelloRiempimento = (FillLayer)immagine.Layers[1];
    PatternFillSettings impostazioniRiempimento = (PatternFillSettings)livelloRiempimento.FillSettings;
    impostazioniRiempimento.Angle = 70;
    livelloRiempimento.Update();
    immagine.Save(fileOutput, new PsdOptions());
}

using (PsdImage immagine = (PsdImage)Image.Load(fileOutput, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer livelloRiempimento = (FillLayer)immagine.Layers[1];
    PatternFillSettings impostazioniRiempimento = (PatternFillSettings)livelloRiempimento.FillSettings;

    Assert.AreEqual(70, impostazioniRiempimento.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Supporto della scala verticale e orizzontale per TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(cartellaBase, "1719_src.psd");
string output = Path.Combine(cartellaOutput, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**(continua...)**
