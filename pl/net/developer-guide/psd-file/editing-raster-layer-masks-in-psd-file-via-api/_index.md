---
title: Edycja masek warstw rastrowych w pliku PSD za pomocą interfejsu API
type: docs
weight: 20
url: /pl/net/edycja-masek-warstw-rastrowych-w-pliku-psd-poprzez-api/
---

## **Przegląd**
**Aby zautomatyzować edycję formatu PSD i zmienić plik PSD bez konieczności korzystania z Adobe® Photoshop®, można skorzystać z poniższego interfejsu API Aspose.PSD. Dostępne są fragmenty kodu w językach C# i .NET, które pomogą w modyfikacji plików PSD.**

Korzystając z masek warstwowych i wektorowych PSD, jesteśmy w stanie ukrywać i pokazywać piksele warstwy bez ich trwałego usuwania. Maska rastrowa jest również nazywana maską warstwową lub maską użytkownika. Dostęp do obu masek rastrowych i wektorowych w Aspose.PSD jest zapewniony poprzez właściwość warstwy [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) , która może być instancją klas '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' oraz '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)', które są klasami podrzędnymi klasy abstrakcyjnej 'LayerMaskData'. Jeśli warstwa posiada zarówno maski rastrowe, jak i wektorowe, dostarczana jest instancja [LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull) . Jeśli warstwa ma jedynie maskę rastrową lub wektorową, dostarczana jest instancja [LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort) . Jeśli właściwość LayerMaskData ma wartość null, oznacza to, że warstwa nie posiada masek lub ma jedynie dezaktywowaną maskę wektorową.
  
|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Maska rastrowa i dezaktywowana maska wektorowa - LayerMaskDataShort</p><p>Dezaktywowana maska rastrowa LayerMaskDataShort</p><p>Maska rastrowa i maska wektorowa LayerMaskDataFull</p><p>Maska rastrowa LayerMaskDataShort</p><p>Maska wektorowa LayerMaskDataShort</p><p>Dezaktywowana maska wektorowa null (Ale zasób wektorowy jest obecny)</p>|

## **Jak uzyskać maskę rastrową warstwy w pliku PSD?**
Na początku powinniśmy sprawdzić, czy warstwa posiada zarówno maski wektorowe, jak i warstwowe:

Poniżej znajduje się przykładowy kod demonstrujący, jak uzyskać maskę rastrową warstwy

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

W przeciwnym razie, jeśli typ właściwości warstwy LayerMaskData to LayerMaskDataShort, wówczas sprawdzamy, czy warstwa ma jedynie maskę rastrową, sprawdzając właściwość Flags. Nie powinien on zawierać flagi [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData**, w przeciwnym razie maska jest buforem maski wektorowej**.**

Fragment kodu uzyskiwania maski:

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Jeśli konieczne jest **wyodrębnienie maski rastrowej** jako LayerMaskDataShort (do dalszych manipulacji) nawet gdy obydwie maski są obecne, należy wyodrębnić LayerMaskDataFull i przekształcić go na LayerMaskDataShort. Poniższy kod może być użyty w obydwu przypadkach:

Wyodrębnienie maski rastrowej z pliku PSD

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}

## **Jak sprawdzić, czy warstwa w pliku PSD posiada maskę rastrową?**
Poniższy kod w języku C# może pomóc Ci sprawdzić, czy warstwa ma maskę rastrową:

Jak sprawdzić, czy maska rastrowa została zastosowana do [warstwy PSD](/psd/pl/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}

## **Jak usunąć / dodać / zaktualizować maskę rastrową warstwy w pliku PSD?**
Tylko usunięcie / dodanie / aktualizacja LayerMaskData nie jest wystarczające do poprawnego zapisywania, ponieważ kanały nie są aktualizowane. Chociaż może to zapewnić poprawne renderowanie. To nie zmienia kanałów maski:

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Powinniśmy użyć metody AddLayerMask warstwy do usuwania / dodawania / aktualizowania.

Ta metoda dodaje/aktualizuje zarówno maskę, jak i kanały:

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Ta metoda usuwa zarówno maskę, jak i kanały:

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}

## **Usuwanie maski rastrowej warstwy obrazu PSD**
Najpierw sprawdzamy, czy maska jest w formacie krótkim, a jeśli nie jest wektorową, możemy po prostu wywołać metodę AddLayerMask z wartością null, aby usunąć maskę rastrową. Ale jeśli jest w formacie pełnym, musimy przekształcić go na krótki format, pozostawiając tylko maskę wektorową. Do usunięcia maski warstwy można użyć tego kodu w języku C# .NET:

Fragment kodu, jak usunąć warstwę maski z pliku PSD.

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

## **Aktualizacja maski rastrowej warstwy obrazu PSD**
Jest to proste: jeżeli maska jest w formacie krótkim, musimy zmienić ImageData i MaskRectangle, jeśli jest to konieczne, w przeciwnym razie należy zmienić [UserMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata) oraz [UserMaskRectangle](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle). Poniższy kod w języku C# .NET może być użyty do aktualizacji maski warstwy:

Aktualizacja maski warstwy PSD za pomocą C#

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Poniżej znajduje się przykład możliwych działań, które zmieniają maskę rastrową. Ten przykład odwraca maskę użytkownika warstwy:

Aktualizacja maski warstwy PSD za pomocą C#

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}

## **Aktualizacja maski wektorowej w pliku PSD, gdy obecna jest maska rastrowa warstwy**
Zakłada się, że użytkownik już zmienił zasób ścieżki wektorowej. Następnie można zaktualizować maskę wektorową, po prostu wywołując metodę [AddLayerMask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask) warstwy:

Aktualizacja [Maski Wektorowej Warstwy PSD](/psd/pl/net/layer-vector-mask/) za pomocą C#

{{< gist "aspose-com-gists" "8a4d34ce16842fc7c0ce974175c9d34" "Dokumentacja-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}

## **Dodanie maski rastrowej warstwy w pliku PSD**
Jeśli warstwa nie posiada maski, można dodać odpowiednią maskę rastrową, po prostu wywołując metodę warstwy AddLayerMask.

Jeżeli maska nie posiada flagi [UserMaskFromRenderingOtherData**](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags) , oznacza to, że już posiada maskę rastrową i należy ją zaktualizować, jak opisano powyżej. W przeciwnym razie, jeżeli maska
