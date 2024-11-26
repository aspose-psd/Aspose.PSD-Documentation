---
title: Praca z warstwami
type: docs
weight: 150
url: /pl/net/working-with-layers/
---

## **Utwórz grupę warstw**
Grupa warstw składa się z jednej lub więcej warstw i pomaga zorganizować podobne lub powiązane warstwy. Korzystając z Aspose.PSD dla .NET, można utworzyć grupę warstw. W tym celu dodano nową metodę [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) do klasy **[PsdImage ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)**, aby dodać grupę warstw.

Kroki do stworzenia grupy warstw są proste, jak poniżej:

- Utwórz instancję obrazu za pomocą klasy PsdImage z określoną szerokością, wysokością i opcjami obrazu.
- Utwórz [**LayerGroup** ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup)z określoną nazwą grupy i indeksem.
- Utwórz instancję klasy Layer i przypisz do niej obraz PSD.
- Dodaj utworzoną warstwę do grupy warstw za pomocą metody AddLayer wystawionej przez klasę LayerGroup.
- Zapisz wyniki.

Poniższy fragment kodu pokazuje, jak utworzyć grupę warstw.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Zmień nazwę warstwy**
Możesz użyć dowolnej nazwy, ale typową praktyką jest użycie ogólnego opisu obiektu lub elementu znajdującego się na tej warstwie. Ten artykuł demonstruje, jak można zmienić nazwę warstwy korzystając z Aspose.PSD dla .NET. W tym celu dodano nową właściwość [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) do klasy Layer, aby właściwie wyświetlać nazwę warstwy. Zauważono, że gdy Photoshop zapisuje nazwę warstwy używając właściwości [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), to koreańskie znaki są przechowywane jako bajt 63'?' w ASCII. Dlatego, jeśli chcesz poprawnie wyświetlić nazwę warstwy, użyj właściwości **DisplayName**, ponieważ właściwość **Name** nie obsługuje koreańskich znaków.

Poniższy przykładowy kod pokazuje, jak zmienić nazwę warstwy.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Wsparcie dla połączonych warstw**
Łączenie warstw jest podobne do grupowania warstw. Jeśli łączysz dwie lub więcej warstw, pozwoli ci to dokonywać określonych zmian w obu połączonych warstwach. Na przykład, jeśli zastosujesz transformacje do jednej warstwy, zostaną one zastosowane do wszystkich innych połączonych warstw. Ten artykuł demonstruje, jak otrzymać i rozłączyć połączone warstwy korzystając z [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}

