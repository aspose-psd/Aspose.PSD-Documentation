---
title: Оновлення Aspose.PSD для Java 20.6
type: документація
weight: 50
url: /uk/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить оновлення для [Aspose.PSD для Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-216|Підтримка LnkEResource (ресурс шару Smart Object)|Функціонал|
|PSDJAVA-219|Підтримка britResource (ресурс шару яскравості/контрастності)|Функціонал|
|PSDJAVA-222|Перенесення налаштування DefaultReplacementFont в клас ImageOptionsBase|Покращення|
|PSDJAVA-217|Неправильна робота зміни розміру файлів PSD, якщо є маска в шарі підгонки з пустими межами|Помилка|
|PSDJAVA-218|Зображення Psd з режимом RGB 16 біт/канал оновлює шари тільки у попередньому перегляді|Помилка|
|PSDJAVA-220|Зміни маски шару PSD скасовуються при збереженні|Помилка|
|PSDJAVA-221|Неправильний порядок шарів після додавання групи шарів до порожньої групи шарів|Помилка|
|PSDJAVA-223|Виняток при завантаженні певного файлу PSD з складеним ресурсом Lnke та властивістю adobeStockLicenseState|Помилка|
|PSDJAVA-224|Збереження файлу AI у форматі Jpeg2000 не працює|Помилка|
|PSDJAVA-225|Група шарів з режимом злиття не рендериться|Помилка|
|PSDJAVA-226|Виняток NullReference під час спроби конвертувати конкретний файл Psd у зображення|Помилка|
|PSDJAVA-227|Переповнення винятку при спробі відкрити конкретний файл Psd|Помилка|
## **Зміни у відкритому API**
## **Додані API:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- ...

## **Вилучені API:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)

# **Приклади використання:**

**PSDJAVA-216: Підтримка LnkEResource (ресурсу шару об'єкта Smart)**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-219: Підтримка britResource (ресурсу шару яскравості/контрастності)**

{{< highlight java >}}
...
{{< /highlight >}}

...
...

**PSDJAVA-217: Розмір файлів PSD змінюється неправильно, якщо є маска в шарі підгонки, яка має пусті межі**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-218: Зображення Psd з режимом RGB 16 біт/канал оновлює шари тільки у попередньому перегляді**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-220: Зміни маски шару PSD скасовуються при збереженні**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-221: Неправильний порядок шарів після додавання групи шарів до порожньої групи шарів**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-223: Виняток при завантаженні певного файлу PSD зі складеним ресурсом LnkE та властивістю adobeStockLicenseState**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-224: Збереження файлу AI у форматі Jpeg2000 не працює**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-225: Група шарів з режимом злиття не рендериться**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-226: Виняток NullReference під час спроби конвертувати конкретний файл Psd у зображення**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-227: Переповнення винятку при спробі відкрити конкретний файл Psd**

{{< highlight java >}}
...
{{< /highlight >}}
