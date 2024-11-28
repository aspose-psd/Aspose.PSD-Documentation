---
title: Преобразование изображений
type: docs
weight: 20
url: /ru/net/converting-images/
---

## **Преобразование изображений в черно-белые и градации серого**
Иногда вам может понадобиться преобразовать цветные изображения в черно-белые или градации серого для печати или архивирования. В этой статье демонстрируется использование API Aspose.PSD для .NET для достижения этой цели с использованием двух методов, описанных ниже.

- Бинаризация
- Преобразование в градации серого
### **Бинаризация**
Чтобы понять концепцию бинаризации, важно определить бинарное изображение; это цифровое изображение, у которого может быть только два возможных значения для каждого пикселя. Обычно два цвета, используемые для бинарного изображения, - черный и белый, хотя можно использовать любые два цвета. Бинаризация - это процесс преобразования изображения в бивалентное, что означает, что каждый пиксель сохраняется как один бит (0 или 1), где 0 обозначает отсутствие цвета, а 1 означает наличие цвета. API Aspose.PSD для .NET в настоящее время поддерживает два метода бинаризации.
#### **Бинаризация с фиксированным порогом**
В следующем фрагменте кода показано, как использовать фиксированную бинаризацию порога на изображении.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Бинаризация с порогом Отсу**
В следующем фрагменте кода показано, как применить бинаризацию с порогом Отсу к изображению.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Преобразование в градации серого**
Градации серого - это процесс преобразования изображения с непрерывным тоном в изображение с дискретными оттенками серого. В следующем фрагменте кода показано, как использовать преобразование в градации серого.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}

## **Преобразование слоев изображения GIF в изображение TIFF**
Иногда необходимо извлечь и преобразовать слои изображения PSD в другой растровый формат изображения для выполнения определенной задачи. API Aspose.PSD поддерживает функцию извлечения и преобразования слоев изображения PSD в другой растровый формат изображения. Сначала мы создадим экземпляр изображения и загрузим изображение PSD с локального диска, затем переберем каждый слой в свойстве Layer. Затем мы преобразуем блок в изображение TIFF. В следующем фрагменте кода показано, как преобразовать слои изображения PSD в TIFF изображения.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}

## **Преобразование CMYK PSD в CMYK TIFF**
С помощью Aspose.PSD для .NET разработчики могут преобразовывать файлы CMYK PSD в формат CMYK tiff. В этой статье показано, как экспортировать/преобразовать файл CMYK PSD в формат tiff CMYK с помощью Aspose.PSD. С помощью Aspose.PSD для .NET можно загружать изображения PSD, а затем устанавливать различные свойства с использованием [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) класса и сохранять или экспортировать изображение. В следующем фрагменте кода показано, как достичь этой функции.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}

## **Экспорт изображений**
Помимо богатого набора обработчиков изображений, Aspose.PSD предоставляет специализированные классы для преобразования форматов файлов PSD в другие форматы. Используя эту библиотеку, конвертация изображений PSD является очень простой и интуитивно понятной. Вот некоторые специализированные классы для этой цели в [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) пространстве имен:

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Экспортировать изображения PSD с Aspose.PSD для .NET API легко. Вам просто нужен объект соответствующего класса из [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) пространства имен. Используя эти классы, вы легко можете экспортировать любое изображение, созданное, отредактированное или просто загруженное с помощью Aspose.PSD для .NET в любой поддерживаемый формат.

## **Объединение изображений**
Этот пример использует класс Graphics и показывает, как объединить два или более изображений в одно общее изображение. Для демонстрации операции пример создает новое PsdImage и рисует изображения на поверхности холста, используя метод DrawImage, предоставленный классом Graphics. С использованием класса Graphics два или более изображений могут быть объединены таким образом, что результирующее изображение будет выглядеть как целое изображение без промежутков между частями изображения и страниц. Размер холста должен быть равен размеру результирующего изображения. Ниже приведен демонстрационный код, показывающий, как использовать метод [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) класса [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), чтобы объединить изображения в одно изображение.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **Расширение и обрезка изображений**
API Aspose.PSD позволяет вам расширять или обрезать изображение во время процесса преобразования изображения. Разработчику необходимо создать прямоугольник с координатами X и Y, а также указать ширину и высоту прямоугольника. X, Y, ширина и высота прямоугольника будут изображать расширение или обрезку загруженного изображения. Если требуется расширить или обрезать изображение во время преобразования изображения, выполните следующие шаги:

1. Создайте экземпляр класса [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) и загрузите существующее изображение.
1. Создайте экземпляр класса ImageOption.
1. Создайте экземпляр класса [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) и инициализируйте координаты X, Y и ширину, высоту прямоугольника.
1. Вызовите метод [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) класса RasterImage, передавая имя выходного файла, параметры изображения и объект прямоугольника в качестве параметров.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **Чтение и запись данных XMP в изображения**
XMP (Extensible Metadata Platform) - это стандарт ISO. XMP стандартизирует модель данных, формат сериализации и основные свойства для определения и обработки расширяемых метаданных. Он также предоставляет рекомендации по встраиванию информации XMP в популярное изображение, такое как JPEG, не нарушая их читаемость приложениями, которые не поддерживают XMP. С помощью Aspose.PSD для .NET API разработчики могут читать или записывать метаданные XMP в изображения. В этой статье показано, как метаданные XMP могут быть прочитаны из изображения и записаны в изображения.
### **Создание метаданных XMP, запись и чтение из файла**
С помощью пространства имен Xmp разработчик может создать объект метаданных XMP и записать его в изображение. Ниже приведен фрагмент кода, показывающий, как использовать пакеты XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage и DublinCorePackage, содержащиеся в пространстве имен [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}

## **Экспорт изображений в многопоточной среде**
Aspose.PSD для .NET теперь поддерживает преобразование изображений в многопоточной среде. Aspose.PSD для .NET гарантирует оптимальную производительность операций во время выполнения кода в многопоточной среде. Все классы опций изображения (например BmpOptions, TiffOptions, JpegOptions и т. д.) в Aspose.PSD для .NET реализуют интерфейс IDisposable. Поэтому разработчику необходимо правильно освободить объект класса опций изображения в случае, если свойство Source задано. Ниже приведен фрагмент кода, демонстрирующий указанную функциональность.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD теперь поддерживает свойство SyncRoot при работе в многопоточной среде. Разработчик может использовать это свойство для синхронизации доступа к исходному потоку. Ниже приведен фрагмент кода, демонстрирующий использование свойства SyncRoot.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}
