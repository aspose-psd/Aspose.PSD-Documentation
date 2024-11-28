---
title: Aspose.PSD dla .NET 24.7 - Notatki dotyczące wydania
type: docs
weight: 60
url: /pl/net/aspose-psd-dla-net-24-7-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klucz**   | **Podsumowanie**                                                                                  | **Kategoria** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Wyjątek "Wystąpił błąd podczas ładowania obrazu." podczas otwierania dokumentu AI                   | Błąd    |
| PSDNET-2022 | Tekst wyświetlany nieprawidłowo w plikach PDF wyjściowych                                         | Błąd    |
| PSDNET-2061 | Naprawa ImageSaveException: Eksport obrazu nie powiódł się dla określonego pliku w systemie Linux  | Błąd    |
| PSDNET-2080 | Naprawa ładowania czcionek podczas korzystania z Aspose.Drawing                                    | Błąd    |
| PSDNET-2085 | 'Operacja arytmetyczna spowodowała przepełnienie' podczas tworzenia warstwy obiektu inteligentnego z dużym obrazem JPEG | Błąd    |
| PSDNET-2100 | Plik AI nie może zostać przekonwertowany na plik JPG                                              | Błąd    |

## **Zmiany w API publicznym**
# **Dodane API:**
- Brak

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDNET-1029. Wyjątek "Wystąpił błąd podczas ładowania obrazu." podczas otwierania dokumentu AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Tekst wyświetlany nieprawidłowo w plikach PDF wyjściowych**

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

**PSDNET-2061. Naprawa ImageSaveException: Eksport obrazu nie powiódł się dla określonego pliku w systemie Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Naprawa ładowania czcionek podczas korzystania z Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Przed aktualizacją. Liczba zainstalowanych czcionek: " + installedFonts.Families.Length);
    Console.WriteLine("- Platforma: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Odśwież pamięć podręczną czcionek próbując uzyskać nazwę czcionki Adobe dla 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Po aktualizacji. Liczba zainstalowanych czcionek: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Operacja arytmetyczna spowodowała przepełnienie' podczas tworzenia warstwy obiektu inteligentnego z dużym obrazem JPEG**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Warstwa testowa";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Plik AI nie może zostać przekonwertowany na plik JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
