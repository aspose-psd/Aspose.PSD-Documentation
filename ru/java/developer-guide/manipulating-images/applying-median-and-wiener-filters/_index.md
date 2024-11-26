---
title: Применение медианного и Винеровского фильтров
type: docs
weight: 10
url: /ru/java/применение-медианного-и-винеровского-фильтров/
---

## **Применение медианного и Винеровского фильтров**
Медианный фильтр - это нелинейная цифровая фильтрационная техника, часто используемая для удаления шума. Такое уменьшение шума является типичным предварительным этапом обработки для улучшения результатов последующей обработки. Фильтр Винера - это оптимальный линейный стационарный фильтр среднеквадратичной ошибки (MSE) для изображений, загрязненных аддитивным шумом и размытием. С помощью Aspose.PSD для Java API разработчики могут применить медианный фильтр для удаления шума с изображения и применить фильтр Гаусса Винера к изображениям. В этой статье показано, как можно применить медианный фильтр и фильтр Гаусса Винера к изображениям.
### **Применение медианного фильтра**
Aspose.PSD предоставляет класс MedianFilterOptions для применения фильтра к RasterImage. Приведенный ниже фрагмент кода демонстрирует, как применить медианный фильтр к растровому изображению.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Применение фильтра Гаусса Винера**
Aspose.PSD предоставляет класс GaussWienerFilterOptions для применения фильтра к RasterImage. Приведенный ниже фрагмент кода демонстрирует, как применить фильтр Гаусса Винера к растровому изображению.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Применение фильтра Гаусса Винера для цветного изображения**
Aspose.PSD также предоставляет класс GaussWienerFilterOptions для цветных изображений. Приведенный ниже фрагмент кода демонстрирует, как применить фильтр Гаусса Винера к цветному изображению.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Применение фильтра движения Винера**
Aspose.PSD предоставляет класс MotionWienerFilterOptions для применения фильтра к RasterImage. Приведенный ниже фрагмент кода демонстрирует, как применить фильтр движения Винера к растровому изображению.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Применение фильтра коррекции к изображению**
Эта статья демонстрирует использование Aspose.PSD для Java для выполнения фильтров коррекции на изображении. API Aspose.PSD предоставляет эффективные и простые в использовании методы для достижения этой цели. Для фильтрации в Java Aspose.PSD были представлены классы BilateralSmoothingFilterOptions и SharpenFilterOptions. Класс BilateralSmoothingFilterOptions требует целого числа в качестве размера. Шаги выполнения изменения размера следующие:


1. Загрузить изображение с помощью метода фабрики Load, предоставленного классом Image.
1. Преобразовать изображение в RasterImage.
1. Создать экземпляры классов BilateralSmoothingFilterOptions и SharpenFilterOptions.
1. Вызвать метод RasterImage.Filter, указав прямоугольник в качестве границ изображения и экземпляр класса BilateralSmoothingFilterOptions.
1. Вызвать метод RasterImage.Filter, указав прямоугольник в качестве границ изображения и экземпляр класса SharpenFilterOptions.
1. Регулировать контраст
1. Установить яркость
1. Сохранить результаты.

В следующем фрагменте кода показано, как применить фильтр коррекции.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Использование алгоритма порога Брэдли**
Пороговая обработка изображения используется в графических приложениях. Цель порогования изображения - классифицировать пиксели как "темные" или "светлые". API Aspose.PSD позволяет использовать пороговую обработку Брэдли при преобразовании изображений. В следующем фрагменте кода показано, как определить пороговое значение, а затем вызвать алгоритм порога Брэдли.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
