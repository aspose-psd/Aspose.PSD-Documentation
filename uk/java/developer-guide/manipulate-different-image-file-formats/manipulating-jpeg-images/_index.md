---
title: Робота з JPEG-зображеннями
type: docs
weight: 20
url: /uk/java/manipulating-jpeg-images/
---

## **Використання класу ExifData для зчитування та зміни тегів JPEG EXIF**


Майже всі цифрові камери (у тому числі смартфони), сканери та інші системи обробки зображень зберігають зображення із інформацією EXIF (Exchangeable Image File). Камера записує налаштування та інформацію про сцену у вихідний файл зображення. Дані EXIF також включають час витримки, дату та час фотографування, фокусну відстань, компенсацію експозиції, зразок вимірювання та використання спалаху. API Aspose.Imaging забезпечило можливість видобування інформації EXIF із заданого зображення дуже легко та просто. Розробники також можуть записувати дані EXIF на зображення або модифікувати наявну інформацію відповідно до своїх потреб. Aspose.Imaging надав клас ExifData для зчитування, запису та модифікації даних EXIF, де простір імен Aspose.PSD.Exif.Enums містить відповідні переліки, використовувані в процесі.
### **Читання даних EXIF**
API Aspose.PSD забезпечує можливість читати дані EXIF з заданого зображення. Нижче наведені кроки демонструють використання класу ExifData для зчитування інформації EXIF із зображення.

- Завантажити PSD-зображення, використовуючи фабричний метод Load.
- Знайти мініатюру JPEG серед ресурсів PSD.
- Витягнути екземпляр класу ExifData.

Витягнути необхідну інформацію та вивести її в консоль.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Запроси за потребою можуть отримати конкретну інформацію, використовуючи наступний фрагмент коду.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Запис та зміна даних EXIF**
За допомогою API Aspose.PSD розробники можуть записувати нову інформацію EXIF та модифікувати наявні дані EXIF на зображенні. Обидва процеси (Запис та Зміна) потребують завантаження зображення та отримання даних EXIF у екземпляр класу ExifData. Після цього можна отримувати доступ до властивостей, які надає клас ExifData, та встановлювати їх відповідно. Зверніть увагу, що зображення для обробки повинні бути зображеннями у форматі JPEG або TIFF, які зазвичай є ескізами PSD. Наведено приклад коду, що демонструє використання:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Вилучення мініатюр із ресурсів PSD**
Мініатюри є зменшеною версією зображень, які використовуються для відображення значущої частини зображення замість повного кадру. Деякі файлів зображень (особливо ті, які зроблені цифровою камерою) містять зображення мініатюри, вбудовані у файл. API Aspose.PSD дозволяє витягти ескізи ресурсів PSD та зберегти їх окремо на диску. Ресурси мініатюр містять властивість ExifData.Thumbnail, яка дозволяє отримувати дані мініатюр. Наведений фрагмент коду демонструє, як цим скористатися.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Використайте вищезазначений підхід для збереження мініатюри в інших підтримуваних форматах файлів. Якщо ви бажаєте експортувати дані мініатюр в інші формати зображень, такі як BMP та PNG, будь ласка, скористайтеся іншими параметрами експорту зображень.


### **Вилучення мініатюр із сегментів JFIF**
Також можливо вилучити мініатюри із сегментів ExifData або JFIF ресурсів PSD. Наступний код показує, як виконати вилучення даних мініатюри із сегментів JFIF або ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Використовуйте вищезазначений підхід для збереження мініатюри в інших підтримуваних форматах файлів. Якщо ви бажаєте експортувати дані мініатюр в інші формати зображень, такі як BMP та PNG, будь ласка, скористайтеся іншими параметрами експорту зображень.
### **Додавання мініатюри до сегменту JFIF**
Фрагмент коду нижче демонструє, як використовувати властивість JFIF.Thumbnail для додавання зображення мініатюри до сегменту JFIF завантаженого PSD-зображення.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Зображення мініатюр з іншою даними сегментів не можуть займати більше 65,545 байтів через специфікацію формату JPEG. У випадку, коли потрібно встановити великі зображення як мініатюру, може виникнути виняток.


### **Додавання мініатюри до сегменту EXIF**
Фрагмент коду нижче показує, як використати властивість ExifData.Thumbnail для додавання зображення мініатюри до сегменту EXIF завантаженого PSD-зображення.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

У цьому випадку API Aspose.PSD не може оцінити розмір мініатюрного зображення, але воно може перевірити розмір всього сегменту даних EXIF. Такий розмір не може перевищувати 65 535 байт.
## **Використання класу JpegExifData для зчитування та модифікації тегів JPEG EXIF**
API Aspose.PSD надає клас JpegExifData, який є ексклюзивним для форматів JPEG зображень для видобування та оновлення інформації EXIF. Ця стаття демонструє використання класу JpegExifData для досягнення того ж самого. Клас Aspose.PSD.Exif.JpegExifData служить контейнером даних EXIF для JPEG зображень і надає засоби для видобування стандартних тегів JPEG EXIF, як продемонстровано нижче:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Повний перелік тегів EXIF**
Вищезазначений фрагмент коду читає кілька тегів EXIF, використовуючи властивості, які пропонує клас Aspose.PSD.Exif.JpegExifData. Повний перелік цих властивостей доступний тут. Наступний код прочитає всі теги EXIF за допомогою класу System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Автоматична корекція орієнтації JPEG зображень**
Фотографії можуть бути зроблені камерою обернутою на 90°, 180°, 270° або без обертання (нормальною орієнтацією). Більшість цифрових камер зберігають інформацію про орієнтацію разом із даними зображення як теги EXIF JPEG зображень. Цю інформацію можна використовувати для автоматичного повороту зображень для виправлення орієнтації. API Aspose.PSD надає метод AutoRotate для класу JpegImage для автоматичної корекції орієнтації JPEG зображень. Ось як ви можете використати метод AutoRotate з Aspose.PSD для Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Підтримка JPEG-LS із моделями кольорів CMYK та YCCK**


API Aspose.PSD для Java забезпечує підтримку моделей кольорів CMYK та YCCK із форматом JPEG-LS. Наведений нижче фрагмент коду демонструє використання цієї підтримки для JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Підтримка 2-7 бітів на піксель у зображеннях JPEG-LS**


API Aspose.PSD для Java забезпечує підтримку зображень JPEG-LS з 2-7 бітами на піксель. Наведений нижче фрагмент коду демонструє використання цієї підтримки для JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Встановлення типу кольору та типу стискання для зображень у форматі JPEG**




API Aspose.PSD для Java забезпечує підтримку типу кольору та типу стискання та встановлює їх як відтінки сірого та прогресивні для зображень у форматі JPEG. Наведений нижче фрагмент коду демонструє використання цієї підтримки.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}





