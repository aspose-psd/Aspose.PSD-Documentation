---
title: Modyfikowanie obrazów PNG
type: docs
weight: 30
url: /pl/java/modyfikowanie-obrazow-png/
---

## **Określanie przezroczystości obrazów PNG**
Jedną z zalet zapisywania obrazów w formacie PNG jest możliwość posiadania przezroczystego tła. Aspose.PSD dla języka Java udostępnia funkcję określania przezroczystości dla klas PngImage & RasterImage, jak pokazano w poniższym rozdziale. API Aspose.PSD dla języka Java można użyć do określenia przezroczystości przy tworzeniu nowych obrazów PNG lub konwertowaniu istniejących obrazów do formatu PNG. W tym celu API Aspose.PSD dla języka Java udostępnił właściwość TransparentColor oraz enumerację PngColorType, które można ustawić, aby określić kolor do renderowania jako przezroczysty na obrazie PNG. Poniższy fragment kodu demonstruje, jak przekonwertować istniejący obraz PSD na obraz PNG, korzystając z przeciążonego konstruktora PngImage i określając pożądany kolor jako przezroczysty.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Ustawianie rozdzielczości obrazów PNG**
Aspose.PSD dla języka Java udostępnia klasę ResolutionSetting, która może być użyta do ustawienia rozdzielczości dla wszystkich formatów obrazów, w tym PNG. Ten artykuł demonstruje używanie API Aspose.PSD dla języka Java do ustawiania parametrów rozdzielczości poziomej i pionowej dla formatu obrazu PNG. Poniższy fragment kodu wczytuje istniejący obraz PSD i konwertuje go do formatu PNG, jednocześnie zmieniając rozdzielczość.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Kompresowanie plików PNG**
Portable Network Graphic (PNG) to format kompresji bezstratnej do przesyłania map bitowych przez sieć. Gdy zapisujesz obraz jako plik PNG w dowolnym programie, możesz zostać poproszony o wybór poziomu kompresji z zakresu od 0 do maksymalnej wartości. Ustawienie tej wartości faktycznie kompresuje rozmiar pliku i nie zmniejsza jakości obrazu. W tym artykule opisano, jak API Aspose.PSD umożliwia kontrolowanie rozmiaru plików PNG. Można użyć API Aspose.PSD do ustawienia Poziomów Kompresji dla formatu pliku PNG, korzystając z klasy PngOptions, która posiada właściwość CompressionLevel typu int. Ta właściwość akceptuje wartość od 0 do 9, gdzie 9 oznacza maksymalną kompresję. Poniższy fragment kodu demonstruje, jak ustawić Poziomy Kompresji za pomocą API Aspose.PSD dla języka Java.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Określanie głębokości bitowej obrazów PNG**
Głębokość bitowa w technice obrazowania to liczba bitów użytych do wskazania koloru jednego piksela w obrazie bitmapowym. Podobnie jak we wszystkich innych formatach bitmapowych, głębokość koloru w PNG jest również wyrażana w bitach, takich jak 1-bit (2 kolory), 2-bit (4 kolory), 4-bit (16 kolorów) i 8-bit (256 kolorów). API Aspose.PSD dla języka Java może być użyte do ustawienia głębokości bitowej dla obrazów PNG, wykorzystując właściwość BitDepth udostępnioną przez klasę PngOptions. Obecnie właściwość BitDepth może być ustawiona na 1, 2, 4 lub 8 bitów dla odcieni szarości i kolorów indeksowanych. Dla wszystkich innych typów kolorów wspierane są tylko 8 bitów. Poniższy fragment kodu demonstruje, jak ustawić Głębokość Bitową dla obrazu PNG.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Zastosowanie metod filtrów do obrazów PNG**
Aspose.PSD dla języka Java udostępnia enumerację PngFilterType, która może być użyta do ustawienia typu filtra dla obrazu PNG. Poniższy fragment kodu demonstruje, jak zastosować filtr na istniejący plik PSD do obrazu PNG, korzystając z PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Zmiana koloru tła obrazu PNG z przezroczystością**
Obrazy w formacie PNG mogą mieć przezroczyste tło. Aspose.PSD dla języka Java dostarcza funkcję zmiany koloru tła obrazu PNG, który ma przezroczyste tło. API Aspose.PSD dla języka Java może być użyte do ustawienia/zmiany koloru przezroczystego obrazu PNG. Poniższy fragment kodu demonstruje, jak ustawić/zmienić kolor tła obrazu PNG z przezroczystym tłem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
