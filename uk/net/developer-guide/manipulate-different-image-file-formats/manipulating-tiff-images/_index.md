---
title: Обробка зображень у форматі TIFF
type: docs
weight: 50
url: /uk/net/manipulating-tiff-images/
---

## **Додавання кадрів з різними налаштуваннями**
TIFF - це дуже гнучкий формат, який дозволяє додавати різні кадри з різними розмірами, стисненням та іншими налаштуваннями. API Aspose.PSD дозволяє додавати будь-який кадр TIFF будь-якого розміру, що допомагає у створенні складних документів. Якщо є вимога під час процесу додавання налаштовувати кадри, щоб зробити їх однаковими, виконайте наступні кроки:

- Створіть новий порожній кадр із бажаними параметрами або скопіюйте вихідний кадр із зазначеними параметрами виведення, використовуючи метод CreateFrameFrom.
- Змініть розмір вихідного кадру/зображення на потрібні розміри за допомогою методу Resize.
- Додайте пікселі вихідного кадру/зображення до нового кадру.
- Додайте новий кадр до вихідного зображення TIFF.

## **Експорт шарів зображення PSD у формат Multi Page Tiff**
Іноді вам потрібно експортувати шари зображення PSD у формат файлу Multi-page TIFF. У цій статті буде продемонстровано, як ми можемо виконати це завдання, використовуючи API Aspose.PSD для .NET. Спочатку ми завантажимо зображення PSD з диска. Потім ми будемо проходити шарами зображення PSD та створювати TiffFrame з відповідних шарів. Нарешті, ми збережемо отримане Tiff зображення в один файл на диску.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **Налаштування TiffOptions**
Розробники можуть настроювати різні властивості класу [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions), щоб отримати бажані результати. У цьому документі ми зосередимось на 4 основних властивостях, які контролюють атрибути результируючого зображення.

