---
title: Notas de Lançamento do Aspose.PSD para Java 20.3
type: docs
weight: 10
url: /pt/java/aspose-psd-for-java-20-3-release-notes/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para [Aspose.PSD para Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-133|Converter arquivos do Adobe Illustrator em PDFs|Recurso|
|PSDJAVA-134|Adicionar capacidade de renderizar estilos diferentes em uma camada de texto|Recurso|
|PSDJAVA-135|Suporte à Camada de Ajuste em Preto e Branco|Recurso|
|PSDJAVA-137|Adicionar suporte para exportar formato AI (Versão 8) para outros formatos|Recurso|
|PSDJAVA-138|Suporte ao processamento do Modo de Mistura PassThrough (Usado apenas para Grupo de Camadas).|Recurso|
|PSDJAVA-136|Exceção: Falha ao carregar imagem com recurso de Nomes Alpha Unicode vazios|Erro|
|PSDJAVA-139|Saída incorreta após alterar a visibilidade de um Grupo de Camadas|Erro|
|PSDJAVA-140|Exceção ao carregar imagem PSD: A seção de cor (Recurso Sombra) deve conter 3 componentes de cor para RGB ou 4 componentes de cor para CMYK|Erro|
|PSDJAVA-141|Exceção ao tentar desenhar em uma camada recém-criada se a versão simples do Construtor for usada|Erro|
# **Mudanças na API Pública**
# **APIs Adicionadas:**
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
## **APIs Removidas:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Exemplos de Uso:**
**PSDJAVA-133. Converter arquivos do Adobe Illustrator em PDFs**

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

**PSDJAVA-134. Adicionar capacidade para renderizar estilos diferentes em uma camada de texto**

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

    ITextPortion[] newPortions = textData.producePortions(new String[] { "E=mc",  "2\r",  "Negrito",  "Itálico\r",  "Texto em minúsculas" }, defaultStyle, defaultParagraph);

    newPortions[0].getStyle().setUnderline(true); // editar estilo de texto "E=mc"

    newPortions[1].getStyle().setFontBaseline(FontBaseline.Superscript); // editar estilo de texto "2\r"

    newPortions[2].getStyle().setFauxBold(true); // editar estilo de texto "Negrito"

    newPortions[3].getStyle().setFauxItalic(true); // editar estilo de texto "Itálico\r"

    newPortions[3].getStyle().setBaselineShift(-25); // editar estilo de texto "Itálico\r"

    newPortions[4].getStyle().setFontCaps(FontCaps.SmallCaps); // editar estilo de texto "Texto em minúsculas"

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

**PSDJAVA-135. Suporte à Camada de Ajuste em Preto e Branco**

{{< highlight java >}}

 // Exemplo do suporte de adicionar a camada de ajuste em preto e branco em tempo de execução.

String inFileName = "Stripes.psd";

String outFileName = "Saída" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer newLayer = image.addBlackWhiteAdjustmentLayer();

    newLayer.setName("CamadaAjustePretoBranco");

    newLayer.setVermelhos(22);

    newLayer.setAmarelos(92);

    newLayer.setVerdes(70);

    newLayer.setCianos(79);

    newLayer.setAzuis(7);

    newLayer.setMagentas(28);

    image.save(outFileName, new PsdOptions());

}

finally

{

    image.dispose();

}

// Exemplo do suporte da camada de ajuste em preto e branco.

inFileName = "MáscaraStripesCamadaAjustePretoBranco.psd";

outFileName = "Saída" + inFileName;

PsdImage image1 = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer blwhLayer = (BlackWhiteAdjustmentLayer)image1.getLayers()[1];

    blwhLayer.setVermelhos(15);

    blwhLayer.setAmarelos(25);

    blwhLayer.setVerdes(35);

    blwhLayer.setCianos(10);

    blwhLayer.setAzuis(50);

    blwhLayer.setMagentas(105);

    blwhLayer.setUseTint(true);

    blwhLayer.setBwPresetKind(4);

    blwhLayer.setBlackAndWhitePresetFileName("NomeArquivoPresetPB");

    blwhLayer.setTintCorVermelho(60);

    blwhLayer.setTintCorVerde(80);

    blwhLayer.setTintCorAzul(200);

    image1.save(outFileName, new PsdOptions());

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-137. Adicionar suporte para exportar formato AI (Versão 8) para outros formatos**

