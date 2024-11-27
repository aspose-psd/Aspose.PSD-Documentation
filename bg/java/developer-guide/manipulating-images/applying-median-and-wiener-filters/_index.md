---
title: Прилагане на медианни и Винер филтри
type: docs
weight: 10
url: /bg/java/прилагане-на-медианни-и-винер-филтри/
---

## **Прилагане на медианни и Винер филтри**
Медианныят филтър е нелинеен цифров филтриращ метод, често използван за премахване на шум. Такова намаляване на шума е типична предварителна обработка, предназначена да подобри резултатите от по-късната обработка. Винер филтърът е средно квадратично грешково оптимален стационарен линеен филтър за изображения, деградирани от добавяне на шум и размазване. Чрез Aspose.PSD за Java API разработчиците могат да приложат медианен филтър, за да стереотипизират изображението и да приложат Гаус Винер филтър върху изображения. Тази статия демонстрира как могат да бъдат приложени медианен филтър и Гаус Винер филтър върху изображения.

### **Прилагане на Медианен Филтър**
Aspose.PSD предоставя клас MedianFilterOptions за прилагане на филтър върху RasterImage. Процесът на код, показан по-долу, демонстрира как да се приложи медианен филтър към растерно изображение.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **Прилагане на Гаус Винер Филтър**
Aspose.PSD предоставя клас GaussWienerFilterOptions за прилагане на филтър върху RasterImage. Процесът на код, показан по-долу, демонстрира как да се приложи Гаус Винер филтър към растерно изображение.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **Прилагане на Гаус Винер Филтър за Цветно изображение**
Aspose.PSD предоставя GaussWienerFilterOptions и за цветни изображения. Процесът на код, показан по-долу, демонстрира как да се приложи Гаус Винер филтър към цветно изображение.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **Прилагане на Мотивен Винер Филтър**
Aspose.PSD предоставя клас MotionWienerFilterOptions за прилагане на филтър върху RasterImage. Процесът на код, показан по-долу, демонстрира как да се приложи мотивен Винер филтър към растерно изображение.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **Приложение на Филтър за Корекция върху Изображение**
Тази статия демонстрира използването на Aspose.PSD за Java за извършване на корекционни филтри върху изображение. Aspose.PSD APIs предоставят ефективни и лесни за използване методи за постигане на тази цел. Aspose.PSD за Java експонира класовете BilateralSmoothingFilterOptions и SharpenFilterOptions за филтрация. Класът BilateralSmoothingFilterOptions изисква цяло число за размер. Стъпките за извършване на преоразмеряване са толкова прости, колкото посоченото по-долу:

1. Заредете изображение, използвайки метода на фабриката Load, изложен от класа Image.
1. Преобразувайте изображението в RasterImage.
1. Създайте инстанции на класовете BilateralSmoothingFilterOptions и SharpenFilterOptions.
1. Извика на метода Filter на RasterImage, като посочите правоъгълника като граници на изображението и инстанцията на класа BilateralSmoothingFilterOptions.
1. Извика на метода Filter на RasterImage, като посочите правоъгълника като граници на изображението и инстанция на класа SharpenFilterOptions.
1. Настройте контраста.
1. Задайте яркостта.
1. Запазете резултатите.

Следният кодов откъс ви показва как да приложите корекционен филтър.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **Използване на Алгоритъма за Прага на Брадли**
Прагът за изображение се използва в графични приложения. Целта на прага на изображението е да класифицира пикселите като "тъмни" или "светли". Aspose.PSD API ви позволява да използвате прага на Брадли, докато преобразувате изображения. Следният кодов откъс ви показва как да дефинирате стойността на прага и след това да извикате алгоритъма за прага на Брадли.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}