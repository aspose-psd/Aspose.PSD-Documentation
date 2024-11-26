---
title: Работа с текстовыми слоями
type: docs
weight: 170
url: /ru/net/working-with-text-layers/
---

## **Добавление текстового слоя**
Aspose.PSD для .NET позволяет добавлять текстовый слой в файл PSD. Шаги для добавления текстового слоя в файл PSD такие же простые, как указано ниже:

- Загрузите файл PSD как изображение с помощью метода фабрики [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index), предоставленного классом [Image](https://reference.aspose.com/psd/net/aspose.psd/image)
- Вызовите метод [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer), который принимает текст и экземпляр класса [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- Сохраните результат

В следующем фрагменте кода показано, как добавить текстовый слой в файл PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **Установка позиции текстового слоя**
Aspose.PSD для .NET позволяет устанавливать позицию текстового слоя в файле PSD. Шаги для установки позиции текстового слоя в файле PSD такие же простые, как указано ниже:

- Загрузите файл PSD как изображение с помощью метода фабрики Load, предоставленного классом Image
- Вызовите метод AddTextLayer, указав левую и верхнюю позиции текстового слоя
- Сохраните результат

В следующем фрагменте кода показано, как установить позицию текстового слоя в файле PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **Получение свойств текста из текстового слоя**
С помощью Aspose.PSD для .NET вы можете получать и обновлять свойства текста различных частей текста, доступных в текстовом слое PSD. В этой статье демонстрируется, как получить абзацы, стили и свойства текста текстового слоя и обновить их.

Нижеприведенный фрагмент кода показывает, как это можно сделать.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}

Вот еще один пример, который демонстрирует, как разработчик может получить форматирование текста различных частей текста из [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer), используя [Aspose.PSD для .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **Обновление текстового слоя в файле PSD**
Aspose.PSD для .NET позволяет манипулировать текстом в текстовом слое файла PSD. Используйте класс Aspose.PSD.FileFormats.Psd.Layers.TextLayer для обновления текста в слое PSD. В следующем фрагменте кода загружается файл PSD, получает доступ к текстовому слою, обновляет текст и сохраняет файл PSD с новым именем с помощью метода [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **Поддержка текстовых слоев при выполнении**
В этой статье показано, как добавить текстовые слои во время выполнения для изображений PSD. Ниже приведен фрагмент кода.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
