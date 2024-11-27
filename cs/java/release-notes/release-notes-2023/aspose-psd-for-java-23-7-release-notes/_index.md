---
title: Aspose.PSD pro Java 23.7 - Poznámky k vydání
type: docs
weight: 40
url: /cs/java/aspose-psd-pro-java-23-7-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Klíč**    | **Shrnutí**                                                                                                             | **Kategorie** |
|:------------|:------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-502 | Přidání možnosti exportovat každou vrstvu souboru PSD do animovaného souboru Gif                                    | Funkce        |
| PSDJAVA-503 | Přiřazení vlastnosti Náplň vrstvy tvaru z prostředků vscg                                                            | Funkce        |
| PSDJAVA-504 | Přidání nových typů deformace (oblouk a klenba)                                                                      | Funkce        |
| PSDJAVA-505 | Změna aplikace, která ukládá soubor PSD na Aspose.PSD, pokud je vlastnost UpdateMetadata nastavena na true          | Funkce        |
| PSDJAVA-510 | Zvýšení výpočetní oblasti deformovaného obrázku                                                                      | Funkce        |
| PSDJAVA-511 | Černobílá upravující vrstva zpracovává poloprůhledně špatně                                                         | Chyba         |
| PSDJAVA-512 | SmartObject ReplaceContents (když jsou aktivní možnosti AllowWarpRepaint) selže po 2 minutách výpočtu               | Chyba         |
| PSDJAVA-513 | Přidání možnosti získat skutečnou levou a horní pozici vrstvy skupiny                                               | Chyba         |
| PSDJAVA-514 | Změna velikosti vrstvy funguje špatně, když má soubor PSD s VogkResource se strukturami v bodech                     | Chyba         |
| PSDJAVA-515 | TextBound nefunguje jak očekáváme                                                                                 | Chyba         |
| PSDJAVA-516 | Přidání vrstvy vytvořené výchozím konstruktorem do obrazu PSD nezahrnuje výchozí prostředky                        | Chyba         |
| PSDJAVA-517 | Timeline.LoopesCount je ignorován při exportu do animovaného GIFu                                                   | Chyba         |

## **Změny ve veřejném rozhraní API**
# **Přidaná rozhraní API:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **Odebraná rozhraní API:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Příklady použití:**

**PSDJAVA-502. Přidání možnosti exportovat každou vrstvu souboru PSD do animovaného souboru Gif**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-503. Přiřazení vlastnosti Náplň vrstvy tvaru z prostředků vscg**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-504. Přidání nových typů deformace (oblouk a klenba)**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-505. Změna aplikace, která ukládá soubor PSD na Aspose.PSD, pokud je vlastnost UpdateMetadata nastavena na true**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-510. Zvýšení výpočetní oblasti deformovaného obrázku**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-511. Černobílá upravující vrstva zpracovává poloprůhledně špatně**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-512. SmartObject ReplaceContents (když jsou aktivní možnosti AllowWarpRepaint) selže po 2 minutách výpočtu**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-513. Přidání možnosti získat skutečnou levou a horní pozici vrstvy skupiny**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-514. Změna velikosti vrstvy funguje špatně, když má soubor PSD s VogkResource se strukturami v bodech**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-515. TextBound nefunguje jak očekáváme**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-516. Přidání vrstvy vytvořené výchozím konstruktorem do obrázku PSD nezahrnuje výchozí prostředky**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}

**PSDJAVA-517. Timeline.LoopesCount je ignorován při exportu do animovaného GIFu**

{{< highlight java >}}
    // Java kód zde
{{< /highlight >}}