---
title: Робота з текстовими шарами
type: docs
weight: 170
url: /uk/net/working-with-text-layers/
---

## **Додавання текстового шару**
Aspose.PSD для .NET дозволяє додавати текстовий шар у файл PSD. Кроки для додавання текстового шару у файл PSD настільки прості, як наведено нижче:

- Завантажте файл PSD як зображення за допомогою методу фабрики [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index), викликнутого класом [Image](https://reference.aspose.com/psd/net/aspose.psd/image)
- Викличте метод [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer), який приймає текст та екземпляр класу [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- Збережіть результат

Наведений нижче фрагмент коду показує, як додати текстовий шар у файл PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **Встановлення позиції текстового шару**
Aspose.PSD для .NET дозволяє встановлювати позицію текстового шару в файлі PSD. Кроки для встановлення позиції текстового шару у файлі PSD настільки прості, як наведено нижче:

- Завантажте файл PSD як зображення за допомогою фабричного методу Load, викликаного класом Image
- Викличте метод AddTextLayer, вказавши ліву та верхню позиції текстового шару
- Збережіть результат

Наведений нижче фрагмент коду показує, як встановити позицію текстового шару в файлі PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **Отримання текстових властивостей з текстового шару**
За допомогою Aspose.PSD для .NET ви можете отримувати та оновлювати текстові властивості різних частин тексту, доступних у текстовому шарі PSD. У цій статті показано, як ви можете отримувати абзаци, стилі та текстові властивості текстового шару та оновлювати їх.

Наведений нижче фрагмент коду показує, як виконати це завдання.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}

Ось ще один приклад, який демонструє, як розробник може отримати форматування тексту різних частин тексту від [TextLayer](https://reference.aspose.com/net/psd/aspose.psd/fileformats/psd/layers/textlayer) за допомогою [Aspose.PSD для .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **Оновлення текстового шару у файлі PSD**
Aspose.PSD для .NET дозволяє маніпулювати текстом у текстовому шарі файлу PSD. Будь ласка, використовуйте клас Aspose.PSD.FileFormats.Psd.Layers.TextLayer для оновлення тексту в шарі PSD. Наведений нижче фрагмент коду завантажує файл PSD, отримує доступ до текстового шару, оновлює текст та зберігає файл PSD під новою назвою за допомогою методу [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer/methods/updatetext/index).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **Підтримка текстових шарів у режимі виконання**
У цій статті показано, як додавати текстові шари на льоту для зображень PSD. Наведений нижче фрагмент коду.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
