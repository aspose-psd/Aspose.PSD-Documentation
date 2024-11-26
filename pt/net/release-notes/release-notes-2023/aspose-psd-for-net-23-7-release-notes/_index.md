---
title: Notas de Lançamento do Aspose.PSD for .NET 23.7
type: docs
weight: 60
url: /pt/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para o [Aspose.PSD for .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                                  | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Adicionar capacidade de exportar cada camada do arquivo PSD para o Arquivo Gif Animado                      | Recurso |
| PSDNET-1441 | Atribuir a propriedade Preencher da camada de forma ao recurso vscg                                          | Recurso |
| PSDNET-1534 | Adicionar novos tipos de distorção (arco e arco)                                                             | Recurso |
| PSDNET-1543 | Mudar a aplicação que salva o arquivo PSD para Aspose.PSD se a propriedade UpdateMetadata estiver definida como true | Recurso |
| PSDNET-1567 | Aumentar a área de cálculo da imagem distorcida                                                              | Recurso |
| PSDNET-1471 | A camada de ajuste em preto e branco processa a semitransparência de forma errada                             | Erro     |
| PSDNET-1505 | O Substituir Conteúdo de SmartObject (quando a opção AllowWarpRepaint está ativa) falha após 2 minutos de processamento | Erro     |
| PSDNET-1585 | Adicionar capacidade de obter a posição real da camada de Grupo de Camadas Left e Top                      | Erro     |
| PSDNET-1589 | O redimensionamento da camada não funciona corretamente quando o arquivo psd tem VogkResource com estruturas em pontos | Erro |
| PSDNET-1608 | TextBound não está funcionando como esperado                                                                | Erro     |
| PSDNET-1612 | Adicionar uma camada criada com o construtor padrão à imagem PSD não adiciona recursos padrão a ela         | Erro     |
| PSDNET-1623 | A propriedade Timeline.LoopesCount é ignorada ao exportar para Gif animado                                   | Erro     |


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P: Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F: Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F: Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P: Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M: Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M: Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P: Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill

# **APIs Removidas:**
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Exemplos de Uso:**

**PSDNET-802. Adicionar capacidade de exportar cada camada do arquivo PSD para o Arquivo Gif Animado**

{{< highlight csharp >}}
string src = "CadaCamadaEhFrame.psd";
string outputGif = "out_CadaCamadaEhFrame.gif";
string outputPsd = "out_CadaCamadaEhFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Criar frames para cada camada.
    int contagemFrames = psdImage.Layers.Length;
    var cronograma = psdImage.Timeline;

    Frame[] frames = new Frame[contagemFrames];
    for (int i = 0; i < contagemFrames; i++)
    {
        frames[i] = new Frame();
        LayerState[] estadosCamada = new LayerState[contagemFrames];

        for (int j = 0; j < contagemFrames; j++)
        {
            estadosCamada[j] = new LayerState();
            estadosCamada[j].Enabled = i == j;
        }

        frames[i].LayerStates = estadosCamada;
    }

    cronograma.Frames = frames;

    // Atualizar estados atuais
    Layer[] camadas = psdImage.Layers;
    LayerState[] estados = cronograma.Frames[cronograma.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < contagemFrames; i++)
    {
        camadas[i].IsVisible = estados[i].Enabled;
    }

    cronograma.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Atribuir a propriedade Preencher da camada de forma ao recurso vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// Verificar alterações salvas
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object esperado, object real, string mensagem = null)
{
    if (!object.Equals(esperado, real))
    {
        throw new Exception(mensagem ?? "Objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1471. A camada de ajuste em preto e branco processa a semitransparência de forma errada**

{{< highlight csharp >}}
string srcFile = "sapo_nosimb.psd";
string outFile = "sapo_nosimb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Verificar alterações salvas
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer camadaAjustePretoBranco = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (camadaAjustePretoBranco == null)
    {
        throw new Exception("A Camada 2 deve ser do tipo AjustePretoBranco");
    }

    image.Save(outFile);
}

void AssertAreEqual(object esperado, object real, string mensagem = null)
{
    if (!object.Equals(esperado, real))
    {
        throw new Exception(mensagem ?? "Objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1505. O Substituir Conteúdo de SmartObject (quando a opção AllowWarpRepaint está ativa) falha após 2 minutos de processamento**

{{< highlight csharp >}}
string sourceFile = "caneca 4.psd";
string changeFile = "arte para substituir.png";
string outputFile = "exportar.png";

int novaAltura = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer camadaSmartObject = (SmartObjectLayer)psdImage.Layers[3];

    var escala = (double)novaAltura / camadaSmartObject.Height;
    var novaLargura = (int)Math.Round(camadaSmartObject.Width * escala);

    PsdImage imagemInterna = new PsdImage(novaLargura, novaAltura);
    imagemInterna.SetResolution(72, 72);

    Stream streamInterno = new FileStream(changeFile, FileMode.Open);
    Layer camada = new Layer(streamInterno) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        imagemInterna.AddLayer(camada);

        camadaSmartObject.ReplaceContents(imagemInterna);
        camadaSmartObject.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        imagemInterna.Dispose();
        streamInterno.Dispose();
        camada.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Adicionar novos tipos de distorção (arco e arco)**

{{< highlight csharp >}}
string sourceArcFile = "arco_dist.psd";
string outputArcFile = "arco_exportar.png";

string sourceArchFile = "arco_dist.psd";
string outputArchFile = "arco_exportar.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. Mudar a aplicação que salva o arquivo PSD para Aspose.PSD se a propriedade UpdateMetadata estiver definida como true**

{{< highlight csharp >}}
string caminho = "saída.psd";
using (var imagem = new PsdImage(100, 100))
{
    // Se você deseja alterar a ferramenta criadora, certifique-se de que a propriedade "UpdateMetadata" esteja definida como true. Por padrão, ela está definida como true.
    var opcoesPsd = new PsdOptions();
    opcoesPsd.UpdateMetadata = true;

    // Salvando a imagem. 
    imagem.Save(caminho, opcoesPsd);

    // Verificar a ferramenta criadora no código.
    var dadosXmp = imagem.XmpData;
    var packageBasico = imagem.XmpData.GetPackage(Namespaces.XmpBasic);

    // Aqui será atualizada a informação da ferramenta criadora.
    var ferramentaAtualCreator = (string)packageBasico[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Aumentar a área de cálculo da imagem distorcida**

{{< highlight csharp >}}
string sourceFile = "caneca4_dist.psd";
string outputFile = "caneca4_exportar.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. Adicionar capacidade de obter a posição real da camada de Grupo de Camadas Left e Top**

{{< highlight csharp >}}
string sourceFile = "camadasGrupoFiguras.psd";

void AssertAreEqual(object esperado, object real)
{
    if (!object.Equals(esperado, real))
    {
        throw new Exception("Os objetos não são iguais.");
    }
}

using (var imagem = (PsdImage)Image.Load(sourceFile))
{
    var camadas = imagem.Layers;

    for (int i = 0; i < camadas.Length; i++)
    {
        var camada = camadas[i];

        if (camada is LayerGroup)
        {
            // Obter o Grupo de Camadas.
            var grupo = (LayerGroup)camada;

            var leftEsperado = int.MaxValue;
            var topEsperado = int.MaxValue;
            var rightEsperado = 0;
            var bottomEsperado = 0;

            // Calcular as posições reais de Left, Top, Right e Bottom.
            foreach (var camadaInterna in grupo.Layers)
            {
                if (camadaInterna is AdjustmentLayer || camadaInterna.Bounds.IsEmpty)
                {
                    continue;
                }

                leftEsperado = Math.Min(leftEsperado, camadaInterna.Left);
                topEsperado = Math.Min(topEsperado, camadaInterna.Top);
                rightEsperado = Math.Max((leftEsperado + grupo.Width), (camadaInterna.Left + camadaInterna.Width));
                bottomEsperado = Math.Max((topEsperado + grupo.Height), (camadaInterna.Top + camadaInterna.Height));
            }

            // As posições de Left, Top, Right e Bottom do Grupo de Camadas são calculadas corretamente agora.
            AssertAreEqual(grupo.Left, leftEsperado);
            AssertAreEqual(grupo.Top, topEsperado);
            AssertAreEqual(grupo.Right, rightEsperado);
            AssertAreEqual(grupo.Bottom, bottomEsperado);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. O redimensionamento da camada não funciona corretamente quando o arquivo psd tem VogkResource com estruturas em pontos**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "OrigemVetorPontos.psd",
    "EstrutVogkTop.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer camada = image.Layers[0];

        camada.Resize(50, 50);

        AssertAreEqual(camada.Height, 50);
        AssertAreEqual(camada.Width, 50);
    }
}

void AssertAreEqual(object esperado, object real, string mensagem = null)
{
    if (!object.Equals(esperado, real))
    {
        throw new Exception(mensagem ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound não está funcionando como esperado**

{{< highlight csharp >}}
string sourceFile = "entrada_Teste_paraBilhete.psd";
string outFile = "out_1608.psd";

Size novaCaixaTexto = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // Etapa: Substituir texto
    TextLayer camadaTexto = (TextLayer)psdImage.Layers[3];
    camadaTexto.TextData.Items[0].Text = "Texto de teste substituído";

    // Etapa: Atualizar TextBoundBox
    camadaTexto.TextData.UpdateLayerData();
    novaCaixaTexto = new Size((int)Math.Ceiling(camadaTexto.TextBoundBox.Width), camadaTexto.Height);

    camadaTexto.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, novaCaixaTexto);
    camadaTexto.TextData.UpdateLayerData();

    psdImage.Save(outFile);
}

// Verificar alterações
using (var psdImage = (PsdImage)Image.Load(outFile))
{
    Txt2Resource recursoTxt2 = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string dadosTexto = Encoding.GetEncoding("Windows-1251").GetString(recursoTxt2.Data);

    string busca = "<< /0 << /1 << /0 ["; // conjunto de caracteres específico para encontrar o valor da caixa de texto neste arquivo.

    int startIndex = dadosTexto.IndexOf(busca) + busca.Length;
    int endIndex = dadosTexto.IndexOf("]", startIndex);
    string itensCaixa = dadosTexto.Substring(startIndex, endIndex - startIndex);

    string altura = novaCaixaTexto.Height.ToString("0.0####").Replace(",", ".");
    string largura = novaCaixaTexto.Width.ToString("0.0####").Replace(",", ".");

    if (!itensCaixa.Contains(altura) || !itensCaixa.Contains(largura))
    {
        throw new Exception("Caixa de texto não foi atualizada.");
    }
}
{{< /highlight >}}

**PSDNET-1612. Adicionar uma camada criada com o construtor padrão à imagem PSD não adiciona recursos padrão a ela**

{{< highlight csharp >}}
string output = "novaCamada.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var camada = new Layer();
    psdImage.AddLayer(camada);

    LyidResource recursoLyid = (LyidResource)FindResource(LyidResource.TypeToolKey, camada.Resources);

    int idCamada = recursoLyid.Value; // Lançava NullReferenceException

    psdImage.Save(output);
}
    
LayerResource FindResource(int resType, LayerResource[] recursos)
{
    if (recursos != null)
    {
        foreach (var recursoCamada in recursos)
        {
            if (recursoCamada.Key == resType)
            {
                return recursoCamada;
            }
        }
    }

    return null;
}
{{< /highlight >}}

**PSDNET-1623. A propriedade Timeline.LoopesCount é ignorada ao exportar para Gif animado**

{{< highlight csharp >}}
string sourceFile = "4_animado.p