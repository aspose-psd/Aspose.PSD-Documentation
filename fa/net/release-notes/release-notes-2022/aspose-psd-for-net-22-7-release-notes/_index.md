---
title: اسپوز-پی‌اس‌دی برای .نت ۲۲.۷ - یادداشت‌های انتشار
type: docs
weight: 60
url: /fa/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار برای [اسپوز-پی‌اس‌دی برای .نت ۲۲.۷](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-482|پشتیبانی از منبع بخش تصویری #4000-4999 پلاگین|ویژگی|
|PSDNET-875|یک استثناء ناشناخته از نوع "System.OutOfMemoryException" در Aspose.PSD.dll رخ می‌دهد|اشکال|
|PSDNET-1050|پس از صادر کردن پرونده PSD، اندازه نتیجه از پرونده منبع بسیار بزرگتر است|اشکال|
|PSDNET-1083|تجزیه‌وتحلیل نادرست اطلاعات برای XmpResource|اشکال|
|PSDNET-1205|پس از صادر کردن، اندازه پرونده‌های PSD دارای زیرپوشه‌ها افزایش یافته است|اشکال|


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- T:ساختار بخش داده متحرک لایه‌ها.Psd.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:کلید ساختار بخش داده متحرک لایه‌ها.Psd.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:طول ساختار بخش داده متحرک لایه‌ها.Psd.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:موارد ساختار بخش داده متحرک لایه‌ها.Psd.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- M:ذخیره‌کردن داده ساختار بخش داده متحرک لایه‌ها.Psd.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure در ظرف اسپوز.PSD.StreamContainer
- F:کلید ساختار بخش داده متحرک لایه‌ها.Psd.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- T:ساختار بخش داده متحرک منبع.Psd.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:اندازه داده متحرک بخش منبع.Psd.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:نسخه حداقل داده متحرک بخش منبع.Psd.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:نام کلید داده متحرک بخش منبع.Psd.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:بخش داده متحرک بخش منبع.Psd.FileFormats.Psd.Resources.AnimatedDataSectionResource
- M:ذخیره‌کردن داده بخش داده متحرک منبع.Psd.FileFormats.Psd.Resources.AnimatedDataSectionResource در ظرف اسپوز.PSD.StreamContainer


# **API‌های حذف شده:**
- هیچ‌کدام


## **مثال‌های استفاده:**

**PSDNET-482. پشتیبانی از منبع بخش تصویری #4000-4999 پلاگین**

{{< highlight csharp >}}
// کد زیر نحوه تنظیم/به‌روزرسانی زمان تأخیر در چارچوب زمانی داده‌های متحرک را نشان می‌دهد.
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

            // Creates the frame delay record with value 100 centi-second that is equal to 1 second.
            var frameDelay = new IntegerStructure(new ClassID("FrDl"));
            frameDelay.Value = 100; // set time in centi-seconds.

            frame1.Structures = AddOrReplaceStructure(frame1.Structures, frameDelay);

            break;
        }
    }

    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-875. یک استثناء ناشناخته از نوع "System.OutOfMemoryException" در Aspose.PSD.dll رخ می‌دهد**

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

**PSDNET-1050. پس از صادر کردن پرونده PSD، اندازه نتیجه از پرونده منبع بسیار بزرگتر است**

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
    throw new Exception("پرونده خروجی بزرگتر از اندازه مناسب است.");
}
{{< /highlight >}}

**PSDNET-1083. تجزیه‌وتحلیل نادرست اطلاعات برای XmpResource**

{{< highlight csharp >}}
string inputPsdImagePath = @"input.psd";
string savedPsdImagePath = @"saved.psd";

bool isOriginalContain = false;
bool isSavedContain = false;

// Find sub XMP key in input file
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

// Find sub XMP key in saved file
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
    // All is ok!
}
else
{
    throw new Exception("کار نمی‌کند");
}
{{< /highlight >}}

**PSDNET-1205. پس از صادر کردن، اندازه پرونده‌های PSD دارای زیرپوشه‌ها افزایش یافته است**

{{< highlight csharp >}}
string[] sourceFiles = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd" };

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
        throw new Exception("پرونده خروجی بزرگتر از اندازه مناسب است.");
    }
}
{{< /highlight >}}
