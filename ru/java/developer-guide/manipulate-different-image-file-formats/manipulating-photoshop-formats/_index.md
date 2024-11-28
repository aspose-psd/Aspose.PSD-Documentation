---
title: Работа с форматами Photoshop
type: документация
weight: 10
url: /ru/java/manipulating-photoshop-formats/
---

## **Замена цвета в слоях PSD**
Aspose.PSD для Java позволяет изменять фоновый цвет каждого слоя файла PSD. Используйте класс Aspose.PSD.FileFormats.Psd.Layers.BackgroundColor для изменения фонового цвета слоя в PSD слое. В следующем кодовом отрывке загружается файл PSD, обращается к слою, обновляется цвет фона и сохраняется файл PSD.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.java" >}}
## **Обновление текстового слоя в файле PSD**
Aspose.PSD для Java позволяет манипулировать текстом в текстовом слое файла PSD. Используйте класс Aspose.PSD.FileFormats.Psd.Layers.TextLayer для обновления текста в слое PSD. В следующем кодовом отрывке загружается файл PSD, обращается к текстовому слою, обновляется текст и сохраняется файл PSD с новым именем, используя метод Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.java" >}}
## **Обнаружение смещенного PSD**
Aspose.PSD для Java позволяет определить, является ли данный файл PSD смещенным или нет. Свойство IsFlatten было введено в классе Aspose.PSD.FileFormats.Psd.PsdImage для достижения этой функциональности. В следующем кодовом отрывке загружается файл PSD и обращается к свойству IsFlatten.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.java" >}}
## **Слияние слоев PSD**
В этой статье показано, как объединить слои в файле PSD при преобразовании файла PSD в JPG с помощью Aspose.PSD. В приведенном ниже примере существующий файл PSD загружается путем передачи пути к файлу в статический метод Load класса Image. После загрузки преобразуйте/приведите изображение к PsdImage. Создайте экземпляр класса JpegOptions и установите его различные свойства. Теперь вызовите метод Save экземпляра PsdImage. В следующем кодовом отрывке показано, как объединить слои PSD.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-MergePSDLayers-MergePSDLayers.java" >}}
## **Поддержка оттенков серого с альфа-каналом для PSD**
В этой статье показано, как поддерживать оттенки серого с альфа-каналом для файла PSD при преобразовании файла PSD в PNG с помощью Aspose.PSD. В приведенном ниже примере существующий файл PSD загружается путем передачи пути к файлу в статический метод Load класса Image. После загрузки преобразуйте/приведите изображение к PsdImage. Создайте экземпляр класса PngOptions и установите его различные свойства. Установите свойство ColorType на TruecolorWithAlpha. Теперь вызовите метод Save экземпляра PngOptions. В следующем кодовом отрывке показано, как конвертировать в оттенки серого PNG с альфа-каналом.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.java" >}}
## **Поддержка эффектов слоя для PSD**
В этой статье показано, как поддерживать различные эффекты, такие как **Размытие**, **Внутренняя** **свечка**, **Внешняя свечка** для слоя PSD. В следующем кодовом отрывке показано, как поддерживать эффекты слоя.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.java" >}}
## **Поддержка даты и времени создания слоя**
В этой статье показано, как поддерживать дату и время создания слоя для слоя PSD. В следующем кодовом отрывке показано, как создавать слои.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LayerCreationDateTime-LayerCreationDateTime.java" >}}
## **Поддержка выделения цветом листа**
В этой статье показано, как загружать изображения PSD, изменять и выделять цвета листа и сохранять их в качестве изображения. Приведен фрагмент кода.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-SheetColorHighlighting-SheetColorHighlighting.java" >}}
## **Поддержка текстовых слоев на этапе выполнения**
В этой статье показано, как добавлять текстовые слои на этапе выполнения для изображений PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.java" >}}
## **Поддержка слоев настройки**
В этой статье показано, как настраивать слои и затем, если слой пустой, сливать слои и сохранять как изображения PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-SupportOfAdjusmentLayers-SupportOfAdjusmentLayers.java" >}}
## **Управление яркостью и контрастом в слоях настройки**
В этой статье показано, как перебирать слои и управлять яркостью и контрастом в слоях, а затем сохранять как изображения PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ManageBrightnessContrastAdjustmentLayer-ManageBrightnessContrastAdjustmentLayer.java" >}}
## **Управление слоями экспозиции**
В этой статье показано, как добавлять и редактировать слои экспозиции и управлять ими, а затем сохранять как изображения PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ManageExposureAdjustmentLayer-ManageExposureAdjustmentLayer.java" >}}
## **Управление слоями смешивания каналов**
В этой статье показано, как управлять слоями настройки и устанавливать разные цвета, а затем сохранять как изображения PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ManageChannelMixerAdjusmentLayer-ManageChannelMixerAdjusmentLayer.java" >}}
## **Слияние слоев PSD c другими слоями**
В этой статье показано, как объединить слои в другие слои в файле PSD с помощью Aspose.PSD. В приведенном ниже примере существующий файл PSD загружается путем передачи пути к файлу в статический метод Load класса Image. Теперь вызовите метод Save экземпляра PsdImage. Приведен фрагмент кода, показывающий, как объединить слои PSD.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-MergeOnePSDlayerToOther-MergeOnePSDlayerToOther.java" >}}
## **Поддержка рамки текста**
В этой статье показано, как поддерживать рамку текста в файле PSD с помощью Aspose.PSD. В приведенном ниже примере существующий файл PSD загружается путем передачи пути к файлу в статический метод Load класса Image. TextBoundBox - это максимальный размер слоя для текстового слоя. Теперь вызовите метод Save экземпляра PsdImage. Приведен фрагмент кода, показывающий, как объединить слои PSD.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-TextLayerBoundBox-TextLayerBoundBox.java" >}}
## **Поддержка ресурсов IOPA**
В этой статье показано, как поддерживать ресурс IOPA в файле PSD с помощью Aspose.PSD. Приведен фрагмент кода, показывающий, как поддерживать IOPA в слоях PSD.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddIopaResource-AddIopaResource.java" >}}
## **Управление непрозрачностью слоев**
В этой статье показано, как управлять непрозрачностью слоев в файле PSD с помощью Aspose.PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-FillOpacityOfLayers-FillOpacityOfLayers.java" >}}
## **Отрисовка слоев коррекции кривых**
В этой статье показано, как отрисовывать коррекцию кривых слоев в файле PSD и рендерить их в PNG с помощью Aspose.PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-RenderingOfCurvesAdjustmentLayer-RenderingOfCurvesAdjustmentLayer.java" >}}
## **Добавление слоев коррекции кривых**
В этой статье показано, как добавлять слои коррекции кривых в файл PSD с помощью Aspose.PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddCurvesAdjustmentLayer-AddCurvesAdjustmentLayer.java" >}}
## **Управление слоем коррекции фильтра фотографии**
В этой статье показано, как итерироваться через каждый слой фотофильтра и добавлять, редактировать и сохранять их как файл PSD с помощью Aspose.PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ManagePhotoFilterAdjustmentLayer-ManagePhotoFilterAdjustmentLayer.java" >}}
## **Поддержка слияния слоев**
Эта статья показывает, как объединить весь файл PSD и сливать один слой в другой, сохраняя их как файл PSD с помощью Aspose.PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.java" >}}
## **Добавление и рендеринг слоев уровня**
В этой статье показано, как итерироваться через каждый слой уровня и устанавливать различные уровни, а затем сохранять их как файл PSD и PNG с помощью Aspose.PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-RenderingOfLevelAdjustmentLayer-RenderingOfLevelAdjustmentLayer.java" >}}
## **Добавление слоя коррекции оттенка**
Эта статья показывает, как итерироваться через каждый слой оттенка и задавать различные диапазоны и цвета, а затем сохранять их как файл PSD с помощью Aspose.PSD. Приведен фрагмент кода ниже.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddHueSaturationAdjustmentLayer-AddHueSaturationAdjustmentLayer.java" >}}
## **Добавление слоя коррекции уровней**
Эта статья показывает, как итерироваться через каждый слой уровня и устанавлив