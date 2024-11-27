---
title: Поддръжка на пълните слоеве
type: docs
weight: 90
url: /bg/net/support-of-fill-layers/
---


## **Пълните слоеве с шаблон за пълнене**
Тази статия демонстрира как да попълните слоя [PSD](https://wiki.fileformat.com/image/psd/)с шаблон за попълване. Шаблон е изображение, цвят, сянка или линия, които се използват за попълване на определена област от изображението. Моля, използвайте Aspose.PSD.FileFormats.Psd.Layers.FillLayer, за да добавите шаблон в слоя на PSD. Следните откъси от код зареждат PSD файл, достъпват класа [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) и задават шаблона, използвайки свойствата на [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



Ето още един пример, който демонстрира как [Aspose.PSD](https://products.aspose.com/psd/net) визуализира шаблона, като използва [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) и [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Пълните слоеве с пълнене с градиент**
Тази статия демонстрира използването на градиентно попълване, за да се запълни слоя в PSD. Aspose.PSD APIs предлагат ефективни и лесни за използване методи за постигане на тази цел. Aspose.PSD е изложил класовете [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) и [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) за добавяне на градиентен ефект в слой.

`Стъпките за попълване [на PSD](https://wiki.fileformat.com/image/psd/)слоя с градиентно попълване са толкова прости, колкото следните:

- Заредете PSD файл като изображение, използвайки фабричния метод [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index), изложен от класа [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Задайте настройките за свойствата на [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) обект.
- Създайте списък с [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) с желаните цветове и позиции на цветовете.
- Създайте списък с точки за прозрачност с необходимата прозрачност и позиция на точката за прозрачност.
- Извикайте метода [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update)
- Запазете резултатите.



Следният откъс от код ви показва как да добавите градиентно попълване в слоя на PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Ето още един пример, който използва свойството [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** за попълване на слоя на PSD с градиентно покритие. Aspose.PSD поддържа следните видове градиент чрез енумерацията GradientType:

- **GradientType.Linear:** В линеен градиент цветът преминава от начален оттенък към края по права линия.
- **GradientType.Radial:** В радиален градиент цветовете се разходжат от началната точка в кръгов манер.
- **GradientType.Angle:** В ъгловия градиент преходът на цвета става по часовниковата стрелка около началната точка.
- **GradientType.Reflected:** В отражения градиент цветовете се отразяват от двете страни на началната точка.
- **GradientType.Diamond:** Градиентът във форма на диамант създава диамантена форма от началната точка.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Поддръжка на собствеността Scale за слой с градиентно попълване**
Тази статия показва как да мащабирате FillLayer с градиентно покритие, използвайки Aspose.PSD за .NET. За тази цел е добавено ново свойство [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) в [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings).

Долу има кодова демонстрация, която показва как да използвате свойството **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Пълните слоеве с цветово покритие**
Тази статия демонстрира как да попълните слоя [PSD](https://wiki.fileformat.com/image/psd/) с цвят. Моля, използвайте класа [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) за добавяне на цвят в слоя на PSD. Следният откъс от код зарежда PSD файл, достъпва класа за попълване и задава цвета, използвайки свойството [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}


