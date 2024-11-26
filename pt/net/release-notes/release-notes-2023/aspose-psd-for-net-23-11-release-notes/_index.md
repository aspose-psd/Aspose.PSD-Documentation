---
title: Notas da Versão do Aspose.PSD para .NET 23.11
type: docs
weight: 20
url: /pt/net/aspose-psd-para-net-23-11-notas-de-versao/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para o [Aspose.PSD for .NET 23.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**    | **Resumo**                                                                                           | **Categoria** |
|:------------|:----------------------------------------------------------------------------------------------------|:--------|
| PSDNET-412  | Suporte ao recurso LMskResource                                                                       | Recurso |
| PSDNET-1669 | [Formato AI] Adicionar capacidade de renderizar arquivo AI baseado em PDF com Aspose.PSD             | Recurso |
| PSDNET-1702 | [Formato AI] Adicionar suporte ao operador PostScript "cm"                                              | Recurso |
| PSDNET-1752 | Adicionar novos tipos de deformação: Onda, casco superior, casco inferior                              | Recurso |
| PSDNET-1797 | Adicionar suporte para deformação vertical                                                             | Recurso |
| PSDNET-1756 | System.ArgumentNullException: 'O valor não pode ser nulo. (Parâmetro 'chave')' ao chamar TextLayer.GetFonts() | Bug |


## **Alterações na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FontSettings.RemoveFontCacheFile
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorSpace
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent1
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent3
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent4
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Flag
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.CMYK
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.Lab
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.GrayScale


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**
**PSDNET-412. Suporte ao recurso LMskResource**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "arquivoFonte.psd");
string psdDeSaida = Path.Combine(pastaSaida, "arquivoFonte_saida.psd");

void AssertAreEqual(object esperado, object atual)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception("Objetos não são iguais.");
    }
}

// Carregar imagem de 16 bits.
using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    // Encontrar LmskResource.
    LmskResource lmskResource = new LmskResource();
    foreach (var res in imagem.GlobalLayerResources)
    {
        if (res is LmskResource)
        {
            lmskResource = (LmskResource)res;
            break;
        }
    }

    // Verificar propriedades do LmskResource.
    AssertAreEqual(lmskResource.ColorSpace, PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB);
    AssertAreEqual(lmskResource.ColorComponent1, (ushort)65535);
    AssertAreEqual(lmskResource.ColorComponent2, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent3, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent4, (ushort)0);
    AssertAreEqual(lmskResource.Opacity, (short)45);
    AssertAreEqual(lmskResource.Flag, (byte)128);

    // Alterar propriedades do LmskResource.
    lmskResource.ColorSpace = PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB;
    lmskResource.ColorComponent1 = 7854;
    lmskResource.ColorComponent2 = 10;
    lmskResource.ColorComponent3 = 15484;
    lmskResource.Opacity = 85;

    // Salvar a imagem.
    imagem.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1669. [Formato AI] Adicionar capacidade de renderizar arquivo AI baseado em PDF com Aspose.PSD**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "ai_um.ai");
string pngDeSaida = Path.Combine(pastaSaida, "ai_um_saida.png");

