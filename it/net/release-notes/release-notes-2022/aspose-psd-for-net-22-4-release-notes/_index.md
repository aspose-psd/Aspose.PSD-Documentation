---
title: Note sulla versione di Aspose.PSD per .NET 22.4
type: docs
weight: 90
url: /it/net/aspose-psd-per-net-22-4-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-261|Rendering dell'Effetto di Strato Glow Esterno|Funzionalità|
|PSDNET-1123|Aggiunta del supporto della Licenza Sha256|Miglioramento|
|PSDNET-1107|Il posizionamento del testo su più righe non corrisponde al risultato in Photoshop|Errore|
|PSDNET-1113|Problema con il caricamento del file PSD sul parsing dei dati delle risorse testuali|Errore|
|PSDNET-1129|Posizione incorretta del modello personalizzato dopo il salvataggio come PSD|Errore|


## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Sinistra
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Destra
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Centro
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AggiungiOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.ColoreDiRiempimento
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.ModoDiMiscelazione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.ÈVisibile
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Opacità
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensità
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.AntialiasingAttivo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Dispersone
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Dimensione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Rumore
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.SfumaturaSoft
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intervallo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Sbalzo


# **API Rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-261. Rendering dell'Effetto di Strato Glow Esterno**
{{< highlight csharp >}}
string src = "GreenLayer.psd";
string output = "output261.png";

using (var image = (PsdImage)Image.Load(src))
{
    OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
    effect.Range = 10;
    effect.Spread = 10;
    ((IColorFillSettings)effect.FillColor).Color = Color.Red;
    effect.Opacity = 128;
    effect.BlendMode = BlendMode.Normal;

    image.Save(output, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1107. Il posizionamento del testo su più righe non corrisponde al risultato in Photoshop**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Linea di testo1\rLinea di testo2\rLinea di testo3", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Sinistra;
   portions[1].Paragraph.Justification = JustificationMode.Destra;
   portions[2].Paragraph.Justification = JustificationMode.Centro;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1113. Problema con il caricamento del file PSD sul parsing dei dati delle risorse testuali**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // Caricato con successo.
}
{{< /highlight >}}


**PSDNET-1129. Posizione incorretta del modello personalizzato dopo il salvataggio come PSD**

{{< highlight csharp >}}
string sourceFile = "input_1129.psd";
string outputPsd = "out_psdnet1129.psd";
string outputPng = "out_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
