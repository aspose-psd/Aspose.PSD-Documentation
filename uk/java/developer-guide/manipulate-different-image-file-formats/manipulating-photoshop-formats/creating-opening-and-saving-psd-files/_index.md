---
title: Створення, відкриття та збереження файлів PSD
type: docs
weight: 10
url: /uk/creating-opening-and-saving-psd-files/
---

## **Експорт зображення в PSD**
PSD, документ PhotoShop, є форматом файлу за замовчуванням, що використовується в Adobe PhotoShop для роботи з зображеннями. Aspose.PSD дозволяє завантажувати, редагувати та зберігати файли в форматі PSD, щоб їх можна було відкрити та відредагувати в PhotoShop. У цій статті показано, як зберегти файл у форматі PSD за допомогою Aspose.PSD, а також обговорюється деякі налаштування, які можна використовувати при збереженні в цей формат. PsdOptions є спеціалізованим класом в просторі імен ImageOptions, який використовується для експорту зображень в PSD. Щоб експортувати в PSD, створіть екземпляр класу Image, що завантажений з існуючого файлу зображення (наприклад, мініатюри) або створений з нуля. Ця стаття пояснює, як це зробити. У поданих нижче прикладах зображення створюється з нуля. Після створення зображення та заповнення піксельних даних збережіть зображення за допомогою методу Save класу Image та вкажіть об'єкт PsdOptions як другий аргумент. Для розширеного перетворення можна встановити кілька властивостей класу PsdOptions, таких як ColorMode, CompressionMethod та Version. Aspose.PSD підтримує такі методи стиснення через перелік CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Наступні режими кольору підтримуються через перелік ColorModes:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Можна додати додаткові ресурси, такі як мініатюри для PSD v4.0, v5.0 та вище, або сітки та ресурси у вигляді підказок для PSD v4.0 та вище. У коді нижче створюється файл BMP з нуля, заповнюються пікселі та зберігається в PSD зі стисненням RLE та режимом кольору відтінків сірого. Нижче поданий уривок коду показує, як експортувати зображення в PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Імпорт зображення на шар PSD**
У цій статті показано використання Aspose.PSD для додавання або імпорту зображення на шар PSD. Aspose.PSD API надає ефективні та прості методи для досягнення цієї мети. Aspose.PSD виклав метод DrawImage класу Layer для додавання/імпорту зображення в файл PSD. Метод DrawImage потребує значень місцезнаходження та зображення для додавання/імпорту зображення в файл PSD. Кроки для імпортування зображення на шар PSD є наступними:

- Завантажте файл PSD як зображення, використовуючи метод завантаження, викритий класом Image.
- Створіть екземпляр класу Layer та присвойте йому шар PSD зображення.
- Завантажте зображення, яке потрібно додати або створіть одне з нуля.
- Викличте метод Layer.DrawImage, вказавши місцезнаходження та екземпляр зображення.
- Збережіть результати.



Наступний уривок коду показує, як імпортувати зображення на шар PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Створення мініатюр з файлів PSD**
PSD є власним форматом документа програми Adobe Photoshop. Adobe Photoshop (версія 5.0 та пізніше) зберігає інформацію про мініатюру для попереднього перегляду в блоку ресурсів зображення, що складається з початкового 28-байтного заголовка, за яким слідує мініатюра JFIF у порядку RGB (червоний, зелений, синій). Aspose.PSD API надає простий механізм доступу до ресурсів файлу PSD. Ці ресурси також включають мініатюрний ресурс, який, в свою чергу, може бути витягнутий та збережений на диск відповідно до потреб програми. Наступний уривок коду показує, як створювати мініатюри з файлів PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Створення індексованих файлів PSD**
Aspose.PSD для Java API може створювати індексовані файли PSD з нуля. Ця стаття демонструє використання класів PsdOptions та PsdImage для створення індексованого PSD під час малювання деяких форм на новоствореному полотні. Для створення індексованого файлу PSD потрібно виконати наступні прості кроки:

- Створіть екземпляр PsdOptions та задайте його джерело.
- Встановіть властивість ColorMode об'єкта PsdOptions на ColorModes.Indexed.
- Створіть нову палітру кольорів з простору RGB та встановіть її в якості властивості Palette об'єкта PsdOptions.
- Встановіть властивість CompressionMethod на потрібний алгоритм стиснення.
- Створіть нове зображення PSD, викликавши метод PsdImage.Create.
- Намалюйте графіку або виконайте інші операції за необхідності.
- Викличіть метод PsdImage.Save для збереження всіх змін.



Наступний уривок коду показує, як створювати індексовані файли PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **Експорт PSD-шару в растрове зображення**
Aspose.PSD для Java дозволяє експортувати шари у файлах PSD в растрові зображення. Будь ласка, використовуйте метод Aspose.PSD.FileFormats.Psd.Layers.Layer.Save для експортування шару в зображення. У наведеному нижче коді відображено завантаження файлу PSD та експорт кожного з його шарів у зображення PNG за допомогою методу Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Після того як всі шари експортовані в зображення PNG, їх можна відкрити за допомогою обраного переглядача зображень. Наступний уривок коду показує, як експортувати PSD-шар у растрове зображення.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}

