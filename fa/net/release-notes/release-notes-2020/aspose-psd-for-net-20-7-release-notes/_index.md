---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 20.7
type: docs
weight: 60
url: /fa/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD برای .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-673|پشتیبانی از منبع LnkE|ویژگی|
|PSDNET-392|پشتیبانی از منبع britResource (منبع لایه تنظیم روشنایی/کنتراست)|ویژگی|
|PSDNET-629|تغییر پیام استثنا هنگام تلاش برای باز کردن فرمت‌های پشتیبانی نشده به عنوان یک تصویر|بهبود|
|PSDNET-594|ناتوانی در ذخیره لایه LayerMask|اشکال|
|PSDNET-597|در صورت ذخیره فایل PSD پس از ایجاد گروه لایه جدید، هشدار فتوشاپ را در باز کردن فایل دریافت می‌کنیم|اشکال|
|PSDNET-618|ماسک برش مورد استفاده در پوشه اعمال نمی‌شود|اشکال|
|PSDNET-625|ناتوانی در باز کردن فایل با Aspose.PSD برای .NET|اشکال|
|PSDNET-650|استثنای عدم موفقیت در ذخیره تصویر هنگام تبدیل PSD به PDF|اشکال|
|PSDNET-655|عملیات rop باعث تروا معتبر پوشه‌ی برش نامعتبر در تصویر PSD می‌شود|اشکال|
|PSDNET-662|استثنای NullReference هنگام تلاش برای ذخیره فایل PSD خاص با افکت سایه|اشکال|
|PSDNET-666|Aspose.PSD هنگام Image.CanLoad(pdfStream) مقدار true را برمی‌گرداند|اشکال|
|PSDNET-676|لایه‌ها در PNG ایجاد شده نمی‌توانند رندر شوند|اشکال|
|PSDNET-677|استثنا در دسترسی به TextData|اشکال|
|PSDNET-679|استثنای ImageSaveException در ذخیره کردن PSD|اشکال|

