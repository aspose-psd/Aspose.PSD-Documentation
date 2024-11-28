---
title: PSD Layer
type: docs
weight: 70
url: /bg/net/psd-layer/
---

## **Преглед**
Adobe® Photoshop® PSD Layer е един от най-добрите концепции в обработката на графика. Слоевете съдържат информация за пикселите и могат да имат различен брой канали.

Една от най-важните части на слоя в Photoshop Document е Ресурсите на слоята. Получавате пълен списък на поддържаните [Ресурси на слоя](/psd/bg/net/list-of-psd-layer-resources/) в PSD от нашата документация.

Можете да намерите потребителски интерфейс за манипулиране на слоята на следващия снимков екран:

![todo:image_alt_text](psd-layer_1.png)

Но Aspose.PSD се специализира в програмно манипулиране на PSD Layer чрез [C#](/psd/bg/net/home/) и [Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home).

Допълнителна документация може да бъде намерена в тази Статия: [Манипулиране на изображения](/psd/bg/net/manipulating-images-html/). Всички манипулации могат да бъдат обработени към PSD Преглед и слой, ще намерите повече информация в [Aspose.PSD Raster Image API Reference](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).

## **API за PSD Layer**
- Ефекти на слоя
- Общи свойства на слоевете
- Метаданни на слоя

## **Примери за Редактиране на слоя чрез C#**
### **Добавяне на нов слой**
Ако искате да добавите празен слой към отворения [PSD файл](/psd/bg/net/psd-file/), можете да използвате следния код.

Добавете нов слой към PSD файл чрез API

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}

### **Добавяне на нов слой от Jpeg, Png, Gif, Ai, Tiff, Bmp файлове**
Файлове от всякакви [поддържани формати](/psd/bg/net/supported-file-formats/) могат да бъдат добавени като нов слой към изображението ви. Но вие не можете да го заредите директно.

Можете да използвате долния код, за да добавите нов PSD слой от файла на всякакъв поддържан формат от потока

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

### **Обединяване на всички слоеве или групи слоеве**
Това може да бъде полезно, ако не искате да предоставяте на вашите потребители редактируем PSD файл. Също така, можете да идентифицирате чрез API дали файла е бил обединен.

Сгъване на слоевете на PSD файл:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}