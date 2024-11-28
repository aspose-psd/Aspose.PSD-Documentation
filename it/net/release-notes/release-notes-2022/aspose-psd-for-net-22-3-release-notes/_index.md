---
title: Note sulla release di Aspose.PSD per .NET 22.3
type: docs
weight: 100
url: /it/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla release di [Aspose.PSD per .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-210|Aggiunta della proprietà IsOpen per Layer Group|Caratteristica|
|PSDNET-643|L'immagine PSD con maschere di livello raster scarta le maschere nel salvataggio in immagine PSD a 16 bit|Bug|
|PSDNET-899|La modalità di fusione Dissolvenza non si applica alla cartella con maschera|Bug|
|PSDNET-1047|Specifico file non può essere aperto da Photoshop dopo il salvataggio in Aspose.PSD 21.11|Bug|
|PSDNET-1068|Rendere scorretto il livello con la modalità di fusione sovrapposizione lineare (Aggiungi)|Bug|
|PSDNET-1069|Il livello di riempimento modello genera un'eccezione durante l'aggiornamento dopo il caricamento|Bug|


## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **API rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-210. Aggiunta della proprietà IsOpen per Layer Group**

{{< highlight csharp >}}
// Esempio di lettura e scrittura della proprietà IsOpen durante l'esecuzione.
string nomeFileSorgente = "LayerGroupOpenClose.psd";
string nomeFileOutput = "Output" + nomeFileSorgente;

using (var immagine = (PsdImage)Image.Load(nomeFileSorgente))
{
    foreach (var livello in immagine.Layers)
    {
        if (livello is LayerGroup && livello.Name == "Gruppo 1")
        {
            bool gruppo1Aperto = ((LayerGroup)livello).IsOpen;
            ((LayerGroup)livello).IsOpen = !gruppo1Aperto;
        }

        if (livello is LayerGroup && livello.Name == "Gruppo 2")
        {
            bool gruppo2Aperto = ((LayerGroup)livello).IsOpen;           
            ((LayerGroup)livello).IsOpen = !gruppo2Aperto;
        }
    }

    immagine.Save(nomeFileOutput);
}
{{< /highlight >}}

**PSDNET-643. L'immagine PSD con maschere di livello raster scarta le maschere nel salvataggio in immagine PSD a 16 bit**

{{< highlight csharp >}}
            string percorsoFileSorgente = "OneRegularAndOneRegularWithMask.psd";
            string percorsoFileOutput = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage immagine = (PsdImage)Image.Load(percorsoFileSorgente))
            {
                immagine.Save(percorsoFileOutput, new PsdOptions(immagine)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. La modalità di fusione Dissolvenza non si applica alla cartella con maschera**

{{< highlight csharp >}}
            string fileSorgente = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage immagine = (PsdImage) Image.Load(fileSorgente))
            {
                immagine.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Specifico file non può essere aperto da Photoshop dopo il salvataggio in Aspose.PSD 21.11**

{{< highlight csharp >}}
            string fileSorgente = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage immagine = (PsdImage) Image.Load(fileSorgente))
            {
                immagine.Save(outputPsd);
            }

            // Bisogna aprire manualmente l'output PSD da Photoshop.

            using (PsdImage immagine = (PsdImage) Image.Load(outputPsd))
            {
                // nessuna eccezione.
            }
{{< /highlight >}}

**PSDNET-1068. Rendere scorretto il livello con la modalità di fusione sovrapposizione lineare (Aggiungi)**

{{< highlight csharp >}}
            string fileSorgente = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var immaginePsd = (PsdImage) Image.Load(fileSorgente))
            {
                immaginePsd.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Il livello di riempimento modello genera un'eccezione durante l'aggiornamento dopo il caricamento**

{{< highlight csharp >}}
            string fileSorgente = "AllTypesLayerPsd.psd";

            using (var immagine = (PsdImage) Image.Load(fileSorgente))
            {
                var livelloRiempimento = (FillLayer)immagine.Layers[9];
                livelloRiempimento.Update();
            }
{{< /highlight >}}
