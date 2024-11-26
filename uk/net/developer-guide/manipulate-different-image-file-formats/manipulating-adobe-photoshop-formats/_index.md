---
title: Редагування Adobe Photoshop Formats
type: docs
weight: 20
url: /uk/net/manipulating-adobe-photoshop-formats/
---

## **Об'єднання шарів PSD у Інші шари**

## **Експорт зображення в PSD**
PSD, документ PhotoShop, є форматом файлу, який використовується за замовчуванням Adobe Photoshop для роботи з зображеннями. Aspose.PSD дозволяє вам завантажувати, редагувати та зберігати файли у форматі PSD, щоб їх можна було відкрити й відредагувати в Photoshop. У цій статті показано, як зберегти файл в форматі PSD за допомогою Aspose.PSD, а також обговорюється деякі параметри, які можна використовувати при збереженні у цей формат. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) - спеціалізований клас у просторі імен [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions), призначений для експорту зображень у PSD. Для експорту в PSD створіть екземпляр класу Image, завантажений з існуючого файлу зображення (наприклад, ескізи) або створений з нуля. У цій статті пояснено, як це зробити. Нижче наведено код створення файлу Image з нуля, заповнення пікселями та збереження його у форматі PSD із стисненням RLE і в режимі відтінків сірого кольору. У кодовому вирізку нижче показано, як експортувати зображення в PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **Імпорт зображення в шар PSD**
Ця стаття демонструє використання Aspose.PSD для додавання або імпорту зображення в шар PSD. API Aspose.PSD розкриває ефективні та прості методи для досягнення цієї мети. Aspose.PSD розкриває метод [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) класа Layer для додавання/імпорту зображення в файл PSD. Метод DrawImage потребує значень розташування та зображення для додавання/імпорту зображення в файл PSD. Кроки імпорту зображення в шар PSD настільки прості, як описано нижче:

- Завантажити файл PSD як зображення за допомогою методу заводу Load, викритого класом Image.
- Створити екземпляр класу Layer з потіком з файлом Png, Jpeg, Tiff, Gif, Bmp, Psd або j2k.
- Додати шар до Psd за допомогою методу AddLayer.
- Зберегти результати.


Даний кодовий вирізок показує вам, як імпортувати зображення в шар PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Заміна кольорів у шарах PSD**
Ця стаття демонструє використання Aspose.PSD для додавання або імпорту зображення в шар PSD. API Aspose.PSD розкриває ефективні та прості методи для досягнення цієї мети. Aspose.PSD розкриває метод DrawImage класа Layer для додавання/імпорту зображення в файл PSD. Метод DrawImage потребує значень розташування та зображення для додавання/імпорту зображення в файл PSD. Кроки імпорту зображення в шар PSD настільки прості, як описано нижче:

- Завантажити файл PSD як зображення за допомогою методу заводу Load, викритого класом Image.
- Створити екземпляр класу Layer і призначити йому шар зображення PSD.
- Завантажити зображення, яке потрібно додати чи створити з нуля.
- Викликати метод Layer.DrawImage, вказавши розташування та екземпляр зображення.
- Зберегти результати.


Даний кодовий вирізок показує вам, як імпортувати зображення в шар PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **Створення ескізів з файлів PSD**
PSD - це власний формат документа застосунку Adobe Photoshop. Adobe Photoshop (версії 5.0 і пізніші) зберігає інформацію про ескіз для попереднього відображення у блоках ресурсів зображення, що складаються з початкового заголовку з 28 байтів, суцільного ескізу JFIF у порядку RGB (червоний, зелений, синій). API Aspose.PSD надає простий механізм доступу до ресурсів файлу PSD. Ці ресурси також включають ресурс ескізів, які, зі свого боку, можуть бути витягнуті і збережені на диск відповідно до потреб програми. Нижче наведено кодовий вирізок, який показує, як створити ескізи з файлів PSD.




{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **Створення індексованих файлів PSD**
API Aspose.PSD для .NET може створювати індексовані файли PSD з нуля. Ця стаття демонструє використання PsdOptions та класів [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage?lang=uk) для створення індексованого PSD при малюванні деяких форм на новому полотні. Для створення індексованого файлу PSD потрібно виконати наступні прості кроки:

- Створіть екземпляр PsdOptions та встановіть його джерело.
- Встановіть властивість ColorMode PsdOptions на ColorModes.Indexed.
- Створіть новий палітра кольорів з простору RGB та встановіть її як властивість Palette PsdOptions.
- Встановіть властивість CompressionMethod на необхідний алгоритм стискання.
- Створіть нове зображення PSD шляхом виклику методу PsdImage.[Створити](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create?lang=uk).
- Малюйте графіку або виконуйте інші операції відповідно до потреб.
- Викличте метод PsdImage.Save для збереження всіх змін.


Даний кодовий вирізок показує вам, як створити індексовані файли PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **Експорт шару PSD у растрове зображення**
Aspose.PSD для .NET дозволяє експортувати шари у файлі PSD у растрові зображення. Будь ласка, використовуйте метод [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index?lang=uk) для експорту шару у зображення. У наступному прикладі коду завантажується файл PSD і експортується кожен з його шарів у зображення PNG за допомогою методу Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Після того як всі шари експортовані у зображення PNG, їх можна відкрити за допомогою улюбленого переглядача зображень. Нижче наведено кодовий вирізок, який показує вам, як експортувати шар PSD у растрове зображення.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}
## **Оновлення текстового шару в файлі PSD**
Aspose.PSD для .NET дозволяє вам маніпулювати текстом у текстовому шарі файлу PSD. Будь ласка, використовуйте клас [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer?lang=uk), щоб оновити текст у шарі PSD. У наступному кодовому вирізку загружається файл PSD, доступ до текстового шару, оновлюється текст та зберігається файл PSD під новою назвою за допомогою методу [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index?lang=uk).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **Виявлення згладжених PSD**
Aspose.PSD для .NET дозволяє вам виявити, чи файл PSD згладжений чи ні. В класі Aspose.PSD.FileFormats.Psd.PsdImage було представлено властивість IsFlatten, щоб здійснити цю функціональність. У наступному кодовому вирізку завантажується файл PSD, а до властивості [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten?lang=uk) звертається через клас isFlatten.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}
## **Об'єднання шарів PSD**
Ця стаття показує, як об'єднувати шари в файлі PSD під час перетворення файлу PSD у JPG за допомогою Aspose.PSD. У прикладі нижче існуючий файл PSD завантажується, передаючи шлях до файлу методу завантаження Image. Після завантаження перетворіть/приведіть зображення до PsdImage. Створіть екземляр класу JpegOptions та встановіть його різні властивості. Зараз викличте метод Save екземпляра PsdImage. Нижче наведено кодовий вирізок, який показує вам, як об'єднати шари PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}
## **Підтримка відтінку сірого з альфа для PSD**
Ця стаття показує, як підтримувати відтінок сірого з альфа для файлу PSD під час перетворення файлу PSD у PNG за допомогою Aspose.PSD. У прикладі нижче існуючий файл PSD завантажується, передаючи шлях до файлу методу завантаження Image. Після завантаження перетворіть/приведіть зображення до PsdImage. Створіть екземляр класу PngOptions та встановіть його різні властивості. Встановіть властивість [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) на TruecolorWithAlpha. Зараз викличте метод Save екз