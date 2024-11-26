---
title: Aspose.PSD for .NET 20.6 - 发行说明
type: docs
weight: 70
url: /zh/net/aspose-psd-for-net-20-6-release-notes/
---

{{% alert color="primary" %}} 

此页面包含 [Aspose.PSD for .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-606 |支持 LnkE 资源|新功能|
|PSDNET-386 |支持 britResource (亮度/对比度调整图层的资源)|新功能|
|PSDNET-219|将 DefaultReplacementFont 设置移到 ImageOptionsBase 类|增强功能|
|PSDNET-596|非PassThrough混合模式的图层组未呈现|错误|
|PSDNET-610|尝试将特定 Psd 文件转换为图像时出现 NullReference 异常|错误|
|PSDNET-636|如果调整图层中具有空边界的蒙版，则调整 PSD 文件大小会出现错误|错误|
|PSDNET-611|尝试打开特定 Psd 文件时出现 OverflowException 异常|错误|
|PSDNET-565|具有 RGB 模式 16 位/通道的 Psd 图像仅在预览时更新图层|错误|
|PSDNET-652|加载具有复合 LnkE 资源和 adobeStockLicenseState 属性的特定 PSD 文件时出现异常|错误|
|PSDNET-640|保存 AI 文件为 Jpeg2000 格式时无法正常工作|错误|
|PSDNET-638|在将图层组添加到空图层组后，图层顺序不正确|错误|

## **公共 API 更改**
# **添加的 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.MaskRectangle
- P:Aspose.PSD.ImageOptionsBase.DefaultReplacementFont
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Type
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileCreator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.ChildDocId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetModTime
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetLockedState
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.IsLibraryLink
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.HasFileOpenDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Length
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.None
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFD
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFE
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFA
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.Date
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileSize
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FullPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.RelativePath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementRef
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockLicenseState
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.IsEmpty
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.DataSourceCount
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.StringStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String)

# **已删除的 API:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **用法示例:**
**PSDNET-606. 支持 LnkE 资源**

{{< highlight java >}}

 string message = "ExampleOfLnkEResourceSupport works incorrectly.";

void AssertIsTrue(bool condition)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

void AssertAreEqual(object actual, object expected)

{

    if (!object.Equals(actual, expected))

    {

        throw new FormatException(message);

    }

}

// 此示例演示如何获取和设置包含外部链接文件信息的 Photoshop Psd LnkE 资源的属性。

void ExampleOfLnkEResourceSupport(

    string filePath,

    int length,

    int length2,

    int length3,

    int length4,

    string fullPath,

    string date,

    double assetModTime,

    string childDocId,

    bool locked,

    string uid,

    string name,

    string originalFileName,

    string fileType,

    long size)

{

    string fileName = Path.GetFileName(filePath);

    string outputPath = @"Output\" + fileName;

    using (PsdImage image = (PsdImage)Image.Load(filePath))

    {

        LnkeResource lnkeResource = null;

        foreach (var resource in image.GlobalLayerResources)

        {

            lnkeResource = resource as LnkeResource;

            if (lnkeResource != null)

            {

                AssertAreEqual(lnkeResource.Length, length);

                AssertAreEqual(lnkeResource.UniqueId, new Guid(uid));

                AssertAreEqual(lnkeResource.FullPath, fullPath);

                AssertAreEqual(lnkeResource.Date.ToString(CultureInfo.InvariantCulture), date);

                AssertAreEqual(lnkeResource.AssetModTime, assetModTime);

                AssertAreEqual(lnkeResource.AssetLockedState, locked);

                AssertAreEqual(lnkeResource.FileName, name);

                AssertAreEqual(lnkeResource.FileSize, size);

                AssertAreEqual(lnkeResource.ChildDocId, childDocId);

                AssertAreEqual(lnkeResource.Version, 7);

                AssertAreEqual(lnkeResource.FileType, fileType);

                AssertAreEqual(lnkeResource.FileCreator, string.Empty);

                AssertAreEqual(lnkeResource.OriginalFileName, originalFileName);

                AssertAreEqual(lnkeResource.CompId, -1);

                AssertAreEqual(lnkeResource.OriginalCompId, -1);

                AssertIsTrue(lnkeResource.HasFileOpenDescriptor);

                AssertIsTrue(!lnkeResource.IsEmpty);

                AssertIsTrue(lnkeResource.Type == LinkResourceType.liFE);

                lnkeResource.FullPath =

                    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png";

                AssertAreEqual(lnkeResource.Length, length2);

                lnkeResource.FileName = "rgb8_2x23.png";

                AssertAreEqual(lnkeResource.Length, length3);

                lnkeResource.ChildDocId = Guid.NewGuid().ToString();

                AssertAreEqual(lnkeResource.Length, length4);

                lnkeResource.Date = DateTime.Now;

                lnkeResource.AssetModTime = double.MaxValue;

                lnkeResource.FileSize = long.MaxValue;

                lnkeResource.FileType = "test";

                lnkeResource.FileCreator = "file";

                lnkeResource.CompId = int.MaxValue;

                break;

            }

        }

        AssertIsTrue(lnkeResource != null);

        image.Save(outputPath, new PsdOptions(image));

    }

    using (PsdImage image = (PsdImage)Image.Load(outputPath))

    {

        image.Save(

            Path.ChangeExtension(outputPath, "png"),

            new PngOptions

            {

                ColorType = PngColorType.TruecolorWithAlpha

            });

    }

}

