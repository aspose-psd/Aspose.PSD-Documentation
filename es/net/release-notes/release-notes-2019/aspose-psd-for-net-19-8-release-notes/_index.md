---
title: Aspose.PSD para .NET 19.8 - Notas de la Versión
type: docs
weight: 50
url: /es/net/aspose-psd-para-net-19-8-notas-de-la-version/
---

{{% alert color="primary" %}} 

Esta página contiene las notas de la versión de Aspose.PSD para .NET 19.8

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-184|Cargar archivos de imagen JPEG, PNG y otros en PsdImage desde la secuencia|Característica|
|PSDNET-134|Implementar renderizado de Capa de Relleno: Degradado|Característica|
|PSDNET-166|Guardar PSD en PDF no proporciona texto seleccionable|Característica|
|PSDNET-158|Soporte para guardar PSB como PDF|Característica|
|PSDNET-189|Alta uso de memoria al cargar PSD con Modo Solo Lectura|Mejora|
|PSDNET-171|Después de la creación de una nueva Capa de Texto, el archivo PSD se vuelve ilegible para PS|Error|
|PSDNET-156|Excepción al cargar PSD|Error|

## **Cambios en la API Pública**
# **APIs Añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **APIs Eliminadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Ejemplos de Uso:**
**PSDNET-184. Cargar archivos de imagen JPEG, PNG y otros en PsdImage desde la secuencia**

{{< highlight java >}}

    // cargar archivos de imagen JPEG, PNG y otros en PsdImage desde la secuencia

    string outputFilePath = "ResultadoPsd.psd";

    var filesList = new string[]

    {

        "EjemploPsd.psd",

        "EjemploBmp.bmp",

        "EjemploGif.gif",

        "EjemploJpeg2000.jpf",

        "EjemploJpeg.jpg",

        "EjemploPng.png",

        "EjemploTiff.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. Implementar renderizado de Capa de Relleno: Degradado**

{{< highlight java >}}

             // Implementar renderizado de Capa de Relleno: Degradado

            string fileName = "CapaRellenoDegradado.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. Guardar PSD en PDF no proporciona texto seleccionable**

{{< highlight java >}}

  // Guardar PSD en PDF no proporciona texto seleccionable

    string sourceFileName = "texto.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "texto.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Después de la creación de una nueva Capa de Texto, el archivo PSD se vuelve ilegible para PS**

{{< highlight java >}}

 // Después de la creación de una nueva Capa de Texto en Servidor de Compilación, el Archivo PSD se volvió ilegible para PS

    string sourceFileName = "UnaCapa.psd";

    string outFileName = "UnaCapaConTextoAgregado.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Algo de texto", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. Excepción al cargar PSD**

{{< highlight java >}}

 using (var image = Image.Load("CopiaAislada.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Alta uso de memoria al cargar PSD con Modo Solo Lectura**

{{< highlight java >}}

 // Alto uso de memoria de Aspose.PSD al cargar PSD con Modo Solo Lectura

            string sourceFileName = "EfectoTexto3DBlanco.psd";

            string outFileName = "Exportado.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // El uso de memoria debe ser inferior a 100 MB para estos ejemplos

            if (memoryUsed > 100)

            {

                throw new Exception("El uso de memoria es demasiado grande");

            }

{{< /highlight >}}

**PSDNET-158. Soporte para guardar PSB como PDF**

{{< highlight java >}}

 // Soporte para guardar PSB como PDF

    string sourceFileName = "muestra.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "muestra.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
