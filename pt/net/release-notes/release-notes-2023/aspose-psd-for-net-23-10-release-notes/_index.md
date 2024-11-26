---
title: Aspose.PSD para .NET 23.10 - Notas da versão
type: docs
weight: 30
url: /pt/net/aspose-psd-for-net-23-10-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                        | **Categoria** |
|:-----------|:--------------------------------------------------------|:---------|
| PSDNET-692  | Suporte à direção de texto vertical | Recurso   |
| PSDNET-1402 | Usar configurações de traço do recurso vstk em renderização de traço de forma | Recurso   |
| PSDNET-1607 | Implementar a renderização da área interna de formas de traço | Recurso   |
| PSDNET-1644 | Não repintar camada de forma se não foi alterada | Recurso   |
| PSDNET-1696 | [Formato AI] Adicionar suporte para leitura do cabeçalho de arquivos AI baseados em PDF | Recurso   |
| PSDNET-1560 | Várias maneiras de definir a resolução do arquivo Psd não funcionam | Bug     |
| PSDNET-1728 | FontSettings.SetFontsFolders não funciona ou Aspose.PSD usa fonte incorreta | Bug     |
| PSDNET-1739 | Regressão. Corrigir exceção de referência nula ao salvar o PsdImage quando tem camada de forma | Bug     |


## **Mudanças na API pública**

# **APIs adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment

# **APIs removidas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **Exemplos de uso:**

**PSDNET-692. Suporte à direção de texto vertical**

{{< highlight csharp >}}
string arquivoFonte = "692_lt1.psd";
string arquivoSaida = "692_output.png";
string pastaFontes = "692_Fonts";

var pastasFonte = new List<string>(FontSettings.GetFontsFolders());
pastasFonte.Add(pastaFontes);
FontSettings.SetFontsFolders(pastasFonte.ToArray(), true);

using (PsdImage psdImage = (PsdImage)Image.Load(arquivoFonte))
{
    psdImage.Save(arquivoSaida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1402. Usar configurações de traço do recurso vstk em renderização de traço de forma**

{{< highlight csharp >}}
string arquivoFonte = "StrokeShapeTest.psd";
string arquivoSaidaPsd = "StrokeShapeTest.out.psd";
string arquivoSaidaPng = "StrokeShapeTest.out.png";

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    Camada camada = imagem.Layers[1];
    CamadaDeForma camadaDeForma = (CamadaDeForma)imagem.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)camadaDeForma.Fill;
    fillSettings.Color = Color.GreenYellow;
    camadaDeForma.Update();

    CamadaDeForma camadaDeForma2 = (CamadaDeForma)imagem.Layers[3];
    GradientFillSettings gradientSettings = (GradientFillSettings)camadaDeForma2.Fill;
    gradientSettings.Dither = true;
    gradientSettings.Reverse = true;
    gradientSettings.AlignWithLayer = false;
    gradientSettings.Angle = 20;
    gradientSettings.Scale = 50;
    gradientSettings.ColorPoints[0].Location = 100;
    gradientSettings.ColorPoints[1].Location = 4000;
    gradientSettings.TransparencyPoints[0].Location = 200;
    gradientSettings.TransparencyPoints[1].Location = 3800;
    gradientSettings.TransparencyPoints[0].Opacity = 90;
    gradientSettings.TransparencyPoints[1].Opacity = 10;
    camadaDeForma2.Update();

    CamadaDeForma camadaDeForma3 = (CamadaDeForma)imagem.Layers[5];
    StrokeSettings strokeSettings = (StrokeSettings)camadaDeForma3.Stroke;
    strokeSettings.Size = 15;
    ColorFillSettings strokeFillSettings = (ColorFillSettings)strokeSettings.Fill;
    strokeFillSettings.Color = Color.GreenYellow;
    camadaDeForma3.Update();

    imagem.Save(arquivoSaidaPsd);
    imagem.Save(arquivoSaidaPng, new PngOptions());
}

