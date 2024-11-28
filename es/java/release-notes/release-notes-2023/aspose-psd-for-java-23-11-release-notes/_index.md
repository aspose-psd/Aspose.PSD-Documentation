---
title: Notas de lanzamiento de Aspose.PSD para Java 23.11
type: docs
weight: 40
url: /es/java/aspose-psd-for-java-23-11-release-notes/
---

{{% alert color="primary" %}} Esta página contiene notas de lanzamiento para [Aspose.PSD para Java 23.11](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.11/) {{% /alert %}}

| **Clave**        | **Resumen**                                                                                                | **Categoría** |
|:---------------|:-----------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-551    | Soporte de LMskResource                                                                                    |    Función   |
| PSDJAVA-552    | [AI Format] Agrega la capacidad de renderizar archivos AI basados en PDF con Aspose.PSD                    |    Función   |
| PSDJAVA-553    | [AI Format] Agrega soporte para el operador PostScript "cm"                                                  |    Función   |
| PSDJAVA-554    | Agrega nuevos tipos de deformación: Onda, concha arriba, concha abajo                                       |    Función   |
| PSDJAVA-555    | Agrega soporte de deformación vertical                                                                      |    Función   |
| PSDJAVA-556    | System.ArgumentNullException: 'El valor no puede ser nulo. (Parámetro 'clave')' al llamar a TextLayer.GetFonts()  |      Error     |

