---
title: Aspose.PSD voor .NET 22.4 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/aspose-psd-voor-net-22-4-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-261|Weergave van Outer Glow Layer Effect|Functie|
|PSDNET-1123|Toevoegen van ondersteuning voor Sha256 Licentie|Verbetering|
|PSDNET-1107|Positionering van meerregelige tekst komt niet overeen met het resultaat in Photoshop|Fout|
|PSDNET-1113|Het probleem met het laden van PSD-bestand bij het parsen van tekstresourcegegevens|Fout|
|PSDNET-1129|Onjuiste positie van het aangepaste patroon na opslaan als PSD|Fout|


## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Left
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Right
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Center
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Noise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsSoftBlend
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Range
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Jitter


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-261. Weergave van Outer Glow Layer Effect**
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


**PSDNET-1107. Positionering van meerregelige tekst komt niet overeen met het resultaat in Photoshop**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Regel 1\rRegel 2\rRegel 3", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Left;
   portions[1].Paragraph.Justification = JustificationMode.Right;
   portions[2].Paragraph.Justification = JustificationMode.Center;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1113. Het probleem met het laden van PSD-bestand bij het parsen van tekstresourcegegevens**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // Succesvol geladen.
}
{{< /highlight >}}


**PSDNET-1129. Onjuiste positie van het aangepaste patroon na opslaan als PSD**

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