// 此示例演示如何获取和设置包含有关外部链接的 JPEG 文件的信息的 PSD LnkE 资源的属性。

this.ExampleOfLnkEResourceSupport(

    @"..\..\..\Issues\IMAGINGNET-2375\photooverlay_5_new.psd",

    0x21c,

    0x26c,

    0x274,

    0x27c,

    @"file:///C:/Users/cvallejo/Desktop/photo.jpg",

    "05/09/2017 22:24:51",

    0,

    "F062B9DB73E8D124167A4186E54664B0",

    false,

    "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

    "photo.jpg",

    "photo.jpg",

    "JPEG",

    0x1520d);

// 此示例演示如何获取和设置包含有关外部链接的 PNG 文件的信息的 PSD LnkE 资源的属性。

this.ExampleOfLnkEResourceSupport(

    "rgb8_2x2_linked.psd",

    0x284,

    0x290,

    0x294,

    0x2dc,

    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

    "04/14/2020 14:23:44",

    0,

    "",

    false,

    "...

{{< /highlight >}}

**PSDNET-201. 文档转换进度支持**

{{< highlight java >}}

 string sourceFilePath = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)

{

      string message = string.Format(

           "{0} {1}: {2} out of {3}",

           progressInfo.Description,

           progressInfo.EventType,

           progressInfo.Value,

           progressInfo.MaxValue);

      Console.WriteLine(message);

};

Console.WriteLine("---------- 加载 Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

      Console.WriteLine("---------- 将 Apple.psd 保存为 PNG 格式 ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- 将 Apple.psd 保存为 PSD 格式 ----------");

      image.Save(

           outputStream,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = localProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-386. 支持 britResource (亮度/对比度调整图层的资源)**

{{< highlight java >}}

 /* 此示例演示如何通过程序更改 PSD 图像亮度/对比度图层资源 - BritResource

   这是一个低级别的 Aspose.PSD API。 您可以通过其 API 使用亮度/对比度图层，这将更容易，

   但直接编辑 PhotoShop 资源可让您更好地控制 PSD 文件内容。  */

string path = @"BrightnessContrastPS6.psd";

string outputPath = @"BrightnessContrastPS6_output.psd";

using (PsdImage im = (PsdImage)Image.Load(path))

{

    foreach (var layer in im.Layers)

    {

        if (layer is BrightnessContrastLayer)

        {

            foreach (var layerResource in layer.Resources)

            {

                if (layerResource is BritResource)

                {

                    var resource = (BritResource)layerResource;

                    isRequiredResourceFound = true;

                    if (resource.Brightness != -40 ||

                        resource.Contrast != 10 ||

                        resource.LabColor != false ||

                        resource.MeanValueForBrightnessAndContrast != 127)

                    {

                        throw new Exception("BritResource was read wrong");

                    }

                    // 测试编辑和保存

                    resource.Brightness = 25;

                    resource.Contrast = -14;

                    resource.LabColor = true;

                    resource.MeanValueForBrightnessAndContrast = 200;

                    im.Save(outputPath, new PsdOptions());

                    break;

                }

            }

        }

    }

}

{{< /highlight >}}

**PSDNET-596. 带有非 PassThrough 混合模式的图层组未呈现**

{{< highlight java >}}

 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";

string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";

using (var input = (PsdImage)Image.Load(sourceFilePath))

{

    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-610. 尝试将特定 Psd 文件转换为图像时出现 NullReference 异常**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

` `**PSDNET-636. 如果调整图层中具有空边界的蒙版，则调整 PSD 文件大小会出现错误**

{{< highlight java >}}

 int scale = 2;

string[] names = {

                     "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                     "LevelsLayerWithLayerMaskRgb",

                     "LevelsLayerWithLayerMaskCmyk",

                 };

for (int i = 0; i < names.Length; i++)

{

    string sourceFilePath = names[i] + ".psd";

    string outputFilePath = "output_" + sourceFilePath;

    string outputPngFilePath = "output_" + names[i] + ".png";

    var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

    using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, psdLoadOptions))

    {

        image.Resize(image.Width * scale, image.Height * scale);

        image.Save(outputFilePath, new PsdOptions());

        image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    }

}

{{< /highlight >}}

**PSDNET-611. 尝试打开特定 Psd 文件时出现 OverflowException 异常**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load("CT_SkillTest_v1.psd"))

{

    psdImage.Save("output.psd");

}

// 加载并保存无异常。

{{< /highlight >}}

**PSDNET-565. 具有 RGB 模式 16 位/通道的 Psd 图像仅在预览时更新图层**

{{< highlight java >}}

 string sourceFilePath = @"in.psd";

string outputFilePath = @"output.psd";

PsdLoadOptions options = new PsdLoadOptions();

using (PsdImage image = (