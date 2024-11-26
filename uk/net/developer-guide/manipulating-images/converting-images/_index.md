---
title: Конвертування Зображень
type: docs
weight: 20
url: /uk/net/converting-images/
---

## **Конвертування Зображень у Чорно-Біле та Відтінки Сірого**
Іноді вам може знадобитися конвертувати кольорові зображення у чорно-білі або відтінки сірого для друку або архівування. Ця стаття демонструє використання Aspose.PSD для API .NET для досягнення цього за допомогою двох наведених нижче методів.

- Бінаризація
- Відтінкування
### **Бінаризація**
Для того, щоб зрозуміти концепцію бінаризації, важливо визначити Бінарне Зображення; це цифрове зображення, у якого кожен піксел може мати лише два можливих значення. Зазвичай для бінарного зображення використовуються чорний та білий кольори, хоча можна використовувати будь-які два кольори. Бінаризація - це процес перетворення зображення на дво-рівневе, що означає, що кожен піксель зберігається як один біт (0 або 1), де 0 позначає відсутність кольору, а 1 означає наявність кольору. API Aspose.PSD для .NET в даний момент підтримує два методи бінаризації.
#### **Бінаризація з Фіксованим Порогом**
Наступний уривок коду показує, як використовувати фіксовану порогову бінаризацію для застосування до зображення.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Бінаризація з Порогом Оцу**
Наступний уривок коду показує, як застосовувати бінаризацію з порогом Оцу до зображення.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Відтінкування**
Відтінкування - це процес перетворення зображення з неперервним відтінком на зображення з розривними відтінками сірого. Наступний уривок коду показує, як використовувати Відтінкування.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}

## **Конвертування Шарів Зображення GIF у Зображення TIFF**
Іноді потрібно видобути та конвертувати шари зображення PSD в інший формат растрового зображення для відповіді на потреби додатка. API Aspose.PSD підтримує функцію видобування та конвертації шарів зображення PSD у інший формат растрового зображення. Спочатку ми створимо екземпляр зображення та завантажимо зображення PSD з локального диска, потім ми будемо перебирати кожен шар у властивості Шари. Потім ми конвертуємо блок в зображення TIFF. Наступний уривок коду показує, як конвертувати шари зображення PSD у зображення TIFF.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}

## **Конвертування CMYK PSD у CMYK TIFF**
За допомогою Aspose.PSD для .NET розробники можуть конвертувати файл CMYK PSD у формат tiff CMYK. Ця стаття показує, як експортувати/конвертувати файл CMYK PSD у формат TIFF CMYK за допомогою Aspose.PSD. За допомогою Aspose.PSD для .NET ви можете завантажувати зображення PSD, потім ви можете встановлювати різні властивості за допомогою класу [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) та зберігати або експортувати зображення. Наступний уривок коду показує, як досягти цієї функціональності.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}

## **Експорт Зображень**
Разом з багатим набором процедур обробки зображень, Aspose.PSD надає спеціалізовані класи для конвертації форматів файлів PSD у інші формати. За допомогою цієї бібліотеки конвертація зображень PSD є дуже простою та інтуітивною. Нижче наведено деякі спеціалізовані класи для цієї мети в просторі імен [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Експортувати зображення PSD з Aspose.PSD для API .NET дуже просто. Вам потрібний лише об'єкт відповідного класу з [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace. Використовуючи ці класи, ви можете легко експортувати будь-яке зображення, створене, відредаговане або просто завантажене за допомогою Aspose.PSD для .NET у будь-який підтримуваний формат.

## **Об'єднання Зображень**
У цьому прикладі використовується клас Graphics та показано, як об'єднати два або більше зображень в єдине повне зображення. Для демонстрації операції приклад створює нове зображення PsdImage та малює зображення на поверхні полотна за допомогою методу Draw Image, що викладений класом Graphics. За допомогою класу Graphics можна об'єднати два або більше зображень таким чином, щоб отримане зображення виглядало як ціле зображення без проміжку між частинами зображення та сторінками. Розмір полотна повинен дорівнювати розміру отриманого зображення. Нижче подано код, який демонструє, як використовувати метод [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) класу [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) для об'єднання зображень в одне зображення.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **Розширення та Обрізання Зображень**
API Aspose.PSD дозволяє розширити або обрізати зображення під час процесу конвертації зображення. Розробник повинен створити прямокутник з координатами X та Y та вказати ширину та висоту прямокутника. Координати X, Y та ширина, висота прямокутника покажуть розширення або обрізання завантаженого зображення. Якщо під час конвертації зображення потрібно розширити або обрізати зображення, виконайте наступні кроки:

1. Створіть екземпляр класу [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) та завантажте існуюче зображення.
1. Створіть екземпляр класу ImageOption.
1. Створіть екземпляр класу [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) та ініціалізуйте X, Y та ширину, висоту прямокутника
1. Викличте метод [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) класу RasterImage, передаючи ім'я вихідного файлу, параметри зображення та об'єкт прямокутника в якості параметрів.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **Читання та Запис Даних XMP в Зображення**
XMP (Extensible Metadata Platform) - це стандарт ISO. XMP стандартизує модель даних, серіалізаційний формат та базові властивості для визначення та обробки розширених метаданих. Він також надає вказівки для вбудовування інформації XMP в популярне зображення, таке як JPEG, без порушення їх читабельності для додатків, які не підтримують XMP. За допомогою Aspose.PSD для .NET API розробники можуть читати або записувати метадані XMP в зображення. Ця стаття демонструє, як метадані XMP можна прочитати з зображення та записати метадані XMP в зображення.
### **Створення Метаданих XMP, Запис та Читання З Файлу**
За допомогою простору імен Xmp розробник може створити об'єкт метаданих XMP та записати його в зображення. Вказаний уривок коду показує, як використовувати пакети XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage та DublinCorePackage, які включені в простір імен [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}

## **Експортування Зображень в Багатопотоковому Середовищі**
Aspose.PSD для .NET тепер підтримує конвертацію зображень у багатопотоковому середовищі. Aspose.PSD для .NET забезпечує оптимізовану продуктивність операцій під час виконання коду в багатопотоковому середовищі. Всі класи [параметрів зображення](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) (наприклад, BmpOptions, TiffOptions, JpegOptions тощо) в Aspose.PSD для .NET реалізують інтерфейс IDisposable. Тому розробник повинен належним чином вивести клас параметрів зображення, якщо властивість джерела встановлена. Наступний уривок коду демонструє вказану функціональність.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD тепер підтримує властивість Sync
