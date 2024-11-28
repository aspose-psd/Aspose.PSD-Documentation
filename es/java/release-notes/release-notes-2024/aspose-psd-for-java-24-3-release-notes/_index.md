---
title: Notas de la versión de Aspose.PSD para Java 24.3
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-24-3-notas-de-lanzamiento/
---

{{% alert color="primary" %}} Esta página contiene notas de lanzamiento para [Aspose.PSD para Java 24.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.3/) {{% /alert %}}

| **Clave**   | **Resumen**                                                              | **Categoría** |
|:-----------|:-------------------------------------------------------------------------|:-------------|
| PSDJAVA-601 | [Formato AI] Reducir el tiempo de carga de imágenes AI multipágina grandes.| Mejora       |
| PSDJAVA-604 | Después de convertir el archivo PSD de 8 bits a 16 bits se volvió ilegible.| Error        |
| PSDJAVA-605 | Después de convertir el archivo PSD de 8 bits a 32 bits se volvió ilegible.| Error        |
| PSDJAVA-606 | [Formato AI] Corregir la representación de la Curva Corta en el archivo AI.| Error        |

## **Cambios en la API Pública**
# **APIs Agregadas:**

- T:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.getFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskEnabled 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskExtendWithWhite 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskLinked 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isValidAtPosition 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.setFilters(com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter[])
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.updateResourceValues 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.apply(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.applyToMask(com.aspose.psd.fileformats.psd.layers.Layer)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.deepClone 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getBlendMode 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getOpacity 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getSourceDescriptor 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.isEnabled 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getAmountNoise 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getDistribution 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setAmountNoise(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setDistribution(int)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setMonochromatic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.isMonochromatic 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer.render(com.aspose.psd.PixelsData)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.FilterType 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getName 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getRadius 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.setRadius(double)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Gaussian 
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Uniform 
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getFilterId 
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getName

# **APIs Eliminadas:**

- Ninguna

## **Ejemplos de Uso:**

** PSDJAVA-604. Después de convertir el archivo PSD de 8 bits a 16 bits se volvió ilegible**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/test_smart_layer.psd";
        String archivoSalida = "src/main/resources/export.psd";

        try (PsdImage imagenPsd8 = (PsdImage) Image.load(archivoFuente)) {
            PsdOptions opcionesPsd16 = new PsdOptions();
            opcionesPsd16.setChannelBitsCount((short) 16);

            imagenPsd8.save(archivoSalida, opcionesPsd16);
        }

        try (PsdImage imagenPsd16 = (PsdImage) Image.load(archivoSalida)) {
            if (imagenPsd16.getGlobalLayerResources()[0] instanceof Lr16Resource) {
                // está bien
            } else {
                throw new Exception("Recurso global incorrecto, el primer recurso debería ser Lr16Resource");
            }
        }

{{< /highlight >}}

** PSDJAVA-605. Después de convertir el archivo PSD de 8 bits a 32 bits se volvió ilegible**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/test_smart_layer.psd";
        String archivoSalida = "src/main/resources/export.psd";

        try (PsdImage imagenPsd8 = (PsdImage) Image.load(archivoFuente)) {
            PsdOptions opcionesPsd32 = new PsdOptions();
            opcionesPsd32.setChannelBitsCount((short) 32);

            imagenPsd8.save(archivoSalida, opcionesPsd32);
        }

        try (PsdImage imagenPsd8 = (PsdImage) Image.load(archivoSalida)) {
            if (imagenPsd8.getGlobalLayerResources()[0] instanceof Lr32Resource) {
                // está bien
            } else {
                throw new Exception("Recurso global incorrecto, el primer recurso debería ser Lr16Resource");
            }
        }

{{< /highlight >}}

** PSDJAVA-606. [Formato AI] Corregir la representación de la Curva Corta en el archivo AI**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/shortCurve.ai";
        String rutaArchivoSalida = "src/main/resources/shortCurve.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
            imagen.save(rutaArchivoSalida, new PngOptions());
        }

{{< /highlight >}}
