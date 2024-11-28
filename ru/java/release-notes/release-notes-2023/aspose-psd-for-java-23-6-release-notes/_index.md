---
title: Релизные заметки Aspose.PSD для Java 23.6
type: документация
weight: 40
url: /ru/java/aspose-psd-for-java-23-6-release-notes/
---

{{% alert color="primary" %}} Эта страница содержит релизные заметки для [Aspose.PSD для Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **Ключ**    | **Содержание**                                                                                                                                   | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | Рефакторинг API временных маркеров                                                                                                                | Улучшение    |
| PSDJAVA-480 | Удаление артефактов при отрисовке искривления                                                                                                     | Улучшение    |
| PSDJAVA-481 | Оптимизация отрисовки искривления                                                                                                                | Улучшение    |
| PSDJAVA-482 | Поддержка слоя настройки порога                                                                                                                  | Функция       |
| PSDJAVA-483 | Поддержка слоя селективной цветовой настройки                                                                                                    | Функция       |
| PSDJAVA-484 | Возможность экспорта временной шкалы PSD в анимированный GIF файл                                                                                 | Функция       |
| PSDJAVA-485 | Добавлена поддержка TextLayer без прямоугольных границ                                                                                            | Функция       |
| PSDJAVA-486 | Поддержка ShapeLayer                                                                                                                            | Функция       |
| PSDJAVA-487 | Замена изображения в умном объекте не обновляется                                                                                                | Ошибка       |
| PSDJAVA-488 | Файл PSD не может быть сохранен как PSD с ошибкой: цветовые режимы Rgb и Lab не могут содержать менее 3 каналов и более 4 каналов              | Ошибка       |
| PSDJAVA-489 | Выравнивание текста теряется при открытии TextLayer в режиме редактирования Photoshop                                                              | Ошибка       |
| PSDJAVA-490 | Исключение пустой ссылки при сохранении файла PSD                                                                                                | Ошибка       |
| PSDJAVA-491 | Исключение при загрузке ShapeLayer: Точки для оригинальных границ вектора пока не поддерживаются                                                  | Ошибка       |
| PSDJAVA-492 | Исключение при загрузке VogkResource: Точки сохранены как DoubleStructures, мы читаем как UnitStructures                                          | Ошибка       |
| PSDJAVA-493 | Тип слоя ShapeLayer пуст                                                                                                                          | Ошибка       |

## **Изменения в общедоступном API**
# **Добавленные API:**
- M:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
...

Полный текст вы можете найти в [исходном документе](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/)## **Примеры использования:**

**PSDJAVA-482. Поддержка слоя настройки порога**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-483. Поддержка слоя селективной цветовой настройки**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-484. Возможность экспорта временной шкалы PSD в анимированный GIF файл**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-487. Замена изображения в умном объекте не обновляется**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-479. Рефакторинг API временных маркеров**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-488. Файл PSD не может быть сохранен как PSD с ошибкой: цветовые режимы Rgb и Lab не могут содержать менее 3 каналов и более 4 каналов**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-480. Удаление артефактов при отрисовке искривления**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-481. Оптимизация отрисовки искривления**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-489. Выравнивание текста теряется при открытии TextLayer в режиме редактирования Photoshop**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-485. Добавлена поддержка TextLayer без прямоугольных границ**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-491. Исключение при загрузке ShapeLayer: Точки для оригинальных границ вектора пока не поддерживаются**

**PSDJAVA-492. Исключение при загрузке VogkResource: Точки сохранены как DoubleStructures, мы читаем как UnitStructures**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-493. Тип слоя ShapeLayer пуст**

{{< highlight java >}}
...
{{< /highlight >}}