---
title: Aspose.PSD für .NET 22.5 - Versionshinweise
type: docs
weight: 80
url: /de/net/aspose-psd-fur-net-22-5-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-952|Fügt die Eigenschaft EffectType zur ILayerEffect-Schnittstelle hinzu|Funktion|
|PSDNET-1146|Refaktorisierung der ChannelData-Klasse|Verbesserung|
|PSDNET-657|Bereitstellung des Opacity-Eigenschaft für DropShadowEffect|Fehler|
|PSDNET-825|Inkorrektes Zeichnen der Anpassungsebene durch die transparente Ebene in einem speziellen Fall|Fehler|
|PSDNET-1168|Verbesserung der Colorize-Methode: Colorize gray + korrekte Farbe festlegen, wenn die Sättigung nicht 100 ist|Fehler|
|Artikel|[Aspose.PSD in Docker ausführen](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Dokumentation|


## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
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


# **Entfernte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Beispiele für die Verwendung:**

**PSDNET-657. Bereitstellung des Opacity-Eigenschaft für DropShadowEffect**

{{< highlight csharp >}}
string Eingabedatei = "input.psd";
string AusgabeBild20 = "outputImage20.png";
string AusgabeBild200 = "outputImage200.png";

using (PsdImage psdImage = (PsdImage)Image.Load(Eingabedatei, new LoadOptions()))
{
    Layer ArbeitsSchicht = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = ArbeitsSchicht.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;

    // Beispiel mit Opacity = 20
    dropShadowEffect.Opacity = 20;
    psdImage.Save(AusgabeBild20, new PngOptions());

    // Beispiel mit Opacity = 200
    dropShadowEffect.Opacity = 200;
    psdImage.Save(AusgabeBild200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Inkorrektes Zeichnen der Anpassungsebene durch die transparente Ebene in einem speziellen Fall**

{{< highlight csharp >}}
string Quelldatei = "input_825.psd";
string AusgabePng = "out_psdnet825.png";

using (var psdImage = (PsdImage)Image.Load(Quelldatei))
{
    foreach (var Element in psdImage.Layers)
    {
        Element.IsVisible = false;
    }
    var Ebene = psdImage.Layers[3];
    psdImage.Layers[1].IsVisible = true;
    psdImage.Layers[3].IsVisible = true;
    psdImage.Layers[4].IsVisible = true;
    psdImage.Layers[7].IsVisible = true;

    var Breite = Ebene.Width;
    var Höhe = Ebene.Height;
    var EbeneGrenzen = new Rectangle(Ebene.Left, Ebene.Top, Breite, Höhe);
    var Grenzen = new Rectangle(0, 0, Breite, Höhe);
    var Bild = new PsdImage(Grenzen.Width, Grenzen.Height);

    Bild.SaveArgb32Pixels(Grenzen, psdImage.LoadArgb32Pixels(EbeneGrenzen));

    Bild.Save(AusgabePng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. Fügt die Eigenschaft EffectType zur ILayerEffect-Schnittstelle hinzu**

{{< highlight csharp >}}
string Eingabedatei = "input.psd";
string AusgabeOhne = "outputWithout.png";
string AusgabeMit = "outputWith.png";

using (PsdImage psdImage = (PsdImage)Image.Load(Eingabedatei, new LoadOptions()))
{
    psdImage.Save(AusgabeOhne, new PngOptions());

    Layer ArbeitsSchicht = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = ArbeitsSchicht.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;
    dropShadowEffect.Opacity = 20;

    foreach (ILayerEffect iEffect in ArbeitsSchicht.BlendingOptions.Effects)
    {
        if (iEffect.EffectType == LayerEffectsTypes.DropShadow)
        {
            // es wurde erfasst
            psdImage.Save(AusgabeMit, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Verbesserung der Colorize-Methode: Colorize gray + korrekte Farbe festlegen, wenn die Sättigung nicht 100 ist**

{{< highlight csharp >}}
string QuellDatei = "Colorize.psd";            
string AusgabeEinfach = "output_simple.png";
string AusgabeColorize = "output_colorize.png";

using (var psdImage = (PsdImage)Image.Load(QuellDatei))
{
    // Bild ohne Colorize-Eigenschaft
    psdImage.Save(AusgabeEinfach, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Colorize-Eigenschaft festlegen
    foreach (Layer ebene in psdImage.Layers)
    {
        if (ebene is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)ebene;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // Bild mit Colorize-Eigenschaft
    psdImage.Save(AusgabeColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
