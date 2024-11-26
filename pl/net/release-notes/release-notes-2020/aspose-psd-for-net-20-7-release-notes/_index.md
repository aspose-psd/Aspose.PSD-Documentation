---
title: Aspose.PSD dla .NET 20.7 - Notatki dotyczące wydania
type: docs
weight: 60
url: /pl/net/aspose-psd-dla-net-20-7-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-673|Obsługa zasobu LnkE|Funkcja|
|PSDNET-392|Obsługa zasobu britResource (Zasób warstwy regulacji jasności/kontrastu)|Funkcja|
|PSDNET-629|Zmiana wiadomości o wyjątku podczas próby otwarcia nieobsługiwanych formatów jako obraz|Udoskonalenie|
|PSDNET-594|Nieudane zapisywanie maski warstwy|Błąd|
|PSDNET-597|Ostrzeżenie Photoshopa o nowej grupie warstw przy próbie zapisu pliku PSD po utworzeniu nowej grupy warstw|Błąd|
|PSDNET-618|Maska obcinająca nie jest stosowana do folderu|Błąd|
|PSDNET-625|Nie można otworzyć pliku za pomocą Aspose.PSD dla .NET|Błąd|
|PSDNET-650|Wyjątek podczas zapisywania obrazu podczas konwersji PSD do PDF|Błąd|
|PSDNET-655|Operacja rop powoduje, że ścieżka obcinająca w obrazie PSD jest nieprawidłowa|Błąd|
|PSDNET-662|Wystąpienie NullReference Exception przy próbie zapisania określonego pliku PSD z efektem cienia|Błąd|
|PSDNET-666|Aspose.PSD zwraca true dla Image.CanLoad(pdfStream)|Błąd|
|PSDNET-676|Warstwy nie renderują się w wygenerowanym pliku PNG|Błąd|
|PSDNET-677|Wyjątek podczas dostępu do TextData|Błąd|
|PSDNET-679|Wyjątek ImageSaveException podczas zapisywania pliku PSD|Błąd|

## **Zmiany w publicznym API**
# **Nowo dodane API:**
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

# **Usunięte API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Przykłady użycia:**
**PSDNET-606. Obsługa zasobu LnkE**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
{
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("Wartość rzeczywista {0} nie jest równa oczekiwanej {1}.", actual, expected));
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
 
 // Zapisuje dane obiektów inteligentnych w pliku PSD do pliku.
 void SaveSmartObjectData(string prefix, string fileName, byte[] data)
 {
     var filePath = basePath + prefix + "_"  + fileName;
 
     using (var container = FileStreamContainer.CreateFileStream(filePath, false))
     {
         container.Write(data);
     }
 }
 
 // Ładuje nowe dane do obiektu inteligentnego w pliku PSD.
 byte[] LoadNewData(string fileName)
 {
     using (var container = FileStreamContainer.OpenFileStream(basePath + fileName))
     {
         return container.ToBytes();
     }
 }
  
 // Pobiera i ustawia właściwości zasobu PSD Lnk2 / Lnk3 oraz jego źródeł danych liFD w obrazie PSD
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
 
 // Ten przykład demonstruje, jak pobrać i ustawić właściwości zasobu PSD Lnk2 / Lnk3 oraz jego źródeł danych liFD w obrazie z 8 bitami na kanał.
 ExampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
 // Ten przykład demonstruje, jak pobrać i ustawić właściwości zasobu PSD Lnk3 oraz jego źródeł danych liFD w obrazie z 32 bitami na kanał.
 ExampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
 // Ten przykład demonstruje, jak pobrać i ustawić właściwości zasobu PSD Lnk2 oraz jego źródeł danych liFD w obrazie z 16 bitami na kanał.
 ExampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}
**PSDNET-201. Obsługa postępu konwersji dokumentu**

{{< highlight csharp >}}
string sourceFilePath = "Apple.psd";
Stream outputStream = new MemoryStream();
ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)
{
      string message = string.Format(
           "{0} {1}: {2} z {3}",
           progressInfo.Description,
           progressInfo.EventType,
           progressInfo.Value,
           progressInfo.MaxValue);
      Console.WriteLine(message);
};
Console.WriteLine("---------- Ładowanie pliku Apple.psd ----------");
var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };
using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))
{
      Console.WriteLine("---------- Zapisywanie pliku Apple.psd w formacie PNG ----------");
      image.Save(
           outputStream,
           new PngOptions()
           {
                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler
           });
      Console.WriteLine("---------- Zapisywanie pliku Apple.psd w formacie PSD ----------");
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
**PSDNET-386. Obsługa zasobu britResource (Zasób warstwy regulacji jasności/kontrastu)**

{{< highlight csharp >}}
 /* Ten przykład demonstruje, jak można programowo zmienić Zasób Warstwy Jasności/Kontrastu obrazu PSD - BritResource

   To jest API Aspose.PSD na niskim poziomie. Możesz użyć Warstwy Jasności/Kontrastu poprzez jej API, co będzie łatwiejsze, 

   ale bezpośrednia edycja zasobów PhotoShop daje większą kontrolę nad treścią pliku PSD.  */

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
                        throw new Exception("Zasób BritResource został błędnie odczytany");
                    }

                    // Test edycji i zapisywania
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
**PSDNET-596. Grupa warstw z trybem mieszania nie przejściowym nie jest renderowana**

{{< highlight csharp >}}
 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";
string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";
using (var input = (PsdImage)Image.Load(sourceFilePath))

{
    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}

{{< /highlight >}}

**PSDNET-610. Wystąpienie NullReference Exception przy próbie konwersji określonego pliku PSD na obraz**

{{< highlight csharp >}}
 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{
    psdImage.Save("output.png", new PngOptions());
}
{{< /highlight >}}

**PSDNET-636. Zmiana rozmiaru plików PSD działa nieprawidłowo, jeśli warstwa regulacji zawiera maskę, która ma puste granice**

{{< highlight csharp >}}

int skala = 2;
string[] nazwy = {
                     "OneRegularAndOneAdjustmentWithVectorAndLayerMask",
                     "LevelsLayerWithLayerMaskRgb",
                     "LevelsLayerWithLayerMaskCmyk",
                 };
for (int i