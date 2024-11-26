---
title: Notas da Versão Aspose.PSD para .NET 23.1
type: docs
weight: 120
url: /pt/net/aspose-psd-para-net-23-1-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-401|Suporte de vstkResource|Recurso|
|PSDNET-1346|Adicionar a propriedade editável BaselineDirection/IsStandardVerticalRomanAlignmentEnabled para a interface IText|Recurso|
|PSDNET-181|PSD não é convertido corretamente para JPEG|Erro|
|PSDNET-958|PSB para PDF falha para arquivos grandes|Erro|
|PSDNET-1171|Adicionar processamento de máscara de recorte para camada de ajuste|Erro|
|PSDNET-1252|Após redimensionar a imagem inteira e depois redimensionar a camada específica, o Aspose.PSD lança exceção ao salvar a camada|Erro|


## **Mudanças na API pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleMiterLimit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineJoinType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleScaleLock
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleStrokeAdjust
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleBlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleOpacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleResolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleContent
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Levels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.TypeToolKey


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-181. PSD não é convertido corretamente para JPEG**

{{< highlight csharp >}}
string arquivoSrc = "helicopter.psd";
string jpgSaida = "output.jpg";

using (var imagemPsd = (PsdImage)Image.Load(arquivoSrc))
{
    imagemPsd.Save(jpgSaida , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. Suporte de vstkResource**

{{< highlight csharp >}}
string arquivoSrc = "StrokeShapeTest1.psd";
string arquivoDst = "StrokeShapeTest2.psd";

using (PsdImage imagem = (PsdImage)Image.Load(arquivoSrc))
{
    Camada camada = imagem.Layers[1];
    foreach (LayerResource recurso in camada.Resources)
    {
        if (recurso is VstkResource)
        {
            VstkResource recursoVstk = (VstkResource)recurso;
            recursoVstk.StrokeStyleLineAlignment = StrokePosition.Outside;
            recursoVstk.StrokeStyleLineWidth = 20;
        }
    }

    imagem.Save(arquivoDst);
}
{{< /highlight >}}

**PSDNET-958. PSB para PDF falha para arquivos grandes**

{{< highlight csharp >}}
string caminhoEntrada = "SteveKohli-CarTOP.psb";
string caminhoSaida ="output.pdf";

using (var imagem = Image.Load(caminhoEntrada))
{
    imagem.Save(caminhoSaida, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. Adicionar processamento de máscara de recorte para camada de ajuste**

{{< highlight csharp >}}
string arquivoSrc = "helicopter_part.psd";
string jpgSaida = "output.jpg";

using (var imagemPsd = (PsdImage)Image.Load(arquivoSrc))
{
    imagemPsd.Save(jpgSaida , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. Após redimensionar a imagem inteira e então redimensionar a camada específica, o Aspose.PSD lança exceção ao salvar a camada**

{{< highlight csharp >}}
string arquivoOrigem = "source.psd";
string imgArquivo1 = "img1.png";
string imgArquivo2 = "img2.png";

var opcoesDeCarregamento = new PsdLoadOptions()
{
    ModoSomenteLeitura = false,
    LoadEffectsResource = true
};

using (var imagem = (PsdImagem)Image.Load(arquivoOrigem, opcoesDeCarga))
{
    // Primeiro redimensionamos a imagem inteira
    imagem.Resize(110, 90);
    var camadas = imagem.Layers;

    var camadaOk = camadas[0];
    camadaOk.Resize(100, 80);

    var camadaExcecao = camadas[1];
    camadaExcecao.Resize(100, 80);

    // Aqui tudo ocorrerá bem
    camadaOk.Save(imgArquivo1, new PngOptions() { TipoCor = PngColorType.TruecolorComAlpha });

    // Agora aqui tudo ocorrerá bem
    camadaExcecao.Save(imgArquivo2, new PngOptions() { TipoCor = PngColorType.TruecolorComAlpha });                
}
{{< /highlight >}}

**PSDNET-1346. Adicionar a propriedade editável BaselineDirection/IsStandardVerticalRomanAlignmentEnabled para a interface IText**

{{< highlight csharp >}}
// O código a seguir demonstra a capacidade de editar a nova propriedade IsStandardVerticalRomanAlignmentEnabled.
// Isso não afeta a renderização no momento, apenas permite editar o valor da propriedade.

string src = "1346test.psd";
string output = "out_1346test.psd";

using (var imagem = (PsdImage)Image.Load(src))
{
    var camadaTexto = imagem.Layers[1] as TextLayer;
    var parteTexto = camadaTexto.TextData.Items[0];
    if (parteTexto.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Leitura correta
    }
    else
    {
        throw new Exception("Leitura incorreta do valor da propriedade IsStandardVerticalRomanAlignmentEnabled");
    }

    parteTexto.Style.IsStandardVerticalRomanAlignmentEnabled = false;
    camadaTexto.TextData.UpdateLayerData();

    imagem.Save(output);
}

using (var imagem = (PsdImage)Image.Load(output))
{
    var camadaTexto = imagem.Layers[1] as TextLayer;
    var parteTexto = camadaTexto.TextData.Items[0];
    if (!parteTexto.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Leitura correta
    }
    else
    {
        throw new Exception("Leitura incorreta do valor da propriedade IsStandardVerticalRomanAlignmentEnabled");
    }
}
{{< /highlight >}}
