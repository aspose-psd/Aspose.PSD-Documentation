---
title: Поддръжка на слоевете за пълнене
type: docs
weight: 50
url: /bg/java/support-of-fill-layers/
---

## **Поддръжка на слоевете за пълнене с цветово пълнене**
Тази статия демонстрира как да попълните PSD слой с цвят. Моля, използвайте FillLayer на Aspose.PSD.FileFormats.Psd.Layers.FillLayer, за да добавите цвят в PSD слоя. Следните откъси от код зареждат PSD файл, достъпват класа FillLayer и задават цвета, използвайки свойството FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Поддръжка на слоевете за пълнене с градиентно пълнене**
Тази статия демонстрира използването на градиентно пълнене за запълване на PSD слой. Aspose.PSD APIs са изложили ефективни и лесни за използване методи за постигане на тази цел. Aspose.PSD е изложил класовете GradientColorPoint и GradientTransparencyPoint, за да добавите градиентен ефект в слой.

Стъпките за попълване на PSD слой с градиентно пълнене са толкова прости, колкото посочено по-долу:

- Заредете PSD файл като изображение, използвайки фабричния метод Load, изложен от Image класа.
- Задайте настройките на FillLayer обекта.
- Създайте списък с ColorPoints с необходимите цветове и позиция на цвета.
- Създайте списък с transparencyPoints с необходимата прозрачност и позиция на точката за прозрачност.
- Извикайте метода FillLayer.Update
- Запазете резултатите.

Следният откъс от код ви показва как да добавите градиентно пълнене, за да запълните PSD слоя.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Ефект на контур с цветово пълнене**
Тази статия демонстрира как да визуализирате ефект на контур с цветово пълнене. Ефектът Stroke се използва за добавяне на контури и граници към слоевете и формите. Той може да се използва за създаване на линии в цвят, цветни градиенти, както и узорни граници.

Стъпките за визуализиране на ефект на контур с цветово пълнене са толкова прости, колкото посочено по-долу:

- Задайте свойството **LoadEffectsResource**.
- Заредете PSD файл като изображение, използвайки фабричния метод Load, изложен от Image класа и дефинирайте **PsdLoadOptions**.
- Задайте настройките на **ColorFillSetting.**
- Запазете резултатите.

Следният откъс от код ви показва как да визуализирате ефекта на контур с цветово пълнене.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}


