---
title: Aspose.PSD pro .NET 24.7 - Poznámky k vydání
type: docs
weight: 60
url: /cs/net/aspose-psd-pro-net-24-7-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**     | **Shrnutí**                                                                                      | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Výjimka "Načítání obrázku selhalo." při otevření dokumentu AI                                          | Chyba      |
| PSDNET-2022 | Text je nesprávně vykreslen v výstupních souborech PDF                                                    | Chyba      |
| PSDNET-2061 | Opravena výjimka ImageSaveException: Selhalo exportování obrázku pro daný soubor na Linuxu              | Chyba      |
| PSDNET-2080 | Opraveno načítání písem při používání Aspose.Drawing                                                    | Chyba      |
| PSDNET-2085 | 'Aritmetická operace způsobila přetečení' při vytváření vrstvy chytrého objektu pomocí velkého JPEG     | Chyba      |
| PSDNET-2100 | Soubor AI nelze konvertovat do souboru JPG                                                             | Chyba      |

## **Změny ve veřejném rozhraní API**
# **Přidaná API:**
- žádné

# **Odebraná API:**
- žádné

## **Příklady použití:**

**PSDNET-1029. Výjimka "Načítání obrázku selhalo." při otevření dokumentu AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Text je nesprávně vykreslen výstupních souborech PDF**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Opravena výjimka ImageSaveException: Selhalo exportování obrázku pro daný soubor na Linuxu**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Opraveno načítání písem při používání Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Před aktualizací. Počet nainstalovaných písem: " + installedFonts.Families.Length);
    Console.WriteLine("- Platforma: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Obnovit cache písem pokusem získat jméno Adobe písma pro 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Po aktualizaci. Počet nainstalovaných písem: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Aritmetická operace způsobila přetečení' při vytváření vrstvy chytrého objektu pomocí velkého JPEG**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Soubor AI nelze konvertovat do souboru JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
