---
title: Notas da Versão Aspose.PSD para .NET 23.5
type: docs
weight: 80
url: /pt/net/aspose-psd-para-net-23-5-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 23.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**     | **Resumo**                                                                  | **Categoria** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDNET-343  | Suporte ao filtro: Sharpen -> Sharpen                                      | Recurso      |
| PSDNET-1179 | Arquivo PSD (RGB/8 bits ou RGB/16 bits) salvando sem camadas em 32 bits    | Recurso      |
| PSDNET-1408 | Implementar manipulação de objetos de caminho de recursos vsms ou vmsk para ShapeLayer | Recurso      |
| PSDNET-1508 | Adicionar a influência dos pontos de grade um no outro                     | Recurso      |


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsDisabled
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.PathOperations
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor(Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord,Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ShapeIndex
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ToVectorPathRecords
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsInverted
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.DescriptorStructure)
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterId
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterType


# **APIs Removidas:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Save(Aspose.PSD.StreamContainer,System.Int32)


## **Exemplos de Uso:**

**PSDNET-343. Suporte ao Filtro: Sharpen -> Sharpen**

{{< highlight csharp >}}
string arquivoOrigem = "fonte_de_afiacao.psd";
string psdSaida = "psd_de_afiacao.psd";
string pngSaida = "png_de_afiacao.png";

void AssertSaoIguais(object esperado, object atual)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception("Os objetos não são iguais.");
    }
}

using (var imagem = (PsdImage)Image.Load(arquivoOrigem))
{
    SmartObjectLayer camadaObjetoInteligente = (SmartObjectLayer)imagem.Layers[1];

    // editar filtros inteligentes
    SharpenSmartFilter afiacao = (SharpenSmartFilter)camadaObjetoInteligente.SmartFilters.Filters[0];

    // verificar valores do filtro
    AssertSaoIguais(BlendMode.Normal, afiacao.BlendMode);
    AssertSaoIguais(100d, afiacao.Opacity);
    AssertSaoIguais(true, afiacao.IsEnabled);

    // atualizar valores do filtro
    afiacao.BlendMode = BlendMode.Divide;
    afiacao.Opacity = 75;
    afiacao.IsEnabled = false;

    // adicionar novos itens de filtro
    var filtros = new List<SmartFilter>(camadaObjetoInteligente.SmartFilters.Filters);
    filtros.Add(new SharpenSmartFilter());
    camadaObjetoInteligente.SmartFilters.Filters = filtros.ToArray();

    // aplicar alterações
    camadaObjetoInteligente.SmartFilters.UpdateResourceValues();
    camadaObjetoInteligente.UpdateModifiedContent();

    imagem.Save(psdSaida);
    imagem.Save(pngSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1179. Arquivo PSD (RGB/8 bits ou RGB/16 bits) salvando sem camadas para 32 bits**

{{< highlight csharp >}}
string arquivoEntrada = "entrada_8bit_rle.psd";
string arquivoPsdSaida = "saida_32bit.psd";
string arquivoImagemSaida32 = "saida_de_32bit.png";

using (PsdImage imgSrc = (PsdImage)Image.Load(arquivoEntrada))
{
    PsdOptions opcoesTotais = new PsdOptions() { ChannelBitsCount = 32, ColorMode = ColorModes.Rgb };
    imgSrc.Save(arquivoPsdSaida, opcoesTotais);

    using (var img32 = Image.Load(arquivoPsdSaida))
    {
        img32.Save(arquivoImagemSaida32, new PngOptions() { ColorType = PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-1408. Implementar manipulação de objetos de caminho de recursos vsms ou vmsk para ShapeLayer**

{{< highlight csharp >}}
string arquivoFonte = "ShapeLayerTest.psd";
string arquivoSaida = "ShapeLayerTest-saida.psd";

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer camadaForma = imagem.Layers[1];
    VectorPathDataResource recursoDadosCaminhoVetorial = (VectorPathDataResource)camadaForma.Resources[1];

    bool preencherIniciaComTodosOsPixels;
    List<IPathShape> formas = ObterFormasDoRecurso(recursoDadosCaminhoVetorial, out preencherIniciaComTodosOsPixels);

    // Remover uma forma
    formas.RemoveAt(1);

    // Salvar dados alterados no recurso
    List<VectorPathRecord> caminho = new List<VectorPathRecord>();
    caminho.Add(new PathFillRuleRecord(null));
    caminho.Add(new InitialFillRuleRecord(preencherIniciaComTodosOsPixels));

    for (ushort i = 0; i < formas.Count; i++)
    {
        PathShape forma = (PathShape)formas[i];
        forma.ShapeIndex = i;
        caminho.AddRange(forma.ToVectorPathRecords());
    }

    recursoDadosCaminhoVetorial.Paths = caminho.ToArray();

    imagem.Save(arquivoSaida);
}

// Verificar valores alterados no arquivo salvo
using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaida, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer camadaForma = imagem.Layers[1];
    VectorPathDataResource recursoDadosCaminhoVetorial = (VectorPathDataResource)camadaForma.Resources[1];

    bool preencherIniciaComTodosOsPixels;
    List<IPathShape> formas = ObterFormasDoRecurso(recursoDadosCaminhoVetorial, out preencherIniciaComTodosOsPixels);

    // O arquivo salvo deve ter 1 forma
    AssertSaoIguais(1, formas.Count);
}

void AssertSaoIguais(object esperado, object atual, string mensagem = null)
{
    if (!object.Equals(esperado, atual))
    {
        throw new Exception(mensagem ?? "Os objetos não são iguais.");
    }
}

List<IPathShape> ObterFormasDoRecurso(VectorPathDataResource recursoDadosCaminhoVetorial, out bool preencherIniciaComTodosOsPixels)
{
    List<IPathShape> formas = new List<IPathShape>();
    LengthRecord registroComprimento = null;
    preencherIniciaComTodosOsPixels = false;
    List<BezierKnotRecord> registrosPontoCurva = new List<BezierKnotRecord>();

    foreach (var registroCaminho in recursoDadosCaminhoVetorial.Paths)
    {
        if (registroCaminho is LengthRecord)
        {
            if (registrosPontoCurva.Count > 0)
            {
                formas.Add(new PathShape(registroComprimento, registrosPontoCurva.ToArray()));
                registroComprimento = null;
                registrosPontoCurva.Clear();
            }

            registroComprimento = (LengthRecord)registroCaminho;
        }
        else if (registroCaminho is BezierKnotRecord)
        {
            registrosPontoCurva.Add((BezierKnotRecord)registroCaminho);
        }
        else if (registroCaminho is InitialFillRuleRecord)
        {
            InitialFillRuleRecord registroRegraPreenchimentoInicial = (InitialFillRuleRecord)registroCaminho;
            preencherIniciaComTodosOsPixels = registroRegraPreenchimentoInicial.IsFillStartsWithAllPixels;
        }
    }

    if (registrosPontoCurva.Count > 0)
    {
        formas.Add(new PathShape(registroComprimento, registrosPontoCurva.ToArray()));
        registroComprimento = null;
        registrosPontoCurva.Clear();
    }

    return formas;
}
{{< /highlight >}}

**PSDNET-1508. Adicionar a influência dos pontos de grade um no outro**

{{< highlight csharp >}}
string arquivoFonte = "Bottom_Right.psd";
string arquivoSaida = "saida.png";

using (var imagem = (PsdImage)Image.Load(arquivoFonte, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    imagem.Save(arquivoSaida, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}