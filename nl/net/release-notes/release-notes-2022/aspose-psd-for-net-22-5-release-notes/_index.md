---
title: Aspose.PSD voor .NET 22.5 - Release-opmerkingen
type: docs
weight: 80
url: /nl/net/aspose-psd-voor-net-22-5-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-952|EffectType-eigenschap toevoegen aan ILayerEffect-interface|Functie|
|PSDNET-1146|Refactoring van ChannelData Class|Verbetering|
|PSDNET-657|Laat de eigenschap opaciteit werken voor DropShadowEffect|Fout|
|PSDNET-825|Onjuiste tekening van aanpassingslaag via de transparante laag in een specifiek geval|Fout|
|PSDNET-1168|Verbeteren van de Colorize-methode. Colorize grijs + juiste kleur instellen wanneer saturatie niet 100 is|Fout|
|Artikel|[Aspose.PSD uitvoeren in Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Documentatie|


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
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

# **Verwijderde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Gebruik voorbeelden:**

**PSDNET-657. Laat de eigenschap opaciteit werken voor DropShadowEffect**

{{< highlight csharp >}}
string invoerBestand = "invoer.psd";
string uitvoerAfbeelding20 = "uitvoerAfbeelding20.png";
string uitvoerAfbeelding200 = "uitvoerAfbeelding200.png";

using (PsdImage psdAfbeelding = (PsdImage)Image.Load(invoerBestand, new LoadOptions()))
{
    Laag werkLaag = psdAfbeelding.Lagen[1];

    DropShadowEffect dropShadowEffect = werkLaag.BlendingOptions.AddDropShadow();
    dropShadowEffect.Afstand = 0;
    dropShadowEffect.Grootte = 8;

    // Voorbeeld met Opaciteit = 20
    dropShadowEffect.Opaciteit = 20;
    psdAfbeelding.Save(uitvoerAfbeelding20, new PngOptions());

    // Voorbeeld met Opaciteit = 200
    dropShadowEffect.Opaciteit = 200;
    psdAfbeelding.Save(uitvoerAfbeelding200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Onjuiste tekening van aanpassingslaag via de transparante laag in een specifiek geval**

{{< highlight csharp >}}
string bronBestand = "invoer_825.psd";
string uitvoerPng = "uit_psdnet825.png";

using (var psdAfbeelding = (PsdImage)Image.Load(bronBestand))
{
    foreach (var item in psdAfbeelding.Lagen)
    {
        item.IsZichtbaar = false;
    }
    var laag = psdAfbeelding.Lagen[3];
    psdAfbeelding.Lagen[1].IsZichtbaar = true;
    psdAfbeelding.Lagen[3].IsZichtbaar = true;
    psdAfbeelding.Lagen[4].IsZichtbaar = true;
    psdAfbeelding.Lagen[7].IsZichtbaar = true;

    var breedte = laag.Breedte;
    var hoogte = laag.Hoogte;
    var laagGebied = new Rechthoek(laag.Links, laag.Boven, breedte, hoogte);
    var gebieden = new Rechthoek(0, 0, breedte, hoogte);
    var afbeelding = new PsdImage(gebieden.Breedte, gebieden.Hoogte);

    afbeelding.SaveArgb32Pixels(gebieden, psdAfbeelding.LoadArgb32Pixels(laagGebied));

    afbeelding.Save(uitvoerPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. EffectType-eigenschap toevoegen aan ILayerEffect-interface**

{{< highlight csharp >}}
string invoerBestand = "invoer.psd";
string uitvoerZonder = "uitvoerZonder.png";
string uitvoerMet = "uitvoerMet.png";

using (PsdImage psdAfbeelding = (PsdImage)Image.Load(invoerBestand, new LoadOptions()))
{
    psdAfbeelding.Save(uitvoerZonder, new PngOptions());

    Laag werkLaag = psdAfbeelding.Lagen[1];

    DropShadowEffect dropShadowEffect = werkLaag.BlendingOptions.AddDropShadow();
    dropShadowEffect.Afstand = 0;
    dropShadowEffect.Grootte = 8;
    dropShadowEffect.Opaciteit = 20;

    foreach (ILayerEffect iEffect in werkLaag.BlendingOptions.Effects)
    {
        if (iEffect.EffectType == LayerEffectsTypes.DropShadow)
        {
            // het heeft gevonden
            psdAfbeelding.Save(uitvoerMet, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Verbeter de Colorize-methode. Colorize grijs + juiste kleur instellen wanneer saturatie niet 100 is**

{{< highlight csharp >}}
string srcBestand = "Kleuren.psd";            
string uitvoerEenvoudig = "uitvoer_eenvoudig.png";
string uitvoerColorize = "uitvoer_colorize.png";

using (var psdAfbeelding = (PsdImage)Image.Load(srcBestand))
{
    // Afbeelding zonder Colorize-eigenschap
    psdAfbeelding.Save(uitvoerEenvoudig, new PngOptions() { KleurType = PngKleurType.TruecolorWithAlpha });
    
    // Zet Colorize-eigenschap
    foreach (Laag laag in psdAfbeelding.Lagen)
    {
        if (laag is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)laag;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // Afbeelding met Colorize-eigenschap
    psdAfbeelding.Save(uitvoerColorize, new PngOptions() { KleurType = PngKleurType.TruecolorWithAlpha });
}
{{< /highlight >}}
