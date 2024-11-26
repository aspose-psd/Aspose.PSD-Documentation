---
title: Обработка изображений JPEG
type: docs
weight: 30
url: /ru/net/manipulating-jpeg-images/
---

## **Использование класса ExifData для чтения и изменения меток Jpeg EXIF**
Почти все цифровые камеры (включая смартфоны), сканеры и другие системы обработки изображений сохраняют изображения с информацией об EXIF (Exchangeable Image File). Настройки камеры и информация о сцене записываются камерой в файл изображения. Данные EXIF также включают выдержку, дату и время съемки фотографии, фокусное расстояние, экспозиционную компенсацию, шаблон замера и использование вспышки. API Aspose.Imaging позволяет извлекать информацию EXIF из заданного изображения очень легко и просто. Разработчики также могут записывать данные EXIF в изображения или изменять существующую информацию в соответствии с их требованиями. Aspose.PSD предоставляет класс [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) для чтения, записи и изменения данных EXIF, а пространство имен [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) содержит соответствующие перечисления, используемые в процессе.
### **Чтение данных EXIF**
API Aspose.PSD предоставляет возможность чтения данных EXIF из заданного изображения. На приведенных ниже шагах показано использование класса ExifData для чтения информации EXIF из изображения.

- Загрузите изображение PSD с помощью фабричного метода Load.
- Найдите миниатюру Jpeg среди ресурсов PSD.
- Извлеките экземпляр класса ExifData.

Извлеките необходимую информацию и выведите ее в консоль.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Кроме того, разработчики могут получить конкретную информацию, используя следующий фрагмент кода.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Запись и изменение данных EXIF**
С помощью API Aspose.PSD разработчики могут записывать новую информацию EXIF и изменять существующие данные EXIF изображения. Оба процесса (запись и изменение) требуют загрузки изображения и получения данных EXIF в экземпляре класса ExifData. Затем можно получить доступ к свойствам, предоставляемым классом ExifData, и установить их соответственно. Обратите внимание, что изображения для манипуляций должны быть Jpeg или Tiff изображениями, которые обычно являются миниатюрами PSD. Пример кода для демонстрации использования приведен ниже:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Извлечение миниатюр из ресурсов PSD**
Миниатюры - это уменьшенные версии изображений, используемые для отображения значительной части изображения вместо всего кадра. Некоторые изображения (особенно те, что сделаны с цифровой камерой) содержат миниатюру встроенную в файл. API Aspose.PSD позволяет извлекать миниатюры PSD-ресурсов и сохранять их отдельно на диск. Ресурсы миниатюр содержат свойство ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail), которое может извлечь данные миниатюры. Приведенный ниже фрагмент кода демонстрирует, как его использовать.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Используйте описанный выше подход для сохранения миниатюры в других поддерживаемых форматах файлов. Если вы хотите экспортировать данные миниатюры в другие форматы изображений, такие как BMP и PNG, пожалуйста, используйте другие опции экспорта изображений.


### **Извлечение миниатюр из сегментов JFIF**
Также возможно извлечь миниатюры из сегментов ExifData или JFIF ресурсов миниатюр PSD. В следующем коде показано, как выполнить извлечение данных миниатюры из сегмента JFIF или ExifData:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Используйте описанный выше подход для сохранения миниатюры в других поддерживаемых форматах файлов. Если вы хотите экспортировать данные миниатюры в другие форматы изображений, такие как BMP и PNG, пожалуйста, используйте другие опции экспорта изображений.
### **Добавить миниатюру в сегмент JFIF**
Фрагмент кода ниже демонстрирует, как использовать свойство JFIF. Thumbnail для добавления миниатюрного изображения в сегмент JFIF загруженного изображения PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Изображения миниатюр с другими данными сегментов не могут занимать более 65 545 байт из-за спецификаций формата JPEG. В случае, если большие изображения должны быть установлены в качестве миниатюры, может возникнуть исключение.


### **Добавить миниатюру в сегмент EXIF**
Фрагмент кода ниже демонстрирует, как использовать свойство ExifData.Thumbnail для добавления миниатюрного изображения в сегмент EXIF загруженного изображения PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


В этом случае API Aspose.PSD не может оценить размер миниатюры, но может проверить размер всего сегмента данных EXIF. Он не может превышать 65 535 байт.
## **Использование класса JpegExifData для чтения и изменения меток Jpeg EXIF**
API Aspose.PSD предоставляет класс [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata), который является эксклюзивным для форматов изображений Jpeg для извлечения и обновления информации EXIF. В данной статье демонстрируется использование класса JpegExifData для достижения того же результата. Класс Aspose.PSD.Exif.JpegExifData служит контейнером данных EXIF для изображений Jpeg и предоставляет возможности для извлечения стандартных меток Jpeg EXIF, как показано ниже:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Полный список меток EXIF**
Приведенный выше фрагмент кода читает несколько меток EXIF, используя свойства, предоставляемые классом Aspose.PSD.Exif.JpegExifData. Полный список этих свойств доступен здесь. Следующий код прочтет все метки EXIF, используя [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) класс.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Автокоррекция ориентации изображений JPEG**
Изображения могут быть сняты камерой, повернутой на 90°, 180°, 270° или без поворота (нормальная ориентация). Большинство цифровых камер сохраняют информацию об ориентации вместе с данными изображения в виде меток EXIF изображений JEPG. Эту информацию можно использовать для выполнения автоматической коррекции ориентации изображений. API Aspose.PSD предоставляет метод AutoRotate для класса JpegImage для автоматической коррекции ориентации изображений JPEG. Вот как вы можете использовать метод AutoRotate с API Aspose.PSD для .NET.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Поддержка JPEG-LS с CMYK и YCCK**
API Aspose.PSD для .NET предоставляет поддержку моделей CMYK и YCCK с JPEG-LS. Приведенный ниже фрагмент кода демонстрирует, как использовать эту поддержку для JPEG-LS.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Поддержка 2-7 бит на выборку в изображениях JPEG-LS**
API Aspose.PSD для .NET предоставляет поддержку изображений JPEG-LS с 2-7 битами на выборку. Приведенный ниже фрагмент кода демонстрирует, как использовать эту поддержку для JPEG-LS.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Установка типа цвета и типа сжатия для изображений JPEG**

API Aspose.PSD для .NET позволяет устанавливать тип цвета и тип сжатия и устанавливать их в оттенки серого и прогрессивный для изображений JPEG. Приведенный ниже фрагмент кода демонстрирует, как использовать эту поддержку.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}



Фрагмент кода ниже демонстрирует использование свойства ExifData.Thumbnail для добавления миниатюрного изображения в сегмент EXIF загруженного изображения PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}



В этом случае API Aspose.PSD не может оценить размер миниатюры, но может проверить размер всего сегмента данных EXIF. Он не может превышать 65 535 байт.
