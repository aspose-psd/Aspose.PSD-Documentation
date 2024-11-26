---
title: PSD Слой
type: docs
weight: 70
url: /ru/net/psd-layer/
---

## **Обзор**
Слой PSD в Adobe® Photoshop® является одним из лучших концепций в обработке графики. Слои содержат информацию о пикселях, могут иметь разное количество каналов.

Одной из наиболее важных частей слоя в документе Photoshop являются Ресурсы слоя. Полный список поддерживаемых [Ресурсов слоя](/ru/psd/net/list-of-psd-layer-resources/) в PSD можно получить из нашей документации.

Вы можете найти пользовательский интерфейс для управления слоем на следующем снимке экрана:

![todo:image_alt_text](psd-layer_1.png)

Но Aspose.PSD специализируется на программном управлении слоем PSD с помощью [C# ](/ru/psd/net/home/)и [Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home).

Дополнительную документацию можно найти в этой статье: [Редактирование изображений](/ru/psd/net/manipulating-images-html/). Вся обработка может быть выполнена с предварительным просмотром PSD и слоем, подробнее об этом можно узнать в [Справочнике по API растрового изображения Aspose.PSD](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
## **Доступные методы API PSD Слоя**
- Эффекты слоя
- Общие свойства слоев
- Метаданные слоя
## **Примеры редактирования слоя с помощью C#**
### **Добавление нового слоя**
Если вы хотите добавить пустой слой к открытому [файлу PSD](/ru/psd/net/psd-file/), вы можете использовать следующий код.

Добавление нового слоя в файл PSD с помощью API

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}
### **Добавление нового слоя из файлов Jpeg, Png, Gif, Ai, Tiff, Bmp**
Файлы любых [поддерживаемых форматов ](/ru/psd/net/supported-file-formats/)могут быть добавлены в качестве нового слоя к вашему изображению. Но вы не можете загрузить их напрямую.

Вы можете использовать код ниже, чтобы добавить новый слой PSD из файла любого поддерживаемого формата из потока.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
### **Сведение всех слоев или групп слоев**
Это может быть полезно, если вы не хотите предоставлять редактируемый файл PSD вашим пользователям. Также, вы можете идентифицировать через API, был ли файл сведен в один слой.

Сведение слоев файла PSD:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}
