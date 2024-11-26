---
title: Aspose.PSD para .NET 20.5 - Notas de Lançamento
type: docs
weight: 80
url: /pt/net/aspose-psd-for-net-20-5-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-595|Suporte a Máscaras de Camada para Grupos de Camadas|Recurso|
|PSDNET-201|Suporte ao progresso de conversão de documento|Recurso|
|PSDNET-275|Suporte ao Recurso Nvrt (Recurso de Camada de Ajuste Inverter)|Recurso|
|PSDNET-124|Suporte ao salvamento de Imagem PSD em Modo de Cor Grayscale com 16 bits por canal|Recurso|
|PSDNET-589|Refatoração de Exemplos no GitHub|Melhoria|
|PSDNET-587|Alinhamento de Texto através do ITextPortion não funciona para idiomas da direita para a esquerda. O arquivo de saída fica danificado.|Erro|
|PSDNET-604|Exceção ao tentar abrir um arquivo Psd específico com Cor Lab e 8 bits/canal|Erro|
|PSDNET-598|Correção ao salvar imagem PSD com Cor Grayscale de 16 bits por canal para formato PSD Grayscale de 8 bits por canal|Erro|
|PSDNET-599|Correção ao salvar imagem PSD com Cor Grayscale de 16 bits por canal para formato PSD RGB de 16 bits por canal|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- Nenhuma
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-595. Suporte a Máscaras de Camada para Grupos de Camadas**

{{< highlight java >}}

 string arquivoFonte = "psdnet595.psd";

string saidaPng = "saida.png";

string saidaPsd = "saida.psd";

using (var entrada = (PsdImage)Image.Load(arquivoFonte))

{

     entrada.Save(saidaPng, new PngOptions());

     entrada.Save(saidaPsd);

}

{{< /highlight >}}

**PSDNET-201. Suporte ao progresso de conversão de documento**

{{< highlight java >}}

 string caminhoArquivoFonte = "Apple.psd";

Stream fluxoSaida = new MemoryStream();

ProgressEventHandler manipuladorProgressoLocal = delegate(ProgressEventHandlerInfo informacaoProgresso)

{

      string mensagem = string.Format(

           "{0} {1}: {2} de {3}",

           informacaoProgresso.Descrição,

           informacaoProgresso.TipoEvento,

           informacaoProgresso.Valor,

           informacaoProgresso.ValorMáximo);

      Console.WriteLine(mensagem);

};

Console.WriteLine("---------- Carregando Apple.psd ----------");

var opçõesCarregamento = new PsdLoadOptions() { ProgressEventHandler = manipuladorProgressoLocal };

using (PsdImage imagem = (PsdImage)Image.Load(caminhoArquivoFonte, opçõesCarregamento))

{

      Console.WriteLine("---------- Salvando Apple.psd no formato PNG ----------");

      imagem.Save(

           fluxoSaida,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = manipuladorProgressoLocal

           });

      Console.WriteLine("---------- Salvando Apple.psd no formato PSD ----------");

      imagem.Save(

           fluxoSaida,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = manipuladorProgressoLocal

           });

}

{{< /highlight >}}

**PSDNET-275. Suporte ao Recurso Nvrt (Recurso de Camada de Ajuste Inverter)**

{{< highlight java >}}

 using (var imagemPsd = (PsdImage)Image.Load("InvertAdjustmentLayer.psd"))

