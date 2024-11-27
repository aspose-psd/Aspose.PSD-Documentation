---
title: Aspose.PSD para .NET 19.6 - Notas de la versión
type: docs
weight: 70
url: /es/net/aspose-psd-para-net-19-6-notas-de-version/
---

{{% alert color="primary" %}} 

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-127|Capacidad para convertir archivos PSD a PSB y viceversa|Funcionalidad|
|PSDNET-154|Portar fuentes de Aspose.Imaging 19.5 a Aspose.PSD|Mejora|
|PSDNET-155|Limpieza de API pública relacionada con Aspose.PSD|Mejora|
|PSDNET-159|Eliminar propiedad IsLicensed|Mejora|
|PSDNET-102|La conversión de PSB a JPG se cuelga|Error|
|PSDNET-150|La posición de la capa de texto recién agregada se desplaza al editar en Photoshop|Error|

## **Cambios en la API Pública**
# **APIs Agregadas:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F:Aspose.PSD.FileFormat.Cdr
- F:Aspose.PSD.FileFormat.Cmx
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P:Aspose.PSD.Image.BufferSizeHint
- P:Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M:Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P:Aspose.PSD.LoadOptions.BufferSizeHint
- T:Aspose.PSD.MemoryManagement.Configuration
- P:Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T:Aspose.PSD.ResolutionUnit
- F:Aspose.PSD.ResolutionUnit.None
- F:Aspose.PSD.ResolutionUnit.Inch
- F:Aspose.PSD.ResolutionUnit.Cm
# **APIs Eliminadas:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
- ...

## **Ejemplos de uso:**
**PSDNET-127. Capacidad para convertir archivos PSD a PSB y viceversa**

{{< highlight java >}}

 // Capacidad para convertir archivos PSD a PSB y viceversa

            string sourceFilePathPsb = "2layers.psb";

            string outputFilePathPsd = "ConvertFromPsb.psd";

            using (Image img = Image.Load(sourceFilePathPsb))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psd };

                img.Save(outputFilePathPsd, options);

            }

            string sourceFilePathPsd = "2layers.psd";

            string outputFilePathPsb = "ConvertFromPsd.psb";

            using (Image img = Image.Load(sourceFilePathPsd))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psb };

                img.Save(outputFilePathPsb, options);

            }

{{< /highlight >}}

**PSDNET-102. Conversión de PSB a JPG se cuelga**

{{< highlight java >}}

  // Conversión de PSB a JPG se cuelga          

            string[] sourceFileNames = new string[] { 

                // Archivos de prueba con capas

                "Pequeño",

                "Simple",

                // Archivos de prueba sin capas

                "psb",

                "psb3"

            };

            var options = new PsdLoadOptions();

            foreach (var fileName in sourceFileNames)

            {

                var sourceFileName = fileName + ".psb";

                using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

                {

                    // Todos los archivos jpeg y psd deben ser legibles

                    image.Save(fileName + "_salida.jpg", new JpegOptions() { Quality = 95 });

                    image.Save(fileName + "_salida.psb");

                }

            }             

{{< /highlight >}}

**PSDNET-150: La posición de la capa de texto recién agregada se desplaza al editar en Photoshop**

{{< highlight java >}}

             // La posición de la capa de texto recién agregada se desplaza al editar en Photoshop

    string sourceFileName = "UnaCapa.psd";

    string exportPath = "UnaCapa_Edita.psd";

    int leftPos = 99;

    int topPos = 47;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        im.AddTextLayer("Algo de texto", new Rectangle(leftPos, topPos, 99, 47));

        TextLayer textLayer = (TextLayer)im.Layers[1];

        if (textLayer.Left != leftPos || textLayer.Top != topPos) 

        {

            throw new Exception("Se creó incorrectamente la capa de texto");

        }

        // No podemos probar la Matriz de Transformación con una API pública,

        // pero al empezar a editar la capa de texto en PSD deberíamos obtener los mismos límites que creamos

        im.Save(exportPath);

    }

{{< /highlight >}}...

{{< /highlight >}}

**PSDNET-154: Portar fuentes de Aspose.Imaging 19.5 a Aspose.PSD**

{{< highlight java >}}

    // Portar fuentes de Aspose.Imaging 19.5 a Aspose.PSD

    using (PsdImage psdImage = (PsdImage)Image.Load("input.psd"))

    {

        FileFormats.Psd.Examples.ExcreptingImages.ExcreptingImage.SaveWithWatermark(psdImage);

    }

{{< /highlight >}}

**PSDNET-155: Limpieza de API pública relacionada con Aspose.PSD**

{{< highlight java >}}

    // Limpieza de la API pública relacionada con Aspose.PSD

    var psdImage = (PsdImage)Image.Load("sample.psd");

    psdImage?.Dispose();

{{< /highlight >}}

**PSDNET-159: Eliminar propiedad IsLicensed**

{{< highlight java >}}

     // Eliminar propiedad IsLicensed

        var psdRasterImage = (PsdImage)Image.Load("sample.psd");

        if (psdRasterImage != null)

        {

            psdRasterImage.IsLicensed = false;

            psdRasterImage.Save("output.psd");

        }

{{< /highlight >}}


¡Gracias por usar Aspose.PSD!