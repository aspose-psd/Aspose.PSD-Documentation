---
title: Aspose.PSD pro .NET 20.7 - Poznámky k vydání
type: docs
weight: 60
url: /cs/net/aspose-psd-pro-net-20-7-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-673|Podpora zdroje LnkE|Funkce|
|PSDNET-392|Podpora zdroje britResource (Resource adjustování jasu/kontrastu)|Funkce|
|PSDNET-629|Změna zprávy o vyjímce při pokusu o otevření nepodporovaných formátů jako snímek|Vylepšení|
|PSDNET-594|Nepodařilo se uložit vrstvu masky|Chyba|
|PSDNET-597|Pokud uložíme soubor PSD po vytvoření nové skupiny vrstev, obdržíme upozornění Photoshopu při otevírání souboru|Chyba|
|PSDNET-618|Ořezová maska se nepoužívá na složce|Chyba|
|PSDNET-625|Nelze otevřít soubor s Aspose.PSD pro .NET|Chyba|
|PSDNET-650|Výjimka při ukládání obrázku při konverzi z PSD do PDF|Chyba|
|PSDNET-655|Operace rop způsobuje neplatnou ořezovou cestu v obrázku PSD|Chyba|
|PSDNET-662|Výjimka NullReference při pokusu o uložení konkrétního souboru PSD se stínovým efektem|Chyba|
|PSDNET-666|Aspose.PSD vrátí true na Image.CanLoad(pdfStream)|Chyba|
|PSDNET-676|Vrstvy se nepodařilo renderovat v generovaném PNG|Chyba|
|PSDNET-677|Výjimka při přístupu k TextData|Chyba|
|PSDNET-679|ImageSaveException při ukládání souboru PSD|Chyba|

## **Změny ve veřejném API**
# **Přidaná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **Odstraněné API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Příklady použití:**
**PSDNET-606. Podpora zdroje LnkE**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-201. Podpora pokroku konverzního dokumentu**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-386. Podpora zdroje britResource (Resource adjustování jasu/kontrastu)**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-596. Skupina vrstev s režimem mísení, který není PassThrough, se nederuje**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-610. Výjimka NullReference při pokusu o konverzi konkrétního souboru PSD na obrázek**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-636. Změna velikosti souborů PSD nefunguje správně, pokud je v ajustační vrstvě maska s prázdnými hranicemi**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-611. OverflowException při pokusu o otevření konkrétního souboru PSD**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-565. Obrázek PSD s režimem RGB 16 bitů/kanál aktualizuje vrstvy pouze v náhledu**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-652. Výjimka při načítání konkrétního souboru PSD s komplexním zdrojem LnkE a atributem adobeStockLicenseState**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDNET-638. Nesprávné pořadí vrstev po přidání skupiny vrstev do prázdné skupiny vrstev**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}

**PSDBET-219. Přesunutí nastavení DefaultReplacementFont do třídy ImageOptionsBase**

{{< highlight csharp >}}
// Kód příkladu
{{< /highlight >}}