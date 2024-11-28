---
title: Notatki wydania Aspose.PSD dla .NET 21.6
type: docs
weight: 70
url: /pl/net/aspose-psd-dla-net-21-6-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-546|Maska obcinająca dla grupy nie renderuje się poprawnie|Błąd|
|PSDNET-547|Maska regularna lub wektorowa dla grupy warstw jest ignorowana podczas renderowania|Błąd|
|PSDNET-647|Obraz PSD z wyłączonymi maskami warstw wektorowych podczas zapisywania włącza maski wektorowe|Błąd|
|PSDNET-786|Wyjątek podczas tworzenia warstwy tekstowej z tekstem dłuższym niż 255 znaków|Błąd|
|PSDNET-900|Tekst warstwy tekstowej nie może być renderowany na systemie Linux|Ulepszenie|

## **Zmiany w interfejsie API publicznym**
# **Dodane API:**
- Brak

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDNET-546. Maska obcinająca dla grupy nie renderuje się poprawnie**

{{< highlight csharp >}}
            string nazwaPlikuWejsciowego = "AppleClip.psd";
            string nazwaPlikuWyjsciowego = "wynik.png";

            using (PsdImage obraz = (PsdImage)Image.Load(nazwaPlikuWejsciowego))
            {
                obraz.Save(nazwaPlikuWyjsciowego, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Maska regularna lub wektorowa dla grupy warstw jest ignorowana podczas renderowania**

{{< highlight csharp >}}
        string nazwaPlikuWejsciowego = "Stripes3Mask.psd";
        string nazwaPlikuWyjsciowego = "OutputStripes3Mask.png";
        using (PsdImage obraz = (PsdImage)Image.Load(nazwaPlikuWejsciowego))
        {
            obraz.Save(nazwaPlikuWyjsciowego, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. Obraz PSD z wyłączonymi maskami warstw wektorowych podczas zapisywania włącza maski wektorowe**

{{< highlight csharp >}}
            string nazwaPlikuWejsciowego = "FourWithMasksVd.psd";
            string nazwaPlikuWyjsciowego = "FourWithMasksVdOutput.psd";

            using (PsdImage obraz = (PsdImage)Image.Load(nazwaPlikuWejsciowego))
            {
                obraz.Save(nazwaPlikuWyjsciowego);
            }
{{< /highlight >}}

**PSDNET-786. Wyjątek podczas tworzenia warstwy tekstowej z tekstem dłuższym niż 255 znaków**

{{< highlight csharp >}}
            string wyjscie = "wynik.psd";

            using (var obraz = new PsdImage(100, 100))
            {
                string tekst = new string('a', 256);
                obraz.AddTextLayer(tekst, Rectangle.Empty);

                obraz.Save(wyjscie);
            }
{{< /highlight >}}
