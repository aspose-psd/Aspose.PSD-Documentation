---
title: Aspose.PSD pro .NET 23.4 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/aspose-psd-pro-net-23-4-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání[Aspose.PSD pro .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1409|Navrhnout třídu RawColor pro veřejné rozhraní k použití v API PSD namísto zastaralé struktury Color|Vylepšení|
|PSDNET-1332|Integrovat vrstvu nastavení mapy přechodů gradientu z probation do hlavního kódu Aspose.PSD|Funkce|
|PSDNET-1448|Úprava textu pomocí částí Textu neukládá správný výsledek|Chyba|
|PSDNET-1449|Začátek a konec stylů nebo odstavců se objevuje na nesprávném místě při úpravě vrstvy textu pomocí ITextPortion|Chyba|
|PSDNET-1509|Formátování se posune při úpravě v photoshopu|Chyba|


## **Změny ve veřejném rozhraní API**
# **Přidané metody:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor


# **Odebrané metody:**
- Žádné


## **Příklady použití:**

**PSDNET-1332. Integrovat vrstvu nastavení mapy přechodů gradientu z probation do hlavního kódu Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // check current values
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);


    grdmResource.Reverse = true;
    // Red color for second gradient color point
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // check changed values
    AssertAreEqual(true, grdmResource.Reverse);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[3].Value);
}
...

{{< /highlight >}}


**PSDNET-1409. Navrhnout třídu RawColor pro veřejné rozhraní API k použití v API PSD místo zastaralé struktury Color**

{{< highlight csharp >}}
/* kód nebyl změněn */
...

{{< /highlight >}}


**PSDNET-1448. Úprava textu pomocí částí Textu neukládá správný výsledek**

{{< highlight csharp >}}
/* kód nebyl změněn */
...

{{< /highlight >}}


**PSDNET-1449. Začátek a konec stylů nebo odstavců se objevuje na nesprávném místě při úpravě vrstvy textu pomocí ITextPortion**

{{< highlight csharp >}}
/* kód nebyl změněn */
...

{{< /highlight >}}


**PSDNET-1509. Formát se posune při úpravě v photoshopu**

{{< highlight csharp >}}
/* kód nebyl změněn */
...

{{< /highlight >}}