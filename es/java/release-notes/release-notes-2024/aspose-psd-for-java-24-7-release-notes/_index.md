---
title: Notas de Lanzamiento de Aspose.PSD para Java 24.7
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-24-7-notas-de-lanzamiento/
---

{{% alert color="primary" %}} Esta página contiene notas de lanzamiento para [Aspose.PSD para Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Clave**    | **Resumen**                                                                                      | **Categoría** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Excepción "Error al cargar la imagen" al abrir un documento AI                                    | Error        |
| PSDJAVA-636 | Texto renderizado incorrectamente en archivos PDF de salida                                         | Error        |
| PSDJAVA-637 | Solucionar ImageSaveException: Error de exportación de imagen para el archivo dado en Linux        | Error        |
| PSDJAVA-638 | Solucionar la carga de fuentes al usar Aspose.Drawing                                               | Error        |
| PSDJAVA-639 | 'La operación aritmética causó un desbordamiento' al crear una capa de objeto inteligente usando una imagen JPEG grande | Error        |
| PSDJAVA-640 | El archivo AI no se puede convertir en un archivo JPG                                               | Error        |

## **Cambios en la API Pública**
# **APIs Agregadas:**

- Ninguna

# **APIs Eliminadas:**

- Ninguna 

## **Ejemplos de Uso:**

**PSDJAVA-635. Excepción "Error al cargar la imagen" al abrir un documento AI**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/[SA]_ID_card_template.ai";
    String archivoSalida = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
        imagen.save(archivoSalida, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Texto renderizado incorrectamente en archivos PDF de salida**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage imagenPsd = (PsdImage) Image.load(src)) {
        PdfOptions opcionesGuardado = new PdfOptions();
        opcionesGuardado.setPdfCoreOptions(new PdfCoreOptions());

        imagenPsd.save(output, opcionesGuardado);
    }

{{< /highlight >}}

**PSDJAVA-637. Solucionar ImageSaveException: Error de exportación de imagen para el archivo dado en Linux**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String archivoSalida = "src/main/resources/output.jpg";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setLoadEffectsResource(true);

    try (var imagenPsd = (PsdImage) Image.load(archivoFuente, opcionesCargaPsd)) {
        JpegOptions opcionesGuardado = new JpegOptions();
        opcionesGuardado.setQuality(70);
        imagenPsd.save(archivoSalida, opcionesGuardado);
    }

{{< /highlight >}}

**PSDJAVA-638. Solucionar la carga de fuentes al usar Aspose.Drawing**

{{< highlight java >}}

    final var coleccionFuentesInstaladas = new InstalledFontCollection();
    try {
        System.out.println("- Antes de la actualización. Cantidad de fuentes instaladas: " + coleccionFuentesInstaladas.getFamilies().length);
        System.out.println("- Plataforma: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Actualizar la caché de fuentes intentando obtener el nombre de fuente de Adobe para 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Después de la actualización. Cantidad de fuentes instaladas: " + coleccionFuentesInstaladas.getFamilies().length);

        assertAreEqual(coleccionFuentesInstaladas.getFamilies().length, 1);
    } finally {
        coleccionFuentesInstaladas.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'La operación aritmética causó un desbordamiento' al crear una capa de objeto inteligente utilizando una imagen JPEG grande**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/source.psd";
    String imagenJpg = "src/main/resources/test.jpg";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var imagen = (PsdImage) Image.load(archivoFuente, opcionesCargaPsd)) {
        final FileStream flujo = new FileStream(imagenJpg, FileMode.Open);
        try {
            var capaAñadida = new SmartObjectLayer(flujo);
            capaAñadida.setName("Capa de Prueba");
            imagen.addLayer(capaAñadida);
        } finally {
            flujo.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. El archivo AI no se puede convertir en un archivo JPG**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/aaa.ai";
    String archivoSalida = "src/main/resources/aaa.png";

    try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
        imagen.save(archivoSalida, new PngOptions());
    }

{{< /highlight >}}
