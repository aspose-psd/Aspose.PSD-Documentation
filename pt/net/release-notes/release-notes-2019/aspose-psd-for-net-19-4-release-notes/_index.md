---
title: Notas de Lançamento do Aspose.PSD para .NET 19.4
type: docs
weight: 90
url: /pt/net/aspose-psd-para-net-19-4-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para o Aspose.PSD para .NET 19.4

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-87|Criar recurso para carregar arquivos de imagem JPEG/PNG/etc no PsdImage sem carregamento direto (que não é suportado no Aspose.PSD)|Recurso|
|PSDNET-120|Suporte para modo de Cor RGB com 16 bits/canal (64 bits por cor)|Recurso|
|PSDNET-108|Suporte de Máscaras de Vetor de Camada e Rotação Personalizada de Texto de Camada|Recurso|
|PSDNET-99|Todos os caracteres asiáticos não são renderizados corretamente|Erro|
|PSDNET-116|Os símbolos \r\n são interpretados como quebra de linha dupla, o que está incorreto|Erro|
|PSDNET-117|Se a Camada de Texto for atualizada com uma string contendo quebras de linha, o arquivo PSD se torna ilegível|Erro|
|PSDNET-118|Se a Camada de Texto for atualizada com uma string contendo símbolos de tabulação, o processamento falha com exceção|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
# **APIs Removidas:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
...
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)

## **Exemplos de Uso:**
**PSDNET-87. Criar recurso para carregar arquivos de imagem JPEG/PNG/etc no PsdImage sem carregamento direto (que não é suportado no Aspose.PSD)**

{{< highlight java >}}

 string caminhoDoArquivo = "ExemploPsd.psd";

string caminhoDeSaida = "ResultadoPsd.psd";

using(var imagem = new PsdImage(200, 200)) {

 using(var im = Image.Load(caminhoDoArquivo)) {

  Layer camada = null;

  try {

   camada = new Layer((RasterImage) im);

   imagem.AddLayer(camada);

  } catch (Exception e) {

   if (camada != null) {

    camada.Dispose();

   }

   throw;

  }

 }

 imagem.Save(caminhoDeSaida);

}  

{{< /highlight >}}

**PSDNET-120. Suporte para modo de Cor RGB com 16 bits/canal (64 bits por cor)**

{{< highlight java >}}

  // Suporte para modo de Cor RGB com 16 bits/canal (64 bits por cor)

string nomeDoArquivoFonte = "inRgb16.psd.psd";

string caminhoArquivoSaidaJpg = "outRgb16.jpg";

string caminhoArquivoSaidaPsd = "outRgb16.psd";

var opcoes = new PsdLoadOptions();

using(PsdImage imagem = (PsdImage) Image.Load(nomeDoArquivoFonte, opcoes)) {

 imagem.Save(caminhoArquivoSaidaPsd, new PsdOptions(imagem));

 imagem.Save(caminhoArquivoSaidaJpg, new JpegOptions() {

  Qualidade = 100

 });

}

// Os arquivos devem ser abertos sem exceção e legíveis para o Photoshop

using(Image imagem = Image.Load(caminhoArquivoSaidaPsd)) {}  

{{< /highlight >}}

**PSDNET-108. Suporte de Máscaras de Vetor de Camada e Rotação Personalizada de Texto de Camada**

{{< highlight java >}}

 // A operação RotateFlip não funciona conforme o esperado com PSD

var arquivoFonte = "1.psd";

var caminhoPng = "TesteRotateFlip2617.png";

var caminhoPsd = "TesteRotateFlip2617.psd";

var tipoRotação = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(arquivoFonte))) {

 im.RotateFlip(tipoRotação);

 im.Save(caminhoPng, new PngOptions() {

  TipoCor = PngColorType.TruecolorWithAlpha

 });

 im.Save(caminhoPsd);

}

{{< /highlight >}}

**PSDNET-99. Todos os caracteres asiáticos não são renderizados corretamente**

[**Por favor, verifique o exemplo anexado**](attachments/86278147/86343681.cs)

