---
title: Notas de la versión de Aspose.PSD para Python via .NET 24.1
type: docs
weight: 10
url: /es/net/aspose-psd-para-python-via-net-24-1-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión para [Aspose.PSD para Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**     | **Resumen**                                                                                                | **Categoría** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [AI Format] Agregar manejo básico para imágenes AI de múltiples páginas                                      |   Característica   |
|  PSDPYTHON-22 | El efecto de texto curvado no se aplica al texto                                                            |     Error     |
|  PSDPYTHON-23 | Renderizado incorrecto de máscara en el archivo específico                                                |     Error     |
|  PSDPYTHON-24 | NullReferenceException en Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor            |     Error     |
|  PSDPYTHON-25 | [AI Format] Corregir el uso de memoria en AiExporterUtils                                                  |     Error     |



## **Cambios en la API pública**
# **APIs agregadas:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDPYTHON-19. [AI Format] Agregar manejo básico para imágenes AI de múltiples páginas**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Cargar la imagen AI.
        with Image.load(sourceFile) as img:
           image = cast(AiImage, img)
           # De forma predeterminada, el ActivePageIndex es 0.
           # Por lo tanto, si guarda la imagen AI sin cambiar esta propiedad, se renderizará y guardará la primera página.
           image.save(firstPageOutputPng, PngOptions())

           # Cambiar el índice de página activo a la segunda página.
           image.active_page_index = 1

           # Guardar la segunda página de la imagen AI como una imagen PNG.
           image.save(secondPageOutputPng, PngOptions())

           # Cambiar el índice de página activo a la tercera página.
           image.active_page_index = 2

           # Guardar la tercera página de la imagen AI como una imagen PNG.
           image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. El efecto de texto curvado no se aplica al texto**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. Renderizado incorrecto de máscara en el archivo específico**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. NullReferenceException en Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fuentes")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI Format] Corregir el uso de memoria en AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # El uso de memoria en C# es de 220, pero para Python no tenemos acceso directo a las actividades de recolección de basura (GC).
        LímiteDeMemoria = 1500
        proceso = psutil.Proceso()
        memoriaInicial = proceso.memory_info().rss
        pngOpt = PngOptions()
        # Cargar la imagen AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Guardar la primera página de la imagen AI como una imagen PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Cambiar el índice de la página activa a la segunda página.
            image.active_page_index = 1

            # Guardar la segunda página de la imagen AI como una imagen PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Cambiar el índice de la página activa a la tercera página.
            image.active_page_index = 2

            # Guardar la tercera página de la imagen AI como una imagen PNG.
            image.save(thirdPageOutputPng, pngOpt)

        memoriaFinal = proceso.memory_info().rss

        memoriaUtilizada = (memoriaFinal - memoriaInicial) / 1024 / 1024

        if memoriaUtilizada > LímiteDeMemoria:
            raise Exception("El uso de memoria es demasiado grande. {} en lugar de {:.1f}".format(memoriaUtilizada, LímiteDeMemoria))
{{< /highlight >}}
