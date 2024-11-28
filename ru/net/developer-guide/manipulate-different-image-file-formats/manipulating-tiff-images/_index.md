---
title: Manipulating TIFF Images
type: docs
weight: 50
url: /ru/net/manipulating-tiff-images/
---

## **Добавление кадров с разными настройками**
TIFF является очень гибким форматом и позволяет добавлять разные кадры с разными размерами, сжатием и другими настройками. API Aspose.PSD позволяет добавлять любой кадр TIFF любого размера, что помогает создавать сложные документы. Если требуется настроить кадры в процессе добавления, чтобы сделать их все одинаковыми, выполните следующие шаги:

- Создайте новый пустой кадр с желаемыми параметрами или скопируйте исходный кадр с указанными параметрами вывода, используя метод CreateFrameFrom.
- Измените размер исходного кадра/изображения на желаемые размеры с помощью метода Resize.
- Добавьте пиксели исходного кадра/изображения в новый кадр.
- Добавьте новый кадр в выходное изображение TIFF.

## **Экспорт слоев изображения PSD в формат файла Multi Page Tiff**
Иногда необходимо экспортировать слои изображения PSD в формат файла Multi-page TIFF. В этой статье будет показано, как выполнить эту задачу с использованием Aspose.PSD для API .NET. Сначала мы загрузим изображение PSD с диска. Затем мы переберем слои изображения PSD и создадим TiffFrame из соответствующих слоев. Наконец, мы сохраним результирующее изображение TIFF в единый файл на диске.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **Конфигурация TiffOptions**
Разработчики могут настраивать различные свойства класса [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) для получения нужных результатов. В этом документе мы сосредоточимся на 4 основных свойствах, которые управляют атрибутами результирующего изображения.

Эти свойства перечислены ниже.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

