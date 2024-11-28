---
title: Нотатки до випуску Aspose.PSD для Java 20.7
type: docs
weight: 50
url: /uk/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить нотатки до випуску для [Aspose.PSD для Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**Ключ**|**Короткий зміст**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-231|Підтримка додавання ефекту обводки під час роботи|Функція|
|PSDJAVA-249|Підтримка ресурсів lnk2 / lnk3 (ресурсів шару розумного об'єкту)|Функція|
|PSDJAVA-247|Зміна повідомлення про виняток при спробі відкрити не підтримані формати як зображення|Покращення|
|PSDJAVA-235|Якщо ми збережемо файл PSD після створення нової групи шарів, ми отримаємо попередження Photoshop при відкритті файлу.|Помилка|
|PSDJAVA-236|Не вдалося зберегти шар маски|Помилка|
|PSDJAVA-237|Маска обрізки не застосовується до папки|Помилка|
|PSDJAVA-238|Неможливо відкрити файл за допомогою Aspose.PSD для Java|Помилка|
|PSDJAVA-239|Виняток при збереженні зображення при конвертації PSD в PDF|Помилка|
|PSDJAVA-240|Операція обрізки робить шлях обрізки недійсним у зображенні PSD|Помилка|
|PSDJAVA-241|Виняток NullReference при спробі зберегти певний файл PSD з ефектом тіні|Помилка|
|PSDJAVA-243|Aspose.PSD повертає true під час Image.CanLoad(pdfStream)|Помилка|
|PSDJAVA-244|Шари не відображаються в згенерованому PNG|Помилка|
|PSDJAVA-245|Виняток при доступі до TextData|Помилка|
|PSDJAVA-246|Виняток ImageSaveException при збереженні PSD|Помилка|

# **Зміни в Публічному API**
# **Додані API:**
- F: com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F: com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F: com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M: com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M: com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M: com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M: com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M: com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M: com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T: com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T: com.aspose.psd.fileformats.psd.resources.WorkingPathResource
## **Вилучені API:**
- F: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M: com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
# **Приклади використання:**

**PSDJAVA-231. Підтримка додавання ефекту обводки під час роботи**
{{< highlight java >}}
// Цей приклад показує, як додати ефект обводки (рамки) до існуючих шарів файлу PSD в Java.
// Існує три типи обводки: кольорова, градієнт та малюнок. Кожен тип має
// три способи (позиції), в яких обводка відображається: всередині, по центру та зовні.
// Цей приклад демонструє використання всіх цих випадків.
 
String srcPsdPath = "ФайлДжерелаЕфектівОбводки.psd";
String dstPngPath = "output.png";
 
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage) Image.load(srcPsdPath, psdLoadOptions);
try
{
    ...
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-249. Підтримка ресурсів lnk2 / lnk3 (ресурсів шару розумного об'єкту)**
{{< highlight java >}}
// Цей приклад демонструє, як працювати з ресурсами розумних об'єктів (зазвичай Lnk2Resource).
// Програма завантажує кілька документів Photoshop і експортує їх розумні об'єкти до
// форматів растрових файлів. Крім того, код демонструє використання публічних методів Lnk2Resource.
 
...
{{< /highlight >}}

**PSDJAVA-247. Зміна повідомлення про виняток при спробі відкрити не підтримані формати як зображення**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-235. Якщо ми збережемо файл PSD після створення нової групи шарів, ми отримаємо попередження Photoshop при відкритті файлу.**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-236. Не вдалося зберегти шар маски**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-237. Маска обрізки не застосовується до папки**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-238. Неможливо відкрити файл за допомогою Aspose.PSD для Java**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-239. Виняток при збереженні зображення при конвертації PSD в PDF**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-240. Операція обрізки робить шлях обрізки недійсним у зображенні PSD**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-241. Виняток NullReference при спробі зберегти певний файл PSD з ефектом тіні**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-243. Aspose.PSD повертає true під час Image.CanLoad(pdfStream)**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-244. Шари не відображаються в згенерованому PNG**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-245. Виняток при доступі до TextData**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-246. Виняток ImageSaveException при збереженні PSD**
{{< highlight java >}}
...
{{< /highlight >}}**PSDJAVA-247. Зміна повідомлення про виняток при спробі відкрити не підтримані формати як зображення**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-235. Якщо ми збережемо файл PSD після створення нової групи шарів, ми отримаємо попередження Photoshop при відкритті файлу.**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-236. Не вдалося зберегти шар маски**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-237. Маска обрізки не застосовується до папки**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-238. Неможливо відкрити файл за допомогою Aspose.PSD для Java**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-239. Виняток при збереженні зображення при конвертації PSD в PDF**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-240. Операція обрізки робить шлях обрізки недійсним у зображенні PSD**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-241. Виняток NullReference при спробі зберегти певний файл PSD з ефектом тіні**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-243. Aspose.PSD повертає true під час Image.CanLoad(pdfStream)**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-244. Шари не відображаються в згенерованому PNG**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-245. Виняток при доступі до TextData**
{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-246. Виняток ImageSaveException при збереженні PSD**
{{< highlight java >}}
...
{{< /highlight >}}