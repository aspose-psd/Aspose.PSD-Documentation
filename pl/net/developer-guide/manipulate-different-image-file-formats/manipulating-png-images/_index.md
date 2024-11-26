---
title: Modyfikowanie obrazów PNG
type: docs
weight: 40
url: /pl/net/modyfikowanie-obrazow-png/
---

## **Określanie przezroczystości obrazów PNG**
Jedną z zalet zapisywania obrazów w formacie PNG jest fakt, że PNG może mieć transparentne tło. Aspose.PSD dla .NET udostępnia funkcję określania przezroczystości dla obrazów PNG i obrazów rastrowych, co zostało pokazane w poniższym rozdziale. Aspose.PSD dla .NET API może być użyte do ustawienia dowolnego koloru jako przezroczysty podczas tworzenia nowych obrazów PNG lub konwertowania istniejących obrazów do formatu PNG. W tym celu Aspose.PSD dla .NET API udostępnia właściwość [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) oraz wyliczenie [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype), które można ustawić, aby określić, który kolor ma być renderowany jako transparentny na obrazie PNG. Poniższy fragment kodu przedstawia, jak przekonwertować istniejący obraz PSD na obraz PNG, określając wybrany kolor jako transparentny.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **Ustawianie rozdzielczości obrazów PNG**
Aspose.PSD dla .NET udostępnia klasę ResolutionSetting, która może być użyta do ustawienia rozdzielczości dla wszystkich formatów obrazów, w tym PNG. Ten artykuł demonstruje wykorzystanie Aspose.PSD dla .NET API do ustawienia parametrów rozdzielczości poziomej i pionowej dla formatu obrazu PNG. Poniższy fragment kodu ładuje istniejący obraz PSD, konwertuje go na format PNG i jednocześnie zmienia rozdzielczość.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **Kompresowanie plików PNG**
Portable Network Graphic (PNG) to bezstratny format kompresji do przesyłania map bitowych przez sieci. Podczas zapisywania obrazu jako plik PNG w dowolnym programie, możesz zostać poproszony o wybranie poziomu kompresji w zakresie od 0 do maksymalnego poziomu. Ustawienie tej wartości faktycznie kompresuje rozmiar pliku i nie zmniejsza jakości obrazu. Ten artykuł opisuje, jak Aspose.PSD APIs pozwala kontrolować rozmiar pliku PNG. Aspose.PSD APIs mogą być używane do ustawienia Poziomów Kompresji dla formatu pliku PNG przy użyciu klasy PngOptions, która posiada właściwość int typu [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel). Ta właściwość przyjmuje wartość od 0 do 9, gdzie 9 oznacza maksymalną kompresję. Poniższy fragment kodu demonstruje, jak ustawić Poziomy Kompresji za pomocą Aspose.PSD dla .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **Określanie głębi bitowej obrazów PNG**
Głębia bitowa w obrazowaniu to liczba bitów używanych do określenia koloru pojedynczego piksela w obrazie bitmapowym. Podobnie jak we wszystkich innych formatach bitmapowych, głębia koloru PNG jest również wyrażana w bitach, takich jak 1-bit (2 kolory), 2-bit (4 kolory), 4-bit (16 kolorów) i 8-bit (256 kolorów). Aspose.PSD dla .NET API może być użyte do ustawienia głębi bitowej dla obrazów PNG za pomocą właściwości [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) udostępnionej przez klasę PngOptions. W chwili obecnej właściwość BitDepth może być ustawiona na 1, 2, 4 lub 8 bitów dla odcieni szarości i typów kolorów indeksowanych. Dla wszystkich innych typów kolorów obsługiwane są tylko 8 bitów. Poniższy fragment kodu przedstawia, jak ustawić Głębię Bitową dla obrazu PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **Zastosowanie metod filtrów do obrazów PNG**
Głębia bitowa w obrazowaniu to liczba bitów używanych do określenia koloru pojedynczego piksela w obrazie bitmapowym. Podobnie jak we wszystkich innych formatach bitmapowych, głębia koloru PNG jest również wyrażana w bitach, takich jak 1-bit (2 kolory), 2-bit (4 kolory), 4-bit (16 kolorów) i 8-bit (256 kolorów). Aspose.PSD dla .NET API może być użyte do ustawienia głębi bitowej dla obrazów PNG za pomocą właściwości BitDepth udostępnionej przez klasę PngOptions. W chwili obecnej właściwość BitDepth może być ustawiona na 1, 2, 4 lub 8 bitów dla odcieni szarości i typów kolorów indeksowanych. Dla wszystkich innych typów kolorów obsługiwane są tylko 8 bitów. Poniższy fragment kodu przedstawia, jak ustawić Głębię Bitową dla obrazu PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **Zmiana koloru tła transparentnego obrazu PNG**
Obrazy w formacie PNG mogą mieć transparentne tło. Aspose.PSD dla .NET zapewnia funkcję zmiany koloru tła obrazu PNG, który ma transparentne tło. Aspose.PSD dla .NET API może być użyte do ustawienia/zmiany koloru transparentnego obrazu PNG. Poniższy fragment kodu przedstawia, jak ustawić/zmienić kolor tła transparentnego obrazu PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
