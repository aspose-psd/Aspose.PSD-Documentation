---
title: Notas de la versión de Aspose.PSD para Java 23.7
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-23-7-notas-de-la-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión de [Aspose.PSD para Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                                                                      | **Categoría** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Agregar la capacidad de exportar cada capa de un archivo PSD a un archivo Gif animado                                           | Función      |
| PSDJAVA-503 | Asignar la propiedad de relleno de la capa de forma desde el recurso vscg                                                       | Función      |
| PSDJAVA-504 | Agregar nuevos tipos de deformación (arco y arco)                                                                                 | Función      |
| PSDJAVA-505 | Cambiar la aplicación que guarda el archivo PSD a Aspose.PSD si la propiedad UpdateMetadata está establecida en true           | Función      |
| PSDJAVA-510 | Aumentar el área de cálculo de la imagen de deformación                                                                          | Función      |
| PSDJAVA-511 | El procesamiento de la capa de ajuste de blanco y negro procesa de forma incorrecta la semitransparencia                       | Error        |
| PSDJAVA-512 | SmartObject ReplaceContents (cuando la opción AllowWarpRepaint está activa) falla después de 2 minutos de cálculo             | Error        |
| PSDJAVA-513 | Agregar la capacidad de obtener la posición real de la izquierda y arriba de LayerGroup                                         | Error        |
| PSDJAVA-514 | La redimensión de la capa funciona incorrectamente cuando el archivo psd tiene VogkResource con estructuras en puntos          | Error        |
| PSDJAVA-515 | TextBound no está funcionando como se esperaba                                                                                   | Error        |
| PSDJAVA-516 | Agregar una capa creada con el constructor predeterminado a la imagen PSD no agrega recursos predeterminados                   | Error        |
| PSDJAVA-517 | Timeline.LoopsCount se ignora al exportar a GIF animado                                                                         | Error        |

## **Cambios en la API Pública**
# **APIs Agregadas:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **APIs Eliminadas:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Ejemplos de uso:**

**PSDJAVA-502. Agregar la capacidad de exportar cada capa de un archivo PSD a un archivo Gif animado**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Crear fotogramas para cada capa.
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }

            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // Actualizar estados actuales
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Asignar la propiedad de relleno de la capa de forma desde el recurso vscg**

{{< highlight java >}}
        // Ejemplo de relleno sólido
        public static void main(String[] args) {
            String srcFile = "src/main/resources/ShapeInternalSolid.psd";
            String outFile = "src/main/resources/ShapeInternalSolid.psd.out.psd";

            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setLoadEffectsResource(true);

            try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
                 ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
                  ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
                 fillSettings.setColor(Color.getRed());

                 shapeLayer.update();

                 image.save(outFile);
            }

            // Verificar cambios guardados
            try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

            assertAreEqual(Color.getRed(), fillSettings.getColor());

            image.save(outFile);
        }

        static void assertAreEqual(Object expected, Object actual, String message) {
            if (!expected.equals(actual)) {
                throw new IllegalArgumentException(message);
            }
        }

        static void assertAreEqual(Object expected, Object actual) {
            assertAreEqual(expected, actual, "Los objetos no son iguales.");
        }
		
		// Ejemplo de relleno degradado:

	public static void main(String[] args) {
    String srcFile = "src/main/resources/ShapeInternalGradient.psd";
    String outFile = "src/main/resources/ShapeInternalGradient.psd.out.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();
        fillSettings.setDither(true);
        fillSettings.setReverse(true);
        fillSettings.setAlignWithLayer(false);
        fillSettings.setAngle(20);
        fillSettings.setScale(50);
        fillSettings.getColorPoints()[0].setLocation(100);
        fillSettings.getColorPoints()[1].setLocation(4000);
        fillSettings.getTransparencyPoints()[0].setLocation(200);
        fillSettings.getTransparencyPoints()[1].setLocation(3800);
        fillSettings.getTransparencyPoints()[0].setOpacity(90);
        fillSettings.getTransparencyPoints()[1].setOpacity(10);

        shapeLayer.update();

        image.save(outFile);
    }

    // Verificar cambios guardados
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();

        assertAreEqual(true, fillSettings.getDither());
        assertAreEqual(true, fillSettings.getReverse());
        assertAreEqual(false, fillSettings.getAlignWithLayer());
        assertAreEqual((double) 20, fillSettings.getAngle());
        assertAreEqual(50, fillSettings.getScale());
        assertAreEqual(100, fillSettings.getColorPoints()[0].getLocation());
        assertAreEqual(4000, fillSettings.getColorPoints()[1].getLocation());
        assertAreEqual(200, fillSettings.getTransparencyPoints()[0].getLocation());
        assertAreEqual(3800, fillSettings.getTransparencyPoints()[1].getLocation());
        assertAreEqual((double) 90, fillSettings.getTransparencyPoints()[0].getOpacity());
        assertAreEqual((double) 10, fillSettings.getTransparencyPoints()[1].getOpacity());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Los objetos no son iguales.");
}

{{< /highlight >}}

**PSDJAVA-504. Agregar nuevos tipos de deformación (arco y arco)**

