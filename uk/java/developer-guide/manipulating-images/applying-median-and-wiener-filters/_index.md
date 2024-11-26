---
title: Застосування фільтрів медіани та Вінера
type: docs
weight: 10
url: /uk/java/applying-median-and-wiener-filters/
---

## **Застосування фільтрів медіани та Вінера**
Фільтр медіани - це нелінійний цифровий фільтр, який часто використовується для видалення шуму. Таке зменшення шуму є типовим кроком передобробки для поліпшення результатів подальшої обробки. Фільтр Вінера є оптимальним MSE (середньоквадратичне значення помилки) стаціонарним лінійним фільтром для зображень, зіпсованих адитивним шумом та розмиттям. Використовуючи Aspose.PSD для Java API, розробники можуть застосовувати фільтр медіани для зменшення шуму на зображенні та застосовувати фільтр Гауса-Вінера на зображеннях. Ця стаття демонструє, як фільтр медіани та фільтр Гауса-Вінера можуть бути застосовані до зображень.
### **Застосування фільтру Медіани**
Aspose.PSD надає клас MedianFilterOptions для застосування фільтру на RasterImage. Наведений нижче фрагмент коду демонструє, як застосувати фільтр медіани до растрового зображення.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Застосування фільтру Гауса-Вінера**
Aspose.PSD надає клас GaussWienerFilterOptions для застосування фільтру на RasterImage. Наведений ниже фрагмент коду демонструє, як застосувати фільтр Гауса-Вінера до растрового зображення.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Застосування фільтру Гауса-Вінера для кольорового зображення**
Aspose.PSD надає GaussWienerFilterOptions для кольорових зображень також. Наведений нижче фрагмент коду демонструє, як застосувати фільтр Гауса-Вінера до кольорового зображення.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Застосування фільтру Мотіон-Вінера**
Aspose.PSD надає клас MotionWienerFilterOptions для застосування фільтру на RasterImage. Наведений нижче фрагмент коду демонструє, як застосувати фільтр мотіон-вінера до растрового зображення.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Застосування фільтру корекції для зображення**
Ця стаття демонструє використання Aspose.PSD для мови Java для застосування корекційних фільтрів до зображення. API Aspose.PSD мають ефективні та прості методи для досягнення цієї мети. Aspose.PSD для Java виклав класи BilateralSmoothingFilterOptions та SharpenFilterOptions для фільтрації. Клас BilateralSmoothingFilterOptions потребує ціле число як розмір. Кроки для виконання змін рядків, які прості, як наведено нижче:


1. Завантажте зображення за допомогою методу завантаження, викладеного класом Image.
1. Конвертувати зображення в RasterImage.
1. Створіть екземпляри класів BilateralSmoothingFilterOptions та SharpenFilterOptions.
1. Викличте метод RasterImage.Filter, вказавши прямокутник як межі зображення та екземпляр класу BilateralSmoothingFilterOptions.
1. Викличте метод RasterImage.Filter, вказавши прямокутник як межі зображення та екземпляр класу SharpenFilterOptions.
1. Налаштуйте контрастність
1. Встановіть яскравість
1. Збережіть результати.

Наведений нижче фрагмент коду показує вам, як застосувати фільтр корекції.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Використання алгоритму порогового значення Бредлі**
Порогове значення зображення використовується в графічних застосунках. Мета порогування зображення полягає в класифікації пікселів як "темні" або "світлі". API Aspose.PSD дозволяє використовувати порог Бредлі під час конвертації зображень. Наведений нижче фрагмент коду показує, як визначити значення порогу, а потім викликати алгоритм порогування Бредлі.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
