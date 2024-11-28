---
title: Aspose.PSD para .NET 22.8 - Notas da Versão
type: docs
weight: 50
url: /pt/net/aspose-psd-para-net-22-8-notas-da-versao/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-1225|Investigar e corrigir os problemas no instalador|Melhoria|
|PSDNET-800|Suporte de Cronograma de Quadros a partir de Arquivo PSD|Recurso|
|PSDNET-1219|Suporte do recurso 'mlst' que contém em ShmdResource como um sub-recurso|Recurso|
|PSDNET-814|Hash de camada muda se chamarmos layer.BlendingOptions.Effects|Erro|


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Delay
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.LayerStates
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.DisposalMethod
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Automatic
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.DoNotDispose
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Dispose
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.HorizontalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.VerticalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.FillOpacity
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
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.DescriptorVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.SubResourcesx


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-800. Suporte de Cronograma de Quadros a partir de Arquivo PSD**

{{< highlight csharp >}}
string arquivoFonte = "imagem1219.psd";
string saidaPsd = "saida_imagem800.psd";

using (PsdImage imagemPsd = (PsdImage)Image.Load(arquivoFonte))
{
    TimeLine linhaTempo = TimeLine.InitializeFrom(imagemPsd);

    // Alterar método de descarte do quadro 1
    linhaTempo.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // Alterar atraso do quadro 2
    linhaTempo.Frames[1].Delay = 15;

    // Alterar opacidade da 'Camada 1' no quadro 2
    LayerState estadoCamada11 = linhaTempo.Frames[1].LayerStates[linhaTempo.LayerIds[1]];
    estadoCamada11.Opacity = 50;

    // mover 'Camada 1' para o canto inferior esquerdo no quadro 3
    LayerState estadoCamada21 = linhaTempo.Frames[2].LayerStates[linhaTempo.LayerIds[1]];
    estadoCamada21.Offset = new Point(-50, 230);

    // Adiciona novo quadro
    List<Frame> quadros = new List<Frame>(linhaTempo.Frames);
    quadros.Add(new Frame(linhaTempo));
    linhaTempo.Frames = quadros.ToArray();

    // Alterar modo de mesclagem da 'Camada 1' no quadro 4
    LayerState estadoCamada31 = linhaTempo.Frames[3].LayerStates[linhaTempo.LayerIds[1]];
    estadoCamada31.BlendMode = BlendMode.Dissolve;

    // Aplicar alterações de volta à instância de PsdImage
    linhaTempo.ApplyTo(imagemPsd);
    imagemPsd.Save(saidaPsd);
}
{{< /highlight >}}

**PSDNET-814. Hash de camada muda se chamarmos layer.BlendingOptions.Effects**

{{< highlight csharp >}}
string arquivoFonte = "AllTypesLayerPsd.psd";

using (var imagem = (PsdImage)Image.Load(arquivoFonte))
{
    var camada = imagem.Layers[0];
    var hashInicial = camada.GetHashCode();
    var efeitos = camada.BlendingOptions.Effects;
    var hashFinal = camada.GetHashCode();

    if (hashInicial != hashFinal)
    {
        throw new Exception("Hash não deve ser alterado");
    }
}
{{< /highlight >}}

**PSDNET-1219. Suporte do recurso 'mlst' que contém em ShmdResource como um sub-recurso**

{{< highlight csharp >}}
string arquivoFonte = "imagem1219.psd";
string saidaPsd = "saida_imagem1219.psd";

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    Layer camada1 = imagem.Layers[1];
    ShmdResource shmdResource = (ShmdResource)camada1.Resources[8];
    MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];

    ListStructure listaEstadosCamada = (ListStructure)mlstResource.Items[1];
    DescriptorStructure estadosCamadasNoQuadro1 = (DescriptorStructure)listaEstadosCamada.Types[1];
    BooleanStructure camadaAtivada = (BooleanStructure)estadosCamadasNoQuadro1.Structures[0];

    // Desativar camada 1 no quadro 1
    camadaAtivada.Value = false;

    imagem.Save(saidaPsd);
}
{{< /highlight >}}
