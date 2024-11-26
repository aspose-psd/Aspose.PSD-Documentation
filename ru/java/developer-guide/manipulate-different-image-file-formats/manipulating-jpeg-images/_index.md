---
title: Обработка изображений JPEG
type: docs
weight: 20
url: /ru/java/manipulating-jpeg-images/
---

## **Использование класса ExifData для чтения и изменения тегов JPEG EXIF**


Почти все цифровые камеры (включая смартфоны), сканеры и другие системы обработки изображений сохраняют изображения с информацией EXIF (Exchangeable Image File). Настройки камеры и информация о сцене записываются камерой в файл изображения. Данные EXIF также включают выдержку, дату и время съемки фотографии, фокусное расстояние, компенсацию экспозиции, шаблон замера и сведения о использовании вспышки. API Aspose.Imaging позволяет извлекать информацию EXIF из заданного изображения очень легко и просто. Разработчики также могут записывать данные EXIF на изображения или изменять существующую информацию по своему усмотрению. Aspose.Imaging предоставил класс ExifData для чтения, записи и модификации данных EXIF, а пространство имен Aspose.PSD.Exif.Enums содержит соответствующие перечисления, используемые в процессе.
### **Чтение данных EXIF**
API Aspose.PSD предоставляет средства для чтения данных EXIF из заданного изображения. Ниже приведены шаги, иллюстрирующие использование класса ExifData для чтения информации EXIF из изображения.

- Загрузите изображение PSD с помощью фабричного метода Load.
- Найдите миниатюру JPEG среди ресурсов PSD.
- Извлеките экземпляр класса ExifData.

Извлеките необходимую информацию и выведите ее в консоль.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Кроме того, разработчики могут получить специфическую информацию с помощью следующего фрагмента кода.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Запись и изменение данных EXIF**
С помощью API Aspose.PSD разработчики могут записывать новую информацию EXIF и изменять существующие данные EXIF изображения. Оба процесса (Запись и Изменение) требуют загрузки изображения и получения данных EXIF в экземпляре класса ExifData. Затем можно получить доступ к свойствам, предоставленным классом ExifData, и установить их соответственно. Обратите внимание, что изображения для манипуляций должны быть в формате JPEG или TIFF, которые обычно являются миниатюрами PSD. Пример кода для демонстрации использования представлен ниже:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Извлечение миниатюр из ресурсов PSD**
Миниатюры - это уменьшенные версии изображений, используемые для отображения значительной части изображения вместо полного кадра. Некоторые файлы изображений (особенно снятые цифровой камерой) содержат встроенное миниатюрное изображение в файле. API Aspose.PSD позволяет извлекать миниатюры PSD-ресурсов и сохранять их отдельно на диск. Ресурсы миниатюр содержат свойство ExifData.Thumbnail, которое позволяет извлечь данные миниатюры. Нижеприведенный фрагмент кода демонстрирует способ его использования.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Используйте описанный выше подход для сохранения миниатюры в других поддерживаемых форматах файлов. Если вы хотите экспортировать данные миниатюры в другие форматы изображений, такие как BMP и PNG, используйте другие опции экспорта изображений.


### **Извлечение миниатюр из сегментов JFIF**
Также можно извлечь миниатюры из сегментов ExifData или JFIF ресурсов миниатюр PSD. В следующем коде показано, как выполнять извлечение данных миниатюры из сегмента JFIF или ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Используйте описанный выше подход для сохранения миниатюры в других поддерживаемых форматах файлов. Если вы хотите экспортировать данные миниатюры в другие форматы изображений, такие как BMP и PNG, используйте другие опции экспорта изображений.
### **Добавление миниатюры в сегмент JFIF**
Нижеприведенный фрагмент кода демонстрирует, как использовать свойство JFIF.Thumbnail для добавления миниатюрного изображения в сегмент JFIF загруженного изображения PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Изображения миниатюры с другими данными сегмента не могут занимать более 65 545 байт из-за спецификаций формата JPEG. В случаях, когда в качестве миниатюры устанавливаются большие изображения, может возникнуть исключение.


### **Добавление миниатюры в сегмент EXIF**
Нижеприведенный фрагмент кода демонстрирует, как использовать свойство ExifData.Thumbnail для добавления миниатюрного изображения в сегмент EXIF загруженного изображения PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

В этом случае API Aspose.PSD не может оценить размер изображения миниатюры, но он может проверить размер всего сегмента данных EXIF. Он не может быть больше 65 535 байт.
## **Использование класса JpegExifData для чтения и изменения тегов JPEG EXIF**
API Aspose.PSD предоставляет класс JpegExifData, который предназначен исключительно для форматов изображений JPEG для извлечения и обновления информации EXIF. В этой статье демонстрируется использование класса JpegExifData для достижения того же результата. Класс Aspose.PSD.Exif.JpegExifData служит контейнером данных EXIF для JPEG-изображений и предоставляет средства извлечения стандартных тегов JPEG EXIF, как показано ниже:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Полный список тегов EXIF**
В приведенном выше фрагменте кода читаются несколько тегов EXIF с использованием свойств, предлагаемых классом Aspose.PSD.Exif.JpegExifData. Полный список этих свойств доступен здесь. Далее приведенный код прочтет все теги EXIF с использованием класса System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Автоматическая коррекция ориентации изображений JPEG**
Фотографии могут быть сняты с под углом 90°, 180°, 270° или без изменений (нормальная ориентация). Большинство цифровых камер сохраняют информацию об ориентации вместе с данными изображения в виде тегов EXIF файлов JPEG. Эту информацию можно использовать для автоматической коррекции ориентации изображения. API Aspose.PSD предоставляет метод AutoRotate для класса JpegImage для автоматической коррекции ориентации изображений JPEG. Вот как вы можете использовать метод AutoRotate с API Aspose.PSD для Java.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Поддержка для JPEG-LS с CMYK и YCCK**


API Aspose.PSD для Java предоставляет поддержку моделей цвета CMYK и YCCK с JPEG-LS. Приведенный ниже фрагмент кода демонстрирует использование этой поддержки для JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Поддержка для изображений JPEG-LS с 2-7 бит на пиксель**


API Aspose.PSD для Java предоставляет поддержку изображений JPEG-LS с 2-7 битами на пиксель. Приведенный ниже фрагмент кода демонстрирует использование этой поддержки для JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Установка типа цвета и типа сжатия для изображений JPEG**




API Aspose.PSD для Java предоставляет поддержку типа цвета и типа сжатия и устанавливает их как челночную и прогрессивную для изображений JPEG. Приведенный ниже фрагмент кода демонстрирует использование этой поддержки.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}





