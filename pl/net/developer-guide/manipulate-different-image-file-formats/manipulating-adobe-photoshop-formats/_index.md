---
title: Manipulowanie formatami Adobe Photoshop
type: docs
weight: 20
url: /pl/manipulowanie-formatami-adobe-photoshop/
---

## **Łączenie warstw PSD z innymi warstwami**

## **Eksportowanie obrazu do PSD**
PSD, dokument PhotoShop, to domyślny format pliku używany przez Adobe Photoshop do pracy z obrazami. Aspose.PSD pozwala na wczytywanie, edytowanie i zapisywanie plików do formatu PSD, dzięki czemu mogą być one otwierane i edytowane w Photoshopie. Ten artykuł pokazuje, jak zapisać plik do formatu PSD przy użyciu Aspose.PSD, omawiając również niektóre ustawienia, które można użyć podczas zapisywania w tym formacie. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) to specjalizowana klasa w przestrzeni nazw [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions), używana do eksportowania obrazów do formatu PSD. Aby wyeksportować do PSD, wykonaj instancję klasy Image, która jest albo wczytana z istniejącego pliku obrazu (np. miniaturki), albo utworzona od podstaw. Ten artykuł wyjaśnia, jak to zrobić. W poniższych przykładach obraz jest tworzony od podstaw. Po stworzeniu i wypełnieniu danych pikseli zapisz obraz, używając metody Save klasy Image, i przekaż obiekt PsdOptions jako drugi argument. Kilka właściwości klasy PsdOptions może zostać ustawionych dla zaawansowanej konwersji. Niektóre z właściwości to ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) i Versio...

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **Importowanie obrazu do warstwy PSD**
Ten artykuł demonstruje wykorzystanie Aspose.PSD do dodawania lub importowania obrazu do warstwy PSD. Interfejsy API Aspose.PSD udostępniają efektywne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD udostępnia metodę [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) klasy Layer, aby dodać/przenieść obraz do pliku PSD. Metoda DrawImage wymaga podania lokalizacji i wartości obrazu, aby dodać/przenieść obraz do pliku PSD. Kroki do importowania obrazu do warstwy PSD są proste, jak poniżej:

- Wczytaj plik PSD jako obraz, używając metody fabrycznej Load udostępnionej przez klasę Image.
- Utwórz instancję klasy Layer z plikiem Png, Jpeg, Tiff, Gif, Bmp, Psd lub j2k
- Dodaj warstwę do PSD używając metody AddLayer
- Zapisz wyniki.


Poniższy fragment kodu pokazuje, jak importować obraz do warstwy PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Zastępowanie kolorów w warstwach PSD**
Ten artykuł demonstruje wykorzystanie Aspose.PSD do dodawania lub importowania obrazu do warstwy PSD. Interfejsy API Aspose.PSD udostępniają efektywne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD udostępnia metodę DrawImage klasy Layer do dodawania/importowania obrazu do pliku PSD. Metoda DrawImage wymaga podania lokalizacji i wartości obrazu do dodania/importowania obrazu do pliku PSD. Kroki do importowania obrazu do warstwy PSD są proste, jak poniżej:

- Wczytaj plik PSD jako obraz, używając metody fabrycznej Load udostępnionej przez klasę Image.
- Utwórz instancję klasy Layer i przypisz warstwę obrazu PSD do niej.
- Wczytaj obraz, który ma zostać dodany lub stwórz jeden od podstaw.
- Wywołaj metodę Layer.DrawImage, podając lokalizację i instancję obrazu.
- Zapisz wyniki.


Poniższy fragment kodu pokazuje, jak importować obraz do warstwy PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **Tworzenie miniatur z plików PSD**
PSD jest natywnym formatem dokumentu aplikacji Adobe Photoshop. Adobe Photoshop (wersja 5.0 i nowsze) przechowuje informacje o miniaturach do podglądu w bloku zasobów obrazu, który składa się z początkowego nagłówka 28 bajtów, a następnie miniatury JFIF w kolejności RGB (czerwony, zielony, niebieski). API Aspose.PSD zapewnia łatwy w użyciu mechanizm dostępu do zasobów pliku PSD. Te zasoby obejmują również zasób miniatury, który z kolei może być pobrany i zapisany na dysku zgodnie z potrzebami aplikacji. Poniższy fragment kodu pokazuje, jak tworzyć miniatury z plików PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **Tworzenie plików PSD indeksowanych**
API Aspose.PSD dla .NET może tworzyć pliki PSD indeksowane od podstaw. Ten artykuł demonstruje użycie klas PsdOptions i [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) do stworzenia pliku PSD indeksowanego, rysując jednocześnie niektóre kształty na nowo utworzonej płótnie. Następujące proste kroki są wymagane do stworzenia pliku PSD indeksowanego:

- Utwórz instancję PsdOptions i ustaw na niej źródło.
- Ustaw właściwość ColorMode PsdOptions na ColorModes.Indexed.
- Utwórz nową paletę kolorów przestrzeni RGB i ustaw ją jako właściwość Palette PsdOptions.
- Ustaw właściwość CompressionMethod na żądany algorytm kompresji.
- Utwórz nowy obraz PSD, wywołując metodę PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Narysuj grafikę lub wykonaj inne operacje zgodnie z wymaganiami.
- Wywołaj metodę PsdImage.Save, aby zatwierdzić wszystkie zmiany.