{

      foreach (var camada in imagemPsd.Layers)

      {

           if (camada is InvertAdjustmentLayer)

           {

                 foreach (var recursoCamada in camada.Resources)

                 {

                      if (recursoCamada is NvrtResource)

                      {

                           // O NvrtResource é suportado.

                           var recurso = (NvrtResource)recursoCamada;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. Correção ao salvar imagem PSD com Cor Grayscale de 16 bits por canal para formato PSD Grayscale de 8 bits por canal**

{{< highlight java >}}

 void SalvarParaPsdDepoisCarregarESalvarParaPng(

    string arquivo,

    ColorModes modoCor,

    short qtdBitsCanal,

    short qtdCanales,

    CompressionMethod compressão,

    int númeroCamada)

{

    string caminhoArquivo = arquivo + ".psd";

    string posfixo = modoCor.ToString() + qtdBitsCanal + "_" + qtdCanales + "_" + compressão;

    string caminhoExportação = @"Saida\" + arquivo + posfixo + ".psd";

    PsdOptions opçõesPsd = new PsdOptions()

    {

        ColorMode = modoCor,

        ChannelBitsCount = qtdBitsCanal,

        ChannelsCount = qtdCanales,

        CompressionMethod = compressão

    };

    using (PsdImage imagem = (PsdImage)Image.Load(caminhoArquivo))

    {

        RasterCachedImage raster = númeroCamada >= 0 ? (RasterCachedImage)imagem.Layers[númeroCamada] : imagem;

        Aspose.PSD.Graphics gráficos = new Graphics(raster);

        int largura = raster.Width;

        int altura = raster.Height;

        Rectangle retângulo = new Rectangle(

            largura / 3,

            altura / 3,

            largura - (2 * (largura / 3)) - 1,

            altura - (2 * (altura / 3)) - 1);

        gráficos.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), retângulo);

        imagem.Save(caminhoExportação, opçõesPsd);

    }

    string caminhoExportarPng = Path.ChangeExtension(caminhoExportação, "png");

    using (PsdImage imagem = (PsdImage)Image.Load(caminhoExportação))

    {

        // Aqui não deve ocorrer exceção.

        imagem.Save(caminhoExportarPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

    }

}

SalvarParaPsdDepoisCarregarESalvarParaPng("grayscale5x5", ColorModes.Cmyk, 16, 5, CompressionMethod.RLE, 0);

SalvarParaPsdDepoisCarregarESalvarParaPng("argb16bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SalvarParaPsdDepoisCarregarESalvarParaPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SalvarParaPsdDepoisCarregarESalvarParaPng("argb8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

SalvarParaPsdDepoisCarregarESalvarParaPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SalvarParaPsdDepoisCarregarESalvarParaPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

SalvarParaPsdDepoisCarregarESalvarParaPng("index8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDNET-587. Alinhamento de Texto através do ITextPortion não funciona para idiomas da direita para a esquerda. O arquivo de saída fica danificado.**

{{< highlight java >}}

 string nomeArquivoFonte = "bidi.psd";

string nomeArquivoSaida = "bidiSaida.psd";

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

{

    var camada = (TextLayer)imagem.Layers[2];

    var porções = camada.TextData.Items;

    porções[0].Paragraph.Justificação = 2;

    camada.TextData.UpdateLayerData();

    imagem.Save(nomeArquivoSaida);

}

{{< /highlight >}}

` `**PSDNET-604. Exceção ao tentar abrir um arquivo Psd específico com Cor Lab e 8 bits/canal**

{{< highlight java >}}

 string arquivoFonte = "Untitled-1.psd";

string arquivoSaidaPsd = "saida.psd";

using (var imagemPsd = (PsdImage)Image.Load(arquivoFonte))

{

    imagemPsd.Save(arquivoSaidaPsd);

}

// Arquivo LAB carregado e salvo sem lançar exceções.

{{< /highlight >}}

**PSDNET-598. Correção ao salvar imagem PSD com Cor Grayscale de 16 bits por canal para formato PSD Grayscale de 8 bits por canal**

{{< highlight java >}}

 string nomeArquivoFonte = "grayscale16bit.psd";

string nomeArquivoExportação = "grayscale16bit_saida.psd";

PsdOptions opçõesPsd = new PsdOptions()

{

    ColorMode = ColorModes.Grayscale,

    ChannelBitsCount = 8,

    ChannelsCount = 2

};

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

{

    RasterCachedImage raster = imagem.Layers[0];

    Aspose.PSD.Graphics gráficos = new Graphics(raster);

    int largura = raster.Width;

    int altura = raster.Height;

    Rectangle retângulo = new Rectangle(largura / 3, altura / 3, largura - (2 * (largura / 3)) - 1, altura - (2 * (altura / 3)) - 1);

    gráficos.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), retângulo);

    imagem.Save(nomeArquivoExportação, opçõesPsd);

}

string caminhoExportarPng = Path.ChangeExtension(nomeArquivoExportação, "png");

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoExportação))

{

    // Aqui não deve ocorrer exceção.

    imagem.Save(caminhoExportarPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

**PSDNET-599. Correção ao salvar imagem PSD com Cor Grayscale de 16 bits por canal para formato PSD RGB de 16 bits por canal**

{{< highlight java >}}

 string nomeArquivoFonte = "grayscale16bit.psd";

string nomeArquivoExportação = "grayscale16bit_saida.psd";

PsdOptions opçõesPsd = new PsdOptions()

{

    ColorMode = ColorModes.Rgb,

    ChannelBitsCount = 8,

    ChannelsCount = 4

};

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

{

    RasterCachedImage raster = imagem.Layers[0];

    Aspose.PSD.Graphics gráficos = new Graphics(raster);

    int largura = raster.Width;

    int altura = raster.Height;

    Rectangle retângulo = new Rectangle(largura / 3, altura / 3, largura - (2 * (largura / 3)) - 1, altura - (2 * (altura / 3)) - 1);

    gráficos.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), retângulo);

    imagem.Save(nomeArquivoExportação, opçõesPsd);

}

string caminhoExportarPng = Path.ChangeExtension(nomeArquivoExportação, "png");

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoExportação))

{

    // Aqui não deve ocorrer exceção.

    imagem.Save(caminhoExportarPng, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}
