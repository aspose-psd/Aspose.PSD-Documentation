---
title: Aspose.PSD за Python via .NET 24.3 - Бележки за изданието
type: docs
weight: 10
url: /bg/net/aspose-psd-za-python-chrez-net-24-3-belezhki-za-izdaniyeto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**      | **Резюме**                                                          | **Категория** |
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [Формат AI] Намалено време за зареждане на големи многостранични изображения AI | Подобрение |
| PSDPYTHON-45 | PSD файл след конвертирането от 8 бита на 16 бита стана неразличим |     Проблем     |
| PSDPYTHON-46 | PSD файл след конвертирането от 8 бита на 32 бита стана неразличим |     Проблем     |
| PSDPYTHON-47 | [Формат AI] Оправяне на извеждането на къса крива във файл AI |     Проблем     |



## **Промени в общественото API**
# **Добавени API:**
- Нито едно

# **Премахнати API:**
- Нито едно


## **Примери за използване:**

**PSDPYTHON-42. [Формат AI] Намалено време за зареждане на големи многостранични изображения AI**

{{< highlight python >}}
   # Няма пример
{{< /highlight >}}

**PSDPYTHON-45. PSD файл след конвертирането от 8 бита на 16 бита стана неразличим**

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
                # is ok
                pass
            else:
                raise Exception("Грешна глобална ресурс, първият ресурс трябва да бъде Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. PSD файл след конвертирането от 8 бита на 32 бита стана неразличим**

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
                # is ok
                pass
            else:
                raise Exception("Грешна глобална ресурс, първият ресурс трябва да бъде Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Формат AI] Оправяне на извеждането на къса крива във файл AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