Poniższy fragment kodu pokazuje, jak tworzyć pliki PSD indeksowane.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **Eksportowanie warstwy PSD do obrazu rastrowego**
Aspose.PSD dla .NET pozwala eksportować warstwy w pliku PSD do obrazów rastrowych. Proszę użyć metody [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) do wyeksportowania warstwy do obrazu. Poniższy przykładowy kod wczytuje plik PSD i eksportuje każdą z jego warstw do obrazu PNG, używając metody Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Po wyeksportowaniu wszystkich warstw do obrazów PNG, można je otworzyć przy użyciu ulubionego przeglądarki obrazów. Poniższy fragment kodu pokazuje, jak eksportować warstwę PSD do obrazu rastrowego.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}
## **Aktualizacja warstwy tekstowej w pliku PSD**
Aspose.PSD dla .NET pozwala manipulować tekstem w warstwie tekstowej pliku PSD. Proszę użyć klasy [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer), aby zaktualizować tekst na warstwie PSD. Poniższy fragment kodu wczytuje plik PSD, uzyskuje dostęp do warstwy tekstowej, aktualizuje tekst i zapisuje plik PSD pod nową nazwą, używając metody [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **Wykrywanie spłaszczonego pliku PSD**
Aspose.PSD dla .NET pozwala określić, czy dany plik PSD jest spłaszczony czy nie. W tym celu właściwość IsFlatten została wprowadzona w klasie Aspose.PSD.FileFormats.Psd.PsdImage. Poniższy fragment kodu wczytuje plik PSD i uzyskuje dostęp do właściwości [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}
## **Łączenie warstw PSD**
Ten artykuł pokazuje, jak łączyć warstwy w pliku PSD podczas konwertowania pliku PSD na JPG za pomocą Aspose.PSD. W poniższym przykładzie istniejący plik PSD jest wczytywany, przekazując ścieżkę pliku do statycznej metody Load klasy Image. Gdy zostanie wczytany, przekształć/wrzuc obraz do klasy PsdImage. Utwórz instancję klasy JpegOptions i ustaw różne właściwości. Następnie wywołaj metodę Save instancji PsdImage. Poniższy fragment kodu pokazuje, jak łączyć warstwy PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}
## **Wsparcie dla odcieni szarości z alfą dla plików PSD**
Ten artykuł pokazuje, jak wspierać odcienie szarości z alfą dla pliku PSD podczas konwertowania pliku PSD do PNG za pomocą Aspose.PSD. W poniższym przykładzie istniejący plik PSD jest wczytywany, przekazując ścieżkę pliku do statycznej metody Load klasy Image. Gdy zostanie wczytany, przekształć/wrzuc obraz do klasy PsdImage. Utwórz instancję klasy PngOptions i ustaw na niej różne właściwości. Ustaw właściwość [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) na TruecolorWithAlpha. Następnie wywołaj metodę Save instancji PngOptions. Poniższy fragment kodu pokazuje, jak konwertować do odcieni szarości PNG z alfą.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.cs" >}}
## **Wsparcie dla efektów warstwy dla plików PSD**
Ten artykuł pokazuje, jak wspierać różne efekty jak **Rozmycie**, **Wewnętrzne** **słabości**, **Zewnętrzne słabości** dla warstwy PSD. Poniższy fragment kodu pokazuje, jak wspierać efekty warstwy.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.cs" >}}
## **Wsparcie dla daty i godziny utworzenia warstwy**
Ten artykuł pokazuje, jak wspierać datę i godzinę utworzenia warstwy dla warstwy PSD. Poniższy fragment kodu pokazuje, jak tworzyć warstwy.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LayerCreationDateTime-LayerCreationDateTime.cs" >}}
## **Wsparcie dla podświetlania kolorów w arkuszu**
Ten artykuł pokazuje, jak wczytać obrazy PSD, a następnie zmienić i podświetlić kolory arkuszy i zapisać je jako obraz. Fragment kodu został dostarczony.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SheetColorHighlighting-SheetColorHighlighting.cs" >}}
## **Wsparcie dla maski warstwy**
Ten artykuł pokazuje, jak wspierać maski warstwowe dla obrazów PSD i zapisywać te obrazy. Fragment kodu został dostarczony poniżej.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerMask-SupportOfLayerMask.cs" >}}
## **Wsparcie dla maski warstw wektorowych**
Ten artykuł pokazuje wsparcie dla maski wektorowej warstw dla Aspose.PSD. Poniższy fragment kodu pokazuje, jak Aspose.PSD obsługuje maski warstw wektorowych.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerVectorMask-SupportOfLayerVectorMask.cs" >}}
## **Wsparcie dla warstw tekstowych w czasie rzeczywistym**
Ten artykuł pokazuje, jak dodawać warstwy tekstowe w czasie rzeczywistym dla obrazów PSD. Fragment kodu został dostarczony poniżej.

{{