{{< highlight java >}}
    String sourceArcFile = "src/main/resources/arc_warp.psd";
    String outputArcFile = "src/main/resources/arc_export.png";

    String sourceArchFile = "src/main/resources/arch_warp.psd";
    String outputArchFile = "src/main/resources/arch_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceArcFile, psdLoadOptions)) {
        psdImage.save(outputArcFile, pngOptions);
    }


    try (PsdImage psdImage = (PsdImage) Image.load(sourceArchFile, psdLoadOptions)) {
        psdImage.save(outputArchFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-505. Cambiar la aplicación que guarda el archivo PSD a Aspose.PSD si la propiedad UpdateMetadata está establecida en true**

{{< highlight java >}}
    String path = "src/main/resources/output.psd";
    try (PsdImage image = new PsdImage(100, 100)) {
        // Si desea que cambie la herramienta de creación, asegúrese de que la propiedad "UpdateMetadata" esté establecida en true. Por defecto está en true.
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setUpdateMetadata(true);

        // Guardar la imagen.
        image.save(path, psdOptions);

        // Comprobar la herramienta de creación en el código.
        XmpPacketWrapper xmpData = image.getXmpData();
        XmpPackage basicPackage = image.getXmpData().getPackage(Namespaces.XmpBasic);

        // Aquí se actualizará la información de la herramienta de creación.
        String currentCreatorTool = (String) basicPackage.get_Item(":CreatorTool");
{{< /highlight >}}

**PSDJAVA-510. Aumentar el área de cálculo de la imagen de deformación**

{{< highlight java >}}
    String sourceFile = "src/main/resources/mug4_warp.psd";
    String outputFile = "src/main/resources/mug4_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-511. El procesamiento de la capa de ajuste de blanco y negro procesa la semitransparencia incorrectamente**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/frog_nosymb.psd";
    String outFile = "src/main/resources/frog_nosymb.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile)) {
        psdImage.addBlackWhiteAdjustmentLayer();
        psdImage.save(outFile);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // Verificar los cambios guardados
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer) image.getLayers()[1];

        if (blackWhiteAdjustmentLayer == null) {
            throw new Exception("La capa 2 debería ser BlackWhiteAdjustmentLayer");
        }

        image.save(outFile);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Los objetos no son iguales.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
       throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-512. SmartObject ReplaceContents (cuando la opción AllowWarpRepaint está activa) falla después de 2 minutos de cálculo**

{{< highlight java >}}
    String sourceFile = "src/main/resources/mug 4.psd";
    String changeFile = "src/main/resources/artwork for replace.png";
    String outputFile = "src/main/resources/export.png";

    int newHeight = 300;

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        SmartObjectLayer smartObjectLayer = (SmartObjectLayer) psdImage.getLayers()[3];

        double scale = (double) newHeight / smartObjectLayer.getHeight();
        int newWidth = (int) Math.round(smartObjectLayer.getWidth() * scale);

        PsdImage innerImage = new PsdImage(newWidth, newHeight);
        innerImage.setResolution(72, 72);

        Stream innerStream = new FileStream(changeFile, FileMode.Open);
        Layer layer = new Layer(innerStream.toInputStream());
        layer.setHorizontalResolution(72);
        layer.setVerticalResolution(72);

        try {
            innerImage.addLayer(layer);

            smartObjectLayer.replaceContents(innerImage);
            smartObjectLayer.updateModifiedContent();

            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            psdImage.save(outputFile, pngOptions);
        } finally {
            innerImage.dispose();
            innerStream.dispose();
            layer.dispose();
        }
    }
{{< /highlight >}}

**PSDJAVA-513. Agregar la capacidad de obtener la posición real de la izquierda y arriba de LayerGroup**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/layerGroupFigures.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        Layer[] layers = image.getLayers();

        for (int i = 0; i < layers.length; i++) {
            Layer layer = layers[i];

            if (layer instanceof LayerGroup) {
                {
                    // Obteniendo el LayerGroup.
                    LayerGroup group = (LayerGroup) layer;

                    int expectedLeft = Integer.MAX_VALUE;
                    int expectedTop = Integer.MAX_VALUE;
                    int expectedRight = 0;
                    int expectedBottom = 0;

                    // Calculando las posiciones reales de la izquierda, arriba, derecha y abajo.
                    for (Layer innerLayer : group.getLayers()) {
                        if (innerLayer instanceof AdjustmentLayer || innerLayer.getBounds().isEmpty()) {
                            continue;
                        }

                        expectedLeft = Math.min(expectedLeft, innerLayer.getLeft());
                        expectedTop = Math.min(expectedTop, innerLayer.getTop());
                        expectedRight = Math.max((expectedLeft + group.getWidth()), (innerLayer.getLeft() + innerLayer.getWidth()));
                        expectedBottom = Math.max((expectedTop + group.getHeight()), (innerLayer.getTop() + innerLayer.getHeight()));
                    }

                    // Las posiciones de la izquierda, arriba, derecha y abajo del LayerGroup se calculan correctamente ahora.
                    assertAreEqual(group.getLeft(), expectedLeft);
                    assertAreEqual(group.getTop(), expectedTop);
                    assertAreEqual(group.getRight(), expectedRight);
                    assertAreEqual(group.getBottom(), expectedBottom);
                }
            }
        }
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Los objetos no son iguales.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-514. La redimensión de la capa funciona incorrectamente cuando el archivo psd tiene VogkResource con estructuras en puntos**

{{< highlight java >}}
public static void main(String[] args) {
    String[] sourceFiles = new String[]
            {
                    "src/main/resources/PointsVectorOrigin.psd",
                    "src/main/resources/TopVogkResStruct.psd"
            };

    for (String sourceFile : sourceFiles) {
        try (PsdImage image = (PsdImage)Image.load(sourceFile))
        {
            Layer layer = image.getLayers()[0];

            layer.resize(50, 50);

            assertAreEqual(layer.getHeight(), 50);