## **تغییرات عمومی API**
# **APIهای افزوده شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **APIهای حذف شده:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **مثال‌های استفاده:**
**PSDNET-606. پشتیبانی از منبع LnkE**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
 {
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("مقدار فعلی {0} برابر با مقدار انتظاری {1} نیست.", actual, expected));
     }
 
 object[] Lnk2ResourceSupportCases = new object[]
 {
     new object[]
     {
         "00af34a0-a90b-674d-a821-73ee508c5479",
         "rgb8_2x2.png",
         "png",
         string.Empty,
         0x53,
         0d,
         string.Empty,
         7,
         true,
         0x124L,
         0x74cL
     }
 };

 object[] LayeredLnk2ResourceSupportCases = new object[]
 {
     new object[]
     {
         "69ac1c0d-1b74-fd49-9c7e-34a7aa6299ef",
         "huset.jpg",
         "JPEG",
         string.Empty,
         0x9d46,
         0d,
         "xmp.did:0F94B342065B11E395B1FD506DED6B07",
         7,
         true,
         0x9E60L,
         0xc60cL
     },
     new object[]
     {
         "5a7d1965-0eae-b24e-a82f-98c7646424c2",
         "panama-papers.jpg",
         "JPEG",
         string.Empty,
         0xF56B,
         0d,
         "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
         7,
         true,
         0xF694L,
         0x10dd4L
     },
 };

 object[] LayeredLnk3ResourceSupportCases = new object[]
 {
     new object[]
     {
         "2fd7ba52-0221-de4c-bdc4-1210580c6caa",
         "panama-papers.jpg",
         "JPEG",
         string.Empty,
         0xF56B,
         0d,
         "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
         7,
         true,
         0xF694l,
         0x10dd4L
     },
     new object[]
     {
         "372d52eb-5825-8743-81a7-b6f32d51323d",
         "huset.jpg",
         "JPEG",
         string.Empty,
         0x9d46,
         0d,
         "xmp.did:0F94B342065B11E395B1FD506DED6B07",
         7,
         true,
         0x9E60L,
         0xc60cL
     },
 };

 var basePath = @"PSDNET392_1\";
 const string Output = "Output\";

 // ذخیره داده یک اشیای هوشمند در فایل PSD به یک فایل
 void SaveSmartObjectData(string prefix, string fileName, byte[] data)
 {
     var filePath = basePath + prefix + "_"  + fileName;

     using (var container = FileStreamContainer.CreateFileStream(filePath, false))
     {
         container.Write(data);
     }
 }

 // بارگذاری داده جدید برای یک اشیای هوشمند در فایل PSD
 byte[] LoadNewData(string fileName)
 {
     using (var container = FileStreamContainer.OpenFileStream(basePath + fileName))
     {
         return container.ToBytes();
     }
 }
  
 // دریافت و تنظیم ویژگی‌ها در Lnk2 / Lnk3 Resource PSD و منابع داده‌ی liFD آن در تصویر PSD
 void ExampleOfLnk2ResourceSupport(
     string fileName,
     int dataSourceCount,
     int length,
     int newLength,
     object[] dataSourceExpectedValues)
 {
     using (PsdImage image = (PsdImage)Image.Load(basePath + fileName))
     {
         Lnk2Resource lnk2Resource = null;
         foreach (var resource in image.GlobalLayerResources)
         {
             lnk2Resource = resource as Lnk2Resource;
             if (lnk2Resource != null)
             {
                 AssertAreEqual(lnk2Resource.DataSourceCount, dataSourceCount);
                 AssertAreEqual(lnk2Resource.Length, length);
                 AssertAreEqual(lnk2Resource.IsEmpty, false);
 
                 for (int i = 0; i < lnk2Resource.DataSourceCount; i++)
                 {
                     LiFdDataSource lifdSource = lnk2Resource[i];
                     object[] expected = (object[])dataSourceExpectedValues[i];
                     AssertAreEqual(LinkDataSourceType.liFD, lifdSource.Type);
                     AssertAreEqual(new Guid((string)expected[0]), lifdSource.UniqueId);
                     AssertAreEqual(expected[1], lifdSource.OriginalFileName);
                     AssertAreEqual(expected[2], lifdSource.FileType.TrimEnd(' '));
                     AssertAreEqual(expected[3], lifdSource.FileCreator.TrimEnd(' '));
                     AssertAreEqual(expected[4], lifdSource.Data.Length);
                     AssertAreEqual(expected[5], lifdSource.AssetModTime);
                     AssertAreEqual(expected[6], lifdSource.ChildDocId);
                     AssertAreEqual(expected[7], lifdSource.Version);
                     AssertAreEqual((bool)expected[8], lifdSource.HasFileOpenDescriptor);
                     AssertAreEqual(expected[9], lifdSource.Length);
 
                     if (lifdSource.HasFileOpenDescriptor)
                     {
                         AssertAreEqual(-1, lifdSource.CompId);
                         AssertAreEqual(-1, lifdSource.OriginalCompId);
                         lifdSource.CompId = int.MaxValue;
                     }
 
                     SaveSmartObjectData(
                         Output + fileName,
                         lifdSource.OriginalFileName,
                         lifdSource.Data);
                     lifdSource.Data = LoadNewData("new_" + lifdSource.OriginalFileName);
                     AssertAreEqual(expected[10], lifdSource.Length);
 
                     lifdSource.ChildDocId = Guid.NewGuid().ToString();
                     lifdSource.AssetModTime = double.MaxValue;
                     lifdSource.FileType = "test";
                     lifdSource.FileCreator = "me";
                 }
 
                 AssertAreEqual(newLength, lnk2Resource.Length);
                 break;
             }
         }
 
         AssertAreEqual(true, lnk2Resource != null);
         if (image.BitsPerChannel < 32) // 32 bit per channel saving is not supported yet
         {
             image.Save(basePath + Output + fileName, new PsdOptions(image));
         }
     }
 }
 
 // این مثال نشان می دهد چگونه ویژگی‌های PSD Lnk2 / Lnk3 Resource و دیداده‌های liFD آن را در تصویر PSD دریافت و تنظیم کنید
 ExampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
 // این مثال نشان می دهد چگونه ویژگی‌های PSD Lnk3 Resource و دیداده‌های liFD آن را برای 32 بیت بر کانال دریافت و تنظیم کنید
 ExampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
 // این مثال نشان می دهد چگونه ویژگی‌های PSD Lnk2 Resource و دیداده‌های liFD آن را برای 16 بیت بر کانال دریافت و تنظیم کنید
 ExampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}

**PSDNET-201. پشتیبانی از پیشرفت تبدیل سند**

{{< highlight csharp >}}
string sourceFilePath = "Apple.psd";
Stream outputStream = new MemoryStream();
ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)
{
      string message = string.Format(
           "{0} {1}: {2} از {3}",
           progressInfo.Description,
           progressInfo.EventType,
           progressInfo.Value,
           progressInfo.MaxValue);
      Console.WriteLine(message);
};
Console.WriteLine("---------- بارگذاری Apple.psd ----------");
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

{{< highlight csharp >}}
 /* این مثال نشان می دهد چگونه می‌توانید برنامه نویسی‌های PSD روشنایی/کنتراست تصویر PSD - BritResource را به صورت برنامه نویسی تغییر دهید

   این یک API پایینی Aspose.PSD می‌باشد. می‌توانید از لایه روشنایی/کنتراست از طریق API‌اش استفاده کنید که به راحتی‌تر خواهد بود، 

   اما ایجاد ویرایش مستقیم منابع فتوشاپ کنترل بیشتری بر محتوای فایل PSD می‌دهد.  */

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
                   