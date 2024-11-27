---
title: Stroke Ефект с Цветно Попълване
type: docs
weight: 60
url: /bg/net/stroke-effect-with-color-fill/
---

## **Stroke Ефект с Цветно Попълване**
Тази статия демонстрира как да рендирате stroke ефект с цветно попълване. Ефектът Stroke се използва за добавяне на обвивки и граници към слоеве и форми. Може да се използва за създаване на линии в цвят, цветни градиенти, както и шаблонирани граници.

Стъпките за рендиране на Stroke ефекта с Цветно попълване са толкова прости, колкото следните:

- Задайте свойството [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource).
- Заредете файл на PSD като изображение, използвайки фабричния метод Load, изложен от Image класа и дефинирайте [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions).
- Задайте настройките на свойствата на [**ColorFillSetting.**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)
- Запазете резултатите.

Следният откъс от код ви показва как да рендирате stroke ефект с цветно попълване.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
