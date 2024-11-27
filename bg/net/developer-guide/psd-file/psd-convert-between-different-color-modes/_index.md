---
title: PSD Конвертиране между различни цветови режими
type: docs
weight: 50
url: /bg/net/psd-convert-between-different-color-modes/
---

Можете да научите поддържаните цветови режими на Aspose.PSD от тази статия.

Aspose.PSD поддържа примерно конверсия от 8 на 16 бита на пиксел и обратно. CMYK ICC-профилни конверсии и други преобразувания от един вид битова дълбочина към друг вид. Тук можете да видите примери как да конвертирате към Градация на сиво в PSD файл.
## **Конвертиране от CMYK, RGB, Градация на сиво към Градация на сиво Цветови режим**
Предоставеният по-долу примерен код демонстрира как да направите конверсия от CMYK, RGB или Градация на сиво без Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **16-битово изображение от Photoshop в 8-битов режим на градация на сиво**
Но какво, ако се нуждаете от конверсия на 16-битово изображение на градация на сиво от Photoshop в 8-битов режим на градация на сиво? Трябва да използвате следния откъс код. 8 бита са обичайна битова дълбочина в PSD файлове.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **Конвертиране на Градация на сиво към RGB**
Другият комплексен случай е, ако трябва да конвертирате изображение Градация на сиво от PSD в изображение RGB.

Изображенията Градация на сиво имат само един канал, но изображенията RGB имат 3 канала: R - червен, G - зелен, B - син. Aspose.PSD може да конвертира Градация на сиво в RGB.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}