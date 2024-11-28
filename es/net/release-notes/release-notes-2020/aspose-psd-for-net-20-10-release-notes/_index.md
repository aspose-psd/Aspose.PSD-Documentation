---
title: Notas de Lanzamiento de Aspose.PSD para .NET 20.10
type: docs
weight: 30
url: /es/net/aspose-psd-para-net-20-10-notas-de-lanzamiento/
---

{{% alert color="primary" %}} 

Esta página contiene notas de lanzamiento para [Aspose.PSD para .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-565|Excepción al guardar el archivo PSD específico con capas de texto|Error|
|PSDNET-680|Se pierden fuentes después de los viajes de ida y vuelta con Aspose.PSD|Error|
|PSDNET-704|Renderización de la Capa de Objeto Inteligente|Función|
|PSDNET-707|Soporte de las transformaciones no destructivas del Objeto Inteligente|Función|
|PSDNET-711|La Capa de Texto se Desplaza Después de guardar sin cambios|Error|
|PSDNET-720|Aspose.PSD 20.8: excepción de conversión de Psd a Tiff|Error|

## **Cambios en la API pública**
# **APIs Agregadas:**
- Ninguna
# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de Uso:**
**PSDNET-565. Excepción al guardar el archivo PSD específico con capas de texto**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Se pierden fuentes después de los viajes de ida y vuelta con Aspose.PSD**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void SonIguales(int esperado, int actual)
            {
                if (esperado != actual)
                {
                    throw new Exception("Los valores no son iguales.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                SonIguales(1, textLayer.TextData.Items[0].Style.FontIndex);
                SonIguales(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                SonIguales(1, textLayer.TextData.Items[0].Style.FontIndex);
                SonIguales(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                SonIguales(1, textLayer.TextData.Items[0].Style.FontIndex);
                SonIguales(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                SonIguales(1, textLayer.TextData.Items[0].Style.FontIndex);
                SonIguales(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-704. Renderización de la Capa de Objeto Inteligente**
{{< highlight csharp >}}
            // Este ejemplo demuestra cómo reemplazar el contenido de la capa de objeto inteligente de Adobe® Photoshop® y su renderización correcta.
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // Este ejemplo demuestra cómo actualizar la caché de imágenes de las capas de objeto inteligente de Adobe® Photoshop® y su renderización correcta.
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-707. Soporte de las transformaciones no destructivas del Objeto Inteligente**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Estos ejemplos demuestran transformaciones no destructivas del archivo PSD con SmartObjectLayer.
            // Podemos escalar, rotar, sesgar, distorsionar, transformar la perspectiva o deformar una capa sin
            // perder datos de imagen originales o calidad porque las transformaciones no afectan los datos originales.

            // Este ejemplo demuestra cómo cambiar el tamaño de la imagen de Adobe® Photoshop® con capas de objeto inteligente:
            EjemploDeSoporteParaCambioDeTamañoDeImagenDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            EjemploDeSoporteParaCambioDeTamañoDeImagenDeObjetoInteligente("picture-frame-4-linked3");
            EjemploDeSoporteParaCambioDeTamañoDeImagenDeObjetoInteligente("gorilla");

            // Este ejemplo demuestra cómo cambiar el tamaño del archivo PSD con capas de objeto inteligente.
            void EjemploDeSoporteParaCambioDeTamañoDeImagenDeObjetoInteligente(string nombreArchivo)
            {
                const int escala = 4;
                string filePath = dataDir + nombreArchivo + ".psd";
                string outputPath = outputDir + "Resize_" + nombreArchivo + ".psd";
                string outputPngPath = outputDir + "Resize_" + nombreArchivo + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int nuevoAncho = image.Width * escala;
                    int nuevoAlto = image.Height * escala;
                    image.Resize(nuevoAncho, nuevoAlto);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este ejemplo demuestra cómo cambiar el tamaño de la capa de objeto inteligente.
            EjemploDeSoporteParaCambioDeTamañoDeCapaDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            EjemploDeSoporteParaCambioDeTamañoDeCapaDeObjetoInteligente("gorilla");

            // Este ejemplo demuestra cómo cambiar el tamaño de una capa de objeto inteligente en el archivo PSD.
            void EjemploDeSoporteParaCambioDeTamañoDeCapaDeObjetoInteligente(string nombreArchivo)
            {
                const double escala = 3.5;
                string filePath = dataDir + nombreArchivo + ".psd";
                string outputPath = outputDir + "ResizeLast_" + nombreArchivo + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + nombreArchivo + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var capaObjetoInteligente = image.Layers[image.Layers.Length - 1];
                    int nuevoAncho = (int)(capaObjetoInteligente.Width * escala);
                    int nuevoAlto = (int)(capaObjetoInteligente.Height * escala);
                    capaObjetoInteligente.Resize(nuevoAncho, nuevoAlto);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este ejemplo demuestra cómo recortar la capa de objeto inteligente de Adobe® Photoshop®.
            EjemploDeSoporteParaRecorteDeCapaDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            EjemploDeSoporteParaRecorteDeCapaDeObjetoInteligente("gorilla");

            // Este ejemplo demuestra cómo recortar una capa de objeto inteligente en el archivo PSD.
            void EjemploDeSoporteParaRecorteDeCapaDeObjetoInteligente(string nombreArchivo)
            {
                string filePath = dataDir + nombreArchivo + ".psd";
                string outputPath = outputDir + "CropLast_" + nombreArchivo + ".psd";
                string outputPngPath = outputDir + "CropLast_" + nombreArchivo + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var capaObjetoInteligente = image.Layers[image.Layers.Length - 1];
                    capaObjetoInteligente.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este ejemplo demuestra cómo recortar la capa de objeto inteligente de Adobe® Photoshop®:
            EjemploDeSoporteParaRecorteDeImagenDeCapaDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            EjemploDeSoporteParaRecorteDeImagenDeCapaDeObjetoInteligente("gorilla");

            // Este ejemplo demuestra cómo recortar el archivo PSD con capas de objeto inteligente.
            void EjemploDeSoporteParaRecorteDeImagenDeCapaDeObjetoInteligente(string nombreArchivo)
            {
                string filePath = dataDir + nombreArchivo + ".psd";
                string outputPath = outputDir + "Crop_" + nombreArchivo + ".psd";
                string outputPngPath = outputDir + "Crop_" + nombreArchivo + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Crop(25, 10, 30, 5);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este ejemplo demuestra cómo rotar y voltear la imagen de Adobe® Photoshop® con capas de objeto inteligente:
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("gorilla", RotateFlipType.Rotate90FlipNone);
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Este ejemplo demuestra cómo rotar y voltear el archivo PSD con capas de objeto inteligente.
            void EjemploDeSoporteParaRotacionYVolteoDeImagenDeCapaObjetoInteligente(string nombreArchivo, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + nombreArchivo + ".psd";
                string outputPath = outputDir + rotateFlipType + "_" + nombreArchivo + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "_" + nombreArchivo + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este ejemplo demuestra cómo rotar y voltear la capa de objeto inteligente de Adobe® Photoshop®.
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("gorilla", RotateFlipType.Rotate90FlipNone);
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Este ejemplo demuestra cómo rotar y voltear una capa de objeto inteligente en el archivo PSD.
            void EjemploDeSoporteParaRotacionYVolteoDeCapaDeObjetoInteligente(string nombreArchivo, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + nombreArchivo + ".psd";
                string outputPath = outputDir + rotateFlipType + "Last_" + nombreArchivo + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "Last_" + nombreArchivo + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var capaObjetoInteligente = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    capaObjetoInteligente.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este ejemplo demuestra cómo rotar la capa de objeto inteligente de Adobe® Photoshop® por cualquier ángulo:
            const string FormatoAngulo = "+#;-#;+0";
            EjemploDeSoporteParaRotacionDeCapaDeObjetoInteligente("gorilla", 45, false);
            EjemploDeSoporteParaRotacionDeCapaDeObjetoInteligente("gorilla", 45, true);
            EjemploDeSoporteParaRotacionDeCapaDeObjetoInteligente("r3-embedded-transform2", -30, true);
            EjemploDeSoporteParaRotacionDeCapaDeObjetoInteligente("r3-embedded-transform2", -30, false);
            EjemploDeSoporteParaRotacionDeCapaDeObjetoInteligente("new_panama-papers-8-trans4-linked", 190, false);
            EjemploDeSoporteParaRotacionDeCapaDeObjetoInteligente("new_panama-papers-8-trans4-linked", 190, true);

            // Este ejemplo demuestra cómo rotar una capa de objeto inteligente en el archivo PSD por cualquier ángulo.
            void EjemploDeSoporteParaRotacionDeCapaDeObjetoInteligente(string nombreArchivo, float angulo, bool redimensionarProporcionalmente)
            {
                string prefijo = "RotateLast" +  angulo.ToString(FormatoAngulo) + (redimensionarProporcionalmente ? "ResizeProportionally" : "") + "_";
                string filePath = dataDir + nombreArchivo + ".psd";
                string outputPath = outputDir + prefijo + nombreArchivo + ".psd";