// Carregar a imagem AI baseada em PDF.
using (AiImage imagem = (AiImage)Image.Load(arquivoFonte))
{
    // Salvar a imagem AI como uma imagem PNG.
    imagem.Save(pngDeSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1702. [Formato AI] Adicionar suporte ao operador PostScript "cm"**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(pastaBase, "ai_dois.ai");
string pngDeSaida = Path.Combine(pastaSaida, "ai_dois_saida.png");

// Carregar a imagem AI.
using (AiImage imagem = (AiImage)Image.Load(arquivoFonte))
{
    // Salvar a imagem AI como uma imagem PNG.
    imagem.Save(pngDeSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1752. Adicionar novos tipos de deformação: Onda, casco superior, casco inferior**

{{< highlight csharp >}}
var loadOptions = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var saveOptions = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string arquivoPeixe = Path.Combine(pastaBase, "1752_deformacao_peixe.psd");
string arquivoAumento = Path.Combine(pastaBase, "1752_deformacao_aumentar.psd");
string arquivoOnda = Path.Combine(pastaBase, "1752_deformacao_onda.psd");

string arquivoSaidaPeixe = Path.Combine(pastaSaida, "1752_saida_peixe.png");
string arquivoSaidaAumento = Path.Combine(pastaSaida, "1752_saida_aumentar.png");
string arquivoSaidaOnda = Path.Combine(pastaSaida, "1752_saida_onda.png");

using (var imagemPsd = (PsdImage)Image.Load(arquivoPeixe, loadOptions))
{
    imagemPsd.Save(arquivoSaidaPeixe, saveOptions);
}

using (var imagemPsd = (PsdImage)Image.Load(arquivoAumento, loadOptions))
{
    imagemPsd.Save(arquivoSaidaAumento, saveOptions);
}

using (var imagemPsd = (PsdImage)Image.Load(arquivoOnda, loadOptions))
{
    imagemPsd.Save(arquivoSaidaOnda, saveOptions);
}
{{< /highlight >}}

**PSDNET-1756. System.ArgumentNullException: 'O valor não pode ser nulo. (Parâmetro 'chave')' ao chamar TextLayer.GetFonts()**

{{< highlight csharp >}}
string src = Path.Combine(pastaBase, "TextoSimples.psd");

FontSettings.RemoveFontCacheFile();

using (var imagemPsd = (PsdImage)Image.Load(src))
{
    foreach (var camada in imagemPsd.Layers)
    {
        if (camada is TextLayer textLayer)
        {
            textLayer.GetFonts();
        }
    }
}
{{< /highlight >}}

**PSDNET-1797. Adicionar suporte para deformação vertical**

{{< highlight csharp >}}
var loadOptions = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var saveOptions = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string arquivoCurvaInferior = Path.Combine(pastaBase, "1797_deformacao_curva_inferior_v.psd");
string arquivoCurvaSuperior = Path.Combine(pastaBase, "1797_deformacao_curva_superior_v.psd");
string arquivoArco = Path.Combine(pastaBase, "1797_deformacao_arco_v.psd");
string arquivoSalto = Path.Combine(pastaBase, "1797_deformacao_salto_v.psd");
string arquivoBandeira = Path.Combine(pastaBase, "1797_deformacao_bandeira_v.psd");
string arquivoPeixe = Path.Combine(pastaBase, "1797_saida_peixe_v.psd");
string arquivoAumentar = Path.Combine(pastaBase, "1797_saida_aumentar_v.psd");
string arquivoOnda = Path.Combine(pastaBase, "1797_saida_onda_v.psd");

string saidaCurvaInferior = Path.Combine(pastaSaida, "1797_saida_curva_inferior_v.png");
string saidaCurvaSuperior = Path.Combine(pastaSaida, "1797_saida_curva_superior_v.png");
string saidaArco = Path.Combine(pastaSaida, "1797_saida_arco_v.png");
string saidaSalto = Path.Combine(pastaSaida, "1797_saida_salto_v.png");
string saidaBandeira = Path.Combine(pastaSaida, "1797_saida_bandeira_v.png");
string saidaPeixe = Path.Combine(pastaSaida, "1797_saida_peixe_v.png");
string saidaAumentar = Path.Combine(pastaSaida, "1797_saida_aumentar_v.png");
string saidaOnda = Path.Combine(pastaSaida, "1797_saida_onda_v.png");

using (var imagemPsd = (PsdImage)Image.Load(arquivoCurvaInferior, loadOptions)) { imagemPsd.Save(saidaCurvaInferior, saveOptions); }
using (var imagemPsd = (PsdImage)Image.Load(arquivoCurvaSuperior, loadOptions)) { imagemPsd.Save(saidaCurvaSuperior, saveOptions); }
using (var imagemPsd = (PsdImage)Image.Load(arquivoArco, loadOptions)) { imagemPsd.Save(saidaArco, saveOptions); }
using (var imagemPsd = (PsdImage)Image.Load(arquivoSalto, loadOptions)) { imagemPsd.Save(saidaSalto, saveOptions); }
using (var imagemPsd = (PsdImage)Image.Load(arquivoBandeira, loadOptions)) { imagemPsd.Save(saidaBandeira, saveOptions); }
using (var imagemPsd = (PsdImage)Image.Load(arquivoPeixe, loadOptions)) { imagemPsd.Save(saidaPeixe, saveOptions); }
using (var imagemPsd = (PsdImage)Image.Load(arquivoAumentar, loadOptions)) { imagemPsd.Save(saidaAumentar, saveOptions); }
using (var imagemPsd = (PsdImage)Image.Load(arquivoOnda, loadOptions)) { imagemPsd.Save(saidaOnda, saveOptions); }
{{< /highlight >}}
