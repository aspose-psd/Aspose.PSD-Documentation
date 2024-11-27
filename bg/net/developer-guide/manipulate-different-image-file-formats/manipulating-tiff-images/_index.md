---
title: Манипулиране на TIFF изображения
type: docs
weight: 50
url: /bg/net/manipulating-tiff-images/
---

## **Добавяне на рамки с различни настройки**
TIFF е много гъвкав формат, който позволява добавянето на различни рамки с различни размери, компресия и други настройки. API на Aspose.PSD ви позволява да добавяте всяка TIFF рамка с произволен размер, което помага за създаването на сложни документи. В случай на необходимост от настройка на рамките по време на добавянето им, за да ги направите равни, изпълнете следните стъпки:

- Създайте нова празна рамка с желаните опции или копирайте изходната рамка със зададените опции за изход, използвайки метода CreateFrameFrom.
- Преоразмерете изходната рамка/изображение до желаните размери, използвайки метода Resize.
- Добавете пикселите на изходната рамка/изображение към новата рамка.
- Добавете новата рамка към изходното TIFF изображение.

## **Изнасяне на слоевете на PSD изображението към файл във формат Multi Page Tiff**
Понякога е необходимо да се изнесат слоевете на PSD изображението във файл във формат Multi-page TIFF. Тази статия ще демонстрира как можем да извършим тази задача чрез API на Aspose.PSD за .NET. Първо ще заредим PSD изображението от диск. След това ще преминем през слоевете на PSD изображението и ще създадем TiffFrame от съответните слоеве. Най-накрая ще запазим полученото Tiff изображение в един файл на диск.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}

## **Конфигурация на TiffOptions**
Програмистите могат да променят различни свойства на [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) класа, за да получат желаните резултати. В този документ ще се фокусираме върху 4 основни свойства, които контролират атрибутите на полученото изображение.

Тези свойства са изброени по-долу.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
2. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
3. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
4. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

