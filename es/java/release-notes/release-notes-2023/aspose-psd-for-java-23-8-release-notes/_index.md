---
title: Notas de la versión Aspose.PSD para Java 23.8
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-23-8-notas-de-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión de [Aspose.PSD para Java 23.8](https://downloads.aspose.com/psd/java/nuevas-versiones/aspose.psd-para-java-23.8/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                                                                                      | **Categoría** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Agregar nuevo tipo de deformación (Flag)                                                                                                          |    Característica   |
| PSDJAVA-519 | Agregar nuevos tipos de deformación: arco hacia arriba, arco hacia abajo, esfera                                                                   |    Característica   |
| PSDJAVA-520 | Implementar el nuevo método PsdImage.AddPosterizeAdjustmentLayer para agregar nueva capa de posterización                                        |    Característica   |
| PSDJAVA-521 | Información PSD perdida al abrir y guardar                                                                                                       |      Error     |
| PSDJAVA-522 | Falla al cargar la imagen                                                                                                                        |      Error     |
| PSDJAVA-523 | Falla al cargar la imagen: No se puede convertir el objeto de tipo UnknownStructure al tipo DescriptorStructure                                 |      Error     |
| PSDJAVA-524 | El archivo modificado en la biblioteca de terceros corrompe el archivo PSD, pero se puede abrir en Photoshop                                    |      Error     |

## **Cambios en la API pública**
# **APIs Agregadas:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **APIs Eliminadas:**

- Ninguna

## **Ejemplos de uso:**

**PSDJAVA-518. Agregar nuevo tipo de deformación (Flag)**

{{< highlight java >}}
    String archivoFuente = "src/main/resources/deformacion_bandera.psd";
    String archivoSalida = "src/main/resources/exportacion_bandera.png";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setAllowWarpRepaint(true);
    opcionesCargaPsd.setLoadEffectsResource(true);
    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente, opcionesCargaPsd)) {
        PngOptions opcionesPng = new PngOptions();
        opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

        imagenPsd.save(archivoSalida, opcionesPng);
    }
{{< /highlight >}}

**PSDJAVA-519. Agregar nuevos tipos de deformación: arco hacia arriba, arco hacia abajo, esfera**

{{< highlight java >}}
    String archivoFuenteArcoSuperior = "src/main/resources/deformacion_arco_superior.psd";
    String archivoFuenteArcoInferior = "src/main/resources/deformacion_arco_inferior.psd";
    String archivoFuenteAbultar = "src/main/resources/deformacion_abultar.psd";

    String archivoSalidaArcoSuperior = "src/main/resources/exportacion_ArcoSuperior.png";
    String archivoSalidaArcoInferior = "src/main/resources/exportacion_ArcoInferior.png";
    String archivoSalidaAbultar = "src/main/resources/exportacion_Abultar.png";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setAllowWarpRepaint(true);
    opcionesCargaPsd.setLoadEffectsResource(true);

    PngOptions opcionesPng = new PngOptions();
    opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuenteArcoSuperior, opcionesCargaPsd)) {
        imagenPsd.save(archivoSalidaArcoSuperior, opcionesPng);
    }

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuenteArcoInferior, opcionesCargaPsd)) {
        imagenPsd.save(archivoSalidaArcoInferior, opcionesPng);
    }

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuenteAbultar, opcionesCargaPsd)) {
        imagenPsd.save(archivoSalidaAbultar, opcionesPng);
    }
{{< /highlight >}}

**PSDJAVA-520. Implementar nuevo método PsdImage.AddPosterizeAdjustmentLayer para agregar nueva capa de posterización**

{{< highlight java >}}
public static void main(String[] args) {
    String archivoSrc = "src/main/resources/zendeya.psd";
    String archivoOut = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoSrc)) {
        imagenPsd.addPosterizeAdjustmentLayer();
        imagenPsd.save(archivoOut);
    }

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setLoadEffectsResource(true);

    // Verificar cambios guardados
    try (PsdImage imagen = (PsdImage) Image.load(archivoOut, opcionesCargaPsd)) {
        assertAreEqual(2, imagen.getLayers().length);

        PosterizeLayer capaPosterizar = (PosterizeLayer) imagen.getLayers()[1];

        assertAreEqual(true, capaPosterizar instanceof PosterizeLayer);
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

**PSDJAVA-521. Información PSD perdida al abrir y guardar**

{{< highlight java >}}
    String src = "src/main/resources/ArchivoOriginal.psd";
    String outputPsd = "src/main/resources/salida_ArchivoOriginal.psd";
    String outputPng = "src/main/resources/salida_ArchivoOriginal.png";

    try (PsdImage imagenPsd = (PsdImage) Image.load(src)) {
        PngOptions opcionesPng = new PngOptions();
        opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

        imagenPsd.save(outputPsd);
        imagenPsd.save(outputPng, opcionesPng);
    }
{{< /highlight >}}

**PSDJAVA-522. Falla al cargar la imagen**

{{< highlight java >}}
    String archivoFuente1 = "src/main/resources/texto_prueba.psd";
    String archivoFuente2 = "src/main/resources/objeto_inteligente_prueba.psd";

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente1)) {
    }

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Falla al cargar la imagen: No se puede convertir el objeto de tipo UnknownStructure al tipo DescriptorStructure**

{{< highlight java >}}
   try (PsdImage nuevoPsd = new PsdImage(10, 10)) {
        nuevoPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream flujoMemoria = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            nuevoPsd.save(flujoMemoria.toOutputStream());

            flujoMemoria.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            flujoMemoria.write(new byte[1], 0, 0);
            flujoMemoria.setPosition(0);

            try (PsdImage imagenPsd = (PsdImage) Image.load(flujoMemoria.toInputStream())) {
                // Debería cargar correctamente
            }
        } finally {
            flujoMemoria.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. El archivo modificado en la biblioteca de terceros corrompe el archivo PSD, pero se puede abrir en Photoshop**

{{< highlight java >}}
    String archivoFuente = "src/main/resources/salida.psd";
    String archivoSalida = "src/main/resources/exportacion.png";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(archivoFuente, opcionesCargaPsd)) {
        PngOptions opcionesPng = new PngOptions();
        opcionesPng.setCompressionLevel(9);
        opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(archivoSalida, opcionesPng);
    }
{{< /highlight >}}
