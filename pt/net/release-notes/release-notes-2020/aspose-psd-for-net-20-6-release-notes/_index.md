---
title: Aspose.PSD for .NET 20.6 - Notas da Versão
type: docs
weight: 70
url: /pt/net/aspose-psd-for-net-20-6-release-notes/
---

{{% alert color="primary" %}} 
  
Esta página contém as notas da versão do [Aspose.PSD for .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-606 |Suporte de recurso LnkE|Recurso|
|PSDNET-386 |Suporte de recurso britResource (Recurso de Camada de Ajuste de Brilho/Contraste)|Recurso|
|PSDNET-219|Mover configuração DefaultReplacementFont para a classe ImageOptionsBase|Aprimoramento|
|PSDNET-596|Grupo de Camadas com Modo de Mistura Não PassThrough Não é Renderizado|Erro|
|PSDNET-610|Exceção de Referência Nula ao tentar converter um arquivo Psd específico em imagem|Erro|
|PSDNET-636|Ajuste Incorreto ao redimensionar arquivos PSD se houver uma máscara na camada de ajuste que tenha limites vazios|Erro|
|PSDNET-611|OverflowException ao tentar abrir um arquivo Psd específico|Erro|
|PSDNET-565|Imagem Psd com modo RGB de 16 bits/canal atualiza apenas camadas na visualização|Erro|
|PSDNET-652|Exceção ao carregar arquivo PSD específico com o recurso composto LnkE e propriedade adobeStockLicenseState|Erro|
|PSDNET-640|Alterações na Máscara da Camada PSD são descartadas ao salvar|Erro|
|PSDNET-593|Salvamento de arquivo AI para formato Jpeg2000 não funciona|Erro|
|PSDNET-638|Ordem Incorreta da Camada após adicionar Grupo de Camadas a Grupo de Camadas vazio|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
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
# **APIs Removidas:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Exemplos de Uso:**
**PSDNET-606. Suporte de Recurso LnkE**

{{< highlight java >}}

 string message = "O Suporte de LnkeResource funciona incorretamente.";

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

// Este exemplo demonstra como obter e definir propriedades do Recurso LnkE do Psd do Photoshop que contém informações sobre um arquivo vinculado externo.

void ExemploDeSuporteDeLnkeResource(

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

// Este exemplo demonstra como obter e definir propriedades do Recurso LnkE do Psd do Photoshop que contém informações sobre um arquivo JPEG vinculado externamente.

this.ExemploDeSuporteDeLnkeResource(

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

// Este exemplo demonstra como obter e definir propriedades do Recurso LnkE do Psd do Photoshop que contém informações sobre um arquivo PNG vinculado externamente.

this.ExemploDeSuporteDeLnkeResource(

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

// Este exemplo demonstra como obter e definir propriedades do Recurso LnkE do Psd do Photoshop que contém informações sobre um Ativo de Bibliotecas CC vinculado externamente.

this.ExemploDeSuporteDeLnkeResource(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Recurso disponível no Photoshop CC 2015)",

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

**PSDNET-201. Suporte para progresso de conversão de documento**

{{< highlight java >}}

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

      Console.WriteLine("---------- Salvando Apple.psd no formato PNG ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Salvando Apple.psd no formato PSD ----------");

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

**PSDNET-386. Suporte de recurso britResource (Recurso de Camada de Ajuste de Brilho/Contraste)**

{{< highlight java >}}

 /* Este exemplo demonstra como você pode alterar programaticamente o recurso de Camada de Brilho/Contraste da Imagem PSD - BritResource

   Esta é uma API de baixo nível do Aspose.PSD. Você pode usar a Camada de Brilho/Contraste através de sua API, o que será muito mais fácil, 

   mas a edição direta de recursos do PhotoShop lhe dá mais controle sobre o conteúdo do arquivo PSD.  */

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

                        throw new Exception("BritResource foi lido incorretamente");

                    }

                    // Teste de edição e salvamento

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

**PSDNET-596. Grupo de Camada com Modo de Mistura Não PassThrough não é Renderizado**

{{< highlight java >}}

 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";

string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";

using (var input = (PsdImage)Image.Load(sourceFilePath))

{

    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-610. Exceção de Referência Nula ao tentar converter um arquivo Psd específico em imagem**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

` `**PSDNET-636. O redimensionamento de arquivos PSD funciona incorretamente se houver uma máscara na camada de ajuste que possui limites vazios**

{{< highlight java >}}

 int escala = 2;

string[] nomes = {

                    