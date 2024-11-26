---
title: Применение медианного и Винеровского фильтров
type: docs
weight: 10
url: /ru/net/applying-median-and-wiener-filters/
---

## **Применение медианного и Винеровского фильтров**
Медианный фильтр является нелинейной цифровой техникой фильтрации, часто используемой для удаления шума. Такое уменьшение шума является типичным предварительным этапом обработки для улучшения результатов последующей обработки. Фильтр Винера является оптимальным линейным стационарным фильтром среднеквадратической ошибки (MSE) для изображений, подвергшихся действию аддитивного шума и размытия. С помощью Aspose.PSD для API .NET разработчики могут применять медианный фильтр для уменьшения шума и могут применять гауссов фильтр Винера к изображениям. В этой статье демонстрируется, как медианный фильтр и гауссов фильтр Винера могут быть применены к изображениям.

### **Применение медианного фильтра**
Aspose.PSD предоставляет класс [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) для применения фильтра к [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Приведенный ниже фрагмент кода демонстрирует, как применить медианный фильтр к растровому изображению.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}

### **Применение гауссового фильтра Винера**
Aspose.PSD предоставляет класс [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) для применения фильтра к [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Приведенный ниже фрагмент кода демонстрирует, как применить гауссов фильтр Винера к растровому изображению.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}

### **Применение гауссового фильтра Винера для цветного изображения**
Aspose.PSD также предоставляет [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)для цветных изображений. Приведенный ниже фрагмент кода демонстрирует, как применить гауссов фильтр Винера к цветному изображению.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}

### **Применение фильтра движущего гауссового фильтра Винера**
Aspose.PSD предоставляет класс [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) для применения фильтра к [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Приведенный ниже фрагмент кода демонстрирует, как применить фильтр движущего гауссового фильтра Винера к растровому изображению.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}

## **Применение коррекционного фильтра к изображению**
Эта статья демонстрирует применение Aspose.PSD для .NET для выполнения коррекционных фильтров на изображении. API Aspose.PSD предоставляет эффективные и простые в использовании методы для достижения этой цели. В Aspose.PSD для .NET предоставлены классы [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) и [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) для фильтрации. Класс BilateralSmoothingFilterOptions требует целое число в качестве размера. Шаги для выполнения изменений просты:

1. Загрузите изображение с использованием фабричного метода Load, открытого классом Image.
1. Преобразуйте изображение в RasterImage.
1. Создайте экземпляры классов BilateralSmoothingFilterOptions и SharpenFilterOptions.
1. Вызовите метод [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), указав прямоугольник в качестве границ изображения и экземпляр класса BilateralSmoothingFilterOptions.
1. Вызовите метод [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), указав прямоугольник в качестве границ изображения и экземпляр класса SharpenFilterOptions.
1. Настройте контраст.
1. Установите яркость.
1. Сохраните результат.

## **Использование алгоритма порога Брэдли**
Пороговая обработка изображения используется в графических приложениях. Цель пороговой обработки изображения - классифицировать пиксели как "темные" или "светлые". API Aspose.PSD позволяет использовать пороговую обработку по Брэдли при конвертации изображений. В следующем фрагменте кода показано, как определить пороговое значение, а затем вызвать алгоритм порога Брэдли.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
