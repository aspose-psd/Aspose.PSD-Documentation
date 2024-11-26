---
title: Notas da Versão Aspose.PSD para .NET 24.2
type: docs
weight: 110
url: /pt/net/aspose-psd-para-net-24-2-notas-de-lan%C3%A7amento/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                  | **Categoria** |
|:------------|:-----------------------------------------------------------------------------|:------------|
| PSDNET-1503 | Manipular propriedade de Ângulo para PatternFillSettings                       |   Feature   |
| PSDNET-1719 | Suporte para escala vertical e horizontal para TextLayer                       |     Feature     |
| PSDNET-1783 | [AI Format] Implementar renderização correta de plano de fundo em Formato AI Baseado em PDF |     Feature     |
| PSDNET-1611 | Alterar mecanismo de distorção em warp                                          |     Melhoria     |
| PSDNET-1802 | Acelerar warp                                                                   |     Melhoria     |
| PSDNET-995  | Exceção "Falha ao carregar imagem." ao abrir documento                          |     Defeito     |
| PSDNET-1491 | Corrigir a gravação de arquivos psd com Padrão de Traço                         |     Defeito     |
| PSDNET-1642 | O estilo de texto está incorreto em um objeto inteligente quando usamos SubstituirConteúdos |     Defeito     |
| PSDNET-1884 | [AI Format] Corrigir a renderização de Bezier Cúbico em arquivo AI             |     Defeito     |

## **Alterações na API Pública**
# **APIs Adicionadas:**
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-1503. Manipular propriedade de Ângulo para PatternFillSettings**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "PadrãoPreenchimentoCamadaLarga_0.psd");
string arquivoSaida = Path.Combine(pastaSaida, "PadrãoPreenchimentoCamadaLarga_0_saida.psd");

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer camadaPreenchimento = (FillLayer)imagem.Layers[1];
    PatternFillSettings configuracoesPreenchimento = (PatternFillSettings)camadaPreenchimento.FillSettings;
    configuracoesPreenchimento.Angle = 70;
    camadaPreenchimento.Update();
    imagem.Save(arquivoSaida, new PsdOptions());
}