Ці властивості перераховані нижче.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Кожна опція при ініціалізації пустої структури TiffOptions встановлюється в його значення за замовчуванням, наприклад, стиснення встановлено як None, BitsPerSample встановлений як 1, Photometric як MinIsWhite. Зберігання у цьому форматі зробить кінцеве зображення чорно-білим, і це очікувана поведінка для таких комбінацій опцій. Для отримання кольорового результату вам потрібно встановити всі вищезгадані властивості на значення, які відповідають бажаному кольоровому простору або ви можете ініціалізувати структуру TiffOptions із попередньо встановленими налаштуваннями, як обговорено пізніше в цій статті. Наведено таблицю, що описує передбачені значення параметрів, які можна встановити для досягнення бажаних результатів. Зверніть увагу, що вам потрібно встановити всі 4 стовпці через TiffOptions, щоб зберегти будь-яке завантажене/створене зображення у форматі TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16 (палітра, кольоровий режим) лише один канал|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (відтінки сірого) лише один канал|None|
|Palette|LZW/Uncompressed|8 (палітра, кольоровий режим), лише один канал|Horizontal (досягається більше стиснення для LZW однакових візирків)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (відтінки сірого) лише один канал|Horizontal (досягається більше стиснення для LZW однакових візирків)|
|RGB|LZW/Uncompressed|[8,8,8] (3 RGB канали)|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 RGB канали та додатковий альфа-канал може бути встановлений через TiffOptions.AlphaStorage) Фактично будь-яка кількість додаткових каналів підтримується, але кожен канал повинен мати розмір 8 біт, наприклад, [8,8,8,8,8,8]|None/Horizontal|
Всі 4 властивості повинні бути встановлені через TiffOptions, щоб зберегти будь-який формат зображення у форматі Tiff. При використанні різних комбінацій деякі переглядачі (включаючи Віджет відображення фотографій у Windows) можуть відмовитися від відображення отриманого зображення через обмежену підтримку, яку вони пропонують. У такому випадку, будь ласка, виберіть інший переглядач для вашого тестування.
### **Попередні налаштування для класу TiffOptions**
Для зручності користувачів та уникнення невірної конфігурації екземпляра TiffOptions, API Aspose.PSD для .NET виклав інший конструктор, який приймає параметр типу [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Залежно від вибраного значення з переліку TiffExpectedFormat, API автоматично конфігурує всі обов'язкові властивості для екземпляра TiffOptions для отримання бажаного результату. Перш ніж ми перейдемо до прикладного коду, ось список полів TiffExpectedFormat і їх деталі для кращого розуміння використання.


- TiffExpectedFormat.Default: Встановлення поля в значення Default працює аналогічно конструктору за замовчуванням класу TiffOptions без встановлення стиснення та BitsPerPixel, щоб отримати чорно-білий результат. Рекомендується використовувати це поле, коли інші властивості, що властиві конкретному формату, потрібно встановити вручну відповідно до бажаних результатів.
- TiffExpectedFormat.TiffCcitRle: Специфічний для кодування RLE під час збереження результату у форматі TIFF з BitsPerPixel 1 (чорно-білий).
- TiffExpectedFormat.TiffCcittFax3: Специфічний для кодування CCITT Fax3 під час збереження результату у форматі TIFF з BitsPerPixel 1 (чорно-білий).
- TiffExpectedFormat.TiffCcittFax4: Специфічний для кодування CCITT Fax4 під час збереження результату у форматі TIFF з BitsPerPixel 1 (чорно-білий).
- TiffExpectedFormat.TiffDeflateBW: Специфічний для стиснення Deflate під час збереження результату у форматі TIFF з BitsPerPixel 1 (чорно-білий).
- TiffExpectedFormat.TiffDeflateRGB: Специфічний для стиснення Deflate під час збереження результату у форматі TIFF кольоровим (RGB).
- TiffExpectedFormat.TiffJpegRGB: Специфічний для стиснення JPEG під час збереження результату у форматі TIFF кольоровим (RGB).
- TiffExpectedFormat.TiffJpegYCBCR: Специфічний для стиснення Deflate під час збереження результату в форматі TIFF у просторі кольорів YCBCR.
- TiffExpectedFormat.TiffLzwBW: Специфічний для стиснення LZW під час збереження результату у форматі TIFF з BitsPerPixel 1 (чорно-білий).
- TiffExpectedFormat.TiffLzwRGB: Специфічний для стиснення LZW під час збереження результату у форматі TIFF кольоровим (RGB).
- TiffExpectedFormat.TiffLzwRGBA: Специфічний для стиснення LZW під час збереження результату у форматі TIFF кольоровим з прозорістю (RGBA).
- TiffExpectedFormat.TiffNoCompressionBW: Специфічний для нестисненого формату TIFF під час збереження результату з BitsPerPixel 1 (чорно-білий).
- TiffExpectedFormat.TiffNoCompressionRGB: Специфічний для нестисненого формату TIFF під час збереження результату кольоровим (RGB).
- TiffExpectedFormat.TiffNoCompressionRGBA: Специфічний для нестисненого формату TIFF під час збереження результату кольоровим з прозорістю (RGBA).



Наведений код демонструє використання полів TiffExpectedFormat при створенні екземпляра класу TiffOptions.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **Підтримка стиснення Deflate та Adobe Deflate Compression**
Формат файлу TIFF (Tagged Image File Format) підтримує різні типи стиснення, в той час як тип стиснення зберігається як тег (ціле число) у файлі. Одним із таких методів стиснення є Adobe Deflate (раніше відомий як Deflate). API Aspose.PSD для .NET підтримує цей метод стиснення для експорту та створення зображень у форматі TIFF.
### **Збереження зображення у форматі TIFF із стисненням Deflate**
Конвертація завантажених зображень у TIFF із стисненням Deflate/Adobe Deflate проста за наступними кроками.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Створення TiffImage із стисненням Adobe Deflate**
Наведений нижче приклад демонструє використання API Aspose.PSD для .NET для створення зображення з нуля за допомогою методу стиснення Adobe Deflate.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Стискання зображень у форматі TIFF**
API Aspose.PSD для .NET може бути використаний для конвертації зображень PSD у формат зображення TIFF, навіть змінюючи стиснення результуючого зображення TIFF. API також може бути використаний для зберігання різних зображень як кадрів у зображенні TIFF за архівними цілями, а також стискання зображень до найменшого обсягу даних. Стискання зображень у будь-якому випадку повинно виконуватися шляхом зменш
