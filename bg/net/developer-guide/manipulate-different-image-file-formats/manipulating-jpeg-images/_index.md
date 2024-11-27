---
title: Обработка на JPEG изображения
type: docs
weight: 30
url: /bg/net/manipulating-jpeg-images/
---

## **Използване на класа ExifData за четене и промяна на Jpeg EXIF тагове**
Почти всички цифрови камери (включително смартфони), скенери и други системи, които обработват изображения, запазват изображения с информация EXIF (Exchangeable Image File). Камерите записват настройките и информацията за сцената в изображението. Информацията EXIF включва също скорост на затвора, дата и час на снимката, фокусно разстояние, корекция на експонацията, зоната за измерване и дали е бил използван светкавицата. Aspose.Imaging APIs позволяват извличането на информацията EXIF от дадено изображение по много лесен и прост начин. Разработчиците могат също така да пишат данни EXIF към изображенията или да променят съществуващата информация според своите изисквания. Aspose.PSD предлага класа [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) за четене, писане и промяна на данните EXIF, докато пространството имена [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) съдържа съответните изброителни типове, използвани в процеса.
### **Четене на данните EXIF**
Aspose.PSD APIs предоставят възможност за четене на данни EXIF от дадено изображение. Предоставените по-долу стъпки илюстрират използването на класа ExifData за четене на информацията EXIF от изображение.

- Зареждане на PSD изображението чрез метода фабрика Load.
- Намиране на Jpeg миниатюра сред ресурсите на PSD.
- Извличане на екземпляр на класа ExifData.

Извличане на необходимата информация и записване на конзолата.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Освен това, разработчиците също могат да получат определена информация, използвайки следния откъс код.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Писане и промяна на данни EXIF**
Използвайки Aspose.PSD APIs, разработчиците могат да пишат нова информация EXIF и да променят съществуващите данни EXIF на изображение. И двете процеса (Писане и Промяна) изискват зареждане на изображение и взимане на данните EXIF в екземпляр на класа ExifData. След това може да се достъпят свойствата, изложени от класа ExifData, за да се зададат съответно. Моля, обърнете внимание, че изображенията за манипулация трябва да бъдат Jpeg или Tiff изображения, които обикновено са миниатюрите на PSD. Примерен код за демонстрация на използването е следният:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Извличане на миниатюри от ресурсите на PSD**
Миниатюрите са намалени версии на изображения, използвани за показване на значима част от изображението вместо пълния кадър. Някои изображения (особено тези, заснети с цифрова камера) включват миниатюрно изображение, вградено във файл. Aspose.PSD API позволява извличането на миниатюри от ресурсите на PSD и запазването им поотделно на диск. Ресурсите за миниатюри включват свойство ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail), което може да извлече данните за миниатюрата. Долният примерен код показва как да се използва това.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Използвайте посочения по-горе подход, за да запазите миниатюрата в други поддържани формати за файлове. Ако желаете да експортирате данните за миниатюрата към други формати за изображения, като BMP и PNG, моля, използвайте други опции за експорт на изображения.
### **Извличане на миниатюри от сегментите JFIF**
Също така е възможно да извлечете миниатюри от сегментите ExifData или JFIF на ресурсите за миниатюри на PSD. Следният код показва как да извършите извличането на данни за миниатюри от сегмента JFIF или ExifData:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Използвайте посочения по-горе подход, за да запазите миниатюрата в други поддържани формати за файлове. Ако желаете да експортирате данните за миниатюрата към други формати за изображения, като BMP и PNG, моля, използвайте други опции за експорт на изображения.
### **Добавяне на миниатюра към сегмента JFIF**
Долният откъс код показва как да се използва свойството JFIF. Thumbnail, за да се добави миниатюрно изображение към JFIF сегмента на заредено PSD изображение.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Миниатюрните изображения с други данни от сегмента не могат да бъдат повече от 65,545 байта поради спецификациите на формата JPEG. В случай, че се опитвате да зададете големи изображение като миниатюра, може да възникне изключение.
### **Добавяне на миниатюра към сегмента EXIF**
Долният откъс код показва как да се използва свойството ExifData.Thumbnail, за да се добави миниатюрно изображение към сегмента EXIF на заредено PSD изображение.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


В този случай, Aspose.PSD API не може да оцени размера на миниатюрното изображение, но може да провери размера на целия сегмент с данни за EXIF. Този размер не може да бъде по-голям от 65,535 байта.
## **Използване на класа JpegExifData за четене и промяна на Jpeg EXIF тагове**
Aspose.PSD APIs предлагат класа [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata), който е ексклузивен за Jpeg изображенията, за извличане и актуализация на информацията EXIF. Този членеклас JpegExifData на Aspose.PSD.Exif.JpegExifData служи като контейнер за данните EXIF за Jpeg изображения и предоставя възможност за извличане на стандартните Jpeg EXIF тагове, както е показано по-долу:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Пълен списък на EXIF таговете**
Горният откъс код чете няколко EXIF тага, използвайки свойствата, предлагани от класа Aspose.PSD.Exif.JpegExifData. Пълният списък с тези свойства е наличен тук. Следващият код ще прочете всички EXIF тагове, използвайки класа [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0):


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Автоматично коригиране на ориентацията на JPEG изображенията**


Снимките могат да бъдат направени с камера, завъртяна на 90°, 180°, 270° или няма завъртане (нормална ориентация). Повечето цифрови фотоапарати запазват информацията за ориентацията заедно с изображението като етикети EXIF на JPEG изображенията. Тази информация може да се използва за автоматично завъртане на изображенията, за да се коригира ориентацията. Aspose.PSD APIs предлагат метода AutoRotate за класа JpegImage за автоматичното коригиране на ориентацията на JPEG изображенията. Ето как можете да използвате метода AutoRotate с Aspose.PSD за .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Поддръжка за JPEG-LS с CMYK и YCCK**


Aspose.PSD за .NET API предоставя поддръжка за модели на цветове CMYK и YCCK с JPEG-LS. Долният откъс код демонстрира как да се използва тази поддръжка за JPEG-LS.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Поддръжка за 2-7 бита за изображение в JPEG-LS изображения**


Aspose.PSD за .NET API предоставя поддръжка за 2-7 бита за изображение в JPEG-LS изображения. Долният откъс код демонстрира как да се използва тази поддръжка за JPEG-LS.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Задаване на ColorType и CompressionType за JPEG изображения**





Aspose.PSD за .NET API предоставя поддръжка за Color Type и Compression Type и ги задава като градации на сиво и прогресивно за JPEG изображения. Долният откъс код демонстрира как да се използва тази поддръжка.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}




Долният откъс код демонстрира как да се използва свойството ExifData.Thumbnail, за да се добави миниатюрно изображение към сегмента EXIF на заредено PSD изображение.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

В този случай, Aspose.PSD API не може да оцени размера на миниатюрното изображение, но може да провери размера на целия сегмент с данни за EXIF. Този размер не може да бъде по-голям от 65,535 байта.