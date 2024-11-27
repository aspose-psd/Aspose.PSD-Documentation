---
title: Преобразуване на изображения
type: docs
weight: 20
url: /bg/net/converting-images/
---

## **Преобразуване на изображения в черно-бяло и в градации на сиво**
Понякога може да се наложи да преобразувате цветни изображения в черно-бяло или в градации на сиво за печат или архивни цели. Тази статия демонстрира използването на Aspose.PSD за .NET API за постигане на това използвайки два метода, както е посочено по-долу.

- Бинаризация
- Преобразуване в градации на сиво
### **Бинаризация**
За да разберете понятието за бинаризация, е важно да се дефинира Бинарно изображение; което е цифрово изображение, което може да има само две възможни стойности за всеки пиксел. Обикновено, двата цвята, използвани за бинарно изображение, са черно и бяло, въпреки че може да се използват всеки два цвята. Бинаризацията е процесът на преобразуване на изображение в двунивен, което означава, че всеки пиксел се съхранява като единичен бит (0 или 1), където 0 означава липса на цвят, а 1 означава присъствието на цвят. Aspose.PSD за .NET API в момента поддържа два метода за бинаризация.
#### **Бинаризация с Фиксиран Праг**
Следната откъс от код показва как може да се приложи бинаризация с фиксиран праг на изображение.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Бинаризация с Отсу Праг**
Следният откъс от код показва как може да се приложи бинаризация с Отсу праг на изображение.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Преобразуване в градации на сиво**
Преобразуването в градации на сиво е процесът на конвертиране на изображение с непрекъснати тонове в изображение с прекъснати сиви нюанси. Следният откъс от код показва как да се използва Преобразуването в градации на сиво.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **Преобразуване на слоевете на изображения GIF в изображение TIFF**
Понякога е необходимо да извлечете и конвертирате слоевете на изображение PSD в друг формат на равнище на пиксели, за да се отговори на нуждите на приложението. Aspose.PSD API подкрепя функцията за извличане и конвертиране на слоевете на изображение PSD в друг формат на равнище на пиксели. Първоначално ще създадем инстанция на изображението и ще заредим изображение PSD от локалния диск, след което ще итерираме всеки слой в свойството Layer. След това ще конвертираме блока в изображение TIFF. Следващият откъс от код показва как да конвертирате слоевете на изображение PSD в TIFF изображения.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **Преобразуване на CMYK PSD в CMYK TIFF**
С помощта на Aspose.PSD за .NET, разработчиците могат да конвертират PSD файл CMYK във формат CMYK tiff. Тази статия показва как да експортирате/конвертирате PSD файл CMYK във формат CMYK tiff с Aspose.PSD. С помощта на Aspose.PSD за .NET можете да зареждате PSD изображения и след това можете да зададете различни свойства, използвайки [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) класа и да запазите или експортирате изображението. Следният откъс от код показва как да постигнете това свойство.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **Изнасяне на изображения**
Освен богат набор от рутини за обработка на изображения, Aspose.PSD предоставя специализирани класове за конвертиране на файлови формати на PSD в други формати. Използвайки тази библиотека, конвертирането на PSD изображения е много лесно и интуитивно. По-долу са някои специализирани класове за тази цел в пространството на имена [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Е лесно да изнесете PSD изображения с Aspose.PSD за .NET API. Всичко, което ви е необходимо, е обект от подходящия клас от [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) пространството на имена. Чрез използването на тези класове, можете лесно да експортирате всяко изображение, създадено, редактирано или просто заредено с Aspose.PSD за .NET в който и да е поддържан формат.
## **Комбиниране на изображения**
Този пример използва класа Graphics и показва как да комбинирате две или повече изображения в едно цялостно изображение. За да се демонстрира операцията, примерът създава ново PsdImage и рисува изображения на повърхността на платното, използвайки метода Draw Image, изложен от класа Graphics. Чрез класа Graphics две или повече изображения могат да бъдат комбинирани по такъв начин, че резултантното изображение ще изглежда като цяло изображение без пространство между частите на изображението и без страници. Големината на платното трябва да бъде равна на големината на резултантното изображение. Последващият код показва как да използвате метода [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) на класа [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) за комбинирането на изображения в едно изображение.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Разширяване и Изрязване на изображения**
Aspose.PSD API ви позволява да разширявате или изрязвате изображение по време на процеса на конвертиране на изображения. Разработчикът трябва да създаде правоъгълник с X и Y координати и да посочи ширината и височината на правоълълния. X, Y и ширината, височината на правоъгълника ще показват разширяването или изрязването на зареденото изображение. Ако е необходимо да разширите или изрежете изображението по време на конвертиране на изображения, изпълнете следните стъпки:

1. Създайте инстанция на [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) класа и заредете съществуващото изображение.
1. Създайте инстанция на клас ImageOption.
1. Създайте инстанция на [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) клас и инициализирайте X, Y и ширината, височината на правоълълника.
1. Извикайте метода [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) на класа RasterImage, докато подадете името на изходния файл, изображения опции и обекта правоълълник като параметри.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **Четене и Записване на XMP Данни към Изображения**
XMP (Extensible Metadata Platform) е ISO стандарт. XMP стандартизира модела на данни, формата за сериализация и основните свойства за дефиниране и обработка на разширими метаданни. Също така предоставлява насоки за вграждане на XMP информация в популярно изображение като JPEG, без да нарушава четимостта им от приложения, които не поддържат XMP. С помощта на Aspose.PSD за .NET API разработчиците могат да четат или пишат XMP метаданни към изображения. Тази статия демонстрира как XMP метаданните могат да бъдат прочетени от едно изображение и как XMP метаданните могат да бъдат записани към изображения.
### **Създаване на XMP метаданни, Записване и Четене от Файл**
С помощта на пространството на имена Xmp, разработчикът може да създаде обект за XMP метаданни и да го запише към изображение. Следният откъс от код показва как да използвате пакетите XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage и DublinCorePackage, съдържащи се в пространството на имена [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Изнасяне на изображения в многонишкова среда**
Aspose.PSD за .NET в момента поддържа конвертирането на изображения в многонишкова среда. Aspose.PSD за .NET гарантира оптимизираното изпълнение на операциите по време на изпълнението на код в многонишкова среда. Всички класове за [изображения](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) (напр. BmpOptions, TiffOptions, JpegOptions и т.н.) в Aspose.PSD за .NET имплементират интерфейса IDisposable. Затова е задължително разработчикът правилно да изтрие обекта на класа за изображението в случай, че свойството Source е зададено. Следният откъс от код демонстрира споменатата функционалност.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD в момента поддържа свойството SyncRoot при работа в многонишкова среда. Разработчикът може да използва това свойство за синхронизиране на достъпа до източника на потока. Следващият откъс от код демонстрира как свойството SyncRoot може да бъде използвано.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}