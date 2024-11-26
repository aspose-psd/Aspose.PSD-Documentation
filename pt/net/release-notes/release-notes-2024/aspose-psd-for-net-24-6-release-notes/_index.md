---
title: Notas de Lançamento Aspose.PSD para .NET 24.6
type: docs
weight: 70
url: /pt/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                         | **Categoria** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | Implementar suporte para camada de mapa de gradiente                                   | Funcionalidade|
| PSDNET-1670 | [Formato AI] Adicionar suporte para Metadados XPacket ao Formato AI                   | Funcionalidade|
| PSDNET-1831 | Implementar tipos de distorção Inflate, Squeeze e Twist                                | Funcionalidade|
| PSDNET-1653 | Modos Rgb e Lab não podem conter menos de 3 canais e mais de 4 canais no arquivo com Camadas de ArtBoard                                         | Bug          |
| PSDNET-1775 | A área de processamento superior deve ser positiva. (Parâmetro 'areaToProcess') no processamento de um arquivo específico   | Bug          |
| PSDNET-2052 | A imagem expandida sobre o canvas é cortada após o salvamento. Os dados são perdidos, mas a visualização parece correta        | Bug          |

## **Alterações na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-1450. Implementar suporte para camada de mapa de gradiente**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "gradient_map_src.psd");
string arquivoSaida = Path.Combine(pastaSaida, "gradient_map_src_output.psd");

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    // Adicionar camada de ajuste do mapa de gradiente.
    GradientMapLayer camada = imagem.AddGradientMapAdjustmentLayer();
    camada.GradientSettings.Reverse = true;

    imagem.Save(arquivoSaida);
}

// Verificar alterações salvas
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida))
{
    GradientMapLayer camadaMapaGradiente = imagem.Layers[1] as GradientMapLayer;
    GradientFillSettings configGradiente = (GradientFillSettings)camadaMapaGradiente.GradientSettings;

    AssertAreEqual(0.0, configGradiente.Angle);
    AssertAreEqual((short)4096, configGradiente.Interpolation);
    AssertAreEqual(true, configGradiente.Reverse);
    AssertAreEqual(false, configGradiente.AlignWithLayer);
    AssertAreEqual(false, configGradiente.Dither);
    AssertAreEqual(GradientType.Linear, configGradiente.GradientType);
    AssertAreEqual(100, configGradiente.Scale);
    AssertAreEqual(0.0, configGradiente.HorizontalOffset);
    AssertAreEqual(0.0, configGradiente.VerticalOffset);
    AssertAreEqual("Personalizado", configGradiente.GradientName);
}

void AssertAreEqual(object esperado, object atual, string mensagem = null)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception(mensagem ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [Formato AI] Adicionar suporte para Metadados XPacket ao Formato AI**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "ai_one.ai");

void AssertAreEqual(object esperado, object atual)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception("Os objetos não são iguais.");
    }
}

void AssertIsNotNull(object objetoTeste)
{
    if (objetoTeste == null)
    {
        throw new Exception("O objeto de teste é nulo.");
    }
}

string chaveCreatorTool = ":CreatorTool";
string chaveNPaginas = "xmpTPg:NPages";
string chaveUnidade = "stDim:unit";
string chaveAltura = "stDim:h";
string chaveLargura = "stDim:w";

string criadorEsperado = "Adobe Illustrator CC 22.1 (Windows)";
string nPaginasEsperado = "1";
string unidadeEsperada = "Pixels";
double alturaEsperada = 768;
double larguraEsperada = 1366;

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte))
{
    // Os Metadados Xmp foram adicionados.
    var metadadosXmp = imagem.XmpData;

    AssertIsNotNull(metadadosXmp);

    // Agora podemos acessar os Pacotes Xmp dos arquivos AI.
    var pacoteBasico = metadadosXmp.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var pacote = metadadosXmp.Packages[4];

    // E temos acesso ao conteúdo desses pacotes.
    var ferramentaCriacao = pacoteBasico[chaveCreatorTool].ToString();
    var nPaginas = pacote[chaveNPaginas];
    var unidade = pacote[chaveUnidade];
    var altura = double.Parse(pacote[chaveAltura].ToString(), CultureInfo.InvariantCulture);
    var largura = double.Parse(pacote[chaveLargura].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(ferramentaCriacao, criadorEsperado);
    AssertAreEqual(nPaginas, nPaginasEsperado);
    AssertAreEqual(unidade, unidadeEsperada);
    AssertAreEqual(altura, alturaEsperada);
    AssertAreEqual(largura, larguraEsperada);
}
{{< /highlight >}}

**PSDNET-1831. Implementar tipos de distorção Inflate, Squeeze e Twist**

{{< highlight csharp >}}
string[] arquivos = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefixo in arquivos)
{
    string arquivoFonte = Path.Combine(pastaBase, prefixo + ".psd");
    string arquivoSaida = Path.Combine(pastaSaida, prefixo + "_export.png");

    using (var imagemPsd = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        imagemPsd.Save(arquivoSaida, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Os modos Rgb e Lab não podem conter menos de 3 canais e mais de 4 canais no arquivo com Camadas de ArtBoard**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "Rgb5Channels.psb");
string arquivoSaida = Path.Combine(pastaSaida, "Rgb5Channels_output.psd");

using (PsdImage imagem = (PsdImage)Aspose.PSD.Image.Load(arquivoFonte))
{
    // Aqui não deve ocorrer exceção
    imagem.Save(arquivoSaida);
}
{{< /highlight >}}

**PSDNET-1775. A área de processamento superior deve ser positiva. (Parâmetro 'areaToProcess') no processamento de um arquivo específico**

{{< highlight csharp >}}
string arquivoFonte = @"BANNERS_2_Intel-Gamer_psak.psd";
string arquivoSaida = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions opcoesCarregamento = new PsdLoadOptions();
opcoesCarregamento.LoadEffectsResource = true;
opcoesCarregamento.AllowWarpRepaint = true;
using (PsdImage imagem = (PsdImage)PsdImage.Load(arquivoFonte, opcoesCarregamento))
{
    imagem.Save(arquivoSaida);
    // Não deveria ocorrer exceção
}
{{< /highlight >}}

**PSDNET-2052. A imagem expandida sobre o canvas é cortada após o salvamento. Os dados são perdidos, mas a visualização parece correta**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "bigfile.psd");

string arquivoSaida = Path.Combine(pastaSaida, "bigfile_output.psd");
string imagemSaida = Path.Combine(pastaSaida, "bigfile.png");

PsdLoadOptions opcoesCarregamento = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var imagemPsd = (PsdImage)Image.Load(arquivoFonte, opcoesCarregamento))
{
    // Não deve haver erro aqui
    imagemPsd.Save(arquivoSaida, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var imagemPsd = (PsdImage)Image.Load(arquivoSaida, opcoesCarregamento))
{
    imagemPsd.Resize(imagemPsd.Width / 10, imagemPsd.Height / 10);

    // Não deve haver erro aqui
    imagemPsd.Save(imagemSaida, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
