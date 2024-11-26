---
title: Aspose.PSD para Java 20.5 - Notas de Lançamento
type: docs
weight: 40
url: /pt/java/aspose-psd-para-java-20-5-notas-de-lancamento/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para [Aspose.PSD para Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

| **Chave** | **Resumo** | **Categoria** |
| :- | :- | :- |
|PSDJAVA-188|Suporte para progresso de conversão de documento|Recurso|
|PSDJAVA-197|Suporte para salvar imagem PSD de modo de cor escala de cinza com 16 bits por canal|Recurso|
|PSDJAVA-198|Suporte para Recurso de Camada de Ajuste de Inversão Nvrt|Recurso|
|PSDJAVA-200|Suporte de Máscaras de Camada para Grupos de Camadas|Recurso|
|PSDJAVA-195|Correção ao salvar imagem PSD com modo de cor escala de cinza de 16 bits por canal para formato PSD de 16 bits por canal RGB|Erro|
|PSDJAVA-196|Correção ao salvar imagem PSD com modo de cor escala de cinza de 16 bits por canal para formato PSD de 8 bits por canal escala de cinza|Erro|
|PSDJAVA-199|Alinhamento de texto através de ITextPortion não funciona para idiomas da direita para a esquerda. O arquivo de saída fica danificado.|Erro|
|PSDJAVA-201|Exceção ao tentar abrir arquivo Psd específico com Cor Lab e 8 bits/canal|Erro|
# **Alterações na API Pública**
# **APIs Adicionadas:**
- Nenhuma
## **APIs Removidas:**
- Nenhuma
# **Exemplos de Uso:**

**PSDJAVA-188. Suporte para progresso de conversão de documento**

{{< highlight java >}}

 // Um exemplo de uso do manipulador de progresso para operações de carregamento e salvamento.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Cria um manipulador de progresso que escreve informações de progresso no console

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s de %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Carregando Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Vincula o manipulador de progresso para mostrar o progresso do carregamento

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Carrega o PSD usando opções de carregamento específicas

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Salvando Apple.psd em formato PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Torna a imagem de saída colorida e não transparente

    pngOptions.setColorType(PngColorType.Truecolor);

    // Vincula o manipulador de progresso para mostrar o progresso do salvamento

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Converte o PSD para PNG com características específicas

    image.save(outputStream, pngOptions);

    System.out.println("---------- Salvando Apple.psd em formato PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Torna o PSD de saída colorido

    psdOptions.setColorMode(ColorModes.Rgb);

    // Define um canal para cada cor (vermelho, verde e azul) mais um canal composto

    psdOptions.setChannelsCount((short)4);

    // Vincula o manipulador de progresso para mostrar o progresso do salvamento

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Salva uma cópia do PSD com características específicas

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Suporte para salvar imagem PSD de modo de cor escala de cinza com 16 bits por canal**

{{< highlight java >}}

 // Um exemplo de aplicação de diferentes combinações de modos de cor, bits por canal, contagens

// de canais e compressões para camadas específicas.

// Faz com que um método seja acessível a partir do escopo local

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String arquivo,

            short modoCor,

            short contagemBitsCanal,

            short contagemCanales,

            short compressão,

            int númeroCamada)

    {

        String caminhoArquivo = arquivo + ".psd";

        String sufixo = Enum.getName(ColorModes.class, modoCor) + contagemBitsCanal + "_" +

                contagemCanales + "_" + Enum.getName(CompressionMethod.class, compressão);

        String caminhoExportação = arquivo + sufixo + ".psd";

        String caminhoExportaçãoPng = arquivo + sufixo + ".png";

        // Carrega um PSD pré-definido de escala de cinza de 16 bits

        PsdImage imagem = (PsdImage)Image.load(caminhoArquivo);

        try

        {

            RasterCachedImage raster = númeroCamada >= 0 ? imagem.getLayers()[númeroCamada] : imagem;

            // Desenha uma borda interna cinza ao redor do perímetro da camada

            Graphics graphics = new Graphics(raster);

            int largura = raster.getWidth();

            int altura = raster.getHeight();

            Rectangle rect = new Rectangle(

                    largura / 3,

                    altura / 3,

                    largura - (2 * (largura / 3)) - 1,

                    altura - (2 * (altura / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Salva uma cópia do PSD com características específicas

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(modoCor);

            psdOptions.setChannelBitsCount(contagemBitsCanal);

            psdOptions.setChannelsCount(contagemCanales);

            psdOptions.setCompressionMethod(compressão);

            imagem.save(caminhoExportação, psdOptions);

        }

        finally

        {

            imagem.dispose();

        }

        // Carrega o PSD salvo

        PsdImage imagem1 = (PsdImage)Image.load(caminhoExportação);

        try

        {

            // Converte o PSD salvo em uma imagem PNG em escala de cinza

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            imagem1.save(caminhoExportaçãoPng, pngOptions); // aqui não deve haver exceção

        }

        finally

        {

            imagem1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("escalaDeCinza5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bits_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bits_5x5_sem_camadas", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bits_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bits_5x5_sem_camadas", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bits_5x5_sem_camadas", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("índice8bits_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Suporte para Recurso de Camada de Ajuste de Inversão Nvrt**

{{< highlight java >}}

 // Um exemplo de encontrar o Recurso Nvrt de uma camada de ajuste de inversão.

String caminhoArquivoPsd = "CamadaDeAjusteDeInversão.psd";

NvrtResource recursoNvrt = null;

// Carrega um PSD pré-definido contendo uma camada de ajuste de inversão

PsdImage imagemPsd = (PsdImage)Image.load(caminhoArquivoPsd);

try

{

    // Tenta encontrar um recurso da camada de ajuste de inversão

    for (Layer camada : imagemPsd.getLayers())

    {

        if (camada instanceof InvertAdjustmentLayer)

        {

            for (LayerResource recursoCamada : camada.getResources())

            {

                if (recursoCamada instanceof NvrtResource)

                {

                    // O Recurso Nvrt é encontrado

                    recursoNvrt = (NvrtResource)recursoCamada;

                    break;

                }

            }

        }

    }

}

finally

{

    imagemPsd.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Suporte de Máscaras de Camada para Grupos de Camadas**

{{< highlight java >}}

 // Um exemplo de suporte de máscaras de camada para grupos de camadas. O programa carrega e salva o PSD

// em diferentes formatos de saída sem lançar exceções.

String arquivoOrigem = "psdnet595.psd";

String saídaPng = "saída.png";

String saídaPsd = "saída.psd";

// Carrega um PSD pré-definido contendo máscaras de camada para grupos de camadas

PsdImage entrada = (PsdImage)Image.load(arquivoOrigem);

try

{

    // Converte o PSD carregado para PNG

    entrada.save(saídaPng, new PngOptions());

    // Salva uma cópia do PSD

    entrada.save(saídaPsd);

}

finally

{

    entrada.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Correção ao salvar imagem PSD com modo de cor escala de cinza de 16 bits por canal para formato PSD de 16 bits por canal RGB**

{{< highlight java >}}

 // Um exemplo de converter um PSD de escala de cinza de 16 bits para um PSD RGB de 16 bits e depois para

// escala de cinza de 16 bits, mas como uma imagem raster.

String caminhoArquivoOrigem = "escalaDeCinza5x5.psd";

String caminhoArquivoExportação = "saídaRGB16Bits5x5.psd";

String caminhoExportaçãoPng = "saídaRGB16Bits5x5.png";

// Carrega um PSD de escala de cinza de 16 bits pré-definido

PsdImage imagem = (PsdImage)Image.load(caminhoArquivoOrigem);

try

{

    RasterCachedImage raster = imagem.getLayers()[0];

    // Desenha uma borda interna cinza ao redor do perímetro da camada

    Graphics graphics = new Graphics(raster);

    int largura = raster.getWidth();

    int altura = raster.getHeight();

    Rectangle rect = new Rectangle(largura / 3, altura / 3, largura - (2 * (largura / 3)) - 1, altura - (2 * (altura / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Salva uma cópia do PSD com o modo de cor alterado para RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    imagem.save(caminhoArquivoExportação, psdOptions);

}

finally

{

    imagem.dispose();

}

// Carrega o PSD salvo

PsdImage imagem1 = (PsdImage)Image.load(caminhoArquivoExportação);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Converte o PSD salvo em uma imagem PNG em escala de cinza

    imagem1.save(caminhoExportaçãoPng, pngOptions); // aqui não deve haver exceção

}

finally

{

    imagem1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Correção ao salvar imagem PSD com modo de cor escala de cinza de 16 bits por canal para formato PSD de 8 bits por canal escala de cinza**

{{< highlight java >}}

 // Um exemplo de converter um PSD de escala de cinza de 16 bits para um de 8 bits e depois para

// uma imagem raster de 8 bits em escala de cinza.

String caminhoArquivoOrigem = "escalaDeCinza16Bits.psd";

String caminhoArquivoExportação = "saídaEscalaDeCinza16Bits.psd";

String caminhoExportaçãoPng = "saídaEscalaDeCinza16Bits.png";

// Carrega um PSD de escala de cinza de 16 bits pré-definido

PsdImage imagem = (PsdImage)Image.load(caminhoArquivoOrigem);

try

{

    RasterCachedImage raster = imagem.getLayers()[0];

    // Desenha uma borda interna cinza ao redor do perímetro da camada

    Graphics graphics = new Graphics(raster);

    int largura = raster.getWidth();

    int altura = raster.getHeight();

    Rectangle rect = new Rectangle(largura / 3, altura / 3, largura - (2 * (largura / 3)) - 1, altura - (2 * (altura / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Salva uma cópia do PSD com a contagem de canais alterada para 8 bits

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    imagem.save(caminhoArquivoExportação, psdOptions);

}

finally

{

    imagem.dispose();

}

// Carrega o PSD salvo

PsdImage imagem1 = (PsdImage)Image.load(caminhoArquivoExportação);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Converte o PSD salvo em uma imagem PNG em escala de cinza

    imagem1.save(caminhoExportaçãoPng, pngOptions); // aqui não deve haver exceção

}

finally

{

    imagem1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Alinhamento de Texto através de ITextPortion não funciona para idiomas da direita para a esquerda. O arquivo de saída fica danificado.**

{{< highlight java >}}

 // Um exemplo de alinhar uma camada de texto RTL através de ITextPortion. O programa modifica

// uma camada de texto RTL existente em um PSD carregado e salva uma cópia do documento modificado.

String nomeArquivoOrigem = "bidi.psd";

String nomeArquivoSaida = "bidiSaida.psd";

// Carrega um PSD pré-definido contendo uma camada de texto RTL

PsdImage imagem = (PsdImage)Image.load(nomeArquivoOrigem);

try

{

    // Obtém porções de texto da camada

    TextLayer camada = (TextLayer)imagem.getLayers()[2];

    ITextPortion[] porções = camada.getTextData().getItems();

    // Altera o alinhamento do texto

    porções[0].getParagraph().setJustification(2);

    // Aplica alterações à camada

    camada.getTextData().updateLayerData();

    // Salva uma cópia modificada do PSD

    imagem.save(nomeArquivoSaida);

}

finally

{

    imagem.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Exceção ao tentar abrir arquivo Psd específico com Cor Lab e 8 bits/canal**

{{< highlight java >}}

 // Um exemplo de suporte a documento Photoshop de 8 bits no modo de cor LAB.

String arquivoOrigem = "SemTítulo-1.psd";

String arquivoSaídaPsd = "saída.psd";

// Carrega um PSD de 8 bits específico no modo de cor LAB

PsdImage imagemPsd = (PsdImage)Image.load(arquivoOrigem);

try

{

    // Salva uma cópia do PSD carregado

    imagemPsd.save(arquivoSaídaPsd);

}

finally

{

    imagemPsd.dispose();

}

{{< /highlight >}}