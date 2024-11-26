---
title: Notas de Lançamento do Aspose.PSD para .NET 22.12
type: docs
weight: 10
url: /pt/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- Neste lançamento, foi corrigida uma regressão com a exportação de 16 bits.

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-1336|Adicionar a propriedade TextOrientation editável para a interface IText|Recurso|
|PSDNET-725|Redimensionar o arquivo PSD especificado com uma máscara de camada produz uma máscara incorreta|Erro|
|PSDNET-1277|Adicionar a capacidade de salvar e carregar uma máscara para 16 imagens|Erro|
|PSDNET-1281|Transparência incorreta ao salvar imagem de 16 bits para imagem de 16 ou 8 bits|Erro|
|PSDNET-1375|Corrigir CMYK na cor de 16 bits|Erro|


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-725. Redimensionar o arquivo PSD especificado com uma máscara de camada produz uma máscara incorreta**

{{< highlight csharp >}}
string arquivoOrigem = "origem.psd";
string caminhoExportacaoPsd = "saida.psd";
string caminhoExportacaoPng = "saida.png";

// Abre o arquivo PSD de origem
using (PsdImage imagem = (PsdImage)Image.Load(arquivoOrigem))
{
    const int Escala = 4;

    int novaLargura = imagem.Width * Escala;
    int novaAltura = imagem.Height * Escala;

    // Redimensiona a imagem
    imagem.Resize(novaLargura, novaAltura);
    imagem.Save(caminhoExportacaoPsd, new PsdOptions(imagem));
}

// Abre o arquivo PSD redimensionado
using (PsdImage imagem = (PsdImage)Image.Load(caminhoExportacaoPsd))
{
    // Renderiza para PNG
    imagem.Save(caminhoExportacaoPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Adicionar a capacidade de salvar e carregar uma máscara para 16 imagens**

{{< highlight csharp >}}
string arquivoPsd8bitsOrigem = @"entrada_8bitsCor.psd";
string arquivoPsd16bitsSaida = @"saida_16bitsCor.psd";

using (var imagem = (PsdImage)Image.Load(arquivoPsd8bitsOrigem))
{
    // As opções permitem salvar com 16 bits de cor
    PsdOptions opcoes16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // O arquivo PSD será salvo com transparência
    imagem.Save(arquivoPsd16bitsSaida, opcoes16);
}
{{< /highlight >}}

**PSDNET-1281. Transparência incorreta ao salvar imagem de 16 bits para imagem de 16 ou 8 bits**

{{< highlight csharp >}}
string arquivoOrigem = @"Exemplo_16bits.psd";
string arquivoReSalvo = @"ReSalvar_16bits.psd";
string arquivoImagem = @"ImagemTotal_16bits.png";

// O arquivo PSD de cor de 16 bits (com transparência) será aberto e salvo como 16 bits de cor
using (var imagem = (PsdImage)Image.Load(arquivoOrigem))
{
    PsdOptions opcoes16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    imagem.Save(arquivoReSalvo, opcoes16);
}

// O arquivo PSD salvo como cor de 16 bits será renderizado como arquivo png com transparência
using (var imagem = (PsdImage)Image.Load(arquivoReSalvo))
{
    imagem.Save(arquivoImagem, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Adicionar a propriedade TextOrientation editável para a interface IText**

{{< highlight csharp >}}
// O código a seguir demonstra a capacidade de editar a nova propriedade TextOrientation.
// Isso não afeta a renderização no momento, mas apenas permite editar o valor da propriedade.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var imagem = (PsdImage)Image.Load(src))
{
    var camadaTexto = imagem.Layers[1] as TextLayer;
    if (camadaTexto.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Leitura correta
    }
    else
    {
        throw new Exception("Leitura incorreta do valor da propriedade TextOrientation");
    }

    camadaTexto.TextData.TextOrientation = TextOrientation.Horizontal;
    camadaTexto.TextData.UpdateLayerData();

    imagem.Save(output);
}

using (var imagem = (PsdImage)Image.Load(output))
{
    var camadaTexto = imagem.Layers[1] as TextLayer;
    if (camadaTexto.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Leitura correta
    }
    else
    {
        throw new Exception("Leitura incorreta do valor da propriedade TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Corrigir CMYK na cor de 16 bits**

{{< highlight csharp >}}
string arquivoSrc = @"MascaraRecorteRegular.psd";
string caminhoExportacao = @"exportar.psd";
string caminhoExportarPng = @"exportar.png";

// Define as opções de conversão
PsdOptions opcoesPsd = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Converte e salva
using (var imagem = (PsdImage)Image.Load(arquivoSrc))
{
    imagem.Convert(opcoesPsd);
    imagem.Save(caminhoExportacao);
}

// Abre o arquivo convertido e renderiza para PNG
using (PsdImage imagem = (PsdImage)Image.Load(caminhoExportacao))
{
    imagem.Save(caminhoExportarPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
