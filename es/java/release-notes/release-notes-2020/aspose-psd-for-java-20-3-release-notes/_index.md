---
title: Notas de la versión Aspose.PSD para Java 20.3
type: docs
weight: 10
url: /es/java/aspose-psd-para-java-20-3-notas-de-la-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión para [Aspose.PSD para Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-133|Convertir archivos de Adobe Illustrator en PDF|Característica|
|PSDJAVA-134|Agregar la capacidad de representar diferentes estilos en una capa de texto|Característica|
|PSDJAVA-135|Soporte de Capa de Ajuste en Blanco y Negro|Característica|
|PSDJAVA-137|Agregar soporte para exportar formato AI (Versión 8) a otros formatos|Característica|
|PSDJAVA-138|Soporte del modo de mezcla "PassThrough" (Solo utilizado para Grupos de Capas)|Característica|
|PSDJAVA-136|Excepción: Falla al cargar la imagen al cargar una imagen con Recurso de Nombres Alfa Unicode vacío|Error|
|PSDJAVA-139|Salida incorrecta después de cambiar la visibilidad de un Grupo de Capas|Error|
|PSDJAVA-140|Excepción al cargar la imagen PSD: La sección de color (Recurso de Sombra Paralela) debe contener 3 componentes de color para RGB o 4 componentes de color para CMYK|Error|
|PSDJAVA-141|Excepción si se intenta dibujar en una capa recién creada si se utiliza la versión simple del Constructor|Error|
# **Cambios en la API pública**
# **APIs añadidas:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **APIs eliminadas:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Ejemplos de uso:**
**PSDJAVA-133. Convertir archivos de Adobe Illustrator en PDF**

{{< highlight java >}}

 String inFile = "rect2_color.ai";

String outFile = "rect2_color.ai_output.pdf";

AiImage aiImage = (AiImage)Image.load(inFile);

try

{

    aiImage.save(outFile, new PdfOptions());

}

finally

{

    aiImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-134. Agregar la capacidad de representar diferentes estilos en una capa de texto**

{{< highlight java >}}

 String inFilePath = "text212.psd";

String outFilePath = "Output_text212.psd";

PsdImage image = (PsdImage)Image.load(inFilePath);

try

{

    TextLayer textLayer = (TextLayer)image.getLayers()[1];

    IText textData = textLayer.getTextData();

    ITextStyle defaultStyle = textData.producePortion().getStyle();

    ITextParagraph defaultParagraph = textData.producePortion().getParagraph();

    defaultStyle.setFillColor(Color.getDimGray());

    defaultStyle.setFontSize(51);

    textData.getItems()[1].getStyle().setStrikethrough(true);

    ITextPortion[] newPortions = textData.producePortions(new String[] { "E=mc",  "2\r",  "Negrita",  "Cursiva\r",  "Texto en minúsculas" }, defaultStyle, defaultParagraph);

    newPortions[0].getStyle().setUnderline(true); // editar estilo de texto "E=mc"

    newPortions[1].getStyle().setFontBaseline(FontBaseline.Superscript); // editar estilo de texto "2\r"

    newPortions[2].getStyle().setFauxBold(true); // editar estilo de texto "Negrita"

    newPortions[3].getStyle().setFauxItalic(true); // editar estilo de texto "Cursiva\r"

    newPortions[3].getStyle().setBaselineShift(-25); // editar estilo de texto "Cursiva\r"

    newPortions[4].getStyle().setFontCaps(FontCaps.SmallCaps); // editar estilo de texto "Texto en minúsculas"

    for (ITextPortion newPortion : newPortions)

    {

        textData.addPortion(newPortion);

    }

    textData.updateLayerData();

    image.save(outFilePath);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-135. Soporte de Capa de Ajuste en Blanco y Negro**

{{< highlight java >}}

 // Ejemplo del soporte para agregar la capa de ajuste en blanco y negro en tiempo de ejecución.

String inFileName = "Stripes.psd";

String outFileName = "Salida" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer nuevaCapa = image.addBlackWhiteAdjustmentLayer();

    nuevaCapa.setName("CapaAjusteBlancoYNegro");

    nuevaCapa.setRojos(22);

    nuevaCapa.setAmarillos(92);

    nuevaCapa.setVerdes(70);

    nuevaCapa.setCianos(79);

    nuevaCapa.setAzules(7);

    nuevaCapa.setMagentas(28);

    image.save(outFileName, new PsdOptions());

}

finally

{

    image.dispose();

}

// Ejemplo del soporte de la capa de ajuste en blanco y negro.

inFileName = "BlackWhiteAdjustmentLayerStripesMask.psd";

outFileName = "Salida" + inFileName;

PsdImage image1 = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer capaBlwh = (BlackWhiteAdjustmentLayer)image1.getLayers()[1];

    capaBlwh.setRojos(15);

    capaBlwh.setAmarillos(25);

    capaBlwh.setVerdes(35);

    capaBlwh.setCianos(10);

    capaBlwh.setAzules(50);

    capaBlwh.setMagentas(105);

    capaBlwh.setUsarTinte(true);

    capaBlwh.setBwPresetKind(4);

    capaBlwh.setBlackAndWhitePresetFileName("bwPresetFileName");

    capaBlwh.setTinteColorRojo(60);

    capaBlwh.setTinteColorVerde(80);

    capaBlwh.setTinteColorAzul(200);

    image1.save(outFileName, new PsdOptions());

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-137. Agregar soporte para exportar formato AI (Versión 8) a otros formatos**

{{< highlight java >}}

 // Ejemplo de exportar un archivo AI a los formatos PSD y PNG

String inFileName = "form_8.ai";

String outFileNamePrefijo = "form_8_export";

AiImage image = (AiImage)Image.load(inFileName);

try

{

    image.save(outFileNamePrefijo + ".psd", new PsdOptions());

    PngOptions opcionesPng = new PngOptions();

    opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

    image.save(outFileNamePrefijo + ".png", opcionesPng);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-138. Soporte del modo de mezcla "PassThrough" (Usado solo para Grupos de Capas)**

{{< highlight java >}}

 class LocalScope

{

    void assertIsTrue(boolean condicion, String mensaje)

    {

        if (!condicion)

        {

            throw new FormatException(mensaje);

        }

    }

}

LocalScope localScope = new LocalScope();

String inFileName = "Apple.psd";

String outFileName = "Salida" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    localScope.assertIsTrue(image.getLayers().length >= 23, "No hay una 23ª capa.");

    LayerGroup capa = (LayerGroup)image.getLayers()[23];

    localScope.assertIsTrue(capa != null, "La 23ª capa no es un grupo de capas.");

    localScope.assertIsTrue(capa.getNombre().equals("GrupoAjuste"), "El nombre de la 23ª capa no es 'GrupoAjuste'.");

    localScope.assertIsTrue(capa.getBlendModeKey() == BlendMode.PassThrough, "La capa de grupo de ajuste debería tener el modo de mezcla 'PassThrough'.");

    image.save(outFileName, new PsdOptions());

    PngOptions opcionesPng = new PngOptions();

    opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("SalidaApple.png", opcionesPng);

    capa.setBlendModeKey(BlendMode.Normal);

    image.save("Normal" + outFileName, new PsdOptions());

    PngOptions opcionesPng1 = new PngOptions();

    opcionesPng1.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("NormalSalidaApple.png", opcionesPng1);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Excepción: Falla al cargar la imagen al cargar una imagen con Recurso de Nombres Alfa Unicode vacío**

{{< highlight java >}}

 String inFilePath = "apple.psd";

PsdImage imagenPsd = null;

try

{

    // Aquí no deberíamos obtener excepciones

    imagenPsd = (PsdImage)Image.load(inFilePath);

}

finally

{

    if (imagenPsd != null) imagenPsd.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Salida incorrecta después de cambiar la visibilidad de un Grupo de Capas**

{{< highlight java >}}

 String inFileName = "input.psd";

String outFileName = "output.psd";

// Realizar cambios en los nombres de las capas y guardarlos

PsdImage imagen = (PsdImage)Image.load(inFileName);

try

{

    for (int i = 0; i < imagen.getLayers().length; i++)

    {

        Layer capa = imagen.getLayers()[i];

        // Apagar todo dentro de un grupo

        if (capa instanceof LayerGroup)

        {

            capa.setVisible(false);

        }

    }

    imagen.save(outFileName);

}

finally

{

    imagen.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. Excepción al cargar la imagen PSD: La sección de color (Recurso de Sombra Paralela) debe contener 3 componentes de color para RGB o 4 componentes de color para CMYK**

{{< highlight java >}}

 String inFilePath = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

PsdImage imagen = null;

try

{

    imagen = (PsdImage)PsdImage.load(inFilePath);

}

finally

{

    if (imagen != null) imagen.dispose();

}       

{{< /highlight >}}

**PSDJAVA-141. Excepción si se intenta dibujar en una capa recién creada si se utiliza la versión simple del Constructor**

{{< highlight java >}}

 String outputFile = "output.psd";

int ancho = 100;

int alto = 100;

PsdImage imagen = new PsdImage(ancho, alto);

try

{

    Layer capa = new Layer();

    capa.setBottom(alto);

    capa.setRight(ancho);

    imagen.addLayer(capa);

    Graphics grafico = new Graphics(capa);

    grafico.clear(Color.getYellow());

    // dibujar un rectángulo con la herramienta de Pluma

    grafico.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

    // dibujar otro rectángulo con un Pincel Sólido en color Azul

    grafico.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));

    imagen.save(outputFile);

}

finally

{

    imagen.dispose();

}

{{< /highlight >}}