{{< highlight java >}}

 // Exemplo da exportação de arquivo AI para os formatos PSD e PNG

String inFileName = "form_8.ai";

String outFileNamePrefix = "form_8_export";

AiImage image = (AiImage)Image.load(inFileName);

try

{

    image.save(outFileNamePrefix + ".psd", new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save(outFileNamePrefix + ".png", pngOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-138. Suporte ao processamento do Modo de Mistura PassThrough (Usado apenas para Grupo de Camadas).**

{{< highlight java >}}

 class EscopoLocal

{

    void assertIsTrue(boolean condition, String message)

    {

        if (!condition)

        {

            throw new FormatException(message);

        }

    }

}

EscopoLocal escopoLocal = new EscopoLocal();

String inFileName = "Apple.psd";

String outFileName = "Saída" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    escopoLocal.assertIsTrue(image.getLayers().length >= 23, "Não existe a 23ª camada.");

    LayerGroup camada = (LayerGroup)image.getLayers()[23];

    escopoLocal.assertIsTrue(camada != null, "A 23ª camada não é um grupo de camadas.");

    escopoLocal.assertIsTrue(camada.getName().equals("GrupoAjuste"), "O nome da 23ª camada não é 'GrupoAjuste'.");

    escopoLocal.assertIsTrue(camada.getBlendModeKey() == BlendMode.PassThrough, "A camada de GrupoAjuste deve ter o modo de mistura 'pass through'.");

    image.save(outFileName, new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("SaídaApple.png", pngOptions);

    camada.setBlendModeKey(BlendMode.Normal);

    image.save("Normal" + outFileName, new PsdOptions());

    PngOptions pngOptions1 = new PngOptions();

    pngOptions1.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("NormalSaídaApple.png", pngOptions1);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Exceção: Falha ao carregar imagem com recurso de Nomes Alpha Unicode vazios**

{{< highlight java >}}

 String inFilePath = "apple.psd";

PsdImage psdImage = null;

try

{

    // Aqui não devemos obter exceções

    psdImage = (PsdImage)Image.load(inFilePath);

}

finally

{

    if (psdImage != null) psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Saída incorreta após alterar a visibilidade de um Grupo de Camadas**

{{< highlight java >}}

 String inFileName = "entrada.psd";

String outFileName = "saída.psd";

// Fazer alterações nos nomes das camadas e salvar

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    for (int i = 0; i < image.getLayers().length; i++)

    {

        Layer camada = image.getLayers()[i];

        // Desligar tudo dentro de um grupo

        if (camada instanceof LayerGroup)

        {

            camada.setVisible(false);

        }

    }

    image.save(outFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. Exceção ao carregar imagem PSD: A seção de cor (Recurso Sombra) deve conter 3 componentes de cor para RGB ou 4 componentes de cor para CMYK**

{{< highlight java >}}

 String inFilePath = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

PsdImage image = null;

try

{

    image = (PsdImage)PsdImage.load(inFilePath);

}

finally

{

    if (image != null) image.dispose();

}       

{{< /highlight >}}

**PSDJAVA-141. Exceção ao tentar desenhar em uma camada recém-criada se a versão simples do Construtor for usada**

{{< highlight java >}}

 String outputFile = "saída.psd";

int largura = 100;

int altura = 100;

PsdImage image = new PsdImage(largura, altura);

try

{

    Layer camada = new Layer();

    camada.setBottom(altura);

    camada.setRight(largura);

    image.addLayer(camada);

    Graphics grafico = new Graphics(camada);

    grafico.clear(Color.getAmarelo());

    // desenhar um retângulo com a ferramenta Caneta

    grafico.drawRectangle(new Pen(Color.getVermelho()), new Rectangle(30, 10, 40, 80));

    // desenhar outro retângulo com Pincel Sólido na cor Azul

    grafico.drawRectangle(new Pen(new SolidBrush(Color.getAzul())), new Rectangle(10, 30, 80, 40));

    image.save(outputFile);

}

finally

{

    image.dispose();

}

{{< /highlight >}}