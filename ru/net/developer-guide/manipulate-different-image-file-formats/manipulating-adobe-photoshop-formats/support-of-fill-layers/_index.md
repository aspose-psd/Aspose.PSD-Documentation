---
title: Поддержка слоев заливки
type: docs
weight: 90
url: /ru/net/support-of-fill-layers/
---


## **Слои заливки с заполнением узором**
Эта статья демонстрирует, как заполнить слой [PSD ](https://wiki.fileformat.com/image/psd/)заполнением узором. Узор* *- это изображение, цвет, тень или линия, используемые для заполнения области изображения. Пожалуйста, используйте FillLayer из Aspose.PSD.FileFormats.Psd.Layers, чтобы добавить узор в слой PSD. В следующем фрагменте кода загружается файл PSD, обращается к классу [Filllayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)и устанавливаются свойства PatternFillSettings для установки узора.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



Вот еще один пример, который демонстрирует, как [Aspose.PSD](https://products.aspose.com/psd/net) рендерит узор с использованием FillLayer и IPatternFillSettings.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Слои заливки градиентом**
Эта статья демонстрирует применение градиентного заливки для заполнения слоя PSD. В API Aspose.PSD предоставлены эффективные и простые в использовании методы для достижения этой цели. Aspose.PSD предоставляет классы GradientColorPoint и GradientTransparencyPoint для добавления градиентного эффекта в слой.

Шаги для заполнения слоя PSD градиентным заливкой просты:

- Загрузить файл PSD как изображение с использованием метода фабрики Load, предоставленного классом Image.
- Установить свойства настроек FillLayer объекта.
- Создать список ColorPoints с требуемыми цветами и позициями цвета.
- Создать список точек прозрачности с требуемой непрозрачностью и позицией точки прозрачности.
- Вызвать метод FillLayer.Update
- Сохранить результаты.

Нижеприведенный фрагмент кода показывает, как добавить градиентное заполнение слою PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Вот еще один пример, который использует свойство [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** для заполнения слоя PSD градиентным заливкой. Aspose.PSD поддерживает следующие типы градиента с помощью перечисления GradientType:

- **GradientType.Linear:** В линейном градиенте цвет переходит от начального до конечного в прямой линии.
- **GradientType.Radial:** В радиальном градиенте цвета веером расходятся от начальной точки по круговому шаблону.
- **GradientType.Angle:** Угловой градиент обходит против часовой стрелке вокруг начальной точки.
- **GradientType.Reflected:** В отраженном градиенте цвет зеркально отражается с обоих сторон начальной точки.
- **GradientType.Diamond:** Градиент в форме ромба создает ромбическую форму от начальной точки.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Поддержка свойства масштабирования для слоя градиентного заполнения**
Эта статья демонстрирует масштабирование FillLayer с градиентным заполнением с использованием Aspose.PSD для .NET. Для этого добавлено новое свойство **Scale** в **IGradientFillSettings**. 

Ниже приведен фрагмент кода, демонстрирующий использование свойства **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Слои заливки цветом**
Эта статья демонстрирует, как заполнить слой PSD цветом. Пожалуйста, используйте класс [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)для добавления цвета в слой PSD. В следующем фрагменте кода загружается файл PSD, обращается к классу Fill layer и устанавливает цвет с помощью свойства [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}


