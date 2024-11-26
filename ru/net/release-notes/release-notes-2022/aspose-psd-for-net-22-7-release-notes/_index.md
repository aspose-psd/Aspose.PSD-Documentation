---
title: "Aspose.PSD для .NET 22.7 - Примечания к выпуску"
type: docs
weight: 60
url: /ru/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Краткое описание**|**Категория**|
| :- | :- | :- |
|PSDNET-482|Поддержка ресурса секции изображения #4000-4999 Plug-In|Функция|
|PSDNET-875|Происходит необработанное исключение типа "System.OutOfMemoryException" в Aspose.PSD.dll|Ошибка|
|PSDNET-1050|После экспорта PSD файла, размер результата значительно превышает размер исходного файла|Ошибка|
|PSDNET-1083|Некорректный разбор данных для XmpResource|Ошибка|
|PSDNET-1205|После экспорта размер файлов PSD с подпапками увеличивается|Ошибка|


## **Изменения в общедоступном API**
# **Добавленные API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.SaveData(Aspose.PSD.StreamContainer)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.KeyName
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.AnimatedDataSection
- M:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.SaveData(Aspose.PSD.StreamContainer)


# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDNET-482. Поддержка ресурса секции изображения #4000-4999 Plug-In**

{{< highlight csharp >}}
// Нижеследующий код демонстрирует, как установить/обновить задержку времени на рамке временной шкалы анимированных данных.
string sourceFile = "3_animated.psd";
string outputPsd = "output_3_animated.psd";

T FindStructure<T>(IEnumerable<OSTypeStructure> structures, string keyName) where T : OSTypeStructure
{
    foreach (var structure in structures)
    {
        if (structure.KeyName.ClassName == keyName)
        {
            return structure as T;
        }
    }

    return null;
}

OSTypeStructure[] AddOrReplaceStructure(IEnumerable<OSTypeStructure> structures, OSTypeStructure newStructure)
{
    List<OSTypeStructure> listOfStructures = new List<OSTypeStructure>(structures);

    for (int i = 0; i < listOfStructures.Count; i++)
    {
        OSTypeStructure structure = listOfStructures[i];
        if (structure.KeyName.ClassName == newStructure.KeyName.ClassName)
        {
            listOfStructures.RemoveAt(i);
            break;
        }
    }

    listOfStructures.Add(newStructure);

    return listOfStructures.ToArray();
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    foreach (var imageResource in image.ImageResources)
    {
        if (imageResource is AnimatedDataSectionResource)
        {
            var animatedData =
            (AnimatedDataSectionStructure) (imageResource as AnimatedDataSectionResource).AnimatedDataSection;
            var framesList = FindStructure<ListStructure>(animatedData.Items, "FrIn");

            var frame1 = (DescriptorStructure)framesList.Types[1];

            // Создает запись задержки кадров со значением 100 сотых секунды, что равно 1 секунде.
            var frameDelay = new IntegerStructure(new ClassID("FrDl"));
            frameDelay.Value = 100; // установить время в сотых секунды.

            frame1.Structures = AddOrReplaceStructure(frame1.Structures, frameDelay);

            break;
        }
    }

    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-875. Происходит необработанное исключение типа "System.OutOfMemoryException" в Aspose.PSD.dll**

{{< highlight csharp >}}
string srcFile = "001-.psd";
string jpgFilePath = "T_0003.jpg";
string outputFilePath = "output_newPsd.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    using (FileStream fs = new FileStream(jpgFilePath, FileMode.Open))
    {
        var newLayer = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        newLayer.DisplayName = "NewLayer";

        im.AddLayer(newLayer);

        im.Save(outputFilePath, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. После экспорта PSD файла, размер результата значительно превышает размер исходного файла**

{{< highlight csharp >}}
string src = "ShimadzuLetterhead100.psd";
string output = "output.psd";
using (var img = (PsdImage)Image.Load(src))
{
    img.Save(output);
}

double outputSizeMb = new FileInfo(output).Length / 1024d / 1024d;
if (outputSizeMb > 6)
{
    throw new Exception("Размер выходного файла больше, чем должен быть.");
}
{{< /highlight >}}

**PSDNET-1083. Некорректный разбор данных для XmpResource**

{{< highlight csharp >}}
string inputPsdImagePath = @"input.psd";
string savedPsdImagePath = @"saved.psd";

bool isOriginalContain = false;
bool isSavedContain = false;

// Найдите вложенный ключ XMP во входном файле
using (PsdImage img = (PsdImage)Image.Load(inputPsdImagePath))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string xmlValue = xmpArray.GetXmlValue();

                if (xmlValue.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    isOriginalContain = true;
                    break;
                }
            }
        }

        if (isOriginalContain)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

// Найдите вложенный ключ XMP в сохраненном файле
using (PsdImage img = (PsdImage)Image.Load(savedPsdImagePath))
{
    foreach (var package in img.XmpData.Packages)
    {
        foreach (var pack in package)
        {
            if (pack.Value is XmpArray)
            {
                XmpArray xmpArray = (XmpArray)pack.Value;

                string xmlValue = xmpArray.GetXmlValue();

                if (xmlValue.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    isSavedContain = true;
                    break;
                }
            }
        }

        if (isSavedContain)
        {
            break;
        }
    }
    img.Save(savedPsdImagePath);
}

if (isOriginalContain && isSavedContain)
{
    // Все в порядке!
}
else
{
    throw new Exception("Это не работает");
}
{{< /highlight >}}

**PSDNET-1205. После экспорта размер файлов PSD с подпапками увеличивается**

{{< highlight csharp >}}
string[] sourceFiles = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var fileName in sourceFiles)
{
    string sourceFilePath = fileName;
    string outputFilePath = "output_" + fileName;

    using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
    {
        image.Save(outputFilePath);
    }

    double outputSizeMb = new FileInfo(outputFilePath).Length / 1024d / 1024d;
    if (outputSizeMb > 1.9)
    {
        throw new Exception("Размер выходного файла больше, чем должен быть.");
    }
}
{{< /highlight >}}
