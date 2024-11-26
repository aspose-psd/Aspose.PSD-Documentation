---
title: Notatki wydania Aspose.PSD dla .NET 22.5
type: docs
weight: 80
url: /pl/net/aspose-psd-dla-net-22-5-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-952|Dodaj właściwość EffectType do interfejsu ILayerEffect|Funkcja|
|PSDNET-1146|Refaktoryzacja klasy ChannelData|Ulepszenie|
|PSDNET-657|Ustawienie właściwości opacity działa dla DropShadowEffect|Błąd|
|PSDNET-825|Niepoprawne rysowanie warstwy korekty przez warstwę transparentną w określonym przypadku|Błąd|
|PSDNET-1168|Ulepsz metodę Colorize. Kolorowanie szarości + ustaw poprawny kolor przy nasyceniu nie wynoszącym 100|Błąd|
|Artykuł|[Jak uruchomić Aspose.PSD w Dockerze](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Dokumentacja|


## **Zmiany w interfejsie publicznym**
# **Dodane interfejsy:**
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


# **Usunięte interfejsy:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Przykłady użycia:**

**PSDNET-657. Ustawienie właściwości opacity działa dla DropShadowEffect**

{{< highlight csharp >}}
string plikWejsciowy = "input.psd";
string obrazWyjsciowy20 = "outputImage20.png";
string obrazWyjsciowy200 = "outputImage200.png";

using (PsdImage obrazPsd = (PsdImage)Image.Load(plikWejsciowy, new LoadOptions()))
{
    Layer warstwaPracy = obrazPsd.Layers[1];

    DropShadowEffect efektDropShadow = warstwaPracy.BlendingOptions.AddDropShadow();
    efektDropShadow.Distance = 0;
    efektDropShadow.Size = 8;

    // Przykład z Opacity = 20
    efektDropShadow.Opacity = 20;
    obrazPsd.Save(obrazWyjsciowy20, new PngOptions());

    // Przykład z Opacity = 200
    efektDropShadow.Opacity = 200;
    obrazPsd.Save(obrazWyjsciowy200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Niepoprawne rysowanie warstwy korekty przez warstwę transparentną w określonym przypadku**

{{< highlight csharp >}}
string plikWejsciowy = "input_825.psd";
string obrazWyjsciowyPng = "out_psdnet825.png";

using (var obrazPsd = (PsdImage)Image.Load(plikWejsciowy))
{
    foreach (var element in obrazPsd.Layers)
    {
        element.IsVisible = false;
    }
    var warstwa = obrazPsd.Layers[3];
    obrazPsd.Layers[1].IsVisible = true;
    obrazPsd.Layers[3].IsVisible = true;
    obrazPsd.Layers[4].IsVisible = true;
    obrazPsd.Layers[7].IsVisible = true;

    var szerokosc = warstwa.Width;
    var wysokosc = warstwa.Height;
    var graniceWarstwy = new Rectangle(warstwa.Left, warstwa.Top, szerokosc, wysokosc);
    var granice = new Rectangle(0, 0, szerokosc, wysokosc);
    var obraz = new PsdImage(granice.Width, granice.Height);

    obraz.SaveArgb32Pixels(granice, obrazPsd.LoadArgb32Pixels(graniceWarstwy));

    obraz.Save(obrazWyjsciowyPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. Dodaj właściwość EffectType do interfejsu ILayerEffect**

{{< highlight csharp >}}
string plikWejsciowy = "input.psd";
string obrazBez = "outputWithout.png";
string obrazZ = "outputWith.png";

using (PsdImage obrazPsd = (PsdImage)Image.Load(plikWejsciowy, new LoadOptions()))
{
    obrazPsd.Save(obrazBez, new PngOptions());

    Layer warstwaPracy = obrazPsd.Layers[1];

    DropShadowEffect efektDropShadow = warstwaPracy.BlendingOptions.AddDropShadow();
    efektDropShadow.Distance = 0;
    efektDropShadow.Size = 8;
    efektDropShadow.Opacity = 20;

    foreach (ILayerEffect iEfekt in warstwaPracy.BlendingOptions.Effects)
    {
        if (iEfekt.EffectType == LayerEffectsTypes.DropShadow)
        {
            // złapane
            obrazPsd.Save(obrazZ, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Ulepsz metodę Colorize. Kolorowanie szarości + ustaw poprawny kolor przy nasyceniu nie wynoszącym 100**

{{< highlight csharp >}}
string plikŹródłowy = "Colorize.psd";            
string outputProsty = "output_simple.png";
string outputKolorize = "output_colorize.png";

using (var obrazPsd = (PsdImage)Image.Load(plikŹródłowy))
{
    // Obraz bez właściwości Colorize
    obrazPsd.Save(outputProsty, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Ustaw właściwość Colorize
    foreach (Layer warstwa in obrazPsd.Layers)
    {
        if (warstwa is HueSaturationLayer)
        {
            HueSaturationLayer warstwaOdcieniowania = (HueSaturationLayer)warstwa;
            warstwaOdcieniowania.Colorize = true;
            break;
        }
    }
    
    // Obraz z właściwością Colorize
    obrazPsd.Save(outputKolorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
