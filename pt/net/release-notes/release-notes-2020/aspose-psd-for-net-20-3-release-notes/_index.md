---
title: Notas de Lançamento Aspose.PSD para .NET 20.3
type: docs
weight: 100
url: /pt/net/aspose-psd-para-net-20-3-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-188|Suporte ao .Net Core|Recurso|
|PSDNET-523|Converter arquivos do Adobe Illustrator em PDFs|Recurso|
|PSDNET-212|Adicionar capacidade de renderizar estilos diferentes em uma camada de texto|Recurso|
|PSDNET-144|Suporte à camada de ajuste Preto e Branco|Recurso|
|PSDNET-233|Adicionar suporte para exportar AI formato (Versão 8) para outros formatos|Recurso|
|PSDNET-540|Suporte ao processamento do Modo de Mistura PassThrough (usado apenas para Grupo de Camadas)|Recurso|
|PSDNET-539|Exceção: Falha ao carregar imagem com Recurso de Nomes Alfa Unicode vazios|Erro|
|PSDNET-541|Saída incorreta após alterar visibilidade de um Grupo de Camadas|Erro|
|PSDNET-516|Exceção ao carregar imagem PSD: a seção de cor (Recurso de Sombra Projetada) deve conter 3 componentes de cor para RGB ou 4 componentes de cor para CMYK|Erro|
|PSDNET-536|Exceção ao tentar desenhar em uma camada recém-criada se a versão simples do Construtor for usada|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Nenhum
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Sobreposição
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscrito
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.Nenhum
- F:Aspose.PSD.FileFormats.Psd.FontCaps.MaiúsculasPequenas
- F:Aspose.PSD.FileFormats.Psd.FontCaps.TodasEmMaiúsculas
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AdicionarCamadaDeAjustePretoBranco
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Ausente
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NegritoForjado
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ItálicoForjado
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Sublinhado
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Riscado
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DeslocamentoBase
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProduzirPorções(Sistema.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-523. Converter arquivos do Adobe Illustrator em PDFs**

{{< highlight java >}}

 string arquivoFonte = "rect2_color.ai";

using (var imagemAi = (AiImage)Image.Load(arquivoFonte))

{

    imagemAi.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Adicionar capacidade de renderizar diferentes estilos em uma camada de texto**

{{< highlight java >}}

 string arquivoFonte = "texto212.psd";

string arquivoEthalon = "Ethalon_text212.psd";

string arquivoSaida = "Saída_text212.psd";

using (var img = (PsdImage)Image.Load(arquivoFonte))

{

    TextLayer camadaTexto = (TextLayer)img.Layers[1];

    IText dadosTexto = camadaTexto.TextData;

    ITextStyle estiloPadrao = dadosTexto.ProducePortion().Style;

    ITextParagraph paragrafoPadrao = dadosTexto.ProducePortion().Paragraph;

    estiloPadrao.FillColor = Color.DimGray;

    estiloPadrao.FontSize = 51;

    dadosTexto.Items[1].Style.Strikethrough = true;

    ITextPortion[] novasPorções = dadosTexto.ProducePortions(new string[] { "E=mc",  "2\r",  "Negrito",  "Itálico\r",  "TextoEmMinúsculas" }, estiloPadrao, paragrafoPadrao);

    novasPorções[0].Style.Underline = true; // editar estilo de texto "E=mc"

    novasPorções[1].Style.FontBaseline = FontBaseline.Sobreposição; // editar estilo de texto "2\r"

    novasPorções[2].Style.FauxBold = true; // editar estilo de texto "Negrito"

    novasPorções[3].Style.FauxItalic = true; // editar estilo de texto "Itálico\r"

    novasPorções[3].Style.BaselineShift = -25; // editar estilo de texto "Itálico\r"

    novasPorções[4].Style.FontCaps = FontCaps.MaiúsculasPequenas; // editar estilo de texto "TextoEmMinúsculas"

    foreach (var novaPorção in novasPorções)

    {

        dadosTexto.AddPortion(novaPorção);

    }

    dadosTexto.UpdateLayerData();

    img.Save(arquivoSaida);

}

{{< /highlight >}}

**PSDNET-233. Adicionar suporte para exportar AI formato (Versão 8) para outros formatos**

{{< highlight java >}}

 // Exemplo de exportação de arquivo AI para formatos PSD e PNG

string nomeArquivoFonte = "form_8.ai";

string nomeArquivoSaida = "form_8_export";

using (AiImage imagem = (AiImage)Image.Load(nomeArquivoFonte))

{

    imagem.Save(nomeArquivoSaida + ".psd", new PsdOptions());

    imagem.Save(nomeArquivoSaida + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Suporte ao processamento do Modo de Mistura PassThrough (usado apenas para Grupo de Camadas)**

{{< highlight java >}}

 void AssertIsTrue(bool condicao, string mensagem)

{

    if (!condicao)

    {

        throw new FormatException(mensagem);

    }

}

string nomeArquivoFonte = "Apple.psd";

string nomeArquivoSaida = "Saída" + nomeArquivoFonte;

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

{

    AssertIsTrue(imagem.Layers.Length >= 23, "Não existe a 23ª camada.");

    var camada = imagem.Layers[23] as LayerGroup;

    AssertIsTrue(camada != null, "A 23ª camada não é um grupo de camadas.");

    AssertIsTrue(camada.Name == "GrupoAjuste", "O nome da 23ª camada não é 'GrupoAjuste'.");

    AssertIsTrue(camada.BlendModeKey == BlendMode.PassThrough, "A camada GrupoAjuste deve ter o modo de mistura 'pass through'.");

    imagem.Save(nomeArquivoSaida, new PsdOptions());

    imagem.Save("SaídaApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    camada.BlendModeKey = BlendMode.Normal;

    imagem.Save("Normal" + nomeArquivoSaida, new PsdOptions());

    imagem.Save("NormalSaídaApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Atualizar texto em camada de texto gera exceção**

{{< highlight java >}}

 // Atualizar texto em camada de texto gera exceção

string caminhoArquivo = "FlipVertical.psd";

string caminhoSaida = "FlipVertical_alterado.psd";

var novoTexto = "Teste";

using (var imagem = Image.Load(caminhoArquivo))

{

    var psdImagem = imagem as PsdImage;

    if (imagem == null)

    {

        return;

    }

    var camadas = psdImagem.Layers;

    for (var indice = camadas.Length - 1; indice >= 0; indice--)

    {

        var camada = camadas[indice] as TextLayer;

        if (camada == null)

        {

            continue;

        }

        camada.UpdateText(novoTexto);

    }

    var opcoesImagem = new PsdOptions(psdImagem);

    psdImagem.Save(caminhoSaida, opcoesImagem);

}

{{< /highlight >}}

**PSDNET-182. Salvar imagem PSD após operação RotateFlip produz arquivo corrompido que não pode ser aberto.**

{{< highlight java >}}

 string nomeArquivoFonte = "1.psd";

RotateFlipType tipoFlip = RotateFlipType.Rotate270FlipXY;

string nomeArquivoSaidaPsd = "RotateFlipTest2617.psd";

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

{

    imagem.RotateFlip(tipoFlip);

    imagem.Save(nomeArquivoSaidaPsd);

}

// Deve ser executado sem exceções

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoSaidaPsd)) 

{

    // Não fazer nada

}

{{< /highlight >}}

**PSDNET-539. Exceção: Falha ao carregar imagem com Recurso de Nomes Alfa Unicode vazios**

{{< highlight java >}}

 string caminhoFonte = "apple.psd";

using (var psdImagem = (PsdImage)Image.Load(caminhoFonte)) // Aqui não devemos obter exceções

{

    // não fazer nada

}

{{< /highlight >}}

**PSDNET-541. Saída incorreta após alterar visibilidade de um Grupo de Camadas**

{{< highlight java >}}

 string arquivoFonte = "input.psd";

string arquivoSaida = "output.psd";

// fazer alterações nos nomes das camadas e salvar

using (var imagem = (PsdImage)Image.Load(arquivoFonte))

{

    for (int i = 0; i < imagem.Layers.Length; i++)

    {

        var camada = imagem.Layers[i];

        // Desligar tudo dentro de um grupo

        if (camada is LayerGroup)

        {

            camada.IsVisible = false;

        }

    }

    imagem.Save(arquivoSaida);

}

{{< /highlight >}}

**PSDNET-516. Exceção ao carregar imagem PSD: a seção de cor (Recurso de Sombra Projetada) deve conter 3 componentes de cor para RGB ou 4 componentes de cor para CMYK**

{{< highlight java >}}

 string arquivoFonte = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(arquivoFonte)) // Aqui não devemos obter exceções

{

    // não fazer nada

}

{{< /highlight >}}

**PSDNET-536. Exceção ao tentar desenhar em uma camada recém-criada se a versão simples do Construtor for usada**

{{< highlight java >}}

 string arquivoSaida = "output.psd";

int largura = 100;

int altura = 100;

using (var imagem = new PsdImage(largura, altura))

{

    var camada = new Layer();

    camada.Bottom = altura;

    camada.Right = largura;

    imagem.AddLayer(camada);

    Graphics grafico = new Graphics(camada);

    grafico.Clear(Color.Yellow);

    // desenhar um retângulo com a ferramenta Caneta

    grafico.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // desenhar outro retângulo com Pincel Sólido na cor Azul

    grafico.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    imagem.Save(arquivoSaida);

}

{{< /highlight >}}
