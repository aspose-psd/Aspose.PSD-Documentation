---
title: Підтримка шарів заповнення
type: docs
weight: 90
url: /uk/net/support-of-fill-layers/
---

## **Шари заповнення за допомогою заповнення за шаблоном**
Ця стаття демонструє, як заповнити шар [PSD](https://wiki.fileformat.com/image/psd/) за допомогою заповнення за шаблоном. Шаблон* *це зображення, колір, тінь або лінія, які використовуються для заповнення певної області зображення. Будь ласка, використовуйте клас Aspose.PSD.FileFormats.Psd.Layers.FillLayer, щоб додати шаблон в шар PSD. Наведені нижче уривки коду завантажують файл PSD, отримують доступ до класу [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) та встановлюють шаблон, використовуючи властивості [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}

Ось ще один приклад, який демонструє, як [Aspose.PSD](https://products.aspose.com/psd/net) відтворює шаблон шляхом використання [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) та [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}

## **Заповнення шарів градієнтним заповненням**
Ця стаття демонструє використання градієнтного заповнення для заповнення шара PSD. API Aspose.PSD надає надійні та прості використання методи для досягнення цієї мети. Aspose.PSD використовує класи [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) та [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint), щоб додати градієнтний ефект на шар.

`Кроки для заповнення шару PSD градієнтним заповненням настільки прості:

- Завантажте файл PSD як зображення за допомогою фабричного методу [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index), використовуючи експонований клас [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Встановіть параметри налаштувань об'єкта [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Створіть список [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) із потрібними кольорами та позиціями кольору.
- Створіть список точок прозорості з вказаною прозорістю та позицією точки прозорості.
- Викличте метод [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Збережіть результат.

Наведений нижче уривок коду показує, як додати градієнтне заповнення для шару PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}

**Ось ще один приклад, який використовує властивість [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** для заповнення шару PSD градієнтним заповненням. Aspose.PSD підтримує наступні типи градієнту через перелік GradientType:

- **Linear:**       У лінійному градієнті колір переходить від початкового відтінку до кінця по прямій лінії.
- **Radial:**       У радіальному градієнті кольори розходяться від початкової точки у кільцевому візерунку.
- **Angle:**        У градієнті під кутом кольори обертаються за годинниковою стрілкою навколо початкової точки.
- **Reflected:** У віддзеркаленому градієнті колір відображається на обох сторонах від початкової точки.
- **Diamond:**   Алмазний градієнт створює форму алмазу від початкової точки.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

## **Підтримка властивості масштабу для шару градієнтного заповнення**
Ця стаття демонструє, як масштабувати FillLayer з градієнтним заповненням за допомогою Aspose.PSD для .NET. Для цього було додано нову властивість [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) у [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings).

Нижче наведено демонстраційний код, який показує, як використовувати властивість **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}

## **Заповнення шарів колірним заповненням**
Ця стаття демонструє, як заповнити шар [PSD](https://wiki.fileformat.com/image/psd/) колірним заповненням. Будь ласка, використовуйте клас [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer), щоб додати колір в шар PSD. Наведений нижче уривок коду завантажує файл PSD, отримує доступ до класу Fill layer та встановлює колір, використовуючи властивість [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}
