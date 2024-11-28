---
title: Notas de Lançamento do Aspose.PSD para .NET 24.5
type: docs
weight: 80
url: /pt/net/aspose-psd-para-net-24-5-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para o [Aspose.PSD para .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

| **Chave**   | **Resumo**                                                                            | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | [Formato AI] Adicionar suporte para manipulação de arquivos AI com cabeçalho EPSF     | Feature      |
| PSDNET-1755 | Semitransparência é processada de forma incorreta na visualização do arquivo psd      | Bug          |
| PSDNET-1942 | Renderização parcialmente incorreta das camadas de forma                              | Bug          |
| PSDNET-1957 | Exceção ao salvar arquivos PSD com tamanho superior a 200 MB e dimensões grandes      | Bug          |
| PSDNET-1998 | Falha ao salvar imagem em PDF após a atualização da versão 23.7 para 24.3            | Bug          |
| PSDNET-2033 | Corrigir o problema no método GetFontInfoRecords para as fontes chinesas              | Bug          |

## **Alterações na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-1755. Semitransparência é processada de forma incorreta na visualização do arquivo psd**

{{< highlight csharp >}}
// Semitransparência é processada de forma incorreta na visualização do arquivo psd.
// BackgroundContents atribuído como Branco. Áreas transparentes devem ter a cor branca.

string arquivoOrigem = Path.Combine(pastaBase, "sapo_nosymb.psd");
string arquivoSaida = Path.Combine(pastaSaida, "sapo_nosymb_backgroundcontents_output.psd");

using (PsdImage imagemPsd = (PsdImage)Image.Load(arquivoOrigem))
{
    RawColor corDeFundo = new RawColor(PixelDataFormat.Rgb32Bpp);
    int valorArgb = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    corDeFundo.SetAsInt(valorArgb); // Branco

    PsdOptions opcoesPsd = new PsdOptions(imagemPsd)
    {
        ColorMode = ColorModes.Rgb,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
        BackgroundContents = corDeFundo,
    };

    imagemPsd.Save(arquivoSaida, opcoesPsd);
}
{{< /highlight >}}

**PSDNET-1897. [Formato AI] Adicionar suporte para manipulação de arquivos AI com cabeçalho EPSF**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "exemplo.ai");
string caminhoSaida = Path.Combine(pastaSaida, "exemplo.png");

void AssertAreEqual(object esperado, object atual)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception("Os objetos não são iguais.");
    }
}

using (AiImage imagem = (AiImage)Image.Load(arquivoOrigem))
{
    AssertAreEqual(imagem.Layers.Length, 2);
    AssertAreEqual(imagem.Layers[0].HasMultiLayerMasks, false);
    AssertAreEqual(imagem.Layers[0].ColorIndex, -1);
    AssertAreEqual(imagem.Layers[1].HasMultiLayerMasks, false);
    AssertAreEqual(imagem.Layers[1].ColorIndex, -1);

    imagem.Save(caminhoSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1942. Renderização parcialmente incorreta das camadas de forma**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "TesteCamadaDeForma.psd");
string arquivoSaida = Path.Combine(pastaSaida, "TesteCamadaDeForma_saida.psd");
const int ImgToPsdRatio = 256 * 65535;

using (var im = (PsdImage)Image.Load(arquivoOrigem))
{
    ShapeLayer camadaDeForma = (ShapeLayer)im.Layers[2];
    IPath caminho = camadaDeForma.Path;
    IPathShape[] formasCaminho = caminho.GetItems();
    List<BezierKnotRecord> listaDeNos = new List<BezierKnotRecord>();
    foreach (IPathShape formaCaminho in formasCaminho)
    {
        BezierKnotRecord[] nos = formaCaminho.GetItems();
        listaDeNos.AddRange(nos);
    }

    // Alterar propriedades da camada
    var novaForma = new PathShape();

    BezierKnotRecord[] nosBezier = new BezierKnotRecord[]
    {
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(100, 100),
                    camadaDeForma.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    camadaDeForma.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    camadaDeForma.Container.Size),
            },
        },
        // Outros nós do Bezier
    };

    novaForma.SetItems(nosBezier);

    List<IPathShape> novasFormas = new List<IPathShape>(formasCaminho);
    novasFormas.Add(novaForma);

    IPathShape[] novoCaminho = novasFormas.ToArray();
    caminho.SetItems(novoCaminho);

    camadaDeForma.Update();

    im.Save(arquivoSaida, new PsdOptions());
}

