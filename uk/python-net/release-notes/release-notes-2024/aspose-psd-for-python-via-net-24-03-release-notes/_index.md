---
title: Оновлення Aspose.PSD для Python via .NET 24.3
type: документація
weight: 10
url: /uk/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}
Ця сторінка містить оновлення для [Aspose.PSD для Python via .NET 24.3](https://pypi.org/project/aspose-psd/)
{{% /alert %}}

| **Ключ**      | **Зведення**                                                          | **Категорія**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [Формат AI] Зменшити час завантаження великих багатосторінкових зображень AI         | Покращення |
| PSDPYTHON-45 | Файл PSD після конвертації з 8 біт в 16 біт став незчитуваним |     Помилка     |
| PSDPYTHON-46 | Файл PSD після конвертації з 8 біт в 32 біт став незчитуваним |     Помилка     |
| PSDPYTHON-47 | [Формат AI] Виправлено відображення короткої кривої в файлі AI                 |     Помилка     |



## **Зміни в публічному API**
# **Додані API:**
- Немає

# **Вилучені API:**
- Немає


## **Приклади використання:**

**PSDPYTHON-42. [Формат AI] Зменшення часу завантаження великих багатосторінкових зображень AI**

{{< highlight python >}}
   # Немає прикладу
{{< /highlight >}}

**PSDPYTHON-45. Файл PSD після конвертації з 8 біт в 16 біт став незчитуваним**

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
                # все гаразд
                pass
            else:
                raise Exception("Неправильний глобальний ресурс, перший ресурс повинен бути Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Файл PSD після конвертації з 8 біт в 32 біт став незчитуваним**

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
                # все гаразд
                pass
            else:
                raise Exception("Неправильний глобальний ресурс, перший ресурс повинен бути Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Формат AI] Виправлено відображення короткої кривої в файлі AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
