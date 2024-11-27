---
title: Aspose.PSD pro .NET 21.6 - Poznámky k vydání
type: docs
weight: 70
url: /cs/net/aspose-psd-pro-net-21-6-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč** | **Souhrn** | **Kategorie** |
| :- | :- | :- |
|PSDNET-546|Čepele masky pro skupinu jsou špatně renderovány|Chyba|
|PSDNET-547|Běžná nebo vektorová maska pro skupinu vrstev je při renderování ignorována|Chyba|
|PSDNET-647|Obraz PSD s deaktivovanými vektorovými maskami vrstev při uložení povoluje vektorové masky|Chyba|
|PSDNET-786|Výjimka při vytváření vrstvy textu s textem delším než 255 znaků|Chyba|
|PSDNET-900|Text vrstvy Text nemůže být renderován na Linuxu|Vylepšení|

## **Změny ve veřejném API**
# **Přidaná API:**
- Žádná

# **Odstraněná API:**
- Žádná

## **Příklady použití:**

**PSDNET-546. Čepel masky pro skupinu je špatně renderována**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Běžná nebo vektorová maska pro skupinu vrstev je při renderování ignorována**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. Obraz PSD s deaktivovanými vektorovými maskami vrstev při uložení povoluje vektorové masky**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Výjimka při vytváření vrstvy textu s textem delším než 255 znaků**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
