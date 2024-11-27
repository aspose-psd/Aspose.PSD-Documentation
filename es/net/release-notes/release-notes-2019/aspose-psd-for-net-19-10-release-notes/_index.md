---
title: Aspose.PSD para .NET 19.10 - Notas de la versión
type: docs
weight: 30
url: /es/net/aspose-psd-para-net-19-10-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de Aspose.PSD para .NET 19.10.

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-207|[Soporte de capa de ajuste de balance de color](/psd/es/net/modificar-imagenes/#modificarimagenes-colorbalanceadjustmentlayer)|Funcionalidad|
|PSDNET-145|[Soporte de capa de ajuste de Invertir](/psd/es/net/modificar-imagenes/#modificarimagenes-invertadjustmentlayer)|Funcionalidad|
|PSDNET-139|[Implementar Resampler bicúbico](/psd/es/net/modificar-imagenes/#modificarimagenes-implementarbicubicresampling)|Funcionalidad|
|PSDNET-169|[Agregar soporte de exportación PSD a PDF con Máscara de Recorte](/psd/es/net/convertir-psd-a-otros-formatos/#convertirpsdaotrosformatos-psdatopdfconmascaraderecorte)|Funcionalidad|
|PSDNET-168|[Agregar soporte de exportación PSD a PDF con Capas de Ajuste](/psd/es/net/convertir-psd-a-otros-formatos/#convertirpsdaotrosformatos-psdatopdfconcapasdeajuste)|Funcionalidad|
|PSDNET-179|Problema al obtener efecto de sombra de capa|Mejora|
|PSDNET-203|Cuando se actualiza texto con caracteres / (barra diagonal), el archivo no se puede abrir en Photoshop|Error|
|PSDNET-199|El archivo PSD no se puede guardar cuando la capa de texto contiene solo saltos de línea|Error|
|PSDNET-185|Se extrajo un tamaño de fuente incorrecto|Error|

## **Cambios en la API Pública**
# **APIs Agregadas:**

- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **APIs Eliminadas:**

- Ninguna

## **Ejemplos de uso:**

**PSDNET-207. Soporte de capa de ajuste de balance de color**

{{< highlight java >}}

            var filePath = "ColorBalance.psd";

            var outputPath = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                foreach (var layer in im.Layers)

                {

                    var cbLayer = layer as ColorBalanceAdjustmentLayer;

                    if (cbLayer != null)

                    {

                        cbLayer.ShadowsCyanRedBalance = 30;

                        cbLayer.ShadowsMagentaGreenBalance = -15;

                        cbLayer.ShadowsYellowBlueBalance = 40;

                        cbLayer.MidtonesCyanRedBalance = -90;

                        cbLayer.MidtonesMagentaGreenBalance = -25;

                        cbLayer.MidtonesYellowBlueBalance = 20;

                        cbLayer.HighlightsCyanRedBalance = -30;

                        cbLayer.HighlightsMagentaGreenBalance = 67;

                        cbLayer.HighlightsYellowBlueBalance = -95;

                        cbLayer.PreserveLuminosity = true;

                    }

                }

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-145. Soporte de capa de ajuste de Invertir**

{{< highlight java >}}

            var filePath = "InvertStripes_before.psd";

            var outputPath = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-139. Implementar Resampler bicúbico**

{{< highlight java >}}

             string sourceFile = "sample.psd";

            string destName = "ResamplerCubicConvolutionStripes_after.psd";

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCatmullRomStripes_after.psd";

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerMitchellStripes_after.psd";

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCubicBSplineStripes_after.psd";

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerSinCStripes_after.psd";

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.SinC);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerBellStripes_after.psd";

            // Cargar una imagen existente en una instancia de la clase PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Bell);

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-169. Agregar soporte de exportación PSD a PDF con Máscara de Recorte**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-168. Agregar soporte de exportación PSD a PDF con Capas de Ajuste**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("example.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Cuando se actualiza texto con / (barra diagonal), el archivo no se puede abrir en Photoshop**

{{< highlight java >}}

         var psdImage = (PsdImage)image;

        var layers = psdImage.Layers;

        for (var index = layers.Length - 1; index >= 0; index--)

        {

            var layer = layers[index];

            if (!(layer is TextLayer)) continue;

            var textLayer = (TextLayer)layer;

            textLayer.UpdateText("/");

        }

        var imageOptions = new PsdOptions(psdImage);

        var fileName = Path.GetFileName(filePath);

        var outputFilePath = Path.GetDirectoryName(filePath) + "\\target_" + fileName;

        psdImage.Save(outputFilePath, imageOptions);

{{< /highlight >}}

**PSDNET-199. El archivo PSD no se puede guardar cuando la capa de texto contiene solo saltos de línea**

{{< highlight java >}}

 string filePath = "testLineBreaks2.psd";

string outputPath = "testLineBreaks2_changed.psd";

var newText = "\r";

        using (var image = Image.Load(filePath))

        {

            var psdImage = image as PsdImage;

            if (image == null)

            {

                return;

            }

            var layers = psdImage.Layers;

            for (var index = layers.Length - 1; index >= 0; index--)

            {

                var layer = layers[index] as TextLayer;

                if (layer == null)

                {

                    continue;

                }

                layer.UpdateText(newText);

            }

            var imageOptions = new PsdOptions(psdImage);

            psdImage.Save(outputPath, imageOptions);

        }

{{< /highlight >}}

**PSDNET-185. Se extrajo un tamaño de fuente incorrecto**

{{< highlight java >}}

             // Se extrajo un tamaño de fuente incorrecto

            string filePath = "直播+电商.psd";

            var tolerancia = 0.001;

            using (var image = Image.Load(filePath))

            {

                int indiceCapa = 22;

                // API Antigua (Usando la fuente del primer párrafo)

                PsdImage psdImage = image as PsdImage;

                double[] matriz = ((TextLayer)psdImage.Layers[indiceCapa]).TransformMatrix;

                double tamañoBaseFuente = ((TextLayer)psdImage.Layers[indiceCapa]).Font.Size;

                double tamañoFuente = matriz[0] * tamañoBaseFuente;

                // Comprobando el tamaño base de fuente

                if (Math.Abs(100.0 - tamañoBaseFuente) > tolerancia)

                {

                    throw new Exception("Se leyó un tamaño de fuente incorrecto");

                }

                // Comprobando el tamaño de fuente real

                if (Math.Abs(88.425 - tamañoFuente) > tolerancia)

                {

                    throw new Exception("Se leyó incorrectamente la matriz de transformación");

                }

                // Nueva API (Una capa de texto puede contener cualquier cantidad de tamaños de fuente)

                ITextPortion[] porciones = ((TextLayer)psdImage.Layers[indiceCapa]).TextData.Items;

                ITextStyle estilo = porciones[0].Style;

                double tamañoFuentePorción = matriz[0] * estilo.FontSize;

                // Comprobando el tamaño de fuente base de la porción

                if (Math.Abs(100.0 - estilo.FontSize) > tolerancia)

                {

                    throw new Exception("Se leyó un tamaño de fuente incorrecto");

                }

                // Comprobando el tamaño real de fuente de la porción

                if (Math.Abs(88.425 - tamañoFuentePorción) > tolerancia)

                {

                    throw new Exception("Se leyó incorrectamente la matriz de transformación");

                }

            }

{{< /highlight >}}

**PSDNET-179. Problema al obtener el efecto de sombra de la capa**

{{< highlight java >}}

       // Cuando la propiedad DropShadowEffect.UseGlobalLight es 'true', entonces el objeto DropShadowEffect usa el valor del ángulo desde la propiedad PsdImage.GlobalAngle.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}
