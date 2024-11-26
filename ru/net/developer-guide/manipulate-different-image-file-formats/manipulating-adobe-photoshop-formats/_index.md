---
title: Manipulation of Adobe Photoshop Formats
type: docs
weight: 20
url: /ru/net/manipulating-adobe-photoshop-formats/
---

## **Объединение слоев PSD с другими слоями**

## **Экспорт изображения в формат PSD**
PSD, документ PhotoShop, является форматом файла по умолчанию, используемым Adobe Photoshop для работы с изображениями. Aspose.PSD позволяет загружать, редактировать и сохранять файлы в формате PSD, чтобы их можно было открывать и редактировать в Photoshop. В данной статье показано, как сохранить файл в формате PSD с помощью Aspose.PSD, и также обсуждаются некоторые настройки, которые можно использовать при сохранении в этот формат. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) - это специализированный класс в пространстве имен [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions), используемый для экспорта изображений в PSD. Чтобы экспортировать в PSD, создайте экземпляр класса Image, загруженный либо из существующего файла изображения (например, миниатюры), либо созданный с нуля. В этой статье объясняется, как это делать. В приведенных ниже примерах изображение создается с нуля. После создания изображение и заполнения пиксельными данными сохраните изображение, используя метод Save класса Image, и предоставьте объект PsdOptions в качестве второго аргумента. Несколько свойств класса PsdOptions могут быть установлены для расширенного преобразования. Некоторые из свойств: ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) и Version. Aspose.PSD поддерживает следующие методы сжатия через перечисление CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Следующие режимы цвета поддерживаются через перечисление [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

Могут быть добавлены дополнительные ресурсы, такие как ресурсы миниатюр для PSD v4.0, v5.0 и более поздних версий или сетка и руководство для PSD v4.0 и более поздних версий. Приведенный ниже код создает файл изображения с нуля, заполняет пиксели и сохраняет его в формате PSD с сжатием RLE и режимом цвета оттенков серого. Приведенный ниже код показывает, как экспортировать изображение в PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}

## **Импорт изображения в слой PSD**
В этой статье демонстрируется использование Aspose.PSD для добавления или импорта изображения в слой PSD. Aspose.PSD API предоставляет эффективные и простые в использовании методы для достижения этой цели. В Aspose.PSD экспонированный метод [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) класса Layer используется для добавления/импорта изображения в файл PSD. Метод DrawImage требует местоположения и значений изображения для добавления/импорта изображения в файл PSD. Шаги импорта изображения в слой PSD просты:

- Загрузите файл PSD в качестве изображения, используя метод фабрики Load, экспонированный классом Image.
- Создайте экземпляр класса Layer из потока с файлом Png, Jpeg, Tiff, Gif, Bmp, Psd или j2k
- Добавьте слой в PSD с помощью метода AddLayer
- Сохраните результат.


Приведенный ниже код показывает, как импортировать изображение в слой PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

## **Замена цвета в слоях PSD**

Эта статья демонстрирует использование Aspose.PSD для добавления или импорта изображения в слой PSD. В Aspose.PSD API предоставляются эффективные и простые в использовании методы для достижения этой цели. Aspose.PSD экспонирует метод DrawImage класса Layer для добавления/импорта изображения в файл PSD. Метод DrawImage требует местоположения и значений изображения для добавления/импорта изображения в файл PSD. Шаги импорта изображения в слой PSD просты:

- Загрузите файл PSD в качестве изображения, используя метод фабрики Load, экспонированный классом Image.
- Создайте экземпляр класса Layer и назначьте ему изображение PSD слоя.
- Загрузите изображение, которое необходимо добавить или создайте изображение с нуля.
- Вызовите метод Layer.DrawImage, указав местоположение и экземпляр изображения.
- Сохраните результат.


Приведенный ниже код показывает, как импортировать изображение в слой PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}} 

## **Создание миниатюр из файлов PSD**
PSD - это собственный формат документа приложения Adobe Photoshop. Adobe Photoshop (версия 5.0 и выше) сохраняет информацию о миниатюрах для предварительного просмотра в блоке ресурсов изображения, который состоит из начального заголовка из 28 байт, за которым следует миниатюра JFIF в порядке RGB (красный, зеленый, синий). API Aspose.PSD предоставляет простой в использовании механизм для доступа к ресурсам файла PSD. Эти ресурсы также включают ресурс миниатюры, которая, в свою очередь, может быть извлечена и сохранена на диск в соответствии с потребностями приложения. Приведенный ниже код показывает, как создать миниатюры из файлов PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}

## **Создание индексированных файлов PSD**
API Aspose.PSD для .NET может создавать индексированные файлы PSD с нуля. В данной статье демонстрируется использование классов PsdOptions и [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) для создания индексированного PSD при рисовании некоторых форм на новом холсте. Для создания индексированного файла PSD требуется выполнить следующие шаги:

- Создайте экземпляр PsdOptions и установите его источник.
- Установите свойство ColorMode PsdOptions в ColorModes.Indexed.
- Создайте новую палитру цветов из RGB пространства и установите ее в качестве свойства Palette PsdOptions.
- Установите свойство CompressionMethod на необходимый алгоритм сжатия.
- Создайте новое изображение PSD, вызвав метод PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Нанесите графику или выполните другие операции по необходимости.
- Вызовите метод PsdImage.Save для применения всех изменений.


Приведенный ниже код показывает, как создать индексированные файлы PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
