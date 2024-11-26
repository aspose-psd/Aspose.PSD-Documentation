---
title: Aspose.PSD for .NET 20.7 - บันทึกการอัพเดต
type: docs
weight: 60
url: /th/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการอัพเดตสำหรับ [Aspose.PSD for .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-673|การสนับสนุนของ LnkE Resource|คุณลักษณะ|
|PSDNET-392|การสนับสนุน britResource (Resource ของ Brightness/Contrast Adjustment Layer)|คุณลักษณะ|
|PSDNET-629|เปลี่ยนข้อความข้อผิดพลาดเมื่อพยายามเปิดรูปแบบที่ไม่รองรับเป็นภาพ|ปรับปรุง|
|PSDNET-594|บันทึก LayerMask ไม่สำเร็จ|ข้อบกพร่อง|
|PSDNET-597|หากบันทึกไฟล์ PSD หลังจากสร้าง Layer Group ใหม่ เราจะได้การเตือนจาก Photoshop เมื่อเปิดไฟล์|ข้อบกพร่อง|
|PSDNET-618|การ Clipping mask ไม่ได้ใช้กับโฟลเดอร์|ข้อบกพร่อง|
|PSDNET-625|ไม่สามารถเปิดไฟล์ด้วย Aspose.PSD for .NET ได้|ข้อบกพร่อง|
|PSDNET-650|ข้อยกเว้นการบันทึกรูปภาพเมื่อแปลง PSD เป็น PDF ไม่สำเร็จ|ข้อบกพร่อง|
|PSDNET-655|การดำเนินการขอบจะทำให้เส้นทาง Clipping ไม่ถูกต้องในรูปภาพ PSD|ข้อบกพร่อง|
|PSDNET-662|NullReference Exception เมื่อพยายามบันทึกไฟล์ PSD ที่เฉพาะเจนด้วยเอฟเฟ็กต์เงา|ข้อบกพร่อง|
|PSDNET-666|Aspose.PSD คืนค่า true ใน Image.CanLoad(pdfStream)|ข้อบกพร่อง|
|PSDNET-676|การแสดงเลเยอร์ไม่สำเร็จใน PNG ที่สร้างขึ้น|ข้อบกพร่อง|
|PSDNET-677|ข้อยกเว้นในการเข้าถึง TextData|ข้อบกพร่อง|
|PSDNET-679|ImageSaveException เมื่อบันทึก PSD|ข้อบกพร่อง|

## **การเปลี่ยนแปลง Public API**
# **เพิ่ม APIs:**
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

# **API ที่ถูกนำออก:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **ตัวอย่างการใช้:**
**PSDNET-606. การสนับสนุน LnkE Resource**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
 {
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("Actual value {0} are not equal to expected {1}.", actual, expected));
     }
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
 
 // บันทึกข้อมูลของอ็อบเจ็กต์อัจฉริยะในไฟล์ PSD เป็นไฟล์
 void SaveSmartObjectData(string prefix, string fileName, byte[] data)
 {
     var filePath = basePath + prefix + "_"  + fileName;
 
     using (var container = FileStreamContainer.CreateFileStream(filePath, false))
     {
         container.Write(data);
     }
 }
 
 // โหลดข้อมูลใหม่สำหรับอ็อบเจ็กต์อัจฉริยะในไฟล์ PSD
 byte[] LoadNewData(string fileName)
 {
     using (var container = FileStreamContainer.OpenFileStream(basePath + fileName))
     {
         return container.ToBytes();
     }
 }
  
 // รับและกำหนดคุณสมบัติของรีซอร์ส Lnk2 / Lnk3 ใน PSD image
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
 
 // ตัวอย่างนี้แสดงวิธีการรับและกำหนดคุณสมบัติของรีซอร์ส Lnk2 / Lnk3 และแหล่งข้อมูล liFD ในรูปภาพ PSD
 ExampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
 // ตัวอย่างนี้แสดงวิธีการรับและกำหนดคุณสมบัติของรีซอร์ส Lnk3 และแหล่งข้อมูล liFD สำหรับ 32 บิตต่อช่อง
 ExampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
 // ตัวอย่างนี้แสดงวิธีการรับและกำหนดคุณสมบัติของรีซอร์ส Lnk2 และแหล่งข้อมูล liFD สำหรับ 16 บิตต่อช่อง
 ExampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}
**PSDNET-201. การสนับสนุนการแปลงเอกสารและความคืบหน้า**

{{< highlight csharp >}}
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
Console.WriteLine("---------- กำลังโหลด Apple.psd ----------");
var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };
using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))
{
      Console.WriteLine("---------- กำลังบันทึก Apple.psd เป็นรูปแบบ PNG ----------");
      image.Save(
           outputStream,
           new PngOptions()
           {
                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler
           });
      Console.WriteLine("---------- กำลังบันทึก Apple.psd เป็นรูปแบบ PSD ----------");
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
**PSDNET-386. การสนับสนุน britResource (Resource ของ Brightness/Contrast Adjustment Layer)**

{{< highlight csharp >}}
 /* ตัวอย่างนี้แสดงวิธีที่คุณสามารถเปลี่ยน Brightness/Contrast Layer Resource เป็นระบบโปรแกรมได้อย่างมีควบคุม
   เป็น API ระดับต่ำของ Aspose.PSD คุณสามารถใช้ Brightness/Contrast Layer ผ่าน API ของมันได้ง่ายกว่ามาก แต่การแก้ไขรีซอร์ทแบบโดยตรงใน Photoshop จะให้ควบคุมมากกว่า */

string path = @"