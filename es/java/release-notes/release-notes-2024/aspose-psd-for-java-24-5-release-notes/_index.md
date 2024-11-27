---
title: Notas de la versión Aspose.PSD for Java 24.5
type: docs
weight: 40
url: /es/java/aspose-psd-for-java-24-5-release-notes/
---

{{% alert color="primary" %}} Esta página contiene las notas de la versión de [Aspose.PSD for Java 24.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.5/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                                                             | **Categoría**  |
|:------------|:------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-617 | [Formato AI] Agregar soporte para manejar archivos AI con encabezado EPSF                                               | Funcionalidad  |
| PSDJAVA-620 | La semitransparencia se procesa de forma incorrecta en la vista previa del archivo psd                                    | Error         |
| PSDJAVA-621 | La representación de la Capa de forma es parcialmente incorrecta                                                          | Error         |
| PSDJAVA-622 | Excepción al guardar archivos PSD con tamaño superior a 200 MB y dimensiones grandes (hay un problema de consumo de memoria) | Error         |
| PSDJAVA-623 | Error de excepción al guardar la imagen en PDF después de actualizar de 23.7 a 24.3                                     | Error         |
| PSDJAVA-624 | Corregir el problema en el método GetFontInfoRecords para las fuentes chinas                                             | Error         |

## **Cambios en la API pública**
# **APIs añadidas:**

- M: com.aspose.psd.fileformats.ai.AiLayerSection.getColorIndex
- M: com.aspose.psd.fileformats.ai.AiLayerSection.setColorIndex(int)
- M: com.aspose.psd.fileformats.ai.AiLayerSection.hasMultiLayerMasks
- M: com.aspose.psd.fileformats.ai.AiLayerSection.setMultiLayerMasks(boolean)
- M: com.aspose.psd.imageoptions.PsdOptions.getBackgroundContents
- M: com.aspose.psd.imageoptions.PsdOptions.setBackgroundContents(com.aspose.psd.fileformats.psd.rawcolor.RawColor)

# **APIs eliminadas:**

- Ninguna

## **Ejemplos de uso:**

**PSDJAVA-617. [Formato AI] Agregar soporte para manejar archivos AI con encabezado EPSF**

{{< highlight java >}}

    public static void main(String[] args) {
        String archivoFuente = "src/main/resources/ejemplo.ai";
        String rutaSalidaArchivo = "src/main/resources/ejemplo.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
            assertAreEqual(imagen.getLayers().length, 2);
            assertAreEqual(imagen.getLayers()[0].hasMultiLayerMasks(), false);
            assertAreEqual(imagen.getLayers()[0].getColorIndex(), -1);
            assertAreEqual(imagen.getLayers()[1].hasMultiLayerMasks(), false);
            assertAreEqual(imagen.getLayers()[1].getColorIndex(), -1);

            imagen.save(rutaSalidaArchivo, new PngOptions());
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

**PSDJAVA-620. La semitransparencia se procesa de forma incorrecta en la vista previa del archivo psd**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/frog_nosymb.psd";
        String archivoSalida = "src/main/resources/frog_nosymb_backgroundcontents_output.psd";

        try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente)) {
            RawColor colorFondo = new RawColor(PixelDataFormat.getRgb32Bpp());
            int valorArgb = 255 << 24 | 255 << 16 | 255 << 8 | 255;
            colorFondo.setAsInt(valorArgb); // Blanco

            PsdOptions opcionesPsd = new PsdOptions(imagenPsd);
            opcionesPsd.setColorMode(ColorModes.Rgb);
            opcionesPsd.setCompressionMethod(CompressionMethod.RLE);
            opcionesPsd.setChannelsCount((short) 4);
            opcionesPsd.setBackgroundContents(colorFondo);

            imagenPsd.save(archivoSalida, opcionesPsd);
        }

{{< /highlight >}}

**PSDJAVA-621. La representación de la Capa de forma es parcialmente incorrecta**

