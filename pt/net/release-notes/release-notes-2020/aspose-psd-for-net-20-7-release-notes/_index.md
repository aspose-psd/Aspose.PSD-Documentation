---
title: Aspose.PSD for .NET 20.7 - Notas da Versão
type: docs
weight: 60
url: /pt/net/aspose-psd-for-net-20-7-notas-da-versao/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para o [Aspose.PSD for .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-673|Suporte ao Recurso LnkE|Funcionalidade|
|PSDNET-392|Suporte ao Recurso britResource (Recurso da Camada de Ajuste de Brilho/Contraste)|Funcionalidade|
|PSDNET-629|Alterar Mensagem de Exceção ao tentar abrir formatos não suportados como uma imagem|Melhoria|
|PSDNET-594|Falha ao salvar a Máscara de Camada|Erro|
|PSDNET-597|Ao salvar arquivo PSD após a criação de novo Grupo de Camadas, é exibido um aviso do Photoshop na abertura do arquivo|Erro|
|PSDNET-618|Máscara de recorte não está sendo aplicada à pasta|Erro|
|PSDNET-625|Não é possível abrir arquivo com o Aspose.PSD para .NET|Erro|
|PSDNET-650|Exceção de falha ao salvar imagem ao converter PSD para PDF|Erro|
|PSDNET-655|Operação de recorte torna o caminho de recorte inválido na imagem PSD|Erro|
|PSDNET-662|Exceção de Referência Nula ao tentar salvar arquivo PSD específico com Efeito Sombra|Erro|
|PSDNET-666|Aspose.PSD retorna true em Image.CanLoad(pdfStream)|Erro|
|PSDNET-676|Camadas não são renderizadas no PNG gerado|Erro|
|PSDNET-677|Exceção ao acessar TextData|Erro|
|PSDNET-679|ImageSaveException ao salvar o PSD|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
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

# **APIs Removidas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Exemplos de Uso:**
**PSDNET-606. Suporte ao Recurso LnkE**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
 {
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("O valor atual {0} não é igual ao esperado {1}.", actual, expected));
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
 
 // Salva os dados de um objeto inteligente no arquivo PSD para um arquivo.
 void SaveSmartObjectData(string prefix, string fileName, byte[] data)
 {
     var filePath = basePath + prefix + "_"  + fileName;
 
     using (var container = FileStreamContainer.CreateFileStream(filePath, false))
     {
         container.Write(data);
     }
 }
 
 // Carrega os novos dados para um objeto inteligente no arquivo PSD.
 byte[] LoadNewData(string fileName)
 {
     using (var container = FileStreamContainer.OpenFileStream(basePath + fileName))
     {
         return container.ToBytes();
     }
 }
  
 // Obtém e configura propriedades do Recurso Lnk2 / Lnk3 da PSD e suas fontes de dados LiFD na imagem PSD.
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
         if (image.BitsPerChannel < 32) // Salvar com 32 bits por canal não é suportado ainda
         {
             image.Save(basePath + Output + fileName, new PsdOptions(image));
         }
     }
 }
 
 // Este exemplo demonstra como obter e configurar propriedades do Recurso Lnk2 e suas fontes LiFD para 8 bits por canal.
 ExampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
 // Este exemplo demonstra como obter e configurar propriedades do Recurso Lnk3 e suas fontes LiFD para 32 bits por canal.
 ExampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
 // Este exemplo demonstra como obter e configurar propriedades do Recurso Lnk2 e suas fontes LiFD para 16 bits por canal.
 ExampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}


**PSDNET-201. Suporte ao Progresso da Conversão de Documentos**

{{< highlight csharp >}}
string sourceFilePath = "Apple.psd";
Stream outputStream = new MemoryStream();
ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo progressInfo)
{
      string message = string.Format(
           "{0} {1}: {2} de {3}",
           progressInfo.Description,
           progressInfo.EventType,
           progressInfo.Value,
           progressInfo.MaxValue);
      Console.WriteLine(message);
};
Console.WriteLine("---------- Carregando Apple.psd ----------");
var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };
using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))
{
      Console.WriteLine("---------- Salvando Apple.psd para formato PNG ----------");
      image.Save(
           outputStream,
           new PngOptions()
           {
                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler
           });
      Console.WriteLine("---------- Salvando Apple.psd para formato PSD ----------");
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

**PSDNET-386. Suporte ao Recurso britResource (Recurso da Camada de Ajuste de Brilho/Contraste)**

{{< highlight csharp >}}
 /* Este exemplo demonstra como você pode alterar programaticamente o Recurso da Camada de Brightness/Contrast Image - BritResource da Imagem PSD
    Esta é uma API de Baixo Nível da Aspose.PSD. Você pode usar a Camada de Brilho/Contraste através de sua API, o que será muito mais fácil,
    mas a edição direta de recursos do Photoshop lhe dá mais controle sobre o conteúdo do arquivo PSD.  */

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

**PSDNET-596. Grupo de Camada com Modo de Mesclagem não de Passagem Não é Renderizado**

{{< highlight csharp >}}
 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";
string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";
using (var input = (PsdImage)Image.Load(sourceFilePath))

{
    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}

{{< /highlight >}}

**PSDNET-610. Exceção NullReference ao tentar converter arquivo PSD específico em imagem**

{{< highlight csharp >}}
 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{
    psdImage.Save("output.png", new PngOptions());
}
{{< /highlight >}}

**PSDNET-636. Redimensionamento de arquivos PSD não funciona corretamente se houver uma máscara na camada de ajuste que possui limites vazios**

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
        image.Resize(image.Width * scale, image.Height * scale);
        image.Save(outputFilePath, new PsdOptions());
        image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-611. OverflowException ao tentar abrir arquivo PSD específico**

{{< highlight csharp >}}
 using (var psdImage = (PsdImage)Image.Load("CT_SkillTest_v1.psd"))
{
    psdImage.Save("output.psd");
}
// Carregado e salvo sem lançar exceções.

{{< /highlight >}}

**PSDNET-565. Imagem PSD com modo RGB 16 bit por canal**

{{< highlight csharp >}}
string sourceFilePath = @"in.psd";
