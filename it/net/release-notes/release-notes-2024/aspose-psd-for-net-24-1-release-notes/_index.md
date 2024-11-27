---
title: Note sulla versione di Aspose.PSD per .NET 24.1
type: docs
weight: 120
url: /it/net/aspose-psd-per-net-24-1-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                      | **Categoria** |
|:-----------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [Formato AI] Aggiunta della gestione di base per immagini AI multipagina                            |   Funzionalità   |
| PSDNET-718  | L'effetto di testo Warp non viene applicato al testo                                               |     Errore     |
| PSDNET-1620 | Rendering non corretto della maschera nel file specifico                                          |     Errore     |
| PSDNET-1855 | NullReferenceException in Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor     |     Errore     |
| PSDNET-1883 | [Formato AI] Risoluzione dell'utilizzo della memoria in AiExporterUtils                            |     Errore     |



## **Modifiche all'API pubblica**
# **API aggiunte:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-718. L'effetto di testo Warp non viene applicato al testo**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(baseFolder, "text_warp.psd");
string fileOutput = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(fileSorgente, opt))
{
    img.Save(fileOutput, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Rendering non corretto della maschera nel file specifico**

{{< highlight csharp >}}
string fileSorgente1 = Path.Combine(baseFolder, "mask_problem.psd");
string fileSorgente2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string fileOutput1 = Path.Combine(outputFolder, "mask_export.png");
string fileOutput2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(fileSorgente1, opt))
{
    img.Save(fileOutput1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(fileSorgente2, opt))
{
    img.Save(fileOutput2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [Formato AI] Aggiunta della gestione di base per immagini AI multipagina**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(baseFolder, "threePages.ai");
string primoOutputPng = Path.Combine(outputFolder, "primoOutputPagina.png");
string secondoOutputPng = Path.Combine(outputFolder, "secondoOutputPagina.png");
string terzoOutputPng = Path.Combine(outputFolder, "terzoOutputPagina.png");

// Carica l'immagine AI.
using (AiImage image = (AiImage)Image.Load(fileSorgente))
{
    // Per impostazione predefinita, ActivePageIndex è 0.
    // Quindi, se si salva l'immagine AI senza modificare questa proprietà, verrà renderizzata e salvata la prima pagina.
    image.Save(primoOutputPng, new PngOptions());

    // Cambia l'indice della pagina attiva alla seconda pagina.
    image.ActivePageIndex = 1;

    // Salva la seconda pagina dell'immagine AI come un'immagine PNG.
    image.Save(secondoOutputPng, new PngOptions());

    // Cambia l'indice della pagina attiva alla terza pagina.
    image.ActivePageIndex = 2;

    // Salva la terza pagina dell'immagine AI come un'immagine PNG.
    image.Save(terzoOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException in Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string cartellaFonts = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { cartellaFonts }, true);

string fileInput = Path.Combine(baseFolder, "1.psd");
string fileOutput = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(fileInput))
{
    psdImage.Save(fileOutput, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [Formato AI] Risoluzione dell'utilizzo della memoria in AiExporterUtils**

{{< highlight csharp >}}
string fileSorgente = Path.Combine(baseFolder, "threePages.ai");
string primoOutputPng = Path.Combine(outputFolder, "primoOutputPagina.png");
string secondoOutputPng = Path.Combine(outputFolder, "secondoOutputPagina.png");
string terzoOutputPng = Path.Combine(outputFolder, "terzoOutputPagina.png");

const double LimiteMemoria = 220;
double memoriaUtilizzata = double.MaxValue;

// Carica l'immagine AI.
using (AiImage image = (AiImage)Image.Load(fileSorgente))
{
    // Salva la prima pagina dell'immagine AI come un'immagine PNG.
    image.Save(primoOutputPng, new PngOptions());

    // Cambia l'indice della pagina attiva alla seconda pagina.
    image.ActivePageIndex = 1;

    // Salva la seconda pagina dell'immagine AI come un'immagine PNG.
    image.Save(secondoOutputPng, new PngOptions());

    // Cambia l'indice della pagina attiva alla terza pagina.
    image.ActivePageIndex = 2;

    // Salva la terza pagina dell'immagine AI come un'immagine PNG.
    image.Save(terzoOutputPng, new PngOptions());
}

GC.Collect();

memoriaUtilizzata = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoriaUtilizzata > LimiteMemoria)
{
    throw new Exception("L'utilizzo della memoria è troppo elevato. " + memoriaUtilizzata + " anziché " + LimiteMemoria.ToString("F1"));
}
{{< /highlight >}}
