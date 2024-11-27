---
title: Прилагане на Медианен и Уинър Филтри
type: docs
weight: 10
url: /bg/applying-median-and-wiener-filters/
---

## **Прилагане на Медианен и Уинър Филтри**
Медианният филтър е нелинеен цифров филтър, често използван за премахване на шум. Такова намаляване на шума е типична предварителна обработка, която подобрява резултатите от по-късната обработка. Уинър-филтърът е оптималният стационарен линеен филтър за средно квадратично отклонение(MSE), приложим за изображения, деградирани от добавяне на шум и размазване. Чрез Aspose.PSD API за .NET разработчиците могат да прилагат медиен филтър за премахване на шум от изображението и да приложат филтър на Гаус Уинър за изображения. Тази статия демонстрира как медиен филтър и Гаус Уинър филтър могат да бъдат приложени към изображения.

### **Прилагане на Медианен Филтър**
Aspose.PSD предоставя класа [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) за прилагане на филтър върху [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Долната предоставена част от кода демонстрира как да се приложи медиен филтър върху растерно изображение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Прилагане на Филтър Гаус Уинър**
Aspose.PSD предоставя класа [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) за прилагане на филтър върху [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Долната предоставена част от кода демонстрира как да се приложи филтър Гаус Уинър върху растерно изображение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Прилагане на Филтър Гаус Уинър за Цветно изображение**
Aspose.PSD предоставя [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) и за цветни изображения. Долната предоставена част от кода демонстрира как да се приложи филтър Гаус Уинър върху цветно изображение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Прилагане на Филтър Моушън Уинър**
Aspose.PSD предоставя класа [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) за прилагане на филтър върху [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Долната предоставена част от кода демонстрира как да се приложи филтър моушън уинър върху растерно изображение.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Прилагане на Филтър за Корекция върху изображение**
Тази статия демонстрира използването на Aspose.PSD за .NET за извършване на корекционни филтри върху изображение. Aspose.PSD API представя ефикасни и лесни за използване методи за постигане на тази цел. Aspose.PSD за .NET е изложил класовете [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) и [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) за филтрация. Класът BilateralSmoothingFilterOptions изисква цяло число като размер. Стъпките за извършване на resize са толкова прости, както следва:

1. Заредете изображение, използвайки фабричния метод Load, предоставен от класа Image.
2. Конвертирайте изображението в RasterImage.
3. Създайте инстанция на класовете BilateralSmoothingFilterOptions и SharpenFilterOptions.
4. Извикайте метода [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), като посочите правоъгълника като граници на изображението и инстанция на класа BilateralSmoothingFilterOptions.
5. Извикайте метода [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter), като посочите правоъгълника като граници на изображението и инстанция на класа SharpenFilterOptions.
6. Настройте контраста.
7. Задайте яркостта.
8. Запазете резултатите.

## **Използване на Алгоритъма за Праг на Брадли**
Прагът за изображение се използва в графични приложения. Целта на прага за изображение е да класифицира пикселите като "тъмни" или "светли". Aspose.PSD API ви позволява да използвате прага на Брадли, докато преобразувате изображения. Долната част от кода ви показва как да дефинирате стойността на прага и след това да извикате алгоритъма за прага на Брадли.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}