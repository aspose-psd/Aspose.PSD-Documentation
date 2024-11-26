---
title: Aspose.PSD para .NET 23.6 - Notas de Lançamento
type: docs
weight: 70
url: /pt/net/aspose-psd-para-net-23-6-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                                                                      | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Refatorar API TimeLine                                                                                                                          | Aprimoramento |
| PSDNET-1517 | Remover artefatos ao renderizar deformação                                                                                                      | Aprimoramento |
| PSDNET-1528 | Otimização de renderização de deformação                                                                                                        | Aprimoramento |
| PSDNET-147  | Suporte à Camada de Ajuste de Limiar                                                                                                            | Recurso      |
| PSDNET-149  | Suporte à Camada de Ajuste de Cor Seletiva                                                                                                      | Recurso      |
| PSDNET-801  | Capacidade de exportar TimeLine PSD para arquivo Gif animado                                                                                     | Recurso      |
| PSDNET-1555 | Adicionar suporte para TextLayer sem bordas retangulares                                                                                         | Recurso      |
| PSDNET-1582 | Suporte à Camada de Forma                                                                                                                      | Recurso      |
| PSDNET-864  | Substituir imagem em objeto Inteligente não está sendo atualizado                                                                               | Bug          |
| PSDNET-1404 | Arquivo PSD não pode ser salvo como PSD com a seguinte exceção: Modos Rgb e Lab não podem conter menos de 3 canais e mais de 4 canais   | Bug          |
| PSDNET-1546 | Justificação de texto é perdida ao abrir TextLayer no modo de edição do Photoshop                                                               | Bug          |
| PSDNET-1548 | Exceção de referência nula ao salvar arquivo PSD                                                                                                 | Bug          |
| PSDNET-1578 | Exceção ao carregar a ShapeLayer: Pontos dos limites de origem do vetor não são suportados ainda                                                | Bug          |
| PSDNET-1579 | Exceção ao carregar VogkResource: Pontos são salvos como DoubleStructures, lemos como UnitStructures                                            | Bug          |
| PSDNET-1581 | O LayerType da ShapeLayer está vazio                                                                                                           | Bug          |


## **Alterações na API Pública**
# **APIs Adicionadas:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)  
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **APIs Removidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **Exemplos de Uso:**

**PSDNET-147. Suporte à Camada de Ajuste de Limiar**

{{< highlight csharp >}}
string arquivoFonteComCamadaLimiar = "flores_limiar_origem.psd";
string arquivoPsdComCamadaLimiar = "flores_limiar_saida.psd";
string arquivoPngComCamadaLimiar = "flores_limiar_saida.png";

string arquivoFonteSemCamadaLimiar = "flores_origem.psd";
string arquivoPsdSemCamadaLimiar = "flores_saida.psd";
string arquivoPngSemCamadaLimiar = "flores_saida.png";

void AssertSaoIguais(object esperado, object atual)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception("Os objetos não são iguais.");
    }
}

// Obter, verificar e alterar a camada de ajuste de Limiar da imagem.
using (var imagem = (PsdImage)Aspose.PSD.Imagem.Carregar(arquivoFonteComCamadaLimiar))
{
    foreach (var camada in imagem.Camadas)
    {
        if (camada é CamadaLimiar)
        {
            // Obter a camada de ajuste de Limiar.
            CamadaLimiar camadaLimiar = (CamadaLimiar)camada;
            var nivel = camadaLimiar.Nivel;

            // Verificar parâmetros das camadas.
            AssertSaoIguais(nivel, (short)115);

            // Configurar parâmetros das camadas.
            camadaLimiar.Nivel = 50;

            imagem.Salvar(arquivoPsdComCamadaLimiar);
            imagem.Salvar(arquivoPngComCamadaLimiar, new OpcoesPng());
        }
    }
}

// Adicionar e configurar a camada de ajuste de Limiar na imagem.
using (var imagem = (PsdImage)Aspose.PSD.Imagem.Carregar(arquivoFonteSemCamadaLimiar))
{
    // Adicionar camada de ajuste de Limiar.
    CamadaLimiar camadaLimiar = imagem.AdicionarCamadaAjusteLimiar();

    // Configurar parâmetros das camadas.
    camadaLimiar.Nivel = 115;

    imagem.Salvar(arquivoPsdSemCamadaLimiar);
    imagem.Salvar(arquivoPngSemCamadaLimiar, new OpcoesPng());
}
{{< /highlight >}}

**PSDNET-149. Suporte à Camada de Ajuste de Cor Seletiva**

{{< highlight csharp >}}
string arquivoComCamadaCorSeletiva = "casas_camadaCorSeletiva_origem.psd";
string arquivoPsdComCamadaCorSeletiva = "casas_camadaCorSeletiva_saida.psd";
string arquivoPngComCamadaCorSeletiva = "casas_camadaCorSeletiva_saida.png";

string arquivoSemCamadaCorSeletiva = "casas_origem.psd";
string arquivoPsdSemCamadaCorSeletiva = "casas_saida.psd";
string arquivoPngSemCamadaCorSeletiva = "casas_saida.png";

void AssertSaoIguais(object esperado, object atual)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception("Os objetos não são iguais.");
    }
}

