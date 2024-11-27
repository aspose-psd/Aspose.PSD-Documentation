---
title: Работа с текстови слоеве
type: docs
weight: 170
url: /bg/net/working-with-text-layers/
---

## **Добавяне на текстов слой**
Aspose.PSD за .NET позволява да добавите текстов слой в PSD файл. Стъпките за добавяне на текстов слой в PSD файл са толкова прости, както по-долу:

- Заредете PSD файл като изображение, използвайки фабричния метод [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index), предоставен от класа [Image](https://reference.aspose.com/psd/net/aspose.psd/image)
- Извикайте метода [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/methods/addtextlayer), който приема текст и екземпляр на класа [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- Запазете резултатите

Следният откъс код ви показва как да добавите текстов слой в PSD файл

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **Задаване на позиция на текстов слой**
Aspose.PSD за .NET ви позволява да зададете позиция на текстов слой в PSD файл. Стъпките за задаване на позиция на текстов слой в PSD файл са толкова прости, както по-долу:

- Заредете PSD файл като изображение, използвайки фабричния метод Load, предоставен от класа Image
- Извикайте метода AddTextLayer, като посочите лява и горна позиция на текстовия слой
- Запазете резултатите

Следният откъс код ви показва как да зададете позиция на текстов слой в PSD файл

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **Вземане на текстови свойства от текстов слой**
С помощта на Aspose.PSD за .NET можете да вземете и актуализирате текстовите свойства на различни части от текста, налични в текстовия слой на PSD. Този статия демонстрира как можете да вземете параграфи, стилове и текстови свойства на текстовия слой и да ги актуализирате.

Откъсът от кода по-долу показва как да постигнете това изискване.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}

Ето още един пример, който демонстрира как разработчик може да получи форматирането на текста от различни части на текста от [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer), използвайки [Aspose.PSD за .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **Актуализиране на текстов слой в PSD файл**
Aspose.PSD за .NET ви позволява да манипулирате текста в текстовия слой на PSD файл. Моля, използвайте класа Aspose.PSD.FileFormats.Psd.Layers.TextLayer, за да актуализирате текста в слоя на PSD. Следният откъс код зарежда PSD файл, има достъп до текстовия слой, актуализира текста и запазва PSD файла с ново име, използвайки метода [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **Поддръжка на текстови слоеве по време на изпълнение**
Тази статия показва как да добавите текстови слоеве по време на изпълнение за PSD изображения. Предоставен е откъс код по-долу.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
