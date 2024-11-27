---
title: Notas de la versión de Aspose.PSD para Python via .NET 24.7
type: docs
weight: 10
url: /es/python-net/aspose-psd-para-python-via-net-24-7-notas-de-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**      | **Resumen**                                                                                                       | **Categoría** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Excepción "Fallo al cargar la imagen." al abrir el documento AI                              | Error      |
| PSDPYTHON-87 | Texto renderizado incorrectamente en archivos PDF de salida                                       | Error      |
| PSDPYTHON-88 | Corregir ImageSaveException: Error de exportación de la imagen para el archivo determinado en Linux                        | Error      |
| PSDPYTHON-89 | Corregir carga de fuentes al usar Aspose.Drawing                                                      | Error      |
| PSDPYTHON-90 | 'La operación aritmética produjo un desbordamiento' al crear una capa de objeto inteligente usando una JPEG grande | Error      |
| PSDPYTHON-91 | El archivo AI no se puede convertir en un archivo JPG                                                   | Error      |

## **Cambios en la API pública**
# **APIs agregadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDPYTHON-86. Excepción "Fallo al cargar la imagen." al abrir el documento AI**
{{< highlight python >}}
        fuenteArchivo = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        archivoSalida = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(fuenteArchivo) as imagen:
            imagen.save(archivoSalida, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Texto renderizado incorrectamente en archivos PDF de salida**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as imagenPsd:
            opcionesGuardado = PdfOptions()
            opcionesGuardado.pdf_core_options = PdfCoreOptions()

            imagenPsd.save(output, opcionesGuardado)
{{< /highlight >}}


**PSDPYTHON-88. Corregir ImageSaveException: Error de exportación de la imagen para el archivo determinado en Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as imagenPsd:
            imagenPsd.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Corregir carga de fuentes al usar Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Antes de la actualización. Cantidad de fuentes instaladas: " + str(len(installedFonts.families)))
            print("- Actualizar la caché de fuentes intentando obtener el nombre de fuente de Adobe para 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Después de la actualización. Cantidad de fuentes instaladas: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'La operación aritmética produjo un desbordamiento' al crear una capa de objeto inteligente usando una JPEG grande**
{{< highlight python >}}
        # Se realizó la corrección, pero hay otro problema en Aspose.PSD para Python que restringe esta prueba
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as imagen:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Capa de prueba"
                #imagen.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. El archivo AI no se puede convertir en un archivo JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as imagen:
            imagen.save(outputFile, PngOptions())
{{< /highlight >}}