// Verificar alterações nos dados.
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaidaPsd))
{
    CamadaDeForma camadaDeForma = (CamadaDeForma)imagem.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)camadaDeForma.Fill;
    AssertAreEqual(Color.GreenYellow, fillSettings.Color);

    CamadaDeForma camadaDeForma2 = (CamadaDeForma)imagem.Layers[3];
    GradientFillSettings gradientSettings = (GradientFillSettings)camadaDeForma2.Fill;
    AssertAreEqual(true, gradientSettings.Dither);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(20.0, gradientSettings.Angle);
    AssertAreEqual(50, gradientSettings.Scale);
    AssertAreEqual(100, gradientSettings.ColorPoints[0].Location);
    AssertAreEqual(4000, gradientSettings.ColorPoints[1].Location);
    AssertAreEqual(200, gradientSettings.TransparencyPoints[0].Location);
    AssertAreEqual(3800, gradientSettings.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, gradientSettings.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, gradientSettings.TransparencyPoints[1].Opacity);

    CamadaDeForma camadaDeForma3 = (CamadaDeForma)imagem.Layers[5];
    StrokeSettings strokeSettings = (StrokeSettings)camadaDeForma3.Stroke;
    ColorFillSettings strokeFillSettings = (ColorFillSettings)strokeSettings.Fill;
    AssertAreEqual(15.0, strokeSettings.Size);
    AssertAreEqual(Color.GreenYellow, strokeFillSettings.Color);
}

void AssertAreEqual(object esperado, object atual, string mensagem = null)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception(mensagem ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1607. Implementar a renderização da área interna de formas de traço**

{{< highlight csharp >}}
string arquivoFonte = "ShapeInternalGradient.psd";
string arquivoSaida = "ShapeInternalGradient.out.psd";

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    CamadaDeForma camadaDeForma = (CamadaDeForma)imagem.Layers[1];
    GradientFillSettings fillSettings = (GradientFillSettings)camadaDeForma.Fill;
    fillSettings.Dither = true;
    fillSettings.Reverse = true;
    fillSettings.AlignWithLayer = false;
    fillSettings.Angle = 20.0;
    fillSettings.Scale = 50;
    fillSettings.ColorPoints[0].Location = 100;
    fillSettings.ColorPoints[1].Location = 4000;
    fillSettings.TransparencyPoints[0].Location = 200;
    fillSettings.TransparencyPoints[1].Location = 3800;
    fillSettings.TransparencyPoints[0].Opacity = 90.0;
    fillSettings.TransparencyPoints[1].Opacity = 10.0;

    camadaDeForma.Update();

    imagem.Save(arquivoSaida);
}

// Verificar alterações nos dados.
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida))
{
    CamadaDeForma camadaDeForma = (CamadaDeForma)imagem.Layers[1];
    GradientFillSettings fillSettings = (GradientFillSettings)camadaDeForma.Fill;

    AssertAreEqual(true, fillSettings.Dither);
    AssertAreEqual(true, fillSettings.Reverse);
    AssertAreEqual(false, fillSettings.AlignWithLayer);
    AssertAreEqual(20.0, fillSettings.Angle);
    AssertAreEqual(50, fillSettings.Scale);
    AssertAreEqual(100, fillSettings.ColorPoints[0].Location);
    AssertAreEqual(4000, fillSettings.ColorPoints[1].Location);
    AssertAreEqual(200, fillSettings.TransparencyPoints[0].Location);
    AssertAreEqual(3800, fillSettings.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, fillSettings.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, fillSettings.TransparencyPoints[1].Opacity);
}

void AssertAreEqual(object esperado, object atual, string mensagem = null)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception(mensagem ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1644. Não repintar camada de forma se não foi alterada**

{{< highlight csharp >}}
string arquivoFonte = "ShapeInternalSolid.psd";
string arquivoSaida = "ShapeInternalSolid.out.psd";

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    CamadaDeForma camadaDeForma = (CamadaDeForma)imagem.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)camadaDeForma.Fill;
    fillSettings.Color = Color.Red;

    // Não atualizar a camada de forma antes de salvar

    imagem.Save(arquivoSaida);

    // Verificar renderização do arquivo salvo
}

