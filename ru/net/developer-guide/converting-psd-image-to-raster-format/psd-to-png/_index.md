---
title: Преобразование PSD в PNG с использованием C#
linktitle: PSD в PNG
type: docs
weight: 30
url: /ru/net/psd-to-png/
description: API для работы с форматом PSD и манипуляций с изображениями в Photoshop на C# .NET может конвертировать из формата PSD в формат PNG с помощью предоставленного в этой статье кода.
---

Aspose.PSD - это SDK для формата PSD и API для манипуляций с изображениями в Photoshop на C# .NET, которые позволяют конвертировать из формата PSD в формат PNG.

Для этого преобразования PSD в PNG следует использовать следующий код на C#:

Ниже предоставленный образец кода демонстрирует, как конвертировать PSD в PNG:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ConvertPsdToPng-ConvertPsdToPng.cs" >}}

Вы можете указать уровень сжатия формата PNG от 0 до 9, где 9 - самый высокий уровень сжатия. Вы можете использовать прогрессивное сжатие PNG и изменить тип цвета файла PNG. [Параметры PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions) имеют различные свойства для любых случаев экспорта PSD.

Использование полупрозрачного PNG с альфа-каналом для вашего сайта или работы - хорошее решение. Файл Adobe Photoshop может быть экспортирован без ошибок с [режимом "только для чтения"](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/readonlymode).

Ниже приведен пример экспортированного файла PSD с [Примененной маской](https://docs.aspose.com/display/psdjava/Apply+Masking), [Слоем с текстом](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) и прозрачным [Слоем заливки цветом](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.filllayers/filllayer) (Aspose.PSD поддерживает все типы [Слоев заливки Adobe Photoshop](https://docs.aspose.com/display/psdjava/Support+of+Fill+Layers)). Также можно увидеть [эффект тени](/ru/net/shadow-effects-in-psd-file/) на Слое формы PSD.

![todo:image_alt_text](psd-to-png_1.png)
