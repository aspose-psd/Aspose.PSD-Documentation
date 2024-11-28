---
title: Aspose.PSD для Python via .NET 24.3 - Примечания к выпуску
type: docs
weight: 10
url: /ru/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к [Aspose.PSD для Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**      | **Краткое содержание**                                                | **Категория**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [Формат AI] Сократить время загрузки больших многостраничных изображений AI | Улучшение |
| PSDPYTHON-45 | Файл PSD после конвертации с 8 бит на 16 бит стал неразборчивым      |     Ошибка     |
| PSDPYTHON-46 | Файл PSD после конвертации с 8 бит на 32 бит стал неразборчивым      |     Ошибка     |
| PSDPYTHON-47 | [Формат AI] Исправление отображения короткой кривой при файле AI     |     Ошибка     |



## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDPYTHON-42. [Формат AI] Сократить время загрузки больших многостраничных изображений AI**

{{< highlight python >}}
   # Нет образца
{{< /highlight >}}

**PSDPYTHON-45. Файл PSD после конвертации с 8 бит на 16 бит стал неразборчивым**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # всё нормально
                pass
            else:
                raise Exception("Неверный глобальный ресурс, первый ресурс должен быть Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Файл PSD после конвертации с 8 бит на 32 бит стал неразборчивым**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # всё нормально
                pass
            else:
                raise Exception("Неверный глобальный ресурс, первый ресурс должен быть Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Формат AI] Исправление отображения короткой кривой при файле AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
