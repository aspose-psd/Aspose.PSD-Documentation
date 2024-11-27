---
title: Notas de lanzamiento de Aspose.PSD para Java 23.9
type: docs
weight: 40
url: /es/java/aspose-psd-for-java-23-9-release-notes/
---

{{% alert color="primary" %}} Esta página contiene notas de lanzamiento para [Aspose.PSD para Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                                                                                        | **Categoría** |
|:------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Implementar la creación de máscara para nuevas capas de ajuste                                                                                      | Característica |
| PSDJAVA-528 | Agregar soporte para la Opción de mezcla de capas recortadas como opción de mezcla de grupo                                                        | Característica |
| PSDJAVA-529 | El archivo PSD con modo de color de 16 bits no aplica la máscara para capas de ajuste                                                               | Error         |
| PSDJAVA-530 | Representación incorrecta de corchetes en la capa de texto                                                                                         | Error         |
| PSDJAVA-531 | No se pueden actualizar los estilos en las capas de texto                                                                                            | Error         |
| PSDJAVA-532 | Después de exportar el archivo PSD con CMYK se rompen los colores en el PSD exportado                                                                | Error         |
| PSDJAVA-533 | El archivo PSB específico arroja la excepción "El rectángulo no tiene un área de procesamiento común"                                               | Error         |
| PSDJAVA-534 | Fallo al cargar la imagen. OverflowException: La operación aritmética resultó en un desbordamiento.                                                 | Error         |

## **Cambios en la API pública**
# **APIs agregadas:**

- M:com.aspose.psd.PixelDataFormat.getMisCmyk16
- M:com.aspose.psd.PixelDataFormat.getMisCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getMisElementosRecortadosMezclados
- M:com.aspose.psd.fileformats.psd.layers.Layer.setMisElementosRecortadosMezclados(boolean)

# **APIs eliminadas:**

- Ninguna

## **Ejemplos de uso:**

** PSDJAVA-527. Implementar la creación de máscara para nuevas capas de ajuste**

{{< highlight java >}}
public static void main(String[] args) {
    String archivoFuente = "src/main/resources/zendeya_BW.psd";
    String archivoDestino = "src/main/resources/zendeya_BW_salida.psd";

    try (PsdImage im = (PsdImage) Image.load(archivoFuente)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(archivoDestino);
    }

    try (PsdImage im = (PsdImage) Image.load(archivoDestino)) {
        Layer capa = im.getLayers()[1];

        assertAreEqual(5, capa.getChannelsCount());
        assertAreEqual((short) -2, capa.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object esperado, Object real) {
    assertAreEqual(esperado, real, "Los objetos no son iguales.");
}

static void assertAreEqual(Object esperado, Object real, String mensaje) {
    if (!esperado.equals(real)) {
        throw new IllegalArgumentException(mensaje);
    }
}
{{< /highlight >}}

** PSDJAVA-528. Agregar soporte para la Opción de mezcla de capas recortadas como opción de mezcla de grupo**

{{< highlight java >}}
    String archivoFuente = "src/main/resources/ejemplo_fuente.psd";
    String psdSalida = "src/main/resources/ejemplo_salida.psd";
    String pngSalida = "src/main/resources/ejemplo_salida.png";

    try (PsdImage imagen = (PsdImage)Image.load(archivoFuente)) {
        imagen.getLayers()[1].setBlendClippedElements(false);
        imagen.save(psdSalida);
        imagen.save(pngSalida, new PngOptions());
    }
{{< /highlight >}}

** PSDJAVA-529. El archivo PSD con modo de color de 16 bits no aplica la máscara para capas de ajuste**

{{< highlight java >}}
	String archivoFuente = "src/main/resources/fuente.psd";
    String pngSalida = "src/main/resources/actual.png";

    try (PsdImage imagen = (PsdImage) Image.load(archivoFuente)) {
        imagen.save(pngSalida, new PngOptions());
    }
{{< /highlight >}}

** PSDJAVA-530. Representación incorrecta de corchetes en la capa de texto**

{{< highlight java >}}
    String archivo = "src/main/resources/archivo1.psd";
    String salida = "src/main/resources/salida_1235.png";

    try (PsdImage psdImagen = (PsdImage) Image.load(archivo)) {
        for (Layer capa : psdImagen.getLayers()) {
            if (capa instanceof TextLayer) {
                TextLayer capaTexto = (TextLayer) capa;
                capaTexto.getTextData().updateLayerData();

                PsdOptions opcionesImagen = new PsdOptions(psdImagen);
                psdImagen.save(salida, opcionesImagen);
            }
        }
    }
{{< /highlight >}}

** PSDJAVA-531. No se pueden actualizar los estilos en las capas de texto**

{{< highlight java >}}
    String archivoFuente = "src/main/resources/Ejemplo_TamañoFuente.psd";
    String archivoSalida = "src/main/resources/salida_Ejemplo_TamañoFuente.psd";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setLoadEffectsResource(true);

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente, opcionesCargaPsd)) {
        TextLayer l1 = (TextLayer) imagenPsd.getLayers()[4];
        TextLayer l2 = (TextLayer) imagenPsd.getLayers()[5];

        ITextPortion[] elementosTexto1 = l1.getTextData().producePortions(new String[]{"texto1", "texto2"},
                l1.getTextData().getItems()[0].getStyle(), l1.getTextData().getItems()[0].getParagraph());

        l1.getTextData().removePortion(0);
        for (ITextPortion elemento : elementosTexto1) {
            l1.getTextData().addPortion(elemento);
        }

        ITextPortion[] elementosTexto2 = l2.getTextData().producePortions(new String[]{"capa de texto 1", "capa de texto 22"},
                l2.getTextData().getItems()[0].getStyle(), l2.getTextData().getItems()[0].getParagraph());

        for (ITextPortion elemento : elementosTexto2) {
            l2.getTextData().addPortion(elemento);
        }

        l1.getTextData().updateLayerData();
        l2.getTextData().updateLayerData();

        imagenPsd.save(archivoSalida);
    }
{{< /highlight >}}

** PSDJAVA-532. Después de exportar el archivo PSD con CMYK se rompen los colores en el PSD exportado**

{{< highlight java >}}
    String archivoFuente = "src/main/resources/cañón.psd";
    String archivoSalidaPng = "src/main/resources/salida_cañón.png";

    MemoryStream flujoSalida = new MemoryStream();

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente)) {
        imagenPsd.save(flujoSalida.toOutputStream());
    }

    flujoSalida.setPosition(0);
    try (PsdImage imagenPsd = (PsdImage) Image.load(flujoSalida.toInputStream())) {
        imagenPsd.save(archivoSalidaPng, new PngOptions());
    }

    flujoSalida.close();
{{< /highlight >}}

