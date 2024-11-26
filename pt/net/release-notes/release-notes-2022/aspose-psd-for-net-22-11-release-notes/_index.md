---
title: Aspose.PSD para .NET 22.11 - Notas de Lançamento
type: docs
weight: 20
url: /pt/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Este lançamento tem uma regressão no caso de exportações de 16 bits, portanto, recomendamos cautela ao usar esse recurso nesse lançamento.
Por favor, não atualize o Aspose.PSD para 22.9-22.11 se o processamento de imagem de 16 bits for sua funcionalidade principal.

Estamos trabalhando em soluções para esses problemas.

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-1320|Não é possível exportar arquivos PSB extremamente grandes|Melhoria|
|PSDNET-659|Tornar o centro do degradê radial movível|Recurso|
|PSDNET-1330|Método de compressão ZipWithoutPrediction não suportado para arquivos específicos|Recurso|
|PSDNET-735|Após usar um método de transformação apenas para uma camada, a camada salva tem uma caixa delimitadora incorreta|Erro|
|PSDNET-1234|Exceção ao carregar imagem PSD com padrão|Erro|
|PSDNET-1244|Falha na exportação da imagem (IndexOutOfRangeException) ao salvar o arquivo PSD com símbolos chineses|Erro|
|PSDNET-1303|TimeLine ActiveFrame aplica incorretamente|Erro|
|PSDNET-1307|Regressão 22.7: renderização incorreta de texto com caracteres árabes|Erro|
|PSDNET-1321|Máscara de vetor no Grupo de Camada funciona incorretamente. A imagem final possui o buraco negro, mas não deveria|Erro|


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-659. Tornar o centro do degradê radial movível**

{{< highlight csharp >}}
string arquivoFonte = "psdnet659.psd";
string arquivoSaida = "output.png";

using (var imagemPsd = (PsdImage)Image.Load(arquivoFonte))
{
    FillLayer camadaRadial = (FillLayer)imagemPsd.Layers[5];
    GradientFillSettings configuracoes = (GradientFillSettings)camadaRadial.FillSettings;

    // Atualizar o ponto de deslocamento
    configuracoes.HorizontalOffset = 10;
    configuracoes.VerticalOffset = -25;

    imagemPsd.Save(arquivoSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Após usar um método de transformação apenas para uma camada, a camada salva tem uma caixa delimitadora incorreta**

{{< highlight csharp >}}
string nomeArquivoFonte = @"CamadaTexto.psd";
string arquivoSaida = "CamadaTextoRedimensionada_output.psd";

using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte, new PsdLoadOptions()))
{
    TextLayer camadaTexto = (TextLayer)imagem.Layers[1];

    // Define o novo tamanho da camada de texto
    const int NovaLargura = 250;
    const int NovaAltura = 250;

    // Define o mecanismo de como a função de redimensionamento irá redimensionar a camada (valor padrão)
    ResizeType tipoRedimensionamento = ResizeType.NearestNeighbourResample;

    // Novo mecanismo de redimensionamento para a camada de texto sendo usado aqui
    // Não apenas a camada, mas também a matriz de transformação da camada de texto será alterada
    camadaTexto.Resize(NovaLargura, NovaAltura, tipoRedimensionamento);

    imagem.Save(arquivoSaida, new PsdOptions(imagem));
}

using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida, new PsdLoadOptions()))
{
    TextLayer camadaTxt = (TextLayer)imagem.Layers[1];

    // Razão do delta é fonte padrão diferente
    if (camadaTxt.TransformMatrix[4] >= 65 
        && camadaTxt.TransformMatrix[4] <= 67
        && camadaTxt.TransformMatrix[5] >= 234
        && camadaTxt.TransformMatrix[5] <= 237)
    {
        // Tudo está correto
    }
    else
    {
        throw new Exception("O ponto de localização está errado");
    }
}
{{< /highlight >}}

**PSDNET-1234. Exceção ao carregar imagem PSD com padrão**

{{< highlight csharp >}}
string arquivoSrc = "teste.psd";
string saida = "output1234.png";

using (PsdImage imagemPsd = (PsdImage)PsdImage.Load(arquivoSrc,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions opcoesPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    imagemPsd.Save(saida, opcoesPng);
}
{{< /highlight >}}

**PSDNET-1244. Falha na exportação da imagem (IndexOutOfRangeException) ao salvar o arquivo PSD com símbolos chineses**

{{< highlight csharp >}}
string arquivoFonte = "entrada.psd";
string caminhoSaida = "output.psd";

var opcoesCarregamento = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var imagem = (PsdImage)Image.Load(arquivoFonte, opcoesCarregamento))
{
    foreach (var camada in imagem.Layers)
    {
        if (camada.Name == "1")
        {
            var camadaTxt = (TextLayer)camada;

            camadaTxt.UpdateText("测试测试");
        }
    }

    // Aqui não deveria haver exceção.
    imagem.Save(caminhoSaida, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame aplica incorretamente**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var imagemPsd = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(imagemPsd);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(imagemPsd);

    imagemPsd.Save(output);
}
{{< /highlight >}}

**PSDNET-1307. Regressão 22.7: renderização incorreta de texto com caracteres árabes**

{{< highlight csharp >}}
string pastaFontesTeste = "Fontes";
FontSettings.SetFontsFolder(pastaFontesTeste);
FontSettings.UpdateFonts();

string caminhoArquivoFonte = "sarbarg.fin12.psd";
string caminhoArquivoSaida = "resultado.tiff";

using (var imagemPsd = (PsdImage)Image.Load(caminhoArquivoFonte))
{
    imagemPsd.Save(caminhoArquivoSaida, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Não é possível exportar arquivos PSB extremamente grandes**

{{< highlight csharp >}}
string arquivoFonte = "hf-mim-liman-han-guc-art-kuvvet.psb";
string caminhoExportacaoPsd = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    imagem.Save(caminhoExportacaoPsd, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. A Máscara de Vetor na Camada do Grupo funciona incorretamente. A imagem final possui o buraco negro, mas não deveria**

{{< highlight csharp >}}
string arquivoSrc = "demo.psd";
string saida = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(arquivoSrc))
{
    PngOptions opcoesPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(saida, opcoesPng);
}
{{< /highlight >}}

**PSDNET-1330. Método de compressão ZipWithoutPrediction não suportado para arquivos específicos**

{{< highlight csharp >}}
string arquivoFonte = "20221017_220706_0000.psd";
string arquivoSaida = "20221017_220706_0000.jpg";

using (var imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase opcoesBase = new JpegOptions() { Quality = 80 };
    imagem.Save(arquivoSaida, opcoesBase);
}
{{< /highlight >}}
