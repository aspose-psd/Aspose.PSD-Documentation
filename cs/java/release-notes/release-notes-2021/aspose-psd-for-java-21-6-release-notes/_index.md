---
title: Aspose.PSD pro Javu 21.6 - Poznámky k vydání
type: docs
weight: 40
url: /cs/java/aspose-psd-pro-java-21-6-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Javu 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-351|Сlipping mask pro skupinu není korektně vykreslena|Chyba|
|PSDJAVA-352|Běžná nebo vektorová maska pro skupinu vrstev je při vykreslování ignorována|Chyba|
|PSDJAVA-353|Obrázek PSD s vypnutými vektorovými maskami vrstev při ukládání povoluje vektorové masky|Chyba|
|PSDJAVA-354|Výjimka při vytváření vrstvy textu s textem delším než 255 znaků|Chyba|

# **Změny ve veřejném API**
# **Přidaná API:**
- Žádné

# **Odstraněná API:**
- Žádné

# **Příklady použití:**

**PSDJAVA-351. Сlipping mask pro skupinu není korektně vykreslena**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Běžná nebo vektorová maska pro skupinu vrstev je při vykreslování ignorována**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. Obrázek PSD s vypnutými vektorovými maskami vrstev při ukládání povoluje vektorové masky**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Výjimka při vytváření vrstvy textu s textem delším než 255 znaků**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
