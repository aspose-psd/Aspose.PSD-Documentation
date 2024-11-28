---
title: Aspose.PSD dla Java 21.6 - Notatki o wydaniu
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-21-6-notatki-o-wydaniu/
---

{{% alert color="primary" %}} Ta strona zawiera notatki o wydaniu dla [Aspose.PSD dla Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDJAVA-351|Maska przycięcia dla grupy nie renderuje się poprawnie|Błąd|
|PSDJAVA-352|Maska regularna lub wektorowa dla grupy warstw jest ignorowana podczas renderowania|Błąd|
|PSDJAVA-353|Obraz PSD z wyłączonymi maskami warstw wektorowych podczas zapisywania włącza maski wektorowe|Błąd|
|PSDJAVA-354|Wyjątek podczas tworzenia warstwy tekstowej z tekstem dłuższym niż 255 znaków|Błąd|

# **Zmiany w API publicznym**
# **Nowo dodane API:**
- Brak

# **Usunięte API:**
- Brak

# **Przykłady użycia:**

**PSDJAVA-351. Maska przycięcia dla grupy nie renderuje się poprawnie**

{{< highlight java >}}
        String nazwaPliku = "AppleClip.psd";
        String nazwaPlikuWyjsciowego = "wynik.png";

        PsdImage obraz = (PsdImage) Image.load(nazwaPliku);
        try
        {
            image.zapisz(nazwaPlikuWyjsciowego, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Maska regularna lub wektorowa dla grupy warstw jest ignorowana podczas renderowania**

{{< highlight java >}}
        String nazwaPliku = "Stripes3Mask.psd";
        String nazwaPlikuWyjsciowego = "OutputStripes3Mask.png";

        PsdImage obraz = (PsdImage) Image.load(nazwaPliku);
        try
        {
            obraz.zapisz(nazwaPlikuWyjsciowego, new PngOptions());
        }finally {
            obraz.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. Obraz PSD z wyłączonymi maskami warstw wektorowych podczas zapisywania włącza maski wektorowe**

{{< highlight java >}}
        String nazwaPliku = "FourWithMasksVd.psd";
        String nazwaPlikuWyjsciowego = "FourWithMasksVdOutput.psd";

        PsdImage obraz = (PsdImage) Image.load(nazwaPliku);
        try
        {
            obraz.zapisz(nazwaPlikuWyjsciowego);
        }finally {
            obraz.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Wyjątek podczas tworzenia warstwy tekstowej z tekstem dłuższym niż 255 znaków**

{{< highlight java >}}
        String wyjscie = "output.psd";

        PsdImage obraz = new PsdImage(100, 100);
        try
        {
            char[] znaki = new char[256];
            Arrays.fill(znaki, '*');
            String tekst = new String(znaki);
            obraz.dodajWarstweTekstu(tekst, Rectangle.getEmpty());

            obraz.zapisz(wyjscie);
        }finally {
            obraz.dispose();
        }
{{< /highlight >}}
