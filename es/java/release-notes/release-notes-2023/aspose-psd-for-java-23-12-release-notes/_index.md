---
title: Notas de la versión de Aspose.PSD para Java 23.12
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-23-12-notas-de-version/
---

{{% alert color="primary" %}} Esta página contiene las notas de la versión de [Aspose.PSD para Java 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                                      | **Categoría** |
|:-----------|:-------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-565 | [Formato AI] Agregar soporte para renderización de imagen de trama en la nueva versión de AI.    | Función      |
| PSDJAVA-566 | Manejar tipo de degradado de ruido en GdflResrource.                                               | Función      |
| PSDJAVA-567 | Error "Referencia de objeto no establecida como instancia de un objeto." al guardar capa de texto después de la actualización. | Error   |
| PSDJAVA-568 | Arreglar la carga manual de fuentes en MacOS utilizando System.Drawing.Common y Aspose.Drawing.  | Error        |
| PSDJAVA-569 | AllowWarpRepaint en las PsdLoadOptions conduce a la excepción.                                    | Error        |
| PSDJAVA-570 | [Formato AI] Implementar procesamiento de flujos de referencias cruzadas.                         | Mejora       |
| PSDJAVA-571 | El control de licencia para VectorPathDataResource funciona incorrectamente.                      | Mejora       |
| PSDJAVA-574 | Abrir cualquier archivo de imagen como un objeto inteligente incrustado en la imagen PSD.         | Mejora       |

## **Cambios en la API pública**
# **APIs añadidas:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setColorModel(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setGradientMode(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setUseVectorColor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.#ctor(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.#ctor
- ...

# **APIs eliminadas:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
  M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle 
- ...
  
## **Ejemplos de uso:** 

** PSDJAVA-565. [Formato AI] Agregar soporte para renderización de imagen de trama en la nueva versión de AI**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/raster.ai";
    String archivoSalida = "src/main/resources/raster_output.png";

    try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
        imagen.save(archivoSalida, new PngOptions());
    }

{{< /highlight >}}

** PSDJAVA-566. Manejar tipo de degradado de ruido en GdflResrource**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/Gradient-Fill.psd";
    String archivoDestino = "src/main/resources/Gradient-Fill-out.psd";

    try (PsdImage imagen = (PsdImage) Image.load(archivoFuente, new PsdLoadOptions())) {
        Layer capa = imagen.getLayers()[1];

        for (LayerResource recurso : capa.getResources()) {
            GdFlResource recursoGdfl = (GdFlResource) recurso;

            if (recursoGdfl != null) {
                recursoGdfl.setScale(90);
                recursoGdfl.setAngle(30);
                recursoGdfl.setDither(false);
                recursoGdfl.setAlignWithLayer(true);
                recursoGdfl.setReverse(false);

                break;
            }
        }
        imagen.save(archivoDestino, new PsdOptions());
    }

{{< /highlight >}}

...