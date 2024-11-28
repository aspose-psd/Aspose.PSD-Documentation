---
title: Notas de la versión Aspose.PSD para .NET 21.4
type: docs
weight: 90
url: /es/net/aspose-psd-para-net-21-4-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para .NET 21.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-259|Renderizado del Efecto de Capa de Superposición de Patrón|Característica|
|PSDNET-861|Agregar propiedades de recursos Vogk desconocidos para admitir el redimensionamiento de capas de forma con trayectorias vectoriales en imagen PSD|Característica|
|PSDNET-90|PSD no Convertido adecuadamente a PDF|Error|
|PSDNET-830|Excepción al guardar el archivo PSD específico con capas de texto|Error| (Corregido anteriormente)

## **Cambios en la API Pública**
# **APIs Agregadas:**
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginBoxCorners
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.Transform
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginBoxCornersPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsTransformPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Tx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Ty

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de Uso:**

**PSDNET-90. PSD no Convertido adecuadamente a PDF**

{{< highlight csharp >}}
            string srcFile = "psd_magical.psd";
            string outputJpg = "output.jpg";
            string outputPdf = "output.pdf";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                JpegOptions jpgOptions = new JpegOptions();
                PdfOptions pdfOptions = new PdfOptions();

                psdImage.Save(outputJpg, jpgOptions);
                psdImage.Save(outputPdf, pdfOptions);
            }
{{< /highlight >}}

**PSDNET-259. Renderizado del Efecto de Capa de Superposición de Patrón**

{{< highlight csharp >}}
            string sourceFile = "imageWithPattern.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-861. Agregar propiedades de recursos Vogk desconocidos para admitir el redimensionamiento de capas de forma con trayectorias vectoriales en imagen PSD**

{{< highlight csharp >}}
            // Este ejemplo muestra cómo obtener y establecer las nuevas propiedades Transform y OriginBoxCorners
            // de ShapeOriginSettings en el recurso Vogk de FillLayer en el archivo PSD
            string sourceFileName = Path.Combine("PSDNET861_1", "vectorShape_25_50.psd");
            string outputPath = Path.Combine("PSDNET861_1", "result.psd");

            VectorShapeOriginSettings originalSetting;
            const int layerIndex = 0;

            // Cargar la imagen original
            using (PsdImage image = (PsdImage)Image.Load(sourceFileName)) 
            {
                AssertIsTrue(layerIndex < image.Layers.Length);
                var layer = image.Layers[layerIndex];
                AssertIsTrue(layer is FillLayer);
                var resource = GetVogkResource((FillLayer)layer);
                AssertAreEqual(1, resource.ShapeOriginSettings.Length);

                // Afirmar después de leer
                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(0, setting.OriginIndex);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(5, setting.OriginType);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(3, 7, 10, 22), setting.OriginShapeBox.Bounds);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(300d, setting.OriginResolution);

                // Afirmar nuevas propiedades
                AssertAreEqual(true, setting.IsTransformPresent);
                AssertAreEqual(0d, setting.Transform.Tx);
                AssertAreEqual(0d, setting.Transform.Ty);
                AssertAreEqual(0.050000000000000003d, setting.Transform.Xx);
                AssertAreEqual(0d, setting.Transform.Yx);
                AssertAreEqual(0d, setting.Transform.Xy);
                AssertAreEqual(0.1d, setting.Transform.Yy);
                AssertAreEqual(true, setting.IsOriginBoxCornersPresent);
                AssertAreEqual(2.9000000000000004d, setting.OriginBoxCorners[0]);
                AssertAreEqual(7.3000000000000007d, setting.OriginBoxCorners[1]);
                AssertAreEqual(10.450000000000001d, setting.OriginBoxCorners[2]);
                AssertAreEqual(7.3000000000000007d, setting.OriginBoxCorners[3]);
                AssertAreEqual(10.450000000000001d, setting.OriginBoxCorners[4]);
                AssertAreEqual(22.400000000000002d, setting.OriginBoxCorners[5]);
                AssertAreEqual(2.9000000000000004d, setting.OriginBoxCorners[6]);
                AssertAreEqual(22.400000000000002d, setting.OriginBoxCorners[7]);

                // Establecer nuevas propiedades
                originalSetting = resource.ShapeOriginSettings[0];
                originalSetting.Transform.Tx = 0.2d;
                originalSetting.Transform.Ty = 0.3d;
                originalSetting.Transform.Xx = 0.4d;
                originalSetting.Transform.Xy = 0.5d;
                originalSetting.Transform.Yx = 0.6d;
                originalSetting.Transform.Yy = 0.7d;
                originalSetting.OriginBoxCorners = new double[8] { 9, 8, 7, 6, 5, 4, 3, 2 };

                // Guardar esta imagen PSD con propiedades modificadas.
                image.Save(outputPath, new PsdOptions(image));
            }

            // Cargar la imagen PSD guardada con propiedades modificadas.
            using (PsdImage image = (PsdImage)Image.Load(outputPath))
            {
                var layer = image.Layers[layerIndex];
                AssertIsTrue(layer is FillLayer);
                var resource = GetVogkResource((FillLayer)layer);
                AssertAreEqual(1, resource.ShapeOriginSettings.Length);

                // Afirmar que las propiedades se guardan y cargan correctamente
                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                AssertAreEqual(true, setting.IsTransformPresent);
                AssertAreEqual(0.2d, setting.Transform.Tx);
                AssertAreEqual(0.3d, setting.Transform.Ty);
                AssertAreEqual(0.4d, setting.Transform.Xx);
                AssertAreEqual(0.5d, setting.Transform.Xy);
                AssertAreEqual(0.6d, setting.Transform.Yx);
                AssertAreEqual(0.7d, setting.Transform.Yy);
                AssertAreEqual(true, setting.IsOriginBoxCornersPresent);
                AssertAreEqual(originalSetting.OriginBoxCorners[0], setting.OriginBoxCorners[0]);
                AssertAreEqual(originalSetting.OriginBoxCorners[1], setting.OriginBoxCorners[1]);
                AssertAreEqual(originalSetting.OriginBoxCorners[2], setting.OriginBoxCorners[2]);
                AssertAreEqual(originalSetting.OriginBoxCorners[3], setting.OriginBoxCorners[3]);
                AssertAreEqual(originalSetting.OriginBoxCorners[4], setting.OriginBoxCorners[4]);
                AssertAreEqual(originalSetting.OriginBoxCorners[5], setting.OriginBoxCorners[5]);
                AssertAreEqual(originalSetting.OriginBoxCorners[6], setting.OriginBoxCorners[6]);
                AssertAreEqual(originalSetting.OriginBoxCorners[7], setting.OriginBoxCorners[7]);
            }

            VogkResource GetVogkResource(FillLayer layer)
            {
                if (layer == null)
                {
                    throw new PsdImageArgumentException("El parámetro layer no debería ser nulo.");
                }

                VogkResource resource = null;
                var resources = layer.Resources;
                for (int i = 0; i < resources.Length; i++)
                {
                    if (resources[i] is VogkResource)
                    {
                        resource = (VogkResource)resources[i];
                        break;
                    }
                }

                if (resource == null)
                {
                    throw new PsdImageException("VogkResource no encontrado.");
                }

                return resource;
            }

            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("Se esperaba verdadero"));
                }
            }

            void AssertAreEqual(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(string.Format("El valor actual {0} no es igual al esperado {1}.", actual, expected));
                }
            }
{{< /highlight >}}