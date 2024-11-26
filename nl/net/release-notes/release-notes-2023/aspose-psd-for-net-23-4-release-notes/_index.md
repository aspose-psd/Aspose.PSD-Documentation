---
title: Aspose.PSD voor .NET 23.4 - Uitgavenotities
type: docs
weight: 90
url: /nl/net/aspose-psd-voor-net-23-4-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat de uitgavenotities voor [Aspose.PSD voor .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-1409|Ontwerp RawColor-klasse voor de openbare API om deze te gebruiken in de PSD API in plaats van de verouderde Color-structuur|Verbetering|
|PSDNET-1332|Integreer de Aanpassingslaag van de Gradiëntenkaart van Probation naar de hoofd Aspose.PSD-code|Functie|
|PSDNET-1448|Bewerken van tekst met Text Portions slaat het juiste resultaat niet op|Fout|
|PSDNET-1449|Het begin en einde van de stijlen of alinea's verschijnen op de verkeerde plaats bij het bewerken van de Tekstlaag door ITextPortion|Fout|
|PSDNET-1509|Opmaak verplaatst tijdens bewerken in Photoshop|Fout|


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersie
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorModus
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.StelPsdVersieIn(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent.ToegestaneVolledigeNamen
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent.BitsDiepte
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent.Waarde
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent.Naam
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent.Beschrijving
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent.VolledigeNaam
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.KleurComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Onderdelen
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.KrijgKleurModusNaam
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.KrijgBitsDiepte
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.KrijgAlsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.StelAlsIntIn(Systeem.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.KrijgAlsLang
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.StelAlsLangIn(Systeem.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDatumFormaat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.KleurModus
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Omkeren
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Stof
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientNaam
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UitbreidingTeller
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolatie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientModus
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndGetalZaad
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ToonTransparantie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GebruikVectorKleur
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Ruwheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.KleurModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.KleurPunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparantiePunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimaleKleur
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximaleKleur


# **Verwijderde API's:**
- Geen


## **Gebruikvoorbeelden:**

**PSDNET-1332. Integreer de Aanpassingslaag van de Gradiëntenkaart van Probation naar de hoofd Aspose.PSD-code**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // controleer huidige waarden
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);


    grdmResource.Reverse = true;
    // Rode kleur voor tweede gradiëntkleurpunt
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // controleer gewijzigde waarden
    AssertAreEqual(true, grdmResource.Reverse);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[3].Value);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1409. Ontwerp RawColor-klasse voor de openbare API om deze te gebruiken in de PSD API in plaats van de verouderde Color-structuur**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objecten zijn niet gelijk.");
    }
}

var color = new RawColor(PixelDataFormat.Rgba32Bpp);
var oldColor = Color.FromArgb(5, 1, 2, 3);

var argbValue = oldColor.ToArgb();
color.SetAsInt(argbValue);

AssertAreEqual("ARGB", color.GetColorModeName());
AssertAreEqual(32, color.GetBitDepth());
AssertAreEqual("A Alpha", color.Components[0].FullName);
AssertAreEqual(5, (int)color.Components[0].Value);
AssertAreEqual("R Rood", color.Components[1].FullName);
AssertAreEqual(1, (int)color.Components[1].Value);
AssertAreEqual("G Groen", color.Components[2].FullName);
AssertAreEqual(2, (int)color.Components[2].Value);
AssertAreEqual("B Blauw", color.Components[3].FullName);
AssertAreEqual(3, (int)color.Components[3].Value);

AssertAreEqual(argbValue, color.GetAsInt());
{{< /highlight >}}

**PSDNET-1448. Bewerken van tekst met Text Portions slaat het juiste resultaat niet op**

{{< highlight csharp >}}
string sourceFile = "originalv5.psd";
string psdExportPath = "export.psd";

using (var imageTestEmail = (PsdImage)Image.Load(sourceFile))
{
    var layers = imageTestEmail.Layers;
    foreach (var layerItem in layers)
    {
        var isTextLayer = layerItem.GetType() == typeof(TextLayer) ? true : false;
        if (isTextLayer)
        {
            var layerTLToUpdateText = (TextLayer)layerItem;

            // Zoek lsak-tekst
            if (layerTLToUpdateText.Text.Contains("lsak"))
            {
                var textDataTL = layerTLToUpdateText.TextData;

                if (textDataTL.Text.Contains(...
{{< /highlight >}}