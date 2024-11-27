---
title: Aspose.PSD pro Java 23.9 - Poznámky k vydání
type: docs
weight: 40
url: /cs/java/aspose-psd-pro-java-23-9-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                                                                      | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Implementovat vytváření masky pro nové vrstvy úprav                                                                                             |    Funkce    |
| PSDJAVA-528 | Přidat podporu pro kombinované výřezy vrstev jako možnost seskupení blendování                                                                  |    Funkce    |
| PSDJAVA-529 | Soubor PSD s režimem barev 16 bitů neaplikuje masku pro úpravní vrstvy                                                                          |      Chyba    |
| PSDJAVA-530 | Nesprávné vykreslování závorek ve vrstvě textu                                                                                                   |      Chyba    |
| PSDJAVA-531 | Nelze aktualizovat styly ve vrstvách textu                                                                                                      |      Chyba    |
| PSDJAVA-532 | Po exportu souboru PSD s CMYK barvami se barvy v exportovaném PSD rozpadnou                                                                     |      Chyba    |
| PSDJAVA-533 | Konkrétní soubor PSB vyvolává výjimku "Obdélník nemá společnou zpracovávanou oblast"                                                           |      Chyba    |
| PSDJAVA-534 | Neúspěšné načtení obrázku. Přetečení výjimky: Aritmetická operace vedla k přetečení                                                            |      Chyba    |

## **Změny v veřejném API**
# **Přidaná API:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **Odstraněná API:**

- žádná

## **Příklady použití:**

**PSDJAVA-527. Implementovat vytváření masky pro nové úpravní vrstvy**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objekty nejsou stejné.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-528. Přidat podporu pro kombinované výřezy vrstev jako možnost seskupení blendování**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

... (Další příklady byly také přeloženy) ...
