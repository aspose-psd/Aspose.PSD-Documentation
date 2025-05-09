---
title: Aspose.PSD cho .NET 20.7 - Ghi Chú Phát Hành
type: docs
weight: 60
url: /vi/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-673|Hỗ trợ nguồn LnkE|Tính năng|
|PSDNET-392|Hỗ trợ nguồn britResource (Nguồn của Lớp Điều Chỉnh Độ Sáng/Độ Tương Phản)|Tính năng|
|PSDNET-629|Thay đổi thông báo ngoại lệ khi cố gắng mở các định dạng không được hỗ trợ làm hình ảnh|Cải tiến|
|PSDNET-594|Lỗi khi thất bại trong việc lưu LayerMask|Lỗi|
|PSDNET-597|Nếu ta lưu tệp PSD sau khi tạo Nhóm Layer mới, ta nhận được cảnh báo Photoshop khi mở tệp|Lỗi|
|PSDNET-618|Clipping mask không áp dụng cho thư mục|Lỗi|
|PSDNET-625|Không thể mở tệp bằng Aspose.PSD cho .NET|Lỗi|
|PSDNET-650|Ngoại lệ thất bại khi lưu hình ảnh khi chuyển đổi PSD sang PDF|Lỗi|
|PSDNET-655|Thao tác rop làm cho đường bao Clipping không hợp lệ trong hình ảnh PSD|Lỗi|
|PSDNET-662|Ngoại lệ NullReference khi cố gắng lưu tệp PSD cụ thể với Hiệu Ứng Bóng|Lỗi|
|PSDNET-666|Aspose.PSD trả về true trên Image.CanLoad(pdfStream)|Lỗi|
|PSDNET-676|Lớp không thể vẽ trong hình ảnh PNG đã tạo|Lỗi|
|PSDNET-677|Ngoại lệ khi truy cập TextData|Lỗi|
|PSDNET-679|ImageSaveException khi lưu tệp PSD|Lỗi|

## **Thay Đổi API Công Khai**
# **API Đã Thêm:**
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

# **API Đã Xóa:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Ví Dụ Sử Dụng:**
**PSDNET-606. Hỗ trợ nguồn LnkE**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
 {
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("Giá trị thực {0} không bằng với dự kiến {1}.", actual, expected));
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
 
 // Lưu dữ liệu của một đối tượng thông minh trong tệp PSD vào một tệp.
 void SaveSmartObjectData(string prefix, string fileName, byte[] data)
 {
     var filePath = basePath + prefix + "_"  + fileName;
 
     using (var container = FileStreamContainer.CreateFileStream(filePath, false))
     {
         container.Write(data);
     }
 }
 
 // Tải dữ liệu mới cho một đối tượng thông minh trong tệp PSD.
 byte[] LoadNewData(string fileName)
 {
     using (var container = FileStreamContainer.OpenFileStream(basePath + fileName))
     {
         return container.ToBytes();
     }
 }
  
 // Nhận và thiết lập các thuộc tính của Nguồn PSD Lnk2 / Lnk3 và các nguồn dữ liệu liFD tương ứng trong hình ảnh PSD
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

 // Ví dụ này minh họa cách nhận và thiết lập các thuộc tính của Nguồn PSD Lnk2/Lnk3 và các nguồn dữ liệu liFD của nó cho 8 bit mỗi kênh.
 ExampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
 // Ví dụ này minh họa cách nhận và thiết lập các thuộc tính của Nguồn PSD Lnk3 và các nguồn dữ liệu liFD của nó cho 32 bit mỗi kênh.
 ExampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
 // Ví dụ này minh họa cách nhận và thiết lập các thuộc tính của Nguồn PSD Lnk2 và các nguồn dữ liệu liFD của nó cho 16 bit mỗi kênh.
 ExampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}
**PSDNET-201. Hỗ trợ tiến trình chuyển đổi tài liệu**

{{< highlight csharp >}}
string sourceFilePath = "Apple.psd";
Stream outputStream = new MemoryStream();
ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)
{
      string message = string.Format(
           "{0} {1}: {2} trong số {3}",
           progressInfo.Description,
           progressInfo.EventType,
           progressInfo.Value,
           progressInfo.MaxValue);
      Console.WriteLine(message);
};
Console.WriteLine("---------- Đang Tải Apple.psd ----------");
var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };
using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))
{
      Console.WriteLine("---------- Đang Lưu Apple.psd sang định dạng PNG ----------");
      image.Save(
           outputStream,
           new PngOptions()
           {
                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler
           });
      Console.WriteLine("---------- Đang Lưu Apple.psd sang định dạng PSD ----------");
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
**PSDNET-386. Hỗ trợ nguồn britResource (Nguồn của Lớp Điều Chỉnh Độ Sáng/Độ Tương Phản)**

{{< highlight csharp >}}
 /* Ví dụ này minh họa cách bạn có thể thay đổi theo cách lập trình Nguồn Độ Sáng/Độ Tương Phản Hình Ảnh PSD - BritResource

   Đây là một API Aspose.PSD ở Mức Thấp. Bạn có thể sử dụng Lớp Độ Sáng/Độ Tương Phản thông qua API của nó, điều này sẽ dễ dàng hơn, 

   nhưng việc chỉnh sửa nguồn của Photoshop trực tiếp sẽ cho bạn kiểm soát hơn về nội dung của tệp PSD.  */

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
                        throw new Exception("Nguồn BritResource đã đọc sai");
                    }

                    // Kiểm tra sửa đổi và lưu
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
**PSDNET-596. Nhóm Layer với Chế Độ Trộn Không Phải PassThrough Không được Render**

{{< highlight csharp >}}
 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";
string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";
using (var input = (PsdImage)Image.Load(sourceFilePath))

{
    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}

{{< /highlight >}}

**PSDNET-610. Ngoại lệ NullReference khi cố gắng chuyển đổi tệp Psd cụ thể thành hình ảnh**

{{< highlight csharp >}}
 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{
    psdImage.Save("output.png