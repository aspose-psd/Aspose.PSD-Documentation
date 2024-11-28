---
title: Konwersja przestrzeni kolorów dla formatu JPEG za pomocą profili ICC
type: docs
weight: 60
url: /pl/net/konwersja-przestrzeni-kolorow-dla-jpeg-poprzez-profile-icc/
---

## **Zarządzanie kolorem formatu JPEG**

Ten artykuł omawia wykorzystanie profili ICC do zarządzania przestrzenią kolorów podczas obsługi formatu JPEG za pomocą interfejsów API Aspose.PSD. Wewnętrzna przestrzeń kolorów JPEG to YCbCr, jednak ten [format](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) może również pomieścić przestrzenie kolorów Grayscale, RGB, CMYK i YCCK do przechowywania metadanych obrazu. Interfejsy API Aspose.PSD działają głównie w przestrzeni RGB, dlatego API musi wykonać konwersję przestrzeni kolorów z i do w celu poprawnego obsługiwania plików JPEG. Konwersje z Grayscale na RGB oraz z YCbCr na RGB można dokonać za pomocą transformacji matematycznych, ale przestrzenie CMYK i YCCK nie mogą być łatwo przekonwertowane do przestrzeni RGB.

Interfejsy API Aspose.PSD muszą przeprowadzić bezpośrednią transformację koloru RGB na CMYK dla obrazów JPEG posiadających przestrzeń kolorów CMYK. Z kolei obrazy posiadające przestrzeń kolorów YCCK wymagają transformacji koloru z RGB na CMYK do YCCK, gdzie transformacja z CMYK do YCCK korzysta z konwersji [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) zastosowanej dla trzech pierwszych kanałów, pozostawiając kanał k nietknięty. W skrócie, interfejsy API Aspose.PSD muszą przeprowadzać wzajemną konwersję przestrzeni kolorów RGB i CMYK zarówno dla obrazów CMYK, jak i YCCK, a takie transformacje są przeprowadzane za pomocą profili ICC, które są w zasadzie tabelami poszukiwań opisującymi właściwości koloru i pomagające przy transformacjach kolorów.


## **Profile ICC**

Mechanizm konwersji ICC używa „Profilów”, które mapują przestrzeń kolorów źródłową na niezależne od urządzenia przestrzenie kolorów CIELAB lub CIEXYZ. Program Aspose.PSD może konwertować dane do przestrzeni kolorów z użyciem tych dwóch przestrzeni kolorów z dodatkowymi profilami. Dlatego w celu konwersji ICC użytkownik musi dostarczyć dwa profile - jeden profil RGB, aby uzyskać dostęp do wewnętrznej przestrzeni kolorów CIE, oraz jeden profil CMYK, aby uzyskać charakterystykę koloru CMYK. Aby osiągnąć konwersję CMYK na RGB, należy wymienić profile; użyć profilu CMYK jako profilu źródłowego oraz profilu RGB jako profilu docelowego.

## **Konwersja kolorów dla JPEG za pomocą profili ICC**

Interfejsy API Aspose.PSD ukrywają szczegóły, zapewniając łatwy mechanizm do określania profili ICC za pośrednictwem klasy [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Ponadto Aspose.PSD wykorzystuje przykładowe profile SWOP, CMYK i sRGB wbudowane w swoje jądro, dlatego w większości powszechnych zastosowań użytkownik nie musi szukać konkretnych profili. Istnieje wada takich korekt, a mianowicie; takie konwersje przestrzeni kolorów są nieodwracalne, ponieważ nie można spodziewać się uzyskania tego samego koloru po konwersji z RGB na CMYK na RGB z powodu niekompatybilnych przestrzeni kolorów i różnych profili kolorów. Poniższy fragment kodu przedstawia sposób użycia Aspose.PSD dla API .NET do określenia profili kolorów RGB i CMYK dla obrazu JPEG YCCK. W poniższym przykładzie profile RGB i CMYK są zmienione, a obraz jest zapisany w przestrzeni kolorów YCCK. Należy pamiętać, że właściwości [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) oraz [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) będą działać do zmiany danych pikseli dla przestrzeni kolorów YCCK. Wszystkie inne przestrzenie kolorów nie pobierają profili kolorów do aktualizacji danych kolorów.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

Jeśli nie są ustawione żadne profile, to interfejs API Aspose.PSD dla .NET użyje profilów domyślnych. Poniższy przykład wykorzystuje właściwości profili docelowych, które zmieniają przestrzeń barw docelową dla większości obrazów JPEG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
