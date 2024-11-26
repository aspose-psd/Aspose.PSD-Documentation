---
title: Aspose.PSD voor .NET 18.12 - Release-opmerkingen
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-net-18-12-release-opmerkingen/
---

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-76|Ondersteuning van de Slaglaag|Functie|
|PSDNET-83|Ondersteuning van het Gradiënt Effect|Functie|
|PSDNET-84|Ondersteuning van het Patroon Effect|Functie|
|PSDNET-89|Mogelijkheid om de nieuw gegenereerde normale laag toe te voegen aan PsdImage|Functie|
|PSDNET-93|Na update van de inhoud van een tekstlaag met het \ (backslash) karakter, kan het resulterende bestand niet worden geopend in Photoshop|Fout|
|PSDNET-39|Gebroken afbeeldingen na export met te grote afbeeldingsgegevens in CMYK-kleurmodus|Fout|
|PSDNET-52|Mogelijkheid: Rotatie in PSD werkt niet|Fout|
|PSDNET-88|Mogelijkheid: Crop-methoden werken niet in Aspose.Psd|Fout|
|PSDNET-91|Veranderingen van Aspose.Imaging toepassen op Aspose.PSD|Verbetering|

## **Wijzigingen in de openbare API**
Methode    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Klasse    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Methode    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Methode    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Locatie

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocatie

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Hoek

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontaleOffset

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticaleOffset

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Kleurpunten

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Transparantiepunten

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerwijderTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerwijderKleurpunt(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Dekking

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Locatie

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocatie

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Gelinkt

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Schaal

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PuntenType

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Patroonnaam

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatroonId

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontaleOffset

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticaleOffset

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overvloeiwijze

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsZichtbaar

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Vullingsinstellingen

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Dekking

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Hoek

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Gereflecteerd

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamant

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Patroongegevens

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatroonId

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Naam

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Hoogte

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Breedte

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Afbeeldingsmodus

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Versie

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Patroonlengte

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Handtekening

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Sleutel

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Lengte

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersie

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPatroon(Stelsel.Int32[],Aspose.PSD.Rechthoek)

Methode```

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Opslaan(Aspose.PSD.StreamContainer,Stelsel.Int32)

Veld/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenererenLfx2ResourceNodes

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Instellingen

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Overvloeiwijze

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsZichtbaar

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Dekking

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Kleur

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BijvoegenGradiëntOverlay

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BijvoegenPatroonOverlay

Methode    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenererenLfx2ResourceNodes(Stelsel.String,Aspose.PSD.Kleur,Stelsel.String,Stelsel.String,Stelsel.Double,Stelsel.Boolean,Aspose.PSD.PointF)

Klasse    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatroonOverlayEffect

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatroonOverlayEffect.Instellingen

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatroonOverlayEffect.Overvloeiwijze

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatroonOverlayEffect.IsZichtbaar

Eigenschap    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatroonOverlayEffect.Dekking

## **Gebruik voorbeelden:**
**PSDNET-76. Ondersteuning van de Slaglaag**

**1) Vul type - Patroon**

{{< highlight nl >}}

	// Slageffect. FillType - Patroon. Voorbeeld

	…

{{< /highlight >}}

**Vul type - Gradiënt**

{{< highlight nl >}}

  // Slageffect. FillType - Gradiënt. Voorbeeld

    ...

{{< /highlight >}}

**Vul type - Kleur**

{{< highlight nl >}}

  // Slageffect. FillType - Kleur. Voorbeeld

    …

{{< /highlight >}}

**PSDNET-83. Ondersteuning van het Gradiënt Effect**

{{< highlight nl >}}

  // Gradiënt overlay effect. Voorbeeld

    ...

{{< /highlight >}}

**PSDNET-84. Ondersteuning van het Patroon Effect**

{{< highlight nl >}}

    // Patroon overlay effect. Voorbeeld

    ...

{{< /highlight >}}

**PSDNET-89. Mogelijkheid om de nieuw gegenereerde normale laag toe te voegen aan PsdImage.**

{{< highlight nl >}}

  // Mogelijkheid om de nieuw gegenereerde normale laag toe te voegen aan PsdImage

    ...

{{< /highlight >}}

**PSDNET-93. Na update van de inhoud van een tekstlaag met het \ (backslash) karakter, kan het resulterende bestand niet worden geopend in Photoshop.**

{{< highlight nl >}}

    ...

{{< /highlight >}}
```