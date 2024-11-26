---
title: Aspose.PSD para .NET 23.3 - Notas de Lançamento
type: docs
weight: 100
url: /pt/net/aspose-psd-para-net-23-3-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave** | **Resumo** | **Categoria** |
| :- | :- | :- |
| PSDNET-146 | Suporte à Camada de Ajuste Posterize | Feature |
| PSDNET-1366 | Implementar suporte à VscgResource | Feature |
| PSDNET-1437 | Adicionar suporte ao recurso PostResource para dados da Camada de Ajuste Posterize | Feature |
| PSDNET-931 | Exportação incorreta para camada PNG com ajuste de Curvas e modo de cor CMYK | Bug |
| PSDNET-1403 | Estilo de Parágrafo ausente após salvar e atualizar o arquivo por PS | Bug |
| PSDNET-1453 | Renderização quebrada de efeitos de brilho e sombra no texto | Bug |


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P: Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P: Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-146. Suporte à Camada de Ajuste Posterize**

{{< highlight csharp >}}
string arquivoFonte = "zendeya_posterize.psd";
string arquivoSaida = "zendeya_posterize_10.psd";

using (var imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions()))
{
    foreach (Layer camada in imagem.Layers)
    {
        if (camada is PosterizeLayer)
        {
            ((PosterizeLayer)camada).Levels = 10;
            imagem.Save(arquivoSaida);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Exportação incorreta para camada PNG com ajuste de Curvas e modo de cor CMYK**

{{< highlight csharp >}}
string arquivoSrc = "input_LevelsLayerWithLayerMaskCmyk.psd";
string arquivoSaida = "output_LevelsLayerWithLayerMaskCmykTest.png";
string arquivoOutputPsd = "output.psd";

var opcoesDeCarregamentoPsd = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSrc, opcoesDeCarregamentoPsd))
{
    imagem.Save(arquivoOutputPsd, new PsdOptions()); // o ', new PsdOptions()' está provocando um bug.
    imagem.Save(arquivoSaida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Implementar suporte à VscgResource**

{{< highlight csharp >}}
string arquivoFonte = "StrokeInternalFill_src.psd";
string arquivoSaida = "StrokeInternalFill_res.psd";

void SãoIguais(double esperado, double atual, double tolerância = 0.1)
{
    if (Math.Abs(esperado - atual) > tolerância)
    {
        throw new Exception(
        $"Os valores não são iguais.\nEsperado:{esperado}\nResultado:{atual}\nDiferença:{esperado - atual}");
    }
}

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    VscgResource recursoVscg = (VscgResource)imagem.Layers[1].Resources[0];
    DescriptorStructure estruturaCorRgb = (DescriptorStructure)recursoVscg.Items[0];

    SãoIguais(89.8, ((DoubleStructure)estruturaCorRgb.Structures[0]).Value);
    SãoIguais(219.6, ((DoubleStructure)estruturaCorRgb.Structures[1]).Value);
    SãoIguais(34.2, ((DoubleStructure)estruturaCorRgb.Structures[2]).Value);

    ((DoubleStructure)estruturaCorRgb.Structures[0]).Value = 255d; // Vermelho
    ((DoubleStructure)estruturaCorRgb.Structures[1]).Value = 0d; // Verde
    ((DoubleStructure)estruturaCorRgb.Structures[2]).Value = 0d; // Azul

    imagem.Save(arquivoSaida);
}

// verificando alterações
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida))
{
    VscgResource recursoVscg = (VscgResource)imagem.Layers[1].Resources[0];
    DescriptorStructure estruturaCorRgb = (DescriptorStructure)recursoVscg.Items[0];

    SãoIguais(255, ((DoubleStructure)estruturaCorRgb.Structures[0]).Value);
    SãoIguais(0, ((DoubleStructure)estruturaCorRgb.Structures[1]).Value);
    SãoIguais(0, ((DoubleStructure)estruturaCorRgb.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Estilo de Parágrafo ausente após salvar e atualizar o arquivo por PS**

{{< highlight csharp >}}
string arquivoFonte = "PSDTest3.psd";
string arquivoSaida = "output.psd";

string[] novoTexto = new string[]
{
    "Título \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage imagem = (PsdImage)Aspose.PSD.Image.Load(arquivoFonte))
{
    TextLayer camadaTexto2 = imagem.AddTextLayer("Nova camada", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var dadosTextoTL = camadaTexto2.TextData;

    ITextStyle estiloPadrãoTL = dadosTextoTL.ProducePortion().Style;

    ITextParagraph parágrafoPadrãoTL = dadosTextoTL.ProducePortion().Paragraph;
    ITextPortion[] novasPorçõesTL = dadosTextoTL.ProducePortions(novoTexto, estiloPadrãoTL, parágrafoPadrãoTL);

    novasPorçõesTL[0].Style.FontSize = 14;
    novasPorçõesTL[0].Style.FontName = "TwCenMT-Bold";

    novasPorçõesTL[1].Style.Leading = 20;
    novasPorçõesTL[1].Style.FontSize = 10;
    novasPorçõesTL[1].Style.FontName = "TwCenMT-Bold";

    // Removendo o texto antigo
    dadosTextoTL.RemovePortion(0);

    // Adicionando novas porções de texto
    foreach (var novaPorção in novasPorçõesTL)
    {
        dadosTextoTL.AddPortion(novaPorção);
    }

    dadosTextoTL.UpdateLayerData();

    imagem.Save(arquivoSaida);
}

using (PsdImage imagemPsd = (PsdImage)Aspose.PSD.Image.Load(arquivoSaida))
{
    Txt2Resource recursoTxt2Saida = (Txt2Resource)imagemPsd.GlobalLayerResources[1];
    byte[] bytes = recursoTxt2Saida.Data;
    string txt2Data = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Data += (char)bytes[i];
    }

    string chave0 = @" >> /6 0 >> >> /1 "; // prefixo para o comprimento do parágrafo 0
    string chave1 = @" >> /6 1 >> >> /1 "; // prefixo para o comprimento do parágrafo 1
    int índice0 = txt2Data.IndexOf(chave0);
    int índice1 = txt2Data.IndexOf(chave1);

    string lenPar0 = txt2Data.Substring(índice0 + chave0.Length, 1);
    string lenPar1 = txt2Data.Substring(índice1 + chave1.Length, 3);

    string esperado0 = novoTexto[0].Length.ToString();
    string esperado1 = (novoTexto[1].Length + 1).ToString();

    if (lenPar0 != esperado0 || lenPar1 != esperado1)
    {
        throw new Exception(
            $"O comprimento dos parágrafos está errado.\nEsperado: {esperado0} e {esperado1}\nResultado: {lenPar0} e {lenPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Adicionar suporte ao recurso PostResource para dados da Camada de Ajuste Posterize**

{{< highlight csharp >}}
string arquivoFonte = "zendeya_posterize.psd";
string arquivoSaida = "zendeya_posterize_10.psd";

using (var imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions()))
{
    Layer camada = imagem.Layers[1];

    foreach (LayerResource recurso in camada.Resources)
    {
        if (recurso is PostResource)
        {
            ((PostResource)recurso).Levels = 10;
            imagem.Save(arquivoSaida);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Renderização quebrada de efeitos de brilho e sombra no texto**

{{< highlight csharp >}}
string outputPsd = "effect_bug.psd";
string outputPng = "effect_bug.png";

using (var imagemPsd = new PsdImage(500, 500))
{
    // Adicionar camadas de texto
    Aspose.PSD.Rectangle areaTexto1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle areaTexto2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle areaTexto3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer camadaTexto1 = imagemPsd.AddTextLayer("Texto com Efeitos", areaTexto1);
    TextLayer camadaTexto2 = imagemPsd.AddTextLayer("Texto com Efeitos", areaTexto2);
    TextLayer camadaTexto3 = imagemPsd.AddTextLayer("Texto com Efeitos", areaTexto3);

    // Modificar camadas de texto
    camadaTexto1.TextData.Items[0].Style.FontSize = 150;
    camadaTexto1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    camadaTexto1.TextData.UpdateLayerData();

    camadaTexto2.TextData.Items[0].Style.FontSize = 150;
    camadaTexto2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    camadaTexto2.TextData.UpdateLayerData();

    camadaTexto3.TextData.Items[0].Style.FontSize = 150;
    camadaTexto3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    camadaTexto3.TextData.UpdateLayerData();

    // Adicionar efeitos
    OuterGlowEffect brilhoExterno = camadaTexto1.BlendingOptions.AddOuterGlow(); // Quebra
    brilhoExterno.Spread = 15;
    ((ColorFillSettings)brilhoExterno.FillColor).Color = Color.Red;

    var sombra = camadaTexto2.BlendingOptions.AddDropShadow(); // Quebra com texto longo
    sombra.Distance = 25;
    sombra.Color = Color.DarkBlue;

    var sombraInterna = camadaTexto3.BlendingOptions.AddInnerShadow(); // Quebra com texto longo
    sombraInterna.UseGlobalLight = false;
    sombraInterna.Angle = -179;
    sombraInterna.Distance = 10;
    sombraInterna.Size = 8;
    sombraInterna.Color = Color.HotPink;

    // exportar
    imagemPsd.Save(outputPsd);
    imagemPsd.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}