При инициализации пустой структуры TiffOptions каждая опция установлена на свое значение по умолчанию, например сжатие установлено на None, BitsPerSample установлен как 1, а Photometric как MinIsWhite. Сохранение в этом формате приведет к тому, что окончательное изображение будет черно-белым, и это ожидаемое поведение для таких комбинаций параметров. Для получения цветных результатов необходимо установить все вышеупомянутые свойства на значения, соответствующие желаемому цветовому пространству, или можно инициализировать структуру TiffOptions с предварительными настройками, как обсуждается позже в этой статье. Ниже приведена таблица, описывающая ожидаемые значения параметров, которые можно установить для достижения желаемых результатов. Обратите внимание, что все 4 столбца должны быть установлены через TiffOptions, чтобы сохранить любой загруженный/созданный образ в формате TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16 (palette, цветовой режим) только один канал|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (оттенки серого) только один канал|None|
|Palette|LZW/Uncompressed|8 (палитра, цветовой режим) только один канал|Horizontal (более эффективное сжатие для LZW одинаковых шаблонов)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (оттенки серого) только один канал|Horizontal (более эффективное сжатие для LZW одинаковых шаблонов)|
|RGB|LZW/Uncompressed|[8,8,8] (3 RGB канала)|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 RGB канала и дополнительный альфа-канал может быть установлен через TiffOptions.AlphaStorage) Фактически поддерживается любое количество дополнительных каналов, но каждый канал должен иметь размер 8 бит, например [8,8,8,8,8,8]|None/Horizontal|
Все 4 свойства должны быть установлены через TiffOptions, чтобы сохранить любой формат изображения в формате Tiff. При использовании различных комбинаций некоторые просмотрщики (включая Просмотр фотографий Windows) могут отказаться отображать окончательное изображение из-за ограниченной поддержки, которую они предлагают. В таком случае выберите другой просмотрщик для тестирования.
### **Предварительные настройки для TiffOptions**
Для облегчения использования пользователям и предотвращения ошибочной конфигурации экземпляра TiffOptions, API Aspose.PSD для .NET предоставляет другой конструктор, который принимает параметр типа [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Исходя из выбранного значения из перечисления TiffExpectedFormat, API автоматически настраивает все обязательные свойства для экземпляра TiffOptions для получения желаемых результатов. Прежде чем мы перейдем к примеру кода, вот список полей TiffExpectedFormat и их описание для лучшего понимания использования.


- TiffExpectedFormat.Default: Установка поля на Default работает аналогично конструктору по умолчанию класса TiffOptions без установки сжатия и BitsPerPixel на 1 для создания черно-белого результата. Рекомендуется использовать это поле, когда другие специфичные для формата свойства должны быть установлены вручную в соответствии с желаемыми результатами.
- TiffExpectedFormat.TiffCcitRle: Специфично для кодирования RLE при сохранении результата в формате TIFF с 1 бит на пиксель (черно-белый).
- TiffExpectedFormat.TiffCcittFax3: Специфично для кодирования CCITT Fax3 при сохранении результата в формате TIFF с 1 бит на пиксель (черно-белый).
- TiffExpectedFormat.TiffCcittFax4: Специфично для кодирования CCITT Fax4 при сохранении результата в формате TIFF с 1 бит на пиксель (черно-белый).
- TiffExpectedFormat.TiffDeflateBW: Специфично для сжатия Deflate при сохранении результата в формате TIFF с 1 бит на пиксель (черно-белый).
- TiffExpectedFormat.TiffDeflateRGB: Специфично для сжатия Deflate при сохранении результата в формате TIFF с цветным изображением.
- TiffExpectedFormat.TiffJpegRGB: Специфично для сжатия JPEG при сохранении результата в формате TIFF с цветным изображением.
- TiffExpectedFormat.TiffJpegYCBCR: Специфично для сжатия JPEG при сохранении результата в формате TIFF с цветным изображением на основе YCBCR.
- TiffExpectedFormat.TiffLzwBW: Специфично для сжатия LZW при сохранении результата в формате TIFF с 1 бит на пиксель (черно-белый).
- TiffExpectedFormat.TiffLzwRGB: Специфично для сжатия LZW при сохранении результата в формате TIFF с цветным изображением.
- TiffExpectedFormat.TiffLzwRGBA: Специфично для сжатия LZW при сохранении результата в формате TIFF с цветным изображением и прозрачностью.
- TiffExpectedFormat.TiffNoCompressionBW: Специфично для несжатого формата TIFF при сохранении результата с 1 бит на пиксель (черно-белый).
- TiffExpectedFormat.TiffNoCompressionRGB: Специфично для несжатого формата TIFF при сохранении результата с цветным изображением.
- TiffExpectedFormat.TiffNoCompressionRGBA: Специфично для несжатого формата TIFF при сохранении результата с цветным изображением и прозрачностью.



Нижеприведенный фрагмент кода поясняет использование полей TiffExpectedFormat при создании экземпляра класса TiffOptions.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **Поддержка сжатия Deflate и Adobe Deflate**
Формат файла TIFF (Tagged Image File Format) поддерживает различные типы сжатия, причем тип сжатия сохраняется как тег (целочисленное значение) в файле. Одним из таких методов сжатия является Adobe Deflate (ранее известный как Deflate). API Aspose.PSD для .NET поддерживает этот метод сжатия для экспорта и создания изображений TIFF.
### **Сохранение изображения в TIFF с сжатием Deflate**
Преобразование загруженных изображений в TIFF с сжатием Deflate/Adobe Deflate происходит легко следующим образом.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Создание TiffImage с сжатием Adobe Deflate**
Ниже приведен пример использования Aspose.PSD для API .NET для создания изображения с нуля с использованием метода сжатия Adobe Deflate.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Сжатие изображений TIFF**
API Aspose.PSD для .NET может использоваться для преобразования изображений PSD в формат изображений TIFF и даже изменения сжатия результирующего изображения TIFF. API также можно использовать для сохранения различных изображений как кадров в изображении TIFF для архивации, сжимая изображения до минимального размера данных. Сжатие изображения в любом случае должно выполняться путем уменьшения размера исходных данных независимо от используемого алгоритма сжатия. Для достижения наилучшего коэффициента сжатия мы можем использовать индексированные цветовые пространства. Нижеприведенный фрагмент кода выполняет лучшее сжатие, используя только 16 индексированных цветов и алгоритм сжатия LZW, хотя цвета исходных данных немного дизерированы.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}
