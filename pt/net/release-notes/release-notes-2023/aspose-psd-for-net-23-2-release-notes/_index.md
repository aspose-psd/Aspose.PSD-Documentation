---
title: Notas da Versão Aspose.PSD for .NET 23.2
type: docs
weight: 110
url: /pt/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de versão para [Aspose.PSD for .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-1359|Rework text rendering to improve text positioning, rendering, and support|Melhoria|
|PSDNET-1270|Adicionar capacidade de processar Efeito de Distorção através da API pública|Recurso|
|PSDNET-1391|Adicionar suporte aos modos de liderança Inferior a Inferior e Superior a Superior das configurações de Parágrafo|Recurso|
|PSDNET-912|Alterar Fonte e Cor para TextLayer PSD|Erro|
|PSDNET-1022|Exportação incorreta de texto nos testes de Atualização de Texto, texto está faltando|Erro|
|PSDNET-1221|Texto extra pequeno está faltando após redimensionar a imagem PSD maior|Erro|
|PSDNET-1301|Aspose.Psd for .NET textLayer.UpdateText() está imprimindo '-' (hífen) como sublinhado de maneira aleatória para diferentes conjuntos de dados|Erro|
|PSDNET-1379|As configurações de Resolução não se aplicam na exportação de PSD para PDF|Erro|


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **APIs Removidas:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Exemplos de Uso:**

**PSDNET-912. Alterar Fonte e Cor para TextLayer PSD**

{{< highlight csharp >}}
string pastaFontes = "Fonts";
string arquivoSrc = "M1PDTT26052021001.psd";
string outputPsd = "resultado.psd";
string outputPng = "resultado.png";

FontSettings.SetFontsFolder(pastaFontes);

using (var imagem = (PsdImage)Image.Load(arquivoSrc))
{
    TextLayer camadaNome = (TextLayer)imagem.Layers[9];
    var porcaoTexto = camadaNome.TextData.Items[0];

    porçãoTexto.Text = "MODESTO SR";
    porçãoTexto.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    porçãoTexto.Style.FillColor = Color.Red;

    camadaNome.TextData.UpdateLayerData();

    imagem.Save(outputPsd);
    imagem.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Exportação incorreta de texto nos testes de Atualização de Texto, texto está faltando**

{{< highlight csharp >}}
string arquivoSrc = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var imagem = (PsdImage)Image.Load(arquivoSrc))
{
    for (int i = 0; i < imagem.Layers.Length; i++)
    {
        var camada = imagem.Layers[i] as TextLayer;

        if (camada != null)
        {
            camada.UpdateText("O texto foi atualizado");
        }
    }

    imagem.Save(outputPsd);
    imagem.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Texto extra pequeno está faltando após redimensionar a imagem PSD maior**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var imagemPSD = (PsdImage)Image.Load(src))
{
    imagemPSD.Resize(30, 30);

    imagemPSD.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Adicionar capacidade de processar Efeito de Distorsão através da API pública**

{{< highlight csharp >}}
string arquivoOrigem = "source.psd";
string pngExportadoDistorcido = "warped.png";
string psdExportadoDistorcido = "warpFile.psd";

var opçõesCarregamentoDistorcidas = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var imagem = (PsdImage)Image.Load(arquivoOrigem, opçõesCarregamentoDistorcidas))
{
    imagem.Save(pngExportadoDistorcido, new PngOptions());
    imagem.Save(psdExportadoDistorcido, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd for .NET textLayer.UpdateText() está imprimindo '-' (hífen) como sublinhado de maneira aleatória para diferentes conjuntos de dados**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var camada in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (camada is TextLayer)
        {
            TextLayer camadaTexto = camada as TextLayer;
            switch (camada.Nome.Trim().ToUpper())
            {
                case "NOME":
                    camadaTexto.UpdateText("SR. JACK SMITH");
                    break;
                case "IDNO":
                    camadaTexto.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNAÇÃO":
                    camadaTexto.UpdateText("FUNCIONÁRIO-001");
                    break;
                case "GRUPOSANG":
                    camadaTexto.UpdateText("AB-");
                    break;
                case "ENDEREÇO":
                    camadaTexto.UpdateText("BLOCO-A, RUA-7, APARTAMENTO Nº - 047, SETOR-024");
                    break;
                case "ENDPERM":
                    camadaTexto.UpdateText("CASA Nº - 42, PISTA -025, PALM GREENS VIEW HOUSING SOCIETY, SETOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. As configurações de Resolução não se aplicam na exportação de PSD para PDF**

{{< highlight csharp >}}
string entrada = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var imagem = Image.Load(entrada, new PsdLoadOptions()))
{
    ResolutionSetting configResolucao = new ResolutionSetting(300, 300);

    imagem.Save(output, new PdfOptions()
    {
        ResolutionSettings = configResolucao
    });
}
{{< /highlight >}}

**PSDNET-1391. Adicionar suporte aos modos de liderança Inferior a Inferior e Superior a Superior das configurações de Parágrafo**

{{< highlight csharp >}}
string entrada = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var imagemPSD = (PsdImage)Image.Load(entrada, new PsdLoadOptions()))
{
    IText texto1 = ((TextLayer)imagemPSD.Layers[1]).TextData;
    foreach (var porçãoTexto in texto1.Items)
    {
        porçãoTexto.Paragraph.LeadingType = LeadingType.TopToTop; // Alterar o valor do LeadingType   
    }
    texto1.Items[8].Text = "TopToTop";
    texto1.Items[8].Style.FillColor = Color.ForestGreen;
    texto1.UpdateLayerData();

    IText texto2 = ((TextLayer)imagemPSD.Layers[2]).TextData;
    foreach (var porçãoTexto in texto2.Items)
    {
        porçãoTexto.Paragraph.LeadingType = LeadingType.BottomToBottom; // Alterar o valor do LeadingType   
    }
    texto2.Items[8].Text = "BottomToBottom";
    texto2.Items[8].Style.FillColor = Color.ForestGreen;
    texto2.UpdateLayerData();

    imagemPSD.Save(output, new PngOptions());
}
{{< /highlight >}}
