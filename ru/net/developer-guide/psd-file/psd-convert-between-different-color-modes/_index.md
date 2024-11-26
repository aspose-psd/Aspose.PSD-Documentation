---
title: Конвертация PSD между различными цветовыми режимами
type: docs
weight: 50
url: /ru/net/psd-convert-between-different-color-modes/
---

Вы можете узнать поддерживаемые цветовые режимы Aspose.PSD из этой статьи.

Например, Aspose.PSD поддерживает конвертацию из 8 в 16 бит на пиксель и наоборот. Конвертация профиля CMYK ICC и другие преобразования из одной глубины бит в другую. Здесь вы можете увидеть примеры того, как конвертировать в оттенки серого в файле PSD.
## **Конвертация из CMYK, RGB, в оттенки серого в режим серого**
Ниже приведен пример кода, демонстрирующий, как выполнить конвертацию из CMYK, RGB или в оттенки серого без использования Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **Изображение Photoshop 16 бит в режим серого 8 бит**
Что, если вам нужно конвертировать изображение Photoshop 16 бит в режиме серого в режим серого 8 бит? Для этого вам понадобится использовать следующий фрагмент кода. 8 бит - это распространенная глубина бит в файлах PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **Конвертация из серого в RGB**
Другой сложный случай - это когда вам нужно конвертировать изображение PSD в градациях серого в изображение RGB.

У градаций серого есть только один канал, а у RGB изображения 3 канала: R - красный, G - зеленый, B - синий. Aspose.PSD может конвертировать градации серого в RGB.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
