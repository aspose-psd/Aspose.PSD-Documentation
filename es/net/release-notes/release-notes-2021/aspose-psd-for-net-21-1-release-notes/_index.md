---
title: Notas de la versión de Aspose.PSD para .NET 21.1
type: docs
weight: 120
url: /es/net/aspose-psd-para-net-21-1-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión para [Aspose.PSD para .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Excepción al intentar convertir un archivo Psd particular a png|Error|
|PSDNET-792|Excepción al guardar PSD con objeto inteligente a PNG|Error|

## **Cambios en la API Pública**
# **APIs Agregadas:**
- Ninguna

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de uso:**
**PSDNET-766. Aspose.PSD 20.10: Excepción al intentar convertir un archivo Psd particular a png**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Excepción al guardar PSD con objeto inteligente a PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Buscar Objeto inteligente
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Estamos cargando la capa de Objeto Inteligente desde un flujo de memoria,
                        // Pero podemos usar smart.ExportContents(somePath) para exportar el objeto inteligente a un archivo.
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Buscar Capa de Texto
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Podemos usar el método UpdateText, pero de esta manera nos proporciona la capacidad de editar el texto por partes
                                        // Crear capas de texto de varias líneas y otras características de estilo de texto y párrafo
                                        // Tenga cuidado. Si el contenido del Objeto Inteligente no es PSD, no puede usar este método de edición de texto.
                                        // En tal caso, debe usar la API Gráfica: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Mejor";

                                        // Debe cambiar el tamaño del texto si desea que la imagen se vea bien.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Es mejor usar ReplaceContents. Se volverá a renderizar automáticamente el Objeto Inteligente.
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // De esta forma estamos guardando el archivo PSD modificado.
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
