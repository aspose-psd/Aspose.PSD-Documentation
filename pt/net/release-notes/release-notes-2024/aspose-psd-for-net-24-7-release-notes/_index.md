---
title: Aspose.PSD para .NET 24.7 - Notas de Lançamento
type: docs
weight: 60
url: /pt/net/aspose-psd-para-net-24-7-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                        | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Exceção "Falha ao carregar imagem." ao abrir documento AI                                          | Bug      |
| PSDNET-2022 | Texto renderizado incorretamente em arquivos PDF de saída                                           | Bug      |
| PSDNET-2061 | Corrigir ImageSaveException: Falha na exportação de imagem para o arquivo fornecido no Linux       | Bug      |
| PSDNET-2080 | Corrigir o carregamento de fontes ao usar Aspose.Drawing                                            | Bug      |
| PSDNET-2085 | 'A operação aritmética resultou em overflow' ao criar uma camada de objeto inteligente usando JPEG grande | Bug      |
| PSDNET-2100 | O arquivo AI não pode ser convertido em um arquivo JPG                                             | Bug      |

## **Alterações na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-1029. Exceção "Falha ao carregar imagem." ao abrir documento AI**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "[SA]_ID_card_template.ai");
string arquivoSaida = Path.Combine(pastaSaida, "[SA]_ID_card_template.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoOrigem))
{
    imagem.Save(arquivoSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Texto renderizado incorretamente em arquivos PDF de saída**

{{< highlight csharp >}}
string src = Path.Combine(pastaBase, "CVFlor.psd");
string output = Path.Combine(pastaSaida, "output.pdf");

using (var psdImagem = (PsdImage)Image.Load(src))
{
    PdfOptions opcoesSalvar = new PdfOptions();
    opcoesSalvar.PdfCoreOpcoes = new PdfCoreOptions();

    psdImagem.Save(output, opcoesSalvar);
}
{{< /highlight >}}

**PSDNET-2061. Corrigir ImageSaveException: Falha na exportação de imagem para o arquivo fornecido no Linux**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "Bed_Roll-Sticker4_1.psd");
string arquivoSaida = Path.Combine(pastaSaida, "output.jpg");

using (var psdImagem = (PsdImage)Image.Load(arquivoOrigem, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var opcoesSalvar = new JpegOptions() { Qualidade = 70 };
    psdImagem.Save(arquivoSaida, opcoesSalvar);
}
{{< /highlight >}}

**PSDNET-2080. Corrigir o carregamento de fontes ao usar Aspose.Drawing**

{{< highlight csharp >}}
using (var fontesInstaladas = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Antes da atualização. Contagem de fontes instaladas: " + fontesInstaladas.Families.Length);
    Console.WriteLine("- Plataforma: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Atualizar o cache de fontes tentando obter o nome da fonte Adobe para 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Após a atualização. Contagem de fontes instaladas: " + fontesInstaladas.Families.Length);

    Assert.Maior(fontesInstaladas.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'A operação aritmética resultou em overflow' ao criar uma camada de objeto inteligente usando JPEG grande**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "source.psd");
string imagemJpeg = Path.Combine(pastaBase, "test.jpg");

using (var imagem = (PsdImage)Image.Load(arquivoOrigem, new PsdLoadOptions { ModoRecuperacaoDados = ModoRecuperacaoDados.RecuperacaoMaxima }))
{
    using (var stream = new FileStream(imagemJpeg, FileMode.Abre))
    {
        var camadaAdicionada = new SmartObjectLayer(stream);
        camadaAdicionada.Nome = "Camada de Teste";
        imagem.AdicionaCamada(camadaAdicionada);
    }
}
{{< /highlight >}}

**PSDNET-2100. O arquivo AI não pode ser convertido em um arquivo JPG**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "aaa.ai");
string arquivoSaida = Path.Combine(pastaSaida, "aaa.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoOrigem))
{
    imagem.Save(arquivoSaida, new PngOptions());
}
{{< /highlight >}}
