---
title: Примітки до версії Aspose.PSD для Java 23.12
type: docs
weight: 40
url: /uk/java/aspose-psd-dlya-java-23-12-primіtki-vidpusku/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до версії [Aspose.PSD для Java 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) {{% /alert %}}

| **Ключ**    | **Зміст**                                                                                         | **Категорія** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-565 | [Формат AI] Додана підтримка рендерингу растрових зображень у новій версії AI.                      | Функція      |
| PSDJAVA-566 | Обробка шуму типу градієнта в GdflResrource.                                                      | Функція      |
| PSDJAVA-567 | Помилка "Звернення до об'єкту не встановлено на екземпляр об'єкта" при збереженні шару тексту після оновлення. | Помилка       |
| PSDJAVA-568 | Виправити ручне завантаження шрифтів на MacOS за допомогою System.Drawing.Common та Aspose.Drawing. | Помилка       |
| PSDJAVA-569 | Параметр AllowWarpRepaint в PsdLoadOptions викликає виняток.                                      | Помилка       |
| PSDJAVA-570 | [Формат AI] Реалізуйте обробку потоків перехресного посилання.                                      | Покращення   |
| PSDJAVA-571 | Керування ліцензією для VectorPathDataResource працює некоректно.                                   | Покращення   |
| PSDJAVA-574 | Відкрити будь-який файл зображення як вбудований розумний об'єкт у зображенні PSD.                  | Покращення   |

## **Зміни в публічному API**
# **Додані API:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setColorModel(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setGradientMode(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setUseVectorColor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.#ctor(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource
…

# **Видалені API:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
  M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getHorizontalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getReverse 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getScale 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getVerticalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setVerticalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColorPoints 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientName 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getTransparencyPoints 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColorPoints(com.aspose.psd.fileformats.psd.layers.IGradientColorPoint[])
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setTransparencyPoints(com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint[])
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

## **Приклади використання:**

**PSDJAVA-565. [Формат AI] Додана підтримка рендерингу растрового зображення у новій версії AI**

{{< highlight java >}}
…
{{< /highlight >}}

**PSDJAVA-566. Обробка шуму типу градієнта в GdflResrource**

{{< highlight java >}}
…
{{< /highlight >}}

**PSDJAVA-567. Помилка "Звернення до об'єкта не встановлено на екземпляр об'єкта." при збереженні текстового шару після оновлення**

{{< highlight java >}}
…
{{< /highlight >}}

**PSDJAVA-569. Параметр AllowWarpRepaint в PsdLoadOptions викликає виняток**

{{< highlight java >}}
…
{{< /highlight >}}

**PSDJAVA-571. Керування ліцензією для VectorPathDataResource працює некоректно**

{{< highlight java >}}
…
{{< /highlight >}}

**PSDJAVA-574. Відкрити будь-який файл зображення як вбудований розумний об’єкт у зображенні PSD**

{{< highlight java >}}
…
{{< /highlight >}}