## **Cambios en la API pública**
# **APIs agregadas:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent1
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent2
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent3
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent4
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorSpace
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getFlag
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getOpacity
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent1(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent2(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent3(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent4(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorSpace(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setOpacity(short)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.TypeToolKey
- T:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.CMYK
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.GrayScale
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.HSB
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.Lab
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB

# **APIs eliminadas:**

- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

## **Ejemplos de uso:**

** PSDJAVA-551. Soporte de LMskResource**

{{< highlight java >}}

    public static void main(String[] args) {
        String archivoFuente = "src/main/resources/sourceFile.psd";
        String psdSalida = "src/main/resources/sourceFile_output.psd";

        // Cargar imagen de 16 bits.
        try (PsdImage imagen = (PsdImage) Image.load(archivoFuente)) {
            // Buscar LmskResource.
            LmskResource lmskResource = new LmskResource();
            for (LayerResource res : imagen.getGlobalLayerResources()) {
                if (res instanceof LmskResource) {
                    lmskResource = (LmskResource) res;
                    break;
                }
            }

            // Verificar propiedades de LmskResource.
            assertAreEqual(lmskResource.getColorSpace(), ColorSpace.RGB);
            assertAreEqual(lmskResource.getColorComponent1(), 65535);
            assertAreEqual(lmskResource.getColorComponent2(), 0);
            assertAreEqual(lmskResource.getColorComponent3(), 0);
            assertAreEqual(lmskResource.getColorComponent4(), 0);
            assertAreEqual(lmskResource.getOpacity(), (short) 45);
            assertAreEqual(lmskResource.getFlag(), (byte) 128);

            // Cambiar propiedades de LmskResource.
            lmskResource.setColorSpace(ColorSpace.HSB);
            lmskResource.setColorComponent1(7854);
            lmskResource.setColorComponent2(10);
            lmskResource.setColorComponent3(15484);
            lmskResource.setOpacity((short) 85);

            // Guardar la imagen.
            imagen.save(psdSalida);
        }
    }

    static void assertAreEqual(Object esperado, Object actual) {
        assertAreEqual(esperado, actual, "Los objetos no son iguales.");
    }

    static void assertAreEqual(Object esperado, Object actual, String mensaje) {
        if (!esperado.equals(actual)) {
        throw new IllegalArgumentException(mensaje);
        }
    }

{{< /highlight >}}

** PSDJAVA-552. [AI Format] Agrega la capacidad de renderizar un archivo AI basado en PDF con Aspose.PSD**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/ai_one.ai";
    String pngSalida = "src/main/resources/ai_one_output.psd";

    // Cargar la imagen AI basada en PDF.
    try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
        // Guardar la imagen AI como una imagen PNG.
        imagen.save(pngSalida, new PngOptions());
    }

{{< /highlight >}}

** PSDJAVA-553. [AI Format] Agrega soporte para el operador PostScript "cm"**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/ai_two.ai";
    String pngSalida = "src/main/resources/ai_two_output.png";

    // Cargar la imagen AI.
    try (AiImage imagen = (AiImage)Image.load(archivoFuente)) {
        // Guardar la imagen AI como una imagen PNG.
        imagen.save(pngSalida, new PngOptions());
    }

{{< /highlight >}}


** PSDJAVA-554. Agrega nuevos tipos de deformación: Onda, concha arriba, concha abajo**

{{< highlight java >}}

    PsdLoadOptions opcionesCarga = new PsdLoadOptions();
    opcionesCarga.setAllowWarpRepaint(true);
    opcionesCarga.setLoadEffectsResource(true);

    PngOptions opcionesGuardado = new PngOptions();
    opcionesGuardado.setColorType(PngColorType.TruecolorWithAlpha);

    String archivoFuentePez = "src/main/resources/1752_warp_fish.psd";
    String archivoFuenteRise = "src/main/resources/1752_warp_rise.psd";
    String archivoFuenteWave = "src/main/resources/1752_warp_wave.psd";

    String archivoSalidaPez = "src/main/resources/1752_output_fish.png";
    String archivoSalidaRise = "src/main/resources/1752_output_rise.png";
    String archivoSalidaWave = "src/main/resources/1752_output_wave.png";

    try (PsdImage imagenPez = (PsdImage)Image.load(archivoFuentePez, opcionesCarga)) {
        imagenPez.save(archivoSalidaPez, opcionesGuardado);
    }

    try (PsdImage imagenRise = (PsdImage)Image.load(archivoFuenteRise, opcionesCarga)) {
        imagenRise.save(archivoSalidaRise, opcionesGuardado);
    }

    try (PsdImage imagenWave = (PsdImage)Image.load(archivoFuenteWave, opcionesCarga)) {
        imagenWave.save(archivoSalidaWave, opcionesGuardado);
    }

{{< /highlight >}}


** PSDJAVA-555. Agrega soporte de deformación vertical**

{{< highlight java >}}

    PsdLoadOptions opcionesCarga = new PsdLoadOptions();
    opcionesCarga.setAllowWarpRepaint(true);
    opcionesCarga.setLoadEffectsResource(true);

    PngOptions opcionesGuardado = new PngOptions();
    opcionesGuardado.setColorType(PngColorType.TruecolorWithAlpha);

    String archivoArcoInferior = "src/main/resources/1797_warp_arc_lower_v.psd";
    String archivoArcoSuperior = "src/main/resources/1797_warp_arc_upper_v.psd";
    String archivoArco = "src/main/resources/1797_warp_arch_v.psd";
    String archivoAbultamiento = "src/main/resources/1797_warp_bulge_v.psd";
    String archivoBandera = "src/main/resources/1797_warp_flag_v.psd";
    String archivoPez = "src/main/resources/1797_warp_fish_v.psd";
    String archivoRise = "src/main/resources/1797_warp_rise_v.psd";
    String archivoWave = "src/main/resources/1797_warp_wave_v.psd";

    String archivoSalidaArcoInferior = "src/main/resources/1797_warp_arc_lower_v.png";
    String archivoSalidaArcoSuperior = "src/main/resources/1797_warp_arc_upper_v.png";
    String archivoSalidaArco = "src/main/resources/1797_warp_arch_v.png";
    String archivoSalidaAbultamiento = "src/main/resources/1797_warp_bulge_v.png";
    String archivoSalidaBandera = "src/main/resources/1797_warp_flag_v.png";
    String archivoSalidaPez = "src/main/resources/1797_output_fish_v.png";
    String archivoSalidaRise = "src/main/resources/1797_output_rise_v.png";
    String archivoSalidaWave = "src/main/resources/1797_output_wave_v.png";

    try (PsdImage imagenArcoInferior = (PsdImage) Image.load(archivoArcoInferior, opcionesCarga)) {
        imagenArcoInferior.save(archivoSalidaArcoInferior, opcionesGuardado);
    }

    try (PsdImage imagenArcoSuperior = (PsdImage) Image.load(archivoArcoSuperior, opcionesCarga)) {
        imagenArcoSuperior.save(archivoSalidaArcoSuperior, opcionesGuardado);
    }

    try (PsdImage imagenArco = (PsdImage) Image.load(archivoArco, opcionesCarga)) {
        imagenArco.save(archivoSalidaArco, opcionesGuardado);
    }

    try (PsdImage imagenAbultamiento = (PsdImage) Image.load(archivoAbultamiento, opcionesCarga)) {
        imagenAbultamiento.save(archivoSalidaAbultamiento, opcionesGuardado);
    }

    try (PsdImage imagenBandera = (PsdImage) Image.load(archivoBandera, opcionesCarga)) {
        imagenBandera.save(archivoSalidaBandera, opcionesGuardado);
    }

    try (PsdImage imagenPez = (PsdImage) Image.load(archivoPez, opcionesCarga)) {
        imagenPez.save(archivoSalidaPez, opcionesGuardado);
    }

    try (PsdImage imagenRise = (PsdImage) Image.load(archivoRise, opcionesCarga)) {
        imagenRise.save(archivoSalidaRise, opcionesGuardado);
    }

    try (PsdImage imagenWave = (PsdImage) Image.load(archivoWave, opcionesCarga)) {
        imagenWave.save(archivoSalidaWave, opcionesGuardado);
    }

{{< /highlight >}}


** PSDJAVA-556. System.ArgumentNullException: 'El valor no puede ser nulo. (Parámetro 'clave')' al llamar a TextLayer.GetFonts()**

{{< highlight java >}}

    String src = "src/main/resources/SimpleText.psd";

    FontSettings.removeFontCacheFile();

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                TextLayer textLayer = (TextLayer) layer;
                textLayer.getFonts();
            }
        }
    }

{{< /highlight >}}