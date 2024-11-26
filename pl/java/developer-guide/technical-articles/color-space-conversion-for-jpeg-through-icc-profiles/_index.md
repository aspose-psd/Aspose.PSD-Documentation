---
title: Konwersja przestrzeni barwnej dla plików JPEG za pomocą profili ICC
type: docs
weight: 50
url: /pl/java/konwersja-przestrzeni-barwnej-dla-plikow-jpeg-przez-profile-icc/
---

## **Zarządzanie kolorem dla formatu JPEG**

Ten artykuł omawia wykorzystanie profili ICC do zarządzania przestrzenią barwną podczas obsługi formatu JPEG przy użyciu interfejsów API Aspose.PSD. Wewnętrzna przestrzeń barwna JPEG to YCbCr, jednak ten format może także pomieścić przestrzenie barwne w odcieniach szarości, RGB, CMYK i YCCK w celu przechowywania metadanych obrazu. Interfejsy API Aspose.PSD operują głównie w przestrzeni RGB, dlatego interfejs API musi wykonać konwersję przestrzeni barwnej do i z przestrzeni barwnej w celu właściwej obsługi plików JPEG. Konwersję z odcieni szarości do RGB oraz z YCbCr do RGB można wykonać za pomocą transformacji matematycznych, ale przestrzenie CMYK i YCCK nie mogą być łatwo przekształcone w przestrzeń RGB.

Interfejsy API Aspose.PSD muszą przeprowadzić bezpośrednią konwersję koloru RGB na CMYK dla obrazów JPEG z przestrzenią barwną CMYK. Z kolei obrazy z przestrzenią barwną YCCK wymagają konwersji koloru z RGB na CMYK na YCCK, gdzie konwersja z CMYK na YCCK używa konwersji ITU-R BT.601 zastosowanej do pierwszych trzech kanałów, pozostawiając kanał k nienaruszony. W skrócie, interfejsy API Aspose.PSD muszą przeprowadzić wzajemną konwersję przestrzeni barwnej RGB i CMYK zarówno dla obrazów CMYK, jak i YCCK, a takie przekształcenia są wykonywane przy użyciu profili ICC, które są podstawowo tabelami poszukiwań opisującymi właściwości koloru i pomagają w przekształceniach kolorów.

## **Profile ICC**

Mechanizm konwersji ICC wykorzystuje „Profile”, które mapują źródłową przestrzeń barwną na niezależne od urządzenia przestrzenie barwne CIELAB lub CIEXYZ. Aspose.PSD może konwertować dane do przestrzeni barwnej, jak wymagane, używają te dwie przestrzenie barwne z dodatkowymi profilami. Dlatego do konwersji ICC użytkownik musi dostarczyć dwa profile – jeden profil RGB, aby przejść do wewnętrznej przestrzeni barwnej CIE oraz jeden profil CMYK, aby uzyskać charakterystykę koloru CMYK. Aby osiągnąć konwersję CMYK na RGB, należy wymienić profile, czyli użyć profilu CMYK jako profilu źródłowego i profilu RGB jako profilu docelowego.

## **Konwersja kolorów dla plików JPEG za pomocą profili ICC**

Interfejsy API Aspose.PSD ukrywają szczegóły, zapewniając prosty mechanizm do określania profili ICC za pomocą klasy JpegOptions. Ponadto Aspose.PSD używa przykładowych profili SWOP CMYK i sRGB wbudowanych w swoje jądro, dlatego w większości powszechnych przypadków użytkownik nie musi szukać konkretnych profili. Istnieje wada takich korekt, a mianowicie takie konwersje przestrzeni barwnej są nieodwracalne, ponieważ nie możemy oczekiwać uzyskania tego samego koloru po konwersji z RGB na CMYK na RGB ze względu na niekompatybilne przestrzenie barwne i różne profile kolorów. Poniższy fragment kodu demonstruje użycie Aspose.PSD dla interfejsu API Java w celu określenia profili koloru RGB i CMYK dla obrazu JPEG w przestrzeni barwnej YCCK. W poniższym przykładzie profile koloru RGB i CMYK są zmienione, a obraz jest zapisany w przestrzeni barwnej YCCK. Należy zauważyć, że właściwości RgbColorProfile i CmykColorProfile będą działać podczas zmiany danych pikseli dla przestrzeni barwnej YCCK. Wszystkie inne przestrzenie barwne nie pobierają profili kolorów w celu aktualizacji danych kolorów.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}

Jeśli nie są ustawione żadne profile, interfejs API Aspose.PSD w języku Java użyje domyślnych profili. Poniższy przykład wykorzystuje właściwości profili docelowych zmieniające przestrzeń barwną docelową dla większości obrazów JpegImages.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}
