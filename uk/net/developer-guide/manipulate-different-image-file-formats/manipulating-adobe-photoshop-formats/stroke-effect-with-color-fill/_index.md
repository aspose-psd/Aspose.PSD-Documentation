---
title: Ефект обведення з кольоровим заповненням
type: docs
weight: 60
url: /uk/net/stroke-effect-with-color-fill/
---

## **Ефект обведення з кольоровим заповненням**
Ця стаття демонструє, як рендерити ефект обведення з кольоровим заповненням. Ефект обведення використовується для додавання ліній контуру та рамок до шарів і форм. З його допомогою можна створювати лінії одного кольору, кольорові градієнти, а також орнаментовані рамки.

Кроки для рендерингу ефекту обведення з кольоровим заповненням наступні:

- Встановіть властивість [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource).
- Завантажте файл PSD як зображення, використовуючи фабричний метод Load, який використовується класом Image і визначіть [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions).
- Встановіть властивості налаштувань [**ColorFillSetting**.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)
- Збережіть результат.

У наступному фрагменті коду показано, як рендерити ефект обведення з кольоровим заповненням.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