// Obter, verificar e alterar a camada de ajuste de Cor Seletiva da imagem.
using (var imagem = (PsdImage)Aspose.PSD.Imagem.Carregar(arquivoComCamadaCorSeletiva))
{
    foreach (var camada in imagem.Camadas)
    {
        if (camada é CamadaCorSeletiva)
        {
            // Obter a camada de ajuste de Cor Seletiva.
            CamadaCorSeletiva camadaCorSel = (CamadaCorSeletiva)camada;
            var correcaoVermelha = camadaCorSel.ObterCorrecaoCmyk(SelecionarTiposCores.Vermelhos);
            var correcaoAmarela = camadaCorSel.ObterCorrecaoCmyk(SelecionarTiposCores.Amarelos);
            var correcaoVerde = camadaCorSel.ObterCorrecaoCmyk(SelecionarTiposCores.Verdes);
            var correcaoAzul = camadaCorSel.ObterCorrecaoCmyk(SelecionarTiposCores.Azuis);

            // Verificar parâmetros das camadas.
            AssertSaoIguais(TiposMetodosCorrecao.Absoluto, camadaCorSel.MetodoCorrecao);

            AssertSaoIguais(correcaoVermelha.Ciano, (short)-31);
            AssertSaoIguais(correcaoVermelha.Magenta, (short)-12);
            AssertSaoIguais(correcaoVermelha.Amarelo, (short)27);
            AssertSaoIguais(correcaoVermelha.Preto, (short)33);

            AssertSaoIguais(correcaoAmarela.Ciano, (short)-22);
            AssertSaoIguais(correcaoAmarela.Magenta, (short)-19);
            AssertSaoIguais(correcaoAmarela.Amarelo, (short)8);
            AssertSaoIguais(correcaoAmarela.Preto, (short)0);

            AssertSaoIguais(correcaoVerde.Ciano, (short)0);
            AssertSaoIguais(correcaoVerde.Magenta, (short)0);
            AssertSaoIguais(correcaoVerde.Amarelo, (short)0);
            AssertSaoIguais(correcaoVerde.Preto, (short)0);

            AssertSaoIguais(correcaoAzul.Ciano, (short)58);
            AssertSaoIguais(correcaoAzul.Magenta, (short)18);
            AssertSaoIguais(correcaoAzul.Amarelo, (short)1);
            AssertSaoIguais(correcaoAzul.Preto, (short)7);

            // Mudar parâmetros das camadas.
            camadaCorSel.MetodoCorrecao = TiposMetodosCorrecao.Relativo;
            camadaCorSel.DefinirCorrecaoCmyk(SelecionarTiposCores.Vermelhos, new CorrecaoCmyk { Ciano = 12, Magenta = -20, Amarelo = 10, Preto = -15 });
            camadaCorSel.DefinirCorrecaoCmyk(SelecionarTiposCores.Brancos, new CorrecaoCmyk { Ciano = 15, Magenta = 20, Amarelo = -75, Preto = 42 });

            imagem.Salvar(arquivoPsdComCamadaCorSeletiva);
            imagem.Salvar(arquivoPngComCamadaCorSeletiva, new OpcoesPng());
        }
    }
}

// Adicionar e configurar a camada de ajuste de Cor Seletiva na imagem.
using (var imagem = (PsdImage)Aspose.PSD.Imagem.Carregar(arquivoSemCamadaCorSeletiva))
{
    // Adicionar camada de ajuste de Cor Seletiva.
    CamadaCorSeletiva camadaCorSel = imagem.AdicionarCamadaAjusteCorSeletiva();

    // Configurar parâmetros das camadas.
    camadaCorSel.MetodoCorrecao = TiposMetodosCorrecao.Absoluto;
    camadaCorSel.DefinirCorrecaoCmyk(SelecionarTiposCores.Brancos, new CorrecaoCmyk { Ciano = 100, Magenta = -100, Amarelo = 100, Preto = 0 });
    camadaCorSel.DefinirCorrecaoCmyk(SelecionarTiposCores.Pretos, new CorrecaoCmyk { Ciano = 10, Magenta = 15, Amarelo = 17, Preto = -3 });
    camadaCorSel.DefinirCorrecaoCmyk(SelecionarTiposCores.Neutros, new CorrecaoCmyk { Ciano = 45, Magenta = 21, Amarelo = -14, Preto = 0 });
    camadaCorSel.DefinirCorrecaoCmyk(SelecionarTiposCores.Magentas, new CorrecaoCmyk { Ciano = 8, Magenta = -10, Amarelo = -14, Preto = 25 });

    imagem.Salvar(arquivoPsdSemCamadaCorSeletiva);
    imagem.Salvar(arquivoPngSemCamadaCorSeletiva, new OpcoesPng());
}
{{< /highlight >}}

**PSDNET-801. Capacidade de exportar TimeLine PSD para arquivo Gif animado**

{{< highlight csharp >}}
string arquivoFonte = "4_animated.psd";
string gifSaida = "out_4_animated.psd.gif";

using (var psdImagem = (PsdImagem)Imagem.Carregar(arquivoFonte, new OpcoesCarregamentoPsd() { CarregarRecursosEfeitos = Verdadeiro }))
{
    psdImagem.TimeLine.Salvar(gifSaida, new OpcoesGif());
}
{{< /highlight >}}

**PSDNET-864. Substituir imagem em objeto Inteligente não está sendo atualizado**

{{< highlight csharp >}}
string arquivoFonte = "neiyi.p