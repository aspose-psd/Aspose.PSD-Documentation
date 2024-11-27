---
title: Промяна на JPEG изображения
type: docs
weight: 20
url: /bg/java/manipulating-jpeg-images/
---

## **Използване на класа ExifData за четене и промяна на JPEG EXIF тагове**

Почти всички цифрови фотоапарати (включително смартфони), скенери и други системи за обработка на изображения запазват изображенията с информация за обмяна на файлове (EXIF). Настройките на камерата и информацията за сцената се записват от камерата във файл на изображението. Данните EXIF включват също скорост на затвора, дата и час на заснемане на снимка, фокусно разстояние, компенсация на експонацията, образец на метриране и дали е използвана светкавица. API на Aspose.Imaging е направило възможно да се извлича информацията за EXIF от дадено изображение по много лесен и прост начин. Разработчиците могат също да пишат данни EXIF върху изображенията или да променят съществуващата информация според техните изисквания. Aspose.Imaging предоставя клас ExifData за четене, писане и модифициране на данните EXIF, където Aspose.PSD.Exif.Enums пространството от имена съдържа съответните изчисления, използвани в процеса.
### **Четене на данните EXIF**
API-тата на Aspose.PSD предоставят начини за четене на данни EXIF от дадено изображение. Предоставените по-долу стъпки илюстрират използването на класа ExifData за четене на информацията EXIF от изображение.

- Заредете PSD изображение, използвайки фабричния метод Load.
- Намерете JPEG миниатюрата сред ресурсите на PSD.
- Извлечете екземпляр на класа ExifData.

Извлечете необходимата информация и я запишете в конзолата.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}

По-друг начин, разработчиците могат да получат специфична информация, използвайки следния код.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Писане и модифициране на данни EXIF**
С помощта на API-тата на Aspose.PSD, разработчиците могат да пишат нова информация EXIF и да модифицират съществуващи данни EXIF на изображение. И двете процеси (Писане и Модифициране) изискват зареждане на изображение и вземане на данните EXIF в екземпляр на класа ExifData. След това може да се достъпят свойствата, изложени от класа ExifData, за да се зададат съответно. Моля, обърнете внимание, че изображенията за манипулация трябва да бъдат JPEG или TIFF изображения, които обикновено са миниатюри PSD. Примерен код, демонстриращ употребата, е както следва:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Извличане на миниатюри от ресурсите на PSD**
Миниатюрите са версии на изображения с намален размер, използвани за показване на значителна част от изображението вместо пълния кадър. Някои файлове с изображения (особено тези, заснети с цифрова камера) съдържат миниатюрно изображение, вградено във файла. Aspose.PSD API позволява да се извличат миниатюри на PSD ресурси и да се запазят отделно на диск. Ресурсите за миниатюри съдържат свойството ExifData.Thumbnail, което може да вземе миниатюрните данни. Предоставеният по-долу откъс от код демонстрира как да се използва това.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

Използвайте подхода, обсъден по-горе, за да запазите миниатюрата в други поддържани формати за файлове. Ако искате да експортирате данни за миниатюрата към други формати за изображения като BMP и PNG, моля, използвайте други опции за експортиране на изображения.
### **Извличане на миниатюри от сегменти на JFIF**
Също така е възможно да се извлекат миниатюри от сегментите JFIF или ExifData на PSD миниатюри. Следният код показва как да се извърши извличането на данните за миниатюрата от сегмента JFIF или ExifData:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

Използвайте подхода, разгледан по-горе, за да запазите миниатюрата в други поддържани формати за файлове. Ако искате да експортирате данни за миниатюрата към други формати за изображения като BMP и PNG, моля, използвайте други опции за експортиране на изображения.
### **Добавяне на миниатюра към сегмент JFIF**
Предоставеният по-долу откъс от кода демонстрира как да използвате свойството JFIF.Thumbnail, за да добавите миниатюрно изображение към сегмента JFIF на заредено PSD изображение.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Миниатюрните изображения с други данни на сегменти не могат да заемат повече от 65 545 байта поради спецификациите на формата JPEG. В случаи, когато се използват големи изображения като миниатюри, може да възникнат изключения.
### **Добавяне на миниатюра към сегмента EXIF**
Предоставеният по-долу откъс от кода демонстрира как да използвате свойството ExifData.Thumbnail, за да добавите миниатюрно изображение към сегмента EXIF на заредено PSD изображение.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

В този случай API на Aspose.PSD не може да оцени размера на миниатюрното изображение, но може да провери размера на целия сегмент с данни EXIF. Този размер не може да бъде по-голям от 65 535 байта.
## **Използване на класа JpegExifData за четене и промяна на JPEG EXIF тагове**

API-тата на Aspose.PSD предоставят клас JpegExifData, който е ексклузивен за форматите на JPEG изображения, за да се извлекат и актуализират данни EXIF. Тази статия демонстрира употребата на класа JpegExifData за постигане на същото. Класът Aspose.PSD.Exif.JpegExifData служи като контейнер на данни EXIF за JPEG изображения и предоставя начини за извличане на стандартни JPEG EXIF тагове, както е показано по-долу:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Пълен списък на EXIF таговете**
Горният откъс от кода чете няколко EXIF тага, използвайки свойствата, предлагани от класа Aspose.PSD.Exif.JpegExifData. Пълен списък на тези свойства е наличен тук. Следният код ще прочете всички EXIF тагове, използвайки класа System.Reflection.PropertyInfo.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Автоматично коригиране на ориентацията на JPEG изображенията**
Снимките може да се заснемат с камера завъртяна на 90°, 180°, 270° или никаква (нормална ориентация). Повечето цифрови фотоапарати запазват информацията за ориентацията заедно с данните за изображението като EXIF тагове на JPEG изображенията. Тази информация може да бъде използвана за извършване на автоматичното завъртане на изображенията, за да се коригира ориентацията. API-тата на Aspose.PSD предоставят метода AutoRotate за класа JpegImage, за автоматичната корекция на ориентацията на JPEG изображенията. Ето как можете да използвате метода AutoRotate с Aspose.PSD за Java API.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Поддръжка за JPEG-LS с CMYK и YCCK**
API-тата на Aspose.PSD за Java предоставят поддръжка за модели на цветовете CMYK и YCCK с JPEG-LS. Откъсът от кода по-долу демонстрира как да се използва тази поддръжка за JPEG-LS.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Поддръжка за JPEG-LS изображения с 2-7 бита на отсечка**
API-тата на Aspose.PSD за Java предоставят поддръжка за изображения с 2-7 бита на отсечка с JPEG-LS. Откъсът от кода по-долу демонстрира как да се използва тази поддръжка за JPEG-LS.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Задаване на ColorType и CompressionType за JPEG изображения**

API-тата на Aspose.PSD за Java предоставят поддръжка за Color Type и Compression Type и задават техните стойности като градации на сивото и прогресивен режим за JPEG изображения. Откъсът от кода по-долу демонстрира как да се използва тази поддръжка.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}