---
title: Застосування медійного та Вінера фільтрів
type: docs
weight: 10
url: /uk/net/applying-median-and-wiener-filters/
---

## **Застосування медійного та Вінера фільтрів**
Медійний фільтр - це нелінійний цифровий метод фільтрації, який часто використовується для видалення шуму. Таке зменшення шуму - типовий етап попередньої обробки для покращення результатів подальшої обробки. Фільтр Вінера є оптимальним лінійним фільтром мінімізації середньоквадратичної помилки для зображень, збурених адитивним шумом і розмиттям. За допомогою Aspose.PSD для розробників API .NET можна застосовувати медійний фільтр для позбавлення зображення від шуму та застосовувати гауссовий фільтр Вінера на зображення. Ця стаття демонструє, як можна застосувати медійний фільтр та гауссівський фільтр Вінера на зображення.

### **Застосування медійного фільтру**
Aspose.PSD надає клас [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions), щоб застосувати фільтр на [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Наведений нижче фрагмент коду демонструє, як застосувати медійний фільтр до растрового зображення.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}

### **Застосування гауссового фільтру Вінера**
Aspose.PSD надає клас [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions), щоб застосувати фільтр на [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Наведений нижче фрагмент коду демонструє, як застосувати гауссовий фільтр Вінера на растрове зображення.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c"  "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}

### **Застосування гауссового фільтру Вінера для кольорового зображення**
Aspose.PSD надає [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) для кольорових зображень також. Наведений нижче фрагмент коду демонструє, як застосувати гауссівський фільтр Вінера на кольорове зображення.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}

### **Застосування рухомого фільтру Вінера**
Aspose.PSD надає клас [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions), щоб застосувати фільтр на [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Наведений нижче фрагмент коду демонструє, як застосувати руховий фільтр Вінера на растрове зображення.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}

## **Застосувати фільтр корекції на зображенні**
Ця стаття демонструє використання Aspose.PSD для .NET для виконання корекційних фільтрів на зображення. API Aspose.PSD надає ефективні та прості методи для досягнення цієї мети. Aspose.PSD для .NET розкрив класи [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) і [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) для фільтрації. Клас BilateralSmoothingFilterOptions потребує ціле число як розмір. Кроки для виконання зменшення прості, як наведено нижче:

1. Завантажте зображення за допомогою фабричного методу Load, що надається класом Image.
1. Конвертуйте зображення в RasterImage.
1. Створіть екземпляр класів BilateralSmoothingFilterOptions та SharpenFilterOptions.
1. Викличте метод [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), вказавши прямокутник як межі зображення та екземпляр класу BilateralSmoothingFilterOptions.
1. Викличте метод [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), вказавши прямокутник як межі зображення та екземпляр класу SharpenFilterOptions.
1. Налаштуйте контрастність
1. Встановіть яскравість
1. Збережіть результати.

## **Використання алгоритму порога Брейдлі**
Порогова обробка зображень використовується в графічних додатках. Мета порогування зображення полягає в класифікації пікселів як "темних" або "світлих". API Aspose.PSD дозволяє використовувати порог Брейдлі при конвертації зображень. Наведений код показує, як визначити значення порога і викликати алгоритм порогування Брейдлі.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