** PSDJAVA-533. El archivo PSB específico arroja la excepción "El rectángulo no tiene un área de procesamiento común"**

{{< highlight java >}}
    String archivoEntrada = "src/main/resources/1619_fuente.psb";
    String archivoSalida = "src/main/resources/1619_salida.png";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setLoadEffectsResource(true);
    try (PsdImage img = (PsdImage) Image.load(archivoEntrada, opcionesCargaPsd)) {
        PngOptions opcionesPng = new PngOptions();
        opcionesPng.setCompressionLevel(9);
        opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);
        img.save(archivoSalida, opcionesPng);
    }
{{< /highlight >}}

** PSDJAVA-534. Fallo al cargar la imagen. OverflowException: La operación aritmética resultó en un desbordamiento.**

{{< highlight java >}}
public static void main(String[] args) {
    String archivoFuente = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

    try (PsdImage im = (PsdImage)PsdImage.load(archivoFuente))
    {
        Layer capa = im.getLayers()[28];
        GrdmResource recursoGrdm = (GrdmResource)capa.getResources()[0];

        assertAreEqual("自定", recursoGrdm.getGradientName());
    }

}

static void assertAreEqual(Object esperado, Object real) {
    assertAreEqual(esperado, real, "Los objetos no son iguales.");
}

static void assertAreEqual(Object esperado, Object real, String mensaje) {
    if (!esperado.equals(real)) {
        throw new IllegalArgumentException(mensaje);
    }
}
{{< /highlight >}}
