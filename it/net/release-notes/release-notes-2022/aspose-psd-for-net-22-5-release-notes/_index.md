---
title: Note sulla versione di Aspose.PSD per .NET 22.5
type: docs
weight: 80
url: /it/net/aspose-psd-for-net-22-5-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-952|Aggiungere la proprietà EffectType all'interfaccia ILayerEffect|Funzionalità|
|PSDNET-1146|Rifattorizzazione della classe ChannelData |Miglioramento|
|PSDNET-657|Rendere funzionante la proprietà opacità per DropShadowEffect|Errore|
|PSDNET-825|Disegno non corretto del livello di regolazione attraverso il livello trasparente in un caso specifico|Errore|
|PSDNET-1168|Migliorare il metodo Colorize. Colorize grigio + impostare il colore corretto quando la saturazione non è al 100|Errore|
|Articolo|[Come Eseguire Aspose.PSD in Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Documentazione|


## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor(Aspose.PSD.FileFormats.Psd.CompressionMethod,System.Int32,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ILayerEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.DropShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EffectType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.DropShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.OuterGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.PatternOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.GradientOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.ColorOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Satin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Stroke
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.BevelEmboss


# **API Rimosse:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Esempi di utilizzo:**

**PSDNET-657. Rendere funzionante la proprietà opacità per DropShadowEffect**

{{< highlight csharp >}}
string fileInput = "input.psd";
string outputImmagine20 = "outputImmagine20.png";
string outputImmagine200 = "outputImmagine200.png";

using (PsdImage immaginePsd = (PsdImage)Image.Load(fileInput, new LoadOptions()))
{
    Layer livelloLavoro = immaginePsd.Layers[1];

    DropShadowEffect dropShadowEffect = livelloLavoro.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;

    // Esempio con Opacità = 20
    dropShadowEffect.Opacity = 20;
    immaginePsd.Save(outputImmagine20, new PngOptions());

    // Esempio con Opacità = 200
    dropShadowEffect.Opacity = 200;
    immaginePsd.Save(outputImmagine200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Disegno non corretto del livello di regolazione attraverso il livello trasparente in un caso specifico**

{{< highlight csharp >}}
string fileSorgente = "input_825.psd";
string outputPng = "out_psdnet825.png";

using (var immaginePsd = (PsdImage)Image.Load(fileSorgente))
{
    foreach (var elemento in immaginePsd.Layers)
    {
        elemento.IsVisible = false;
    }
    var livello = immaginePsd.Layers[3];
    immaginePsd.Layers[1].IsVisible = true;
    immaginePsd.Layers[3].IsVisible = true;
    immaginePsd.Layers[4].IsVisible = true;
    immaginePsd.Layers[7].IsVisible = true;

    var larghezza = livello.Width;
    var altezza = livello.Height;
    var limitiLivello = new Rectangle(livello.Left, livello.Top, larghezza, altezza);
    var limiti = new Rectangle(0, 0, larghezza, altezza);
    var immagine = new PsdImage(limiti.Width, limiti.Height);

    immagine.SaveArgb32Pixels(limiti, immaginePsd.LoadArgb32Pixels(limitiLivello));

    immagine.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. Aggiungere la proprietà EffectType all'interfaccia ILayerEffect**

{{< highlight csharp >}}
string fileInput = "input.psd";
string outputSenza = "outputSenza.png";
string outputCon = "outputCon.png";

using (PsdImage immaginePsd = (PsdImage)Image.Load(fileInput, new LoadOptions()))
{
    immaginePsd.Save(outputSenza, new PngOptions());

    Layer livelloLavoro = immaginePsd.Layers[1];

    DropShadowEffect dropShadowEffect = livelloLavoro.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;
    dropShadowEffect.Opacity = 20;

    foreach (ILayerEffect iEffetto in livelloLavoro.BlendingOptions.Effects)
    {
        if (iEffetto.EffectType == LayerEffectsTypes.DropShadow)
        {
            // è stato rilevato
            immaginePsd.Save(outputCon, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Migliorare il metodo Colorize. Colorize grigio + impostare il colore corretto quando la saturazione non è al 100**

{{< highlight csharp >}}
string fileSorgente = "Colorize.psd";            
string outputSemplice = "outputSemplice.png";
string outputColorize = "outputColorize.png";

using (var immaginePsd = (PsdImage)Image.Load(fileSorgente))
{
    // Immagine senza la proprietà Colorize
    immaginePsd.Save(outputSemplice, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Imposta la proprietà Colorize
    foreach (Layer livello in immaginePsd.Layers)
    {
        if (livello is HueSaturationLayer)
        {
            HueSaturationLayer livelloHueSaturation = (HueSaturationLayer)livello;
            livelloHueSaturation.Colorize = true;
            break;
        }
    }
    
    // Immagine con la proprietà Colorize
    immaginePsd.Save(outputColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