using (var im = (PsdImage)Image.Load(arquivoSaida))
{
    ShapeLayer camadaDeForma = (ShapeLayer)im.Layers[2];
    IPath caminho = camadaDeForma.Path;
    IPathShape[] formasCaminho = caminho.GetItems();
    List<BezierKnotRecord> listaDeNos = new List<BezierKnotRecord>();
    foreach (IPathShape formaCaminho in formasCaminho)
    {
        BezierKnotRecord[] nos = formaCaminho.GetItems();
        listaDeNos.AddRange(nos);
    }

    AssertAreEqual(3, formasCaminho.Length);
    AssertAreEqual(42, camadaDeForma.Left);
    AssertAreEqual(14, camadaDeForma.Top);
    AssertAreEqual(1600, camadaDeForma.Bounds.Width);
    AssertAreEqual(1086, camadaDeForma.Bounds.Height);
}

Point PointFToResourcePoint(PointF ponto, Size tamanhoImagem)
{
    return new Point(
        (int)Math.Round(ponto.Y * (ImgToPsdRatio / tamanhoImagem.Height)),
        (int)Math.Round(ponto.X * (ImgToPsdRatio / tamanhoImagem.Width)));
}

void AssertAreEqual(object esperado, object atual, string mensagem = null)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception(mensagem ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1957. Exceção ao salvar arquivos PSD com tamanho superior a 200 MB e dimensões grandes**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "arquivoGrande.psd");
string arquivoSaida = Path.Combine(pastaSaida, "saida_raw.psd");

PsdLoadOptions opcoesCarregamento = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var imagemPsd = (PsdImage)Image.Load(arquivoOrigem, opcoesCarregamento))
{
    // Não deve haver erro aqui
    imagemPsd.Save(arquivoSaida, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. Falha na salvamento da imagem ao salvar em PDF após atualização da versão 23.7 para 24.3**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "CVFlor.psd");
string arquivoSaida = Path.Combine(pastaSaida, "_export.pdf");

using (var imagemPsd = (PsdImage)Image.Load(arquivoOrigem))
{
    PdfOptions opcoesSalvar = new PdfOptions();
    opcoesSalvar.PdfCoreOptions = new PdfCoreOptions();

    imagemPsd.Save(arquivoSaida, opcoesSalvar);
}
{{< /highlight >}}

**PSDNET-2033. Corrigir o problema no método GetFontInfoRecords para as fontes chinesas**

{{< highlight csharp >}}
var pastaFonte = Path.Combine(pastaBase, "Fonte");
string arquivoOrigem = Path.Combine(pastaBase, "bd-worlds-best-pink.psd");

PsdLoadOptions opcoesCarregamentoPsd = new PsdLoadOptions();
opcoesCarregamentoPsd.LoadEffectsResource = true;
opcoesCarregamentoPsd.AllowWarpRepaint = true;
try
{
    FontSettings.SetFontsFolders(new string[] { pastaFonte }, true);
    FontSettings.UpdateFonts();

    using (PsdImage imagem = (PsdImage)PsdImage.Load(arquivoOrigem, opcoesCarregamentoPsd))
    {
        foreach (var camada in imagem.Layers)
        {
            var camadaTexto = camada as TextLayer;

            if (camadaTexto != null)
            {
                if (camadaTexto.Text == "melhor")
                {
                    // Sem essa correção, haverá exceção devido à fonte chinesa.
                    camadaTexto.UpdateText("SUCESSO");
                }
            }
        }
    }
}
finally
{
    FontSettings.Reset();
    FontSettings.UpdateFonts();
}
{{< /highlight >}}
