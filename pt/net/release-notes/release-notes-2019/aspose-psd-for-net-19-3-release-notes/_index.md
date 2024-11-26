---
title: Notas da Versão Aspose.PSD para .NET 19.3
type: docs
weight: 100
url: /pt/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém notas da versão para Aspose.PSD para .NET 19.3

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-104|Renderização de Camadas de Texto Rotacionadas por TransformMatrix|Recurso|
|PSDNET-96|Implementar renderização do efeito Stroke com Preenchimento de Cor para exportação|Recurso|
|PSDNET-112|Transformadores de InnerData corrompem algumas camadas com máscaras vetoriais|Erro|
|PSDNET-113|Atualizar camada de texto para imagem PSD gera erro ao ser aberto no Photoshop|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- Nenhuma
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-104. Renderização de Camadas de Texto Rotacionadas por TransformMatrix**

{{< highlight java >}}

 string nomeArquivoFonte = "TextoTransformado.psd";

string caminhoExportacao = "ExportacaoTextoTransformado.psd";

string caminhoExportacaoPng = "ExportacaoTextoTransformado.png";

var im = (PsdImage) Image.Load(nomeArquivoFonte);

using(im) {

 im.Save(caminhoExportacao);

 im.Save(caminhoExportacaoPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Implementar renderização do efeito Stroke com Preenchimento de Cor para exportação**

{{< highlight java >}}

  // Implementar renderização do efeito Stroke com Preenchimento de Cor para exportação

 string nomeArquivoFonte = "ContornoComplexo.psd";

 string caminhoExportacao = "RenderizacaoContornoComplexo.psd";

 string caminhoExportacaoPng = "RenderizacaoContornoComplexo.png";

 var loadOptions = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(nomeArquivoFonte, loadOptions)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var efeito = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var configuracoes = (ColorFillSettings) efeito.FillSettings;

   configuracoes.Color = Color.DeepPink;

  }

  // Salvar psd

  im.Save(caminhoExportacao, new PsdOptions());

  // Salvar png

  im.Save(caminhoExportacaoPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Transformadores de InnerData corrompem algumas camadas com máscaras vetoriais**

{{< highlight java >}}

 // Transformadores de InnerData corrompem algumas camadas com máscaras vetoriais

var arquivoFonte = "1.psd";

var caminhoPng = "TesteRotacaoInversao2617.png";

var caminhoPsd = "TesteRotacaoInversao2617.psd";

var tipoRotacao = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(arquivoFonte))) {

 im.RotateFlip(tipoRotacao);

 im.Save(caminhoPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(caminhoPsd);

}

{{< /highlight >}}

**PSDNET-113. Atualizar camada de texto para imagem PSD gera erro ao ser aberto no Photoshop**

{{< highlight java >}}

 string nomeArquivoFonte = "Teste.psd";

string caminhoExportacao = "Resultado.psd";

using(Image imagem = Image.Load(nomeArquivoFonte)) {

 if (!(imagem is PsdImage)) {

  return;

 }

 PsdImage imagemPsd = (PsdImage) imagem;

 Layer[] camadas = imagemPsd.Layers;

 for (int indice = camadas.Length - 1; indice >= 0; indice--) {

  Layer camada = camadas[indice];

  if (!(camada is TextLayer)) {

   continue;

  }

  TextLayer camadaTexto = (TextLayer) camada;

  camadaTexto.UpdateText("\\()");

 }

 PsdOptions opcoesImagem = new PsdOptions(imagemPsd);

 imagemPsd.Save(caminhoExportacao, opcoesImagem);

}

// O arquivo deve ser aberto sem exceções e deve ser legível para o Photoshop

using(Image imagem = Image.Load(caminhoExportacao)) {}

{{< /highlight >}}
