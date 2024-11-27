---
title: Notas de la versión de Aspose.PSD para .NET 20.6
type: docs
weight: 70
url: /es/net/aspose-psd-para-net-20-6-notas-de-version/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión de [Aspose.PSD para .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-606 |Soporte de recurso LnkE|Característica|
|PSDNET-386 |Soporte de britResource (Recurso de Capa de Ajuste de Brillo/Contraste)|Característica|
|PSDNET-219|Mover la configuración DefaultReplacementFont a la clase ImageOptionsBase|Mejora|
|PSDNET-596|Grupo de Capas con Modo de Mezcla no PasaPor Se No Se Renderiza|Error|
|PSDNET-610|Excepción de NullReference al intentar convertir un archivo Psd específico a imagen|Error|
|PSDNET-636|El redimensionamiento de archivos PSD no funciona correctamente si hay una máscara en la capa de ajuste que tiene límites vacíos|Error|
|PSDNET-611|OverflowException al intentar abrir un archivo Psd específico|Error|
|PSDNET-565|La imagen Psd con modo RGB de 16 bits por canal actualiza las capas solo en vista previa|Error|
|PSDNET-652|Excepción al cargar un archivo PSD específico con el recurso compuesto LnkE y la propiedad adobeStockLicenseState|Error|
|PSDNET-640|Los cambios en la máscara de capa PSD se descartan al guardar|Error|
|PSDNET-593|La guardado de Archivo AI en formato Jpeg2000 no funciona|Error|
|PSDNET-638|Orden de Capas Incorrectas después de agregar un Grupo de Capas a un Grupo de Capas vacío|Error|

## **Cambios en la API pública**
# **APIs Agregadas:**
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

# **APIs Eliminadas:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Ejemplos de Uso:**
**PSDNET-606. Soporte de recurso LnkE**

{{< highlight java >}}

 string message = "El soporte de EjemploOfLnkEResourceSupport funciona incorrectamente.";

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

// Este ejemplo muestra cómo obtener y establecer propiedades del recurso Photoshop Psd LnkE que contiene información sobre un archivo vinculado externo.

void EjemploDeSoporteDeRecursosLnkE(

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

// Este ejemplo demuestra cómo obtener y establecer propiedades del recurso Psd LnkE que contiene información sobre un archivo JPEG externo vinculado.

this.EjemploDeSoporteDeRecursosLnkE(

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

// Este ejemplo demuestra cómo obtener y establecer propiedades del recurso LnkE de Psd que contiene información sobre un archivo PNG vinculado externamente.

this.EjemploDeSoporteDeRecursosLnkE(

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

// Este ejemplo demuestra cómo obtener y establecer propiedades del recurso Photoshop Psd LnkE que contiene información sobre un activo de biblioteca de CC.

this.EjemploDeSoporteDeRecursosLnkE(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (La función está disponible en Photoshop CC 2015)",

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

**PSDNET-201. Soporte para progreso de conversión de documentos**

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

Console.WriteLine("---------- Cargando Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, loadOptions))

{

      Console.WriteLine("---------- Guardando Apple.psd en formato PNG ----------");

      image.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Guardando Apple.psd en formato PSD ----------");

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

**PSDNET-386. Soporte de britResource (Recurso de Capa de Ajuste de Brillo/Contraste)**

{{< highlight java >}}

 /* Este Ejemplo demuestra cómo puede cambiar programáticamente el Recurso de Capa de Brillo/Contraste de la Imagen Psd 

   Este es un API de bajo nivel de Aspose.PSD. Puede utilizar la Capa de Brillo/Contraste a través de su API, que será mucho más fácil, 

   pero editar directamente los recursos de Photoshop le da más control sobre el contenido del archivo PSD.  */

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

                        throw new Exception("El Recurso de Brillo/Contraste se leyó incorrectamente");

                    }

                    // Prueba de edición y guardado

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

**PSDNET-596. Grupo de Capas con Modo de Mezcla no PasaPor No Se Renderiza**

{{< highlight java >}}

 string sourceFilePath = "MaskTestNormalBlendMaskOnGroup.psd";

string outputFilePath = "MaskTestNormalBlendMaskOnGroup.png";

using (var input = (PsdImage)Image.Load(sourceFilePath))

{

    input.Save(outputFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-610. Excepción de NullReference al intentar convertir un archivo Psd específico a imagen**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load("Certificate.psd"))

{

    psdImage.Save("output.png", new PngOptions());

}

{{< /highlight >}}

` `**PSDNET-636. El redimensionamiento de archivos PSD funciona incorrectamente si hay una máscara en la capa de ajuste que tiene límites vacíos**

{{< highlight java >}}

 int escala = 2;

string[] nombres = {

                     "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                     "LevelsLayerWithLayerMaskRgb",

                     "