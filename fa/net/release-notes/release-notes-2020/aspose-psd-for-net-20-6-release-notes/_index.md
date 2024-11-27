---
title: فارسی
type: docs
weight: 70
url: /fa/net/aspose-psd-for-net-20-6-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD for .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-606 |پشتیبانی از منبع LnkE|ویژگی|
|PSDNET-386 |پشتیبانی از منبع britResource (منبع لایه تنظیم روشنایی/کنتراست)|ویژگی|
|PSDNET-219|انتقال تنظیم DefaultReplacementFont به کلاس ImageOptionsBase|بهبود|
|PSDNET-596|لایه گروه با حالت ادغامی PassThrough نمی‌شود رندر شده|اشکال|
|PSDNET-610|NullReference استثنا هنگام تبدیل یک فایل خاص Psd به تصویر|اشکال|
|PSDNET-636|تغییر اندازه فایل‌های PSD اشتباه کار می‌کند اگر یک ماسک در لایه تنظیمی وجود داشته باشد که حدود خالی دارد|اشکال|
|PSDNET-611|Overflow استثنا هنگام باز کردن یک فایل خاص Psd|اشکال|
|PSDNET-565|تصویر Psd با حالت RGB 16 بیت/کانال فقط در پیش‌نمایش لایه‌ها را به‌روز می‌کند|اشکال|
|PSDNET-652|استثنا در بارگذاری فایل PSD خاص با منبع گروه LnkE ترکیبی و خصوصیت adobeStockLicenseState|اشکال|
|PSDNET-640|تغییرات ماسک لایه PSD در هنگام ذخیره نادیده گرفته می‌شود|اشکال|
|PSDNET-593|ذخیره AI File به فرمت Jpeg2000 کار نمی‌کند|اشکال|
|PSDNET-638|ترتیب لایه نادرست پس از افزودن گروه لایه به گروه لایه خالی|اشکال|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
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
# **API‌های حذف شده:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **مثال‌های استفاده:**
**PSDNET-606. پشتیبانی از منبع LnkE**

{{< highlight java >}}

 string message = "ExampleOfLnkEResourceSupport کار نمی‌کند.";

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

// این مثال نشان می‌دهد چگونه مشخصات منبع Photoshop Psd LnkE که شامل اطلاعات درباره یک فایل خارجی متصل شده است را بدست آوریم و تنظیم کنیم.

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

// این مثال نشان می‌دهد چگونه مشاخص لایه Psd LnkE که اطلاعاتی درباره یک فایل JPEG خارجی دارد را بدست آوریم و تنظیم کنیم.

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

// این مثال نشان می‌دهد چگونه مشاخص لایه PSD LnkE که اطلاعاتی درباره یک فایل خارجی محلی PNG دارد را بدست آوریم و تنظیم کنیم.

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

    "5867318f-3174-9f41-abca-22f56a75247e",

    "rgb8_2x2.png",

    "rgb8_2x2.png",

    "png",

    0x53);

// این مثال نشان می‌دهد چگونه مشاخص لایه Photoshop Psd LnkE که اطلاعاتی درباره یک دارایی کتابخانه CC لینک شده دارد را بدست آوریم و تنظیم کنیم.

this.ExampleOfLnkEResourceSupport(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (قابلیت موجود است در فتوشاپ CC 2015)",

    "01/01/0001 00:00:00",

    1588890915488.0d,

    "",

    false,

    "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

    "rgb8_2x2_linked",

    "rgb8_2x2.png",

    "png",

    0);

{{< /highlight >}}

**PSDNET-201. پشتیبانی از پیشرفت تبدیل سند**

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

Console.WriteLine("---------- بارگیری Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

    Console.WriteLine("---------- ذخیره Apple.psd به فرمت PNG ----------");

    image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

    Console.WriteLine("---------- ذخیره Apple.psd به فرمت PSD ----------");

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

**PSDNET-386. پشتیبانی از منبع britResource (منبع لایه تنظیم روشنایی/کنتراست)**

{{< highlight java >}}

 /* این مثال نشان می‌دهد چگونه می‌توانید به صورت برنامه نویسی منبع لایه Brightness/Contrast Layer PSD تغییر دهید - BritResource

   این یک API پایین برنامه Aspose.PSD است. شما می‌ت