using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer camadaPreenchimento = (FillLayer)imagem.Layers[1];
    PatternFillSettings configuracoesPreenchimento = (PatternFillSettings)camadaPreenchimento.FillSettings;

    Assert.AreEqual(70, configuracoesPreenchimento.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Suporte para escala vertical e horizontal para TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(pastaBase, "1719_src.psd");
string output = Path.Combine(pastaSaida, "out_1719.png");

using (var imagemPsd = (PsdImage)Image.Load(src))
{
    imagemPsd.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [AI Format] Implementar renderização correta de plano de fundo em Formato AI Baseado em PDF**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "abacaxis.ai");
string caminhoSaida = Path.Combine(pastaSaida, "abacaxis.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte))
{
    imagem.Save(caminhoSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. Exceção "Falha ao carregar imagem." ao abrir documento**

{{< highlight csharp >}}
string arquivoFonte1 = Path.Combine(pastaBase, "PRODUTO.ai");
string arquivoSaida1 = Path.Combine(pastaSaida, "PRODUTO.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte1))
{
    imagem.Save(arquivoSaida1, new PngOptions());
}

string arquivoFonte2 = Path.Combine(pastaBase, "Dolota.ai");
string arquivoSaida2 = Path.Combine(pastaSaida, "Dolota.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte2))
{
    imagem.Save(arquivoSaida2, new PngOptions());
}

string arquivoFonte3 = Path.Combine(pastaBase, "ARS_novelty_2108_out_01(1).ai");
string arquivoSaida3 = Path.Combine(pastaSaida, "ARS_novelty_2108_out_01(1).png");

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte3))
{
    imagem.Save(arquivoSaida3, new PngOptions());
}

string arquivoFonte4 = Path.Combine(pastaBase, "bit_gear.ai");
string arquivoSaida4 = Path.Combine(pastaSaida, "bit_gear.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte4))
{
    imagem.Save(arquivoSaida4, new PngOptions());
}

string arquivoFonte5 = Path.Combine(pastaBase, "teste.ai");
string arquivoSaida5 = Path.Combine(pastaSaida, "teste.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte5))
{
    imagem.Save(arquivoSaida5, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1491. Corrigir a gravação de arquivos psd com Padrão de Traço**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "TraçoFormaPadrão.psd");
string arquivoSaida = Path.Combine(pastaSaida, "TraçoFormaPadrão_saida.psd");

Rectangle novosLimitesPadrão = new Rectangle(0, 0, 4, 4);
Guid guid = Guid.NewGuid();
string novoNomePadrão = "$$$/Presets/Padrões/LinhaHorizontal1=Linha Horizontal 9\0";
int[] novoPadrão = new int[]
{
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
};

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    ShapeLayer camadaForma = (ShapeLayer)imagem.Layers[1];
    PatternFillSettings configuraçõesPreenchimentoInternoTraço = (PatternFillSettings)camadaForma.Fill;

    PattResource recursoPatt;
    foreach (var recursoGlobalCamada in imagem.GlobalLayerResources)
    {
        if (recursoGlobalCamada is PattResource)
        {
            recursoPatt = (PattResource)recursoGlobalCamada;
            PattResourceData itemPadrão = recursoPatt.Patterns[0]; // Dados de padrão interno de traço

            itemPadrão.PatternId = guid.ToString();
            itemPadrão.Name = novoNomePadrão;
            itemPadrão.SetPattern(novoPadrão, novosLimitesPadrão);

            break;
        }
    }

    configuraçõesPreenchimentoInternoTraço.PatternName = novoNomePadrão;
    configuraçõesPreenchimentoInternoTraço.PatternId = guid.ToString() + "\0";

    camadaForma.Update();

    imagem.Save(arquivoSaida);
}

// Verifique os dados alterados.
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida))
{
    ShapeLayer camadaForma = (ShapeLayer)imagem.Layers[1];
    PatternFillSettings configuraçõesPreenchimentoInternoTraço = (PatternFillSettings)camadaForma.Fill;

    Assert.AreEqual(guid.ToString().ToUpper(), configuraçõesPreenchimentoInternoTraço.PatternId);
    Assert.AreEqual(novoNomePadrão, configuraçõesPreenchimentoInternoTraço.PatternName + "\0");
}
{{< /highlight >}}

**PSDNET-1642. O estilo de texto está incorreto em um objeto inteligente quando usamos SubstituirConteúdos**

{{< highlight csharp >}}
string arquivoEntrada = Path.Combine(pastaBase, "origem.psd");
string saida2 = Path.Combine(pastaSaida, "saída.png");

PsdLoadOptions opçõesCarregamentoPsd = new PsdLoadOptions();
opçõesCarregamentoPsd.LoadEffectsResource = true;

using (PsdImage imagemPsd = (PsdImage)Image.Load(arquivoEntrada, opçõesCarregamentoPsd))
{
    SmartObjectLayer objetoInteligente = (SmartObjectLayer)imagemPsd.Layers[1];

    using (PsdImage imagemObjetoInteligente = (PsdImage)objetoInteligente.LoadContents(opçõesCarregamentoPsd))
    {
        objetoInteligente.ReplaceContents(imagemObjetoInteligente);
    }

    imagemPsd.Save(saida2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1884. [AI Format] Corrigir a renderização de Bezier Cúbico em arquivo AI**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "Tipografia.ai");
string caminhoSaida = Path.Combine(pastaSaida, "Tipografia.png");

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte))
{
    imagem.Save(caminhoSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1611. Alterar mecanismo de distorção em warp**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "grade_corvo.psd");
string arquivoSaida = Path.Combine(pastaSaida, "exportar.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(arquivoFonte, opt))
{
    img.Save(arquivoSaida, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1802. Acelerar warp**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "saída.psd");
string arquivoSaida = Path.Combine(pastaSaida, "exportar.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

var sw = new Stopwatch();
sw.Start();

using (PsdImage img = (PsdImage)Image.Load(arquivoFonte, opt))
{
    img.Save(arquivoSaida, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}

sw.Stop();

// valor antigo = 193300
// novo valor =  55500
int tempoEmSeg = (int)sw.Elapsed.TotalMilliseconds;
if (tempoEmSeg > 100000)
{
    throw new Exception("O tempo de processamento é muito longo");
}
{{< /highlight >}}