{{< highlight java >}}

    private static final int RelacionImgToPsd = 256 * 65535;

    public static void main(String[] args) {
        String archivoFuente = "src/main/resources/ShapeLayerTest.psd";
        String archivoSalida = "src/main/resources/ShapeLayerTest_output.psd";
        
        try (PsdImage im = (PsdImage) Image.load(archivoFuente)) {
            ShapeLayer capaForma = (ShapeLayer) im.getLayers()[2];
            IPath ruta = capaForma.getPath();
            IPathShape[] formasRuta = ruta.getItems();
            List<BezierKnotRecord> listaNudos = new ArrayList<>();
            for (IPathShape formaRuta : formasRuta) {
                BezierKnotRecord[] nudos = formaRuta.getItems();
                Collections.addAll(listaNudos, nudos);
            }

            // Cambiar propiedades de la capa
            PathShape nuevaForma = new PathShape();

            BezierKnotRecord primerRegistroNudoBezier = new BezierKnotRecord();
            primerRegistroNudoBezier.setLinked(true);
            primerRegistroNudoBezier.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            capaForma.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            capaForma.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            capaForma.getContainer().getSize())});

            BezierKnotRecord segundoRegistroNudoBezier = new BezierKnotRecord();
            segundoRegistroNudoBezier.setLinked(true);
            segundoRegistroNudoBezier.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(50, 490),
                            capaForma.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 490),
                            capaForma.getContainer().getSize()), // Punto de anclaje
                    pointFToResourcePoint(
                            new PointF(150, 490),
                            capaForma.getContainer().getSize())
            });

            BezierKnotRecord tercerRegistroNudoBezier = new BezierKnotRecord();
            tercerRegistroNudoBezier.setLinked(true);
            tercerRegistroNudoBezier.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(490, 150),
                            capaForma.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 50),
                            capaForma.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 20),
                            capaForma.getContainer().getSize()),
            });

            BezierKnotRecord[] nudosBezier = new BezierKnotRecord[]
                    {primerRegistroNudoBezier, segundoRegistroNudoBezier, tercerRegistroNudoBezier};

            nuevaForma.setItems(nudosBezier);

            List<IPathShape> nuevasFormas = new ArrayList<>(Arrays.asList(formasRuta));
            nuevasFormas.add(nuevaForma);

            IPathShape[] formasRutaNueva = nuevasFormas.toArray(new IPathShape[0]);
            ruta.setItems(formasRutaNueva);

            capaForma.update();

            im.save(archivoSalida, new PsdOptions());
        }

        try (PsdImage im = (PsdImage) Image.load(archivoSalida)) {
            ShapeLayer capaForma = (ShapeLayer) im.getLayers()[2];
            IPath ruta = capaForma.getPath();
            IPathShape[] formasRuta = ruta.getItems();
            List<BezierKnotRecord> listaNudos = new ArrayList<>();
            for (IPathShape formaRuta : formasRuta) {
                BezierKnotRecord[] nudos = formaRuta.getItems();
                listaNudos.addAll(Arrays.asList(nudos));
            }

            assertAreEqual(3, formasRuta.length);
            assertAreEqual(42, capaForma.getLeft());
            assertAreEqual(14, capaForma.getTop());
            assertAreEqual(1600, capaForma.getBounds().getWidth());
            assertAreEqual(1086, capaForma.getBounds().getHeight());
        }
    }

    static Point pointFToResourcePoint(PointF punto, Size tamañoImagen) {
        return new Point(
                (int) Math.round(punto.getY() * (RelacionImgToPsd / tamañoImagen.getHeight())),
                (int) Math.round(punto.getX() * (RelacionImgToPsd / tamañoImagen.getWidth())));
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

**PSDJAVA-622. Excepción al guardar archivos PSD con tamaño superior a 200 MB y dimensiones grandes (hay un problema de consumo de memoria)**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/archivogrande.psd";
    String archivoSalida = "src/main/resources/salida_raw.psd";

    PsdLoadOptions opcionesCarga = new PsdLoadOptions();
    opcionesCarga.setLoadEffectsResource(true);
    opcionesCarga.setUseDiskForLoadEffectsResource(true);

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente, opcionesCarga)) {
        PsdOptions opcionesPsd = new PsdOptions();
        opcionesPsd.setCompressionMethod(CompressionMethod.RLE);

        // No debería haber errores aquí
        imagenPsd.save(archivoSalida, opcionesPsd);
    }

{{< /highlight >}}

**PSDJAVA-623. Error de excepción al guardar la imagen en PDF después de actualizar de 23.7 a 24.3**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/CVFlor.psd";
    String archivoSalida = "src/main/resources/_export.pdf";

    try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente)) {
        PdfOptions opcionesGuardado = new PdfOptions();
        opcionesGuardado.setPdfCoreOptions(new PdfCoreOptions());

        imagenPsd.save(archivoSalida, opcionesGuardado);
    }

{{< /highlight >}}

**PSDJAVA-624. Corregir el problema en el método GetFontInfoRecords para las fuentes chinas**

{{< highlight java >}}

    String carpetaFuente = "src/main/resources/Fuente";
    String archivoFuente = "src/main/resources/bd-worlds-best-pink.psd";

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setLoadEffectsResource(true);
    opcionesCargaPsd.setAllowWarpRepaint(true);

    try {
        FontSettings.setFontsFolders(new String[]{carpetaFuente}, true);

        try (PsdImage imagen = (PsdImage) PsdImage.load(archivoFuente, opcionesCargaPsd)) {
            for (Layer capa : imagen.getLayers()) {
                if (capa instanceof TextLayer) {
                    TextLayer capaTexto = (TextLayer) capa;

                    if ("best".equals(capaTexto.getText())) {
                        // Sin esta corrección aquí habría una excepción debido a la fuente china.
                        capaTexto.updateText("ÉXITO");
                    }
                }
            }
        }
    } finally {
        FontSettings.reset();
    }

{{< /highlight >}}