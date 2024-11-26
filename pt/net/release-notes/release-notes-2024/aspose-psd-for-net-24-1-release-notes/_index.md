---
title: Aspose.PSD para .NET 24.1 - Notas de Lançamento
type: docs
weight: 120
url: /pt/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento do [Aspose.PSD para .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                        | **Categoria**|
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [Formato AI] Adiciona manipulação básica para imagens AI com várias páginas                        | Recurso      |
| PSDNET-718  | Efeito de Texto Distorcido não se aplica ao texto                                                 | Erro         |
| PSDNET-1620 | Renderização incorreta de máscara em arquivo específico                                          | Erro         |
| PSDNET-1855 | NullReferenceException em Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor    | Erro         |
| PSDNET-1883 | [Formato AI] Corrigindo o uso de memória em AiExporterUtils                                      | Erro         |



## **Alterações na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-718. Efeito de Texto Distorcido não se aplica ao texto**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(baseFolder, "texto_distorcido.psd");
string arquivoSaida = Path.Combine(outputFolder, "export.png");

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

**PSDNET-1620. Renderização incorreta de máscara em arquivo específico**

{{< highlight csharp >}}
string arquivoFonte1 = Path.Combine(baseFolder, "problema_mascara.psd");
string arquivoFonte2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string arquivoSaida1 = Path.Combine(outputFolder, "mascara_export.png");
string arquivoSaida2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(arquivoFonte1, opt))
{
    img.Save(arquivoSaida1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(arquivoFonte2, opt))
{
    img.Save(arquivoSaida2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [Formato AI] Adiciona manipulação básica para imagens AI com várias páginas**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(baseFolder, "tresPaginas.ai");
string primeiroPagOutputPng = Path.Combine(outputFolder, "primeiraPagOutput.png");
string segundoPagOutputPng = Path.Combine(outputFolder, "segundaPagOutput.png");
string terceiroPagOutputPng = Path.Combine(outputFolder, "terceiraPagOutput.png");

// Carrega a imagem AI.
using (AiImage image = (AiImage)Image.Load(arquivoFonte))
{
    // Por padrão, o ActivePageIndex é 0.
    // Portanto, se você salvar a imagem AI sem alterar esta propriedade, a primeira página será renderizada e salva.
    image.Save(primeiroPagOutputPng, new PngOptions());

    // Altere o índice da página ativa para a segunda página.
    image.ActivePageIndex = 1;

    // Salve a segunda página da imagem AI como uma imagem PNG.
    image.Save(segundoPagOutputPng, new PngOptions());

    // Altere o índice da página ativa para a terceira página.
    image.ActivePageIndex = 2;

    // Salve a terceira página da imagem AI como uma imagem PNG.
    image.Save(terceiroPagOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException em Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string pastaFontes = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { pastaFontes }, true);

string arquivoEntrada = Path.Combine(baseFolder, "1.psd");
string arquivoSaida = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(arquivoEntrada))
{
    psdImage.Save(arquivoSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [Formato AI] Corrigindo o uso de memória em AiExporterUtils**

{{< highlight csharp >}}
string arquivoFonte = Path.Combine(baseFolder, "tresPaginas.ai");
string primeiroPagOutputPng = Path.Combine(outputFolder, "primeiraPagOutput.png");
string segundoPagOutputPng = Path.Combine(outputFolder, "segundaPagOutput.png");
string terceiroPagOutputPng = Path.Combine(outputFolder, "terceiraPagOutput.png");

const double LimiteMemoria = 220;
double memoriaUtilizada = double.MaxValue;

// Carrega a imagem AI.
using (AiImage image = (AiImage)Image.Load(arquivoFonte))
{
    // Salve a primeira página da imagem AI como uma imagem PNG.
    image.Save(primeiroPagOutputPng, new PngOptions());

    // Altere o índice da página ativa para a segunda página.
    image.ActivePageIndex = 1;

    // Salve a segunda página da imagem AI como uma imagem PNG.
    image.Save(segundoPagOutputPng, new PngOptions());

    // Altere o índice da página ativa para a terceira página.
    image.ActivePageIndex = 2;

    // Salve a terceira página da imagem AI como uma imagem PNG.
    image.Save(terceiroPagOutputPng, new PngOptions());
}

GC.Collect();

memoriaUtilizada = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoriaUtilizada > LimiteMemoria)
{
    throw new Exception("O uso da memória é muito grande. " + memoriaUtilizada + " em vez de " + LimiteMemoria.ToString("F1"));
}
{{< /highlight >}}
