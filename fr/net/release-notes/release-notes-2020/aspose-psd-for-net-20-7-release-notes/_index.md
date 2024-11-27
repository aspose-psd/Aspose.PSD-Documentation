---
title: Notes de version Aspose.PSD pour .NET 20.7
type: docs
weight: 60
url: /fr/net/aspose-psd-pour-net-20-7-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-673|Prise en charge de la ressource LnkE|Fonctionnalité|
|PSDNET-392|Prise en charge de la ressource britResource (Ressource de la couche d'ajustement de luminosité/contraste)|Fonctionnalité|
|PSDNET-629|Changement du message d'erreur lors de la tentative d'ouverture de formats non pris en charge en tant qu'image|Amélioration|
|PSDNET-594|Échec de l'enregistrement de LayerMask|Bogue|
|PSDNET-597|Avertissement de Photoshop lors de l'ouverture d'un fichier PSD après la création d'un nouveau groupe de calques|Bogue|
|PSDNET-618|Masque d'écrêtage non appliqué au dossier|Bogue|
|PSDNET-625|Impossible d'ouvrir un fichier avec Aspose.PSD pour .NET|Bogue|
|PSDNET-650|Exception d'échec d'enregistrement de l'image lors de la conversion PSD en PDF|Bogue|
|PSDNET-655|L'opération de rognage rend le chemin de rognage invalide dans l'image PSD|Bogue|
|PSDNET-662|Exception de NullReference lors de la tentative d'enregistrement d'un fichier PSD spécifique avec l'effet d'ombrage|Bogue|
|PSDNET-666|Aspose.PSD renvoie vrai sur Image.CanLoad(pdfStream)|Bogue|
|PSDNET-676|Échec du rendu des calques dans PNG généré|Bogue|
|PSDNET-677|Exception lors de l'accès à TextData|Bogue|
|PSDNET-679|ImageSaveException lors de l'enregistrement du PSD|Bogue|

## **Changements dans l'API publique**
# **APIs ajoutées:**
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

# **APIs supprimées:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Exemples d'utilisation:**
**PSDNET-606. Support de la ressource LnkE**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
 {
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("La valeur réelle {0} n'est pas égale à {1} attendue.", actual, expected));
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

 // Enregistre les données d'un objet intelligent dans un fichier PSD.
 void SaveSmartObjectData(string prefix, string fileName, byte[] data)
 {
     var filePath = basePath + prefix + "_"  + fileName;
 
     using (var container = FileStreamContainer.CreateFileStream(filePath, false))
     {
         container.Write(data);
     }
 }
 
 // Charge les nouvelles données pour un objet intelligent dans un fichier PSD.
 byte[] LoadNewData(string fileName)
 {
     using (var container = FileStreamContainer.OpenFileStream(basePath + fileName))
     {
         return container.ToBytes();
     }
 }
  
 // Obtient et définit les propriétés de la ressource Lnk2 / Lnk3 PSD et de ses sources de données LiFD dans l'image PSD
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
 
 // Cet exemple montre comment obtenir et définir les propriétés de la ressource Lnk2 PSD et de ses sources de données LiFD pour 8 bits par canal.
 ExampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
 // Cet exemple montre comment obtenir et définir les propriétés de la ressource Lnk3 PSD et de ses sources de données LiFD pour 32 bits par canal.
 ExampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
 // Cet exemple montre comment obtenir et définir les propriétés de la ressource Lnk2 PSD et de ses sources de données LiFD pour 16 bits par canal.
 ExampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}

**PSDNET-201. Prise en charge de la progression de conversion de document**

{{< highlight csharp >}}
string sourceFilePath = "Apple.psd";
Stream outputStream = new MemoryStream();
ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)
{
      string message = string.Format(
           "{0} {1}: {2} sur {3}",
           progressInfo.Description,
           progressInfo.EventType,
           progressInfo.Value,
           progressInfo.MaxValue);
      Console.WriteLine(message);
};
Console.WriteLine("---------- Chargement d'Apple.psd ----------");
var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };
using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))
{
      Console.WriteLine("---------- Enregistrement d'Apple.psd au format PNG ----------");
      image.Save(
           outputStream,
           new PngOptions()
           {
                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler
           });
      Console.WriteLine("---------- Enregistrement d'Apple.psd au format PSD ----------");
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

**PSDNET-386. Prise en charge de britResource (Ressource de la couche d'ajustement de luminosité/contraste)**

{{< highlight csharp >}}
 /* Cet exemple montre comment changer programmation la ressource britResource de luminosité/contraste de l'image PSD

   Il s'agit d'une API Aspose.PSD de bas niveau. Vous pouvez utiliser la couche luminosité/contraste à travers son API, ce qui sera beaucoup plus facile, 

   mais la modification directe des ressources PhotoShop vous donne plus de contrôle sur le contenu du fichier PSD.  */

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
                        throw new Exception("La ressource BritResource a été lue incorrectement");
                    }

                    // Test d'édition et d'enregistrement
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

**PSDNET-596. Le groupe de calques avec un mode de fusion autre que PassThrough n'est pas rendu**

{{< highlight csharp >}}
 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";
string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";
using (var input = (PsdImage)Image.Load(sourceFilePath))

{
    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}

{{< /highlight >}}

**PSDNET-610. Exception NullReference lors de la tentative de conversion d'un fichier Psd particulier en image**

{{< highlight csharp >}}
 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{
    psdImage.Save("output.png", new PngOptions());
}
{{< /highlight >}}

**PSDNET-636. Le redimensionnement des fichiers PSD ne fonctionne pas correctement s'il y a un masque dans la couche d'ajustement qui a des limites vides**

{{< highlight csharp >}}

int échelle = 2;
string[] noms = {
                     "OneRegularAndOneAdjustmentWithVectorAndLayerMask",
                     "LevelsLayerWithLayerMaskRgb",
                     "LevelsLayerWithLayerMaskCmyk",
                 };
for (int i = 0; i < noms.Length; i++)
{
    string sourceFilePath = noms[i] + ".psd";
    string outputFilePath = "output_" + sourceFilePath;
    string outputPngFilePath = "output_" + noms[i] + ".png";
    var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
    using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, psdLoadOptions))
    {
        image.Resize(image.Width * scale, image.Height * scale);
        image.Save(outputFilePath, new PsdOptions());
        image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-611. OverflowException lors de la tentative d'ouverture d'un fichier Psd spécifique**

{{< highlight csharp >}}
 using (var psdImage = (