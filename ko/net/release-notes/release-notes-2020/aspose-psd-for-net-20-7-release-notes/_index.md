---
title: Aspose.PSD for .NET 20.7 - 릴리스 노트
type: docs
weight: 60
url: /ko/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

이 페이지에는 [Aspose.PSD for .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-673|LnkE 리소스 지원|기능|
|PSDNET-392|britResource 지원 (밝기/대비 조정 레이어의 리소스)|기능|
|PSDNET-629|이미지로 열 수 없는 형식을 시도할 때 예외 메시지 변경|향상|
|PSDNET-594|레이어 마스크 저장 실패|버그|
|PSDNET-597|새 레이어 그룹 생성 후 PSD 파일 저장 시 Photoshop 경고 메시지 표시|버그|
|PSDNET-618|클리핑 마스크가 폴더에 적용되지 않음|버그|
|PSDNET-625|Aspose.PSD for .NET으로 파일 열기 불가|버그|
|PSDNET-650|PSD를 PDF로 변환 시 이미지 저장 실패 예외|버그|
|PSDNET-655|PSD 이미지에서 rop 작업 클리핑 경로를 잘못 설정함|버그|
|PSDNET-662|그림자 효과가 있는 특정 PSD 파일 저장 시 NullReference 예외 발생|버그|
|PSDNET-666|이미지에서 Image.CanLoad(pdfStream)이 true를 반환함|버그|
|PSDNET-676|생성된 PNG에서 레이어가 렌더링되지 않음|버그|
|PSDNET-677|TextData에 액세스할 때 예외 발생|버그|
|PSDNET-679|PSD 저장 시 ImageSave 예외 발생|버그|

## **공개 API 변경**
# **추가된 API:**
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

# **제거된 API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **사용 예시:**
**PSDNET-606. LnkE 리소스 지원**

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
 const string Output = "Output\\";
 
 // Saves the data of a smart object in PSD file to a file.
 void SaveSmartObjectData(string prefix, string fileName, byte[] data)
 {
     var filePath = basePath + prefix + "_"  + fileName;
 
     using (var container = FileStreamContainer.CreateFileStream(filePath, false))
     {
         container.Write(data);
     }
 }
 
 // Loads the new data for a smart object in PSD file.
 byte[] LoadNewData(string fileName)
 {
     using (var container = FileStreamContainer.OpenFileStream(basePath + fileName))
     {
         return container.ToBytes();
     }
 }
  
 // Gets and sets properties of the PSD Lnk2 / Lnk3 Resource and its liFD data sources in PSD image
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
         if (image.BitsPerChannel < 32) // 32 비트 채널당 저장은 아직 지원되지 않음
         {
             image.Save(basePath + Output + fileName, new PsdOptions(image));
         }
     }
 }
 
 // 이 예제는 8 비트 채널을 위한 PSD Lnk2 리소스와 liFD 데이터 소스의 속성을 가져오고 설정하는 방법을 보여줍니다.
 ExampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
 // 이 예제는 32 비트 채널을 위한 PSD Lnk3 리소스와 liFD 데이터 소스의 속성을 가져오고 설정하는 방법을 보여줍니다.
 ExampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
 // 이 예제는 16 비트 채널을 위한 PSD Lnk2 리소스와 liFD 데이터 소스의 속성을 가져오고 설정하는 방법을 보여줍니다.
 ExampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}
**PSDNET-201. 문서 변환 진행 상황 지원**

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
Console.WriteLine("---------- Loading Apple.psd ----------");
var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };
using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))
{
      Console.WriteLine("---------- Saving Apple.psd to PNG format ----------");
      image.Save(
           outputStream,
           new PngOptions()
           {
                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler
           });
      Console.WriteLine("---------- Saving Apple.psd to PSD format ----------");
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
**PSDNET-386. britResource (밝기/대비 조정 레이어의 리소스)**

{{< highlight csharp >}}
 /* 이 예제는 PSD 이미지의 밝기/대비 조정 레이어 리소스인 BritResource를 프로그래밍적으로 변경하는 방법을 보여줍니다.
   
   이것은 Low-Level Aspose.PSD API입니다. 밝기/대비 조정 레이어 API를 사용할 수도 있지만, 직접 PhotoShop 리소스 편집은 PSD 파일 내용에 대해 더 많은 제어를 제공합니다. */

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

                    // Test editing and saving
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
**PSDNET-596. PassThrough 혼합 모드가 아닌 레이어 그룹이 렌더링되지 않음**

{{< highlight csharp >}}
 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";
string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";
using (var input = (PsdImage)Image.Load(sourceFilePath))

{
    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}

{{< /highlight >}}

**PSDNET-610. 특정 Psd 파일을 이미지로 변환하려고 할 때 NullReference 예외가 발생하는 문제**

{{< highlight csharp >}}
 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{
    psdImage.Save("output.png", new PngOptions());
}
{{< /highlight >}}

**PSDNET-636. 빈 바운드를 갖는 조정 레이어 마스크가 있는 경우 PSD 파일 크기 조정이 잘못 작동함**

{{< highlight csharp >}}

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
        image.Resize(image.Width * 
{{< /highlight >}}