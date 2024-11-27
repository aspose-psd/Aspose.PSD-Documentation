---
title: Работа със слоеве
type: docs
weight: 150
url: /bg/net/работа-със-слоеве/
---

## **Създаване на група слоеве**
Група от слоеве се състои от един или повече слоеве и помага за организиране на подобни или свързани слоеве. С помощта на Aspose.PSD за .NET можете да създадете група слоеве. За целта е добавен нов метод [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) в класа **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** за добавяне на групата слоеве.

Стъпките за създаване на групи слоеве са толкова прости, както следва:

- Създайте инстанция на изображение, използвайки класа PsdImage с посочената ширина, височина и опции за изображението.
- Създайте [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) с посоченото име на групата и индекса.
- Създайте инстанция на класа Layer и присвоете изображението на PSD на него.
- Добавете създадения слой към групата от слоеве, използвайки метода AddLayer, който е достъпен от класа LayerGroup.
- Запазете резултатите.

Следният откъс код ви показва как да създадете група слоеве.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Преименуване на слой**
Можете да използвате каквото име искате, но типичната практика е да използвате общо описание на обекта или елемента, който се намира върху този слой. Този материал демонстрира как можете да промените името на слоя, използвайки Aspose.PSD за .NET. За целта е добавено ново свойство [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) в класа Layer, за да се покаже правилно име на слоя. Забелязано е, че когато Photoshop запазва име на слой с помощта на свойството [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), тогава корейските знаци се съхраняват като байт 63'?' в ASCII. Затова, ако искате да покажете името на слоя правилно, използвайте свойството **DisplayName**, защото свойството **Name** не поддържа корейски знаци.

Следният примерен код показва как можете да преименувате слой.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **Поддръжка на свързани слоеве**
Свързването на слоеве е като групиране на слоевете. Ако свържете два или повече слоя, ще може да направите определени промени по и двата свързани слоя. Например, ако приложите трансформации към един слой, те ще се приложат към всички останали свързани слоеве. Този материал демонстрира как можете да получите и отвържете свързаните слоеве, използвайки [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
