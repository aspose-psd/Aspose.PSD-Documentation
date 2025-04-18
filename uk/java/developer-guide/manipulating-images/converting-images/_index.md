---
title: Конвертування Зображень
type: docs
weight: 20
url: /uk/java/converting-images/
---

## **Конвертування Зображень у Чорно-біле та Відтінки Сірих**
Іноді вам може знадобитися конвертувати кольорові зображення в чорно-біле або відтінки сірих для друку чи архівування. Ця стаття демонструє використання Aspose.PSD для Java API для досягнення цього за допомогою двох методів, які вказані нижче.

- Бінаризація
- Перетворення на відтінки сірих

### **Бінаризація**
Для розуміння концепції бінаризації важливо визначити Бінарне Зображення; це цифрове зображення, у якому для кожного пікселя можливі лише дві значення. Зазвичай два кольори, які використовуються для бінарного зображення, є чорний та білий, хоча можна використовувати будь-які два кольори. Бінаризація - це процес перетворення зображення на бі-рівневе, що означає, що кожен піксель зберігається як один біт (0 або 1), де 0 позначає відсутність кольору, а 1 означає наявність кольору. Aspose.PSD для Java API наразі підтримує два методи бінаризації.

#### **Бінаризація з Фіксованим Порогом**
Наведений нижче фрагмент коду показує вам, як можна застосувати бінаризацію з фіксованим порогом до зображення.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}

#### **Бінаризація з Порогом Otsu**
Наведений нижче фрагмент коду показує вам, як можна застосувати бінаризацію з порогом Otsu до зображення.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}

### **Перетворення на Відтінки Сірих**
Перетворення на відтінки сірих - це процес перетворення зображення з неперервними тонами в зображення з розривними відтінками сірого кольору. Наведений нижче фрагмент коду показує вам, як використовувати перетворення на відтінки сірих.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}

## **Конвертування Шарів Зображення GIF у Зображення TIFF**
Іноді потрібно видобути та конвертувати шари зображення PSD в інший растровий формат зображення для відповідності потребам додатка. Aspose.PSD API підтримує функцію видобуття та конвертації шарів зображення PSD в інший растровий формат зображення. Спочатку ми створимо екземпляр зображення й завантажимо зображення PSD з локального диска, потім ми будемо ітерувати кожен шар у властивості Шар. Потім ми конвертуємо блок в зображення TIFF. Наведений нижче фрагмент коду показує вам, як конвертувати шари зображення PSD у зображення TIFF.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}

## **Конвертування CMYK PSD в CMYK TIFF**
За допомогою Aspose.PSD для Java розробники можуть конвертувати файл CMYK PSD у формат tiff CMYK. Ця стаття показує, як експортувати / конвертувати файл CMYK PSD у формат TIFF CMYK за допомогою Aspose.PSD. За допомогою Aspose.PSD для Java ви можете завантажувати зображення PSD, встановлювати різноманітні властивості за допомогою класу TiffOptions та зберігати або експортувати зображення. Наведений нижче фрагмент коду показує вам, як досягти цієї функції.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}

## **Експорт Зображень**
Поміж багатим набором операцій обробки зображень Aspose.PSD надає спеціалізовані класи для конвертації форматів файлів PSD в інші формати. За допомогою цієї бібліотеки конвертація зображень PSD дуже проста і інтуїтивно зрозуміла. Нижче наведені деякі спеціалізовані класи для цієї мети в просторі імен ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Є легко експортувати зображення PSD за допомогою Aspose.PSD для Java API. Вам потрібно лише об'єкт відповідного класу з ImageOptions namespace. Використовуючи ці класи, ви можете легко експортувати будь-яке зображення, створене, відредаговане або просто завантажене за допомогою Aspose.PSD для Java у будь-який підтримуваний формат.

## **Комбінування Зображень**
Цей приклад використовує клас Graphics і показує, як об'єднати два чи більше зображень в одне повне зображення. Для демонстрації операції приклад створює нове зображення PsdImage та малює зображення на поверхні полотна за допомогою методу Draw Image, який надається класом Graphics. За допомогою класу Graphics два чи більше зображень можна поєднати таким чином, що отримане зображення виглядатиме як повне зображення без прогалин між його частинами та сторінками. Розмір полотна повинен бути рівним розміру отриманого зображення. Нижче наведено демонстрацію коду, що показує, як використовувати метод Draw Image класу Graphics для об'єднання зображень в одне зображення.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}

## **Розширення та Обрізка Зображень**
API Aspose.PSD дозволяє вам розширювати або обрізати зображення під час процесу конвертації зображення. Розробнику потрібно створити прямокутник з координатами X та Y та вказати ширину та висоту прямокутника. Координати X, Y та ширина, висота прямокутника визначатимуть розширення або обрізку завантаженого зображення. Якщо потрібно розширити або обрізати зображення під час його конвертації, слід виконати наступні кроки:

1. Створіть екземпляр класу RasterImage та завантажте існуюче зображення.
1. Створіть екземпляр класу ImageOption.
1. Створіть екземпляр класу Rectangle та ініціалізуйте X,Y та ширину, висоту прямокутника.
1. Викличте метод Save класу RasterImage, передавши ім'я вихідного файлу, опції зображення та об'єкт прямокутника у якості параметрів.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}

## **Читання та Запис Даних XMP до Зображень**
XMP (Extensible Metadata Platform) є міжнародним стандартом. XMP стандартизує модель даних, серіалізаційний формат та основні властивості для визначення та обробки розширених метаданих. Він також надає вказівки для вбудовування інформації XMP у популярні зображення, такі як JPEG, без порушення їх читабельності програмами, які не підтримують XMP. За допомогою Aspose.PSD для Java API розробники можуть читати або записувати метадані XMP до зображень. Ця стаття демонструє, як метадані XMP можна прочитати з зображення та записати метадані XMP до зображень.

### **Створення Метаданих XMP, Запис та Читання з Файлу**
За допомогою простору імен XMP розробник може створити об'єкт метаданих XMP та записати його на зображення. Наведений нижче фрагмент коду показує вам, як використати пакети XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage та DublinCorePackage, які містяться в просторі імен XMP.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}

## **Експорт Зображень у Мультипотоковому Середовищі**
Aspose.PSD для Java тепер підтримує конвертацію зображень у мультипотоковому середовищі. Aspose.PSD для Java забезпечує оптимізований режим виконання операцій під час виконання коду у мультипотоковому середовищі. Усі класи опцій зображень (наприклад, BmpOptions, TiffOptions, JpegOptions та ін.) у Aspose.PSD для Java реалізують інтерфейс IDisposable. Тому розробник повинен належним чином видаляти об'єкт класу опцій зображення у випадку встановлення властивості джерела. Наведений нижче фрагмент коду демонструє вказану функціональність.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}

Aspose.PSD тепер підтримує властивість SyncRoot при роботі в мультипотоковому середовищі. Розробник може використовувати цю властивість для синхронізації доступу до потоку джерела. Наведений нижче фрагмент коду демонструє, як можна використати властивість SyncRoot.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}