При инициализирането на празната структура на TiffOptions, всяка опция се задава на стойността си по подразбиране, например компресията е зададена на None, BitsPerSample е зададен като 1, а Photometric като MinIsWhite. Запазването в този формат ще направи крайното изображение черно и бяло, което е очаквано поведение за такива комбинации от опции. За да получите цветните резултати, трябва да зададете всички горепосочени свойства на стойности, които съответстват на желания цветови пространство или да инициализирате структурата на TiffOptions с предварително зададени настройки, както е обсъдено по-късно в този документ. Предоставена по-долу е таблица, която описва очакваните стойности на параметрите, които можете да зададете, за да постигнете желаните резултати. Моля, обърнете внимание, че трябва да зададете всички 4 стълба чрез TiffOptions, за да запазите всяко заредено/създадено изображение във формат TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16 (palette, color mode) single channel only|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (gray-scale mode) single channel only|None|
|Palette|LZW/Uncompressed|8 (palette, color mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (gray-scale mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|RGB|LZW/Uncompressed|[8,8,8] (3 RGB channels)|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 RGB channels and additional alpha channel may be set through TiffOptions.AlphaStorage) Actually any additional channels count is supported but each channel must have 8 bit size like [8,8,8,8,8,8]|None/Horizontal|

Всички 4 свойства трябва да бъдат зададени чрез TiffOptions, за да се запази всяко изображение във формат TIFF. При използване на различни комбинации някои програми (включително Windows Photo Viewer) може да откажат да визуализират полученото изображение поради лимитираната поддръжка, която предлагат. В такъв случай, моля, използвайте различен програма за вашите тестове.

### **Предварително зададени настройки за класа TiffOptions**
За да улесни потребителите и да се избегне грешна конфигурация на екземпляра на TiffOptions, API на Aspose.PSD за .NET е изложил друг конструктор, който приема параметър от тип [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Въз основа на избраната стойност от изброяването TiffExpectedFormat, API автоматично конфигурира всички задължителни свойства за екземпляра на TiffOptions с цел производството на желаните резултати. Преди да преминем към примерния код, ето списък на полетата на TiffExpectedFormat и техните детайли за по-добро разбиране на употребата.

- TiffExpectedFormat.Default: Задаването на полето като Default действа подобно на конструктора по подразбиране на класа TiffOptions без компресия и BitsPerPixel зададени на 1, за да се получи черно и бяло изображение. Съветва се да се използва това поле, когато други специфични за формата свойства трябва да бъдат зададени ръчно в съответствие с желаните резултати.
- TiffExpectedFormat.TiffCcitRle: Специфично за кодирането чрез RLE при запазване на резултата в TIFF формат с BitsPerPixel зададен на 1 (черно и бяло изображение).
- TiffExpectedFormat.TiffCcittFax3: Специфично за кодирането с CCITT Fax3 при запазване на резултата в TIFF формат с BitsPerPixel зададен на 1 (черно и бяло изображение).
- TiffExpectedFormat.TiffCcittFax4: Специфично за кодирането с CCITT Fax4 при запазване на резултата в TIFF формат с BitsPerPixel зададен на 1 (черно и бяло изображение).
- TiffExpectedFormat.TiffDeflateBW: Специфично за компресията с Deflate при запазване на резултата в TIFF формат с BitsPerPixel зададен на 1 (черно и бяло изображение).
- TiffExpectedFormat.TiffDeflateRGB: Специфично за компресията с Deflate при запазване на резултата в RGB (цветно) TIFF формат.
- TiffExpectedFormat.TiffJpegRGB: Специфично за компресията с JPEG при запазване на резултата в RGB (цветно) TIFF формат.
- TiffExpectedFormat.TiffJpegYCBCR: Специфично за компресията с JPEG при запазване на резултата в YCBCR (цветно) TIFF формат.
- TiffExpectedFormat.TiffLzwBW: Специфично за компресията с LZW при запазване на резултата в TIFF формат с BitsPerPixel зададен на 1 (черно и бяло изображение).
- TiffExpectedFormat.TiffLzwRGB: Специфично за компресията с LZW при запазване на резултата в RGB (цветно) TIFF формат.
- TiffExpectedFormat.TiffLzwRGBA: Специфично за компресията с LZW при запазване на резултата в RGBA (цветно с прозрачност) TIFF формат.
- TiffExpectedFormat.TiffNoCompressionBW: Специфично за некомпресиран формат TIFF при запазване на резултата с BitsPerPixel зададен на 1 (черно и бяло).
- TiffExpectedFormat.TiffNoCompressionRGB: Специфично за некомпресиран формат TIFF при запазване на резултата в RGB (цветно).
- TiffExpectedFormat.TiffNoCompressionRGBA: Специфично за некомпресиран формат TIFF при запазване на резултата в RGBA (цветно с прозрачност).

Долу предоставеният код демонстрира употребата на полетата на TiffExpectedFormat при създаването на инстанция на класа TiffOptions.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}

## **Поддръжка за Deflate и Adobe Deflate компресия**
Форматът на файловете TIFF (Tagged Image File Format) поддържа различни видове компресия, като типът на компресията се съхранява като таг (цяло число) във файла. Един от такива методи за компресия е Adobe Deflate (преди известен като Deflate). API на Aspose.PSD за .NET поддържа този метод на компресия за експортиране & създаване на TIFF изображения.
### **Запазване на изображение в TIFF с Deflate компресия**
Конвертирането на заредените изображения в TIFF с Deflate/Adobe Deflate компресия е лесно като следва.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}

### **Създаване на TiffImage с Adobe Deflate компресия**
Предоставеният по-долу пример демонстрира използването на API на Aspose.PSD за .NET за създаване на изображение от нулата, използвайки метода на Adobe Deflate компресия.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}

### **Компресиране на TIFF изображения**
API на Aspose.PSD за .NET може да се използва за преобразуване на PSD изображения в формат на изображения TIFF и дори за промяна на компресията на полученото TIFF изображение. API-то също може да се използва за запазване на различни изображения като рамки в TIFF изображение за архивни цели, като компресира изображенията до най-малкия размер на данните. Компресията на изображението във всеки случай трябва да се извършва чрез намаляване на размера на източните данни, независимо от използвания компресиращ алгоритъм. За постигане на най-добро съотношение на компресия можем да използваме индексирани цветови пространства. Предоставеният по-долу код осигурява най-добрата компресия, използвайки само 16 индексирани цветове и алгоритъм за компресия LZW, но с източниците на цветове, които са лека шумни.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}