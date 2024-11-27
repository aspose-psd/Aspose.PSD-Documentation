---
title: Aspose.PSD pro .NET 22.5 - Poznámky k vydání
type: docs
weight: 80
url: /cs/net/aspose-psd-pro-net-22-5-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-952|Přidat vlastnost EffectType k rozhraní ILayerEffect|Funkce|
|PSDNET-1146|Refaktoring třídy ChannelData|Vylepšení|
|PSDNET-657|Oprava vlastnosti průhlednosti pro DropShadowEffect|Chyba|
|PSDNET-825|Nesprávný výkres vrstvy úpravy skrz průhlednou vrstvu v konkrétním případě|Chyba|
|PSDNET-1168|Vylepšení metody Colorize. Barevné zabarvení šedé + nastavení správné barvy, pokud sytost není 100|Chyba|
|Článek|[Jak spustit Aspose.PSD v Dockeru](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Dokumentace|


## **Změny v verejné API**
# **Přidaná rozhraní:**
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


# **Odstraněná rozhraní:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Příklady použití**

**PSDNET-657. Oprava vlastnosti průhlednosti pro DropShadowEffect**

{{< highlight csharp >}}
string vstupniSoubor = "vstup.psd";
string vystupniObrazek20 = "vystupniObrazek20.png";
string vystupniObrazek200 = "vystupniObrazek200.png";

using (PsdImage obrazPsd = (PsdImage)Image.Load(vstupniSoubor, new LoadOptions()))
{
    Layer praceVrstva = obrazPsd.Layers[1];

    DropShadowEffect dropShadowEffect = praceVrstva.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;

    // Příklad s průhledností = 20
    dropShadowEffect.Opacity = 20;
    obrazPsd.Save(vystupniObrazek20, new PngOptions());

    // Příklad s průhledností = 200
    dropShadowEffect.Opacity = 200;
    obrazPsd.Save(vystupniObrazek200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Nesprávný výkres vrstvy úpravy skrz průhlednou vrstvu v konkrétním případě**

{{< highlight csharp >}}
string zdrojovySoubor = "vstup_825.psd";
string vystupniPng = "vystup_psdnet825.png";

using (var obrazPsd = (PsdImage)Image.Load(zdrojovySoubor))
{
    foreach (var prvek in obrazPsd.Layers)
    {
        prvek.IsVisible = false;
    }
    var vrstva = obrazPsd.Layers[3];
    obrazPsd.Layers[1].IsVisible = true;
    obrazPsd.Layers[3].IsVisible = true;
    obrazPsd.Layers[4].IsVisible = true;
    obrazPsd.Layers[7].IsVisible = true;

    var sirka = vrstva.Width;
    var vyska = vrstva.Height;
    var hraniceVrstvy = new Rectangle(vrstva.Left, vrstva.Top, sirka, vyska);
    var hranice = new Rectangle(0, 0, sirka, vyska);
    var obraz = new PsdImage(hranice.Width, hranice.Height);

    obraz.SaveArgb32Pixels(hranice, obrazPsd.LoadArgb32Pixels(hraniceVrstvy));

    obraz.Save(vystupniPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. Přidat vlastnost EffectType k rozhraní ILayerEffect**

{{< highlight csharp >}}
string vstupniSoubor = "vstup.psd";
string vystupBez = "vystupBez.png";
string vystupS = "vystupS.png";

using (PsdImage obrazPsd = (PsdImage)Image.Load(vstupniSoubor, new LoadOptions()))
{
    obrazPsd.Save(vystupBez, new PngOptions());

    Layer praceVrstva = obrazPsd.Layers[1];

    DropShadowEffect dropShadowEffect = praceVrstva.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;
    dropShadowEffect.Opacity = 20;

    foreach (ILayerEffect iEffect in praceVrstva.BlendingOptions.Effects)
    {
        if (iEffect.EffectType == LayerEffectsTypes.DropShadow)
        {
            // zachyceno
            obrazPsd.Save(vystupS, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Vylepšit metodu Colorize. Barevné zabarvení šedé + nastavit správnou barvu, když sytost není 100**

{{< highlight csharp >}}
string srcSoubor = "Colorize.psd";            
string vystupJednoduche = "vystup_jednoduche.png";
string vystupColorize = "vystup_colorize.png";

using (var obrazPsd = (PsdImage)Image.Load(srcSoubor))
{
    // Obrázek bez vlastnosti Colorize
    obrazPsd.Save(vystupJednoduche, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Nastavit vlastnost Colorize
    foreach (Layer vrstva in obrazPsd.Layers)
    {
        if (vrstva is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)vrstva;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // Obrázek s vlastností Colorize
    obrazPsd.Save(vystupColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