// Verificar que os dados da camada de forma permanecem inalterados.
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida))
{
    CamadaDeForma camadaDeForma = (CamadaDeForma)imagem.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)camadaDeForma.Fill;

    AssertAreEqual(Color.FromArgb(45, 211, 31), fillSettings.Color);
}

void AssertAreEqual(object esperado, object atual, string mensagem = null)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception(mensagem ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1696. [Formato AI] Adicionar suporte para leitura do cabeçalho de arquivos AI baseados em PDF**

{{< highlight csharp >}}
string arquivoFonte = "ai_source.ai";

void AssertIsNotNull(object esperado)
{
    if (esperado == null)
    {
        throw new Exception("O objeto é nulo.");
    }
}

using (AiImage imagem = (AiImage)Image.Load(arquivoFonte))
{
    AssertIsNotNull(imagem);
    AssertIsNotNull(imagem.Header);
    AssertIsNotNull(imagem.Header.BoundingBox);
}
{{< /highlight >}}

**PSDNET-1560. Várias maneiras de definir a resolução do arquivo Psd não funcionam**

{{< highlight csharp >}}
string saida1 = "1560_1_output.psd";
string saida2 = "1560_2_output.psd";
string saida3 = "1560_3_output.psd";

using (PsdImage novoPsd = (PsdImage)new PsdImage(600, 400))
{
    novoPsd.ImageResources = new ResourceBlock[] { new ResolutionInfoResource() };
    novoPsd.VerticalResolution = 100;
    novoPsd.HorizontalResolution = 100;
    novoPsd.Save(saida1);
}

using (PsdImage novoPsd = (PsdImage)new PsdImage(600, 400))
{
    novoPsd.SetResolution(200, 200);
    novoPsd.Save(saida2);
}

using (PsdImage novoPsd = (PsdImage)new PsdImage(600, 400))
{
    PsdOptions psdOptions = new PsdOptions()
    {
        ResolutionSettings = new ResolutionSetting()
        {
            HorizontalResolution = 300,
            VerticalResolution = 300
        }
    };
    novoPsd.Save(saida3, psdOptions);
}

using (var psdImage1 = (PsdImage)Image.Load(saida1))
{
    var resResource = psdImage1.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(100, resResource.VDpi.Integer);
    AreEqual(100, resResource.HDpi.Integer);
}

using (var psdImage2 = (PsdImage)Image.Load(saida2))
{
    var resResource = psdImage2.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(200, resResource.VDpi.Integer);
    AreEqual(200, resResource.HDpi.Integer);
}

using (var psdImage3 = (PsdImage)Image.Load(saida3))
{
    var resResource = psdImage3.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(300, resResource.VDpi.Integer);
    AreEqual(300, resResource.HDpi.Integer);
}

void IsNotNull(object obj)
{
    if (obj == null)
    {
        throw new NullReferenceException();
    }
}

void AreEqual(object esperado, object atual)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception("Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1728. FontSettings.SetFontsFolders não funciona ou Aspose.PSD usa fonte incorreta**

{{< highlight csharp >}}
string src = "1728_Untitled-1.psd";
string fontsDir = "Fonts";
string outputPng = "1728_output.png";

FontSettings.SetFontsFolders(new string[] { fontsDir }, true);
using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var camada in psdImage.Layers)
    {
        if (camada is TextLayer)
        {
            TextLayer textLayer = camada as TextLayer;
            var textData = textLayer.TextData;
            textData.UpdateLayerData();
        }
    }

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1739. Regressão. Corrigir exceção de referência nula ao salvar o PsdImage quando tiver camada de forma**

{{< highlight csharp >}}
string arquivoFonte = "ShapeInternalSolid.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(arquivoFonte))
{
    // Deve carregar sem exceção

    CamadaDeForma camadaDeForma = (CamadaDeForma)im.Layers[1];

    if (camadaDeForma.RawDataSettings == null)
    {
        throw new Exception("RawDataSettings não deve ser nulo.");
    }
}
{{< /highlight >}}