**PSDNET-116. Os símbolos \r\n são interpretados como quebra de linha dupla, o que está incorreto**

{{< highlight java >}}

 // Os símbolos \r\n são interpretados como quebra de linha dupla, o que está incorreto

string nomeDoArquivoFonte = "TesteTexto.psd";

string caminhoExportação = "Resultado.psd";

using(Image imagem = Image.Load(nomeDoArquivoFonte)) {

 if (!(imagem is PsdImage)) {

  return;

 }

 PsdImage psdImagem = (PsdImage) imagem;

 Layer[] camadas = psdImagem.Layers;

 for (int indice = camadas.Length - 1; indice >= 0; indice--) {

  Layer camada = camadas[indice];

  if (!(camada is TextLayer)) {

   continue;

  }

  TextLayer camadaTexto = (TextLayer) camada;

  camadaTexto.UpdateText("Primeiro Parágrafo\r\nSegundo Parágrafo\rTerceiro parágrafo\nQuarto Parágrafo");

 }

 PsdOptions opçõesImagem = new PsdOptions(psdImagem);

 psdImagem.Save(caminhoExportação, opçõesImagem);

}

// O arquivo deve ser aberto sem exceção e deve ser legível para o Photoshop. Deve conter 3 quebras de linha, uma entre cada linha

using(Image imagem = Image.Load(caminhoExportação)) {}

{{< /highlight >}}

**PSDNET-117. Se a Camada de Texto for atualizada com uma string que contém quebras de linha, o arquivo PSD se torna ilegível**

{{< highlight java >}}

 // Se a Camada de Texto for atualizada com uma string que contém quebras de linha, o arquivo PSD se torna ilegível

string nomeDoArquivoFonte = "TesteTexto.psd";

string caminhoExportação = "Resultado.psd";

using(Image imagem = Image.Load(nomeDoArquivoFonte)) {

 if (!(imagem is PsdImage)) {

  return;

 }

 PsdImage psdImagem = (PsdImage) imagem;

 Layer[] camadas = psdImagem.Layers;

 for (int indice = camadas.Length - 1; indice >= 0; indice--) {

  Layer camada = camadas[indice];

  if (!(camada is TextLayer)) {

   continue;

  }

  TextLayer camadaTexto = (TextLayer) camada;

  camadaTexto.UpdateText("Primeiro Parágrafo\r\nSegundo Parágrafo\r\nTerceiro parágrafo\r\nQuarto Parágrafo");

 }

 PsdOptions opçõesImagem = new PsdOptions(psdImagem);

 psdImagem.Save(caminhoExportação, opçõesImagem);

}

// O arquivo deve ser aberto sem exceção e deve ser legível para o Photoshop

using(Image imagem = Image.Load(caminhoExportação)) {}

{{< /highlight >}}

**PSDNET-118. Se a Camada de Texto for atualizada com uma string que contém símbolos de tabulação, o processamento falha com exceção**

{{< highlight java >}}

 // Se a Camada de Texto for atualizada com uma string que contém símbolos de tabulação, o processamento falha com exceção

string nomeDoArquivoFonte = "TesteTexto.psd";

string caminhoExportação = "Resultado.psd";

using(Image imagem = Image.Load(nomeDoArquivoFonte)) {

 if (!(imagem is PsdImage)) {

  return;

 }

 PsdImage psdImagem = (PsdImage) imagem;

 Layer[] camadas = psdImagem.Layers;

 for (int indice = camadas.Length - 1; indice >= 0; indice--) {

  Layer camada = camadas[indice];

  if (!(camada is TextLayer)) {

   continue;

  }

  TextLayer camadaTexto = (TextLayer) camada;

  camadaTexto.UpdateText("Texto de Início\tTexto Após Tabulação");

 }

 PsdOptions opçõesImagem = new PsdOptions(psdImagem);

 psdImagem.Save(caminhoExportação, opçõesImagem);

}

// O arquivo deve ser aberto sem exceção e deve ser legível para o Photoshop

using(Image imagem = Image.Load(caminhoExportação)) {}

{{< /highlight >}}