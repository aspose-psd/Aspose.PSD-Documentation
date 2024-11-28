---
title: Tworzenie, Otwieranie i Zapisywanie Plików PSD
type: docs
weight: 10
url: /pl/tworzenie-otwieranie-i-zapisywanie-plikow-psd/
---

## **Eksportowanie Obrazu do Formatu PSD**
PSD, dokument PhotoShop, to domyślny format pliku używany przez Adobe PhotoShop do pracy z obrazami. Aspose.PSD pozwala na ładowanie, edytowanie i zapisywanie plików do formatu PSD, tak aby mogły być one otwierane i edytowane w PhotoShop. Ten artykuł pokazuje, jak zapisać plik do formatu PSD za pomocą Aspose.PSD i omawia również niektóre ustawienia, które można wykorzystać podczas zapisywania w tym formacie. PsdOptions to specjalizowana klasa w przestrzeni nazw ImageOptions używana do eksportowania obrazów do formatu PSD. Aby wyeksportować do PSD, utwórz instancję klasy Image, która albo zostanie wczytana z istniejącego pliku obrazu (na przykład miniaturki), albo stworzona od podstaw. Ten artykuł wyjaśnia, jak to zrobić. W poniższych przykładach obraz jest tworzony od podstaw. Po utworzeniu i uzuepłnieniu danych pikseli, zapisz obraz za pomocą metody Save klasy Image i dostarcz obiekt PsdOptions jako drugi argument. Kilka właściwości klasy PsdOptions może być ustawione dla zaawansowanej konwersji. Niektóre z właściwości to ColorMode, CompressionMethod i Version. Aspose.PSD obsługuje następujące metody kompresji poprzez enumerację CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Następujące tryby kolorów są obsługiwane poprzez enumerację ColorModes:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Można dodać dodatkowe zasoby, takie jak zasoby miniatur dla PSD w wersji 4.0, 5.0 i nowsze, lub zasoby siatki i przewodnika dla wersji PSD 4.0 i nowsze. Poniższy kod tworzy plik BMP od zera, uzupełnia piksele i zapisuje go w formacie PSD z kompresją RLE i trybem kolorów w odcieniach szarości. Poniższy fragment kodu pokazuje, jak wyeksportować obraz do formatu PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Importowanie obrazu do warstwy PSD**
Ten artykuł demonstruje użycie Aspose.PSD do dodawania lub importowania obrazu do warstwy PSD. API Aspose.PSD udostępniło efektywne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD udostępniło metodę DrawImage klasy Layer do dodawania/importowania obrazu do pliku PSD. Metoda DrawImage wymaga lokalizacji i wartości obrazu do dodania/importowania obrazu do pliku PSD. Kroki do importowania obrazu do warstwy PSD są proste, jak poniżej:

- Wczytaj plik PSD jako obraz za pomocą metody fabrycznej Load udostępnionej przez klasę Image.
- Utwórz instancję klasy Layer i przypisz do niej warstwę obrazu PSD.
- Wczytaj obraz, który ma być dodany lub stwórz nowy od podstaw.
- Wywołaj metodę Layer.DrawImage, podając lokalizację i instancję obrazu.
- Zapisz wyniki.



Poniższy fragment kodu pokazuje, jak importować obraz do warstwy PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Tworzenie Miniatur z Plików PSD**
PSD to domyślny format dokumentu aplikacji Adobe Photoshop. Adobe Photoshop (wersja 5.0 i nowsze) przechowuje informacje o miniaturze do podglądu w bloku zasobów obrazu składającego się z początkowego nagłówka 28 bajtów, a następnie miniatury JFIF w kolejności RGB (czerwony, zielony, niebieski). API Aspose.PSD zapewnia mechanizm łatwego dostępu do zasobów pliku PSD. Te zasoby obejmują również zasób miniatury, który z kolei może być pobrany i zapisany na dysku zgodnie z potrzebami aplikacji. Poniższy fragment kodu pokazuje, jak tworzyć miniatury z plików PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Tworzenie Plików PSD z Indeksem**
Aspose.PSD dla Java API może tworzyć pliki PSD z indeksem od zera. Ten artykuł demonstruje użycie klas PsdOptions i PsdImage do utworzenia indeksowanego pliku PSD podczas rysowania kształtów na nowo utworzonej płótnie. Poniższe proste kroki są wymagane do utworzenia pliku PSD z indeksem.

- Utwórz instancję PsdOptions i ustaw jej źródło.
- Ustaw właściwość ColorMode klasy PsdOptions na ColorModes.Indexed.
- Utwórz nową paletę kolorów z przestrzeni RGB i ustaw ją jako właściwość Palette klasy PsdOptions.
- Ustaw właściwość CompressionMethod na wymagany algorytm kompresji.
- Utwórz nowy obraz PSD, wywołując metodę PsdImage.Create.
- Narysuj grafikę lub wykonaj inne operacje zgodnie z wymaganiami.
- Wywołaj metodę PsdImage.Save, aby zatwierdzić wszystkie zmiany.



Poniższy fragment kodu pokazuje, jak tworzyć pliki PSD z indeksem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **Eksportowanie Warstwy PSD do Obrazu Rastrowego**
Aspose.PSD dla Java pozwala na eksportowanie warstw w pliku PSD do obrazów rastrowych. Proszę użyć metody Aspose.PSD.FileFormats.Psd.Layers.Layer.Save do wyeksportowania warstwy do obrazu. Poniższy przykładowy kod wczytuje plik PSD i eksportuje każdą z jego warstw do obrazu PNG za pomocą metody Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Po wyeksportowaniu wszystkich warstw do obrazów PNG, można je otworzyć za pomocą ulubionego przeglądarki obrazów. Poniższy fragment kodu pokazuje, jak eksportować warstwę PSD do obrazu rastrowego.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}
