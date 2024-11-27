---
title: Aspose.PSD pro .NET 22.3 - Poznámky k vydání
type: docs
weight: 100
url: /cs/net/aspose-psd-pro-net-22-3-poznamky-k-vydani/
---

{{% upozorneni barva="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /upozorneni %}}

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-210|Přidání vlastnosti IsOpen pro skupinu vrstev|Funkce|
|PSDNET-643|PSD obrázek s rastrovými maskami vrstev zahodí masky při ukládání do obrázku PSD s hloubkou 16 bitů|Chyba|
|PSDNET-899|Mód promíchávání Dissolve se neaplikuje na složku s maskou|Chyba|
|PSDNET-1047|Konkrétní soubor nelze otevřít v programu Photoshop po uložení v Aspose.PSD 21.11|Chyba|
|PSDNET-1068|Nesprávné zobrazování vrstvy s módem promíchávání Lineárního Odečtení (Přidat)|Chyba|
|PSDNET-1069|Vrstva vyplnění vzorem vyvolá výjimku při aktualizaci po načtení|Chyba|


## **Změny ve veřejném API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Odebrané API:**
- Žádné


## **Příklady použití:**

**PSDNET-210. Přidání vlastnosti IsOpen pro skupinu vrstev**

{{< highlight csharp >}}
// Příklad čtení a zápisu vlastnosti IsOpen za běhu.
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Skupina 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Skupina 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. PSD obrázek s vrstvami rastrových masek zahodí masky při ukládání do obrázku PSD s hloubkou 16 bitů**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Mód promíchávání Dissolve se neaplikuje na složku s maskou**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Konkrétní soubor nelze otevřít v programu Photoshop po uložení v Aspose.PSD 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Je třeba manuálně otevřít výstupní PSD v programu Photoshop.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // žádná výjimka.
            }
{{< /highlight >}}

**PSDNET-1068. Nesprávné zobrazování vrstvy s módem promíchávání Lineárního Odečtení (Přidat)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Vrstva vyplnění vzorem vyvolá výjimku při aktualizaci po načtení**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}
