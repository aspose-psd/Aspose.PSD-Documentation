---
title: Notas de Lançamento Aspose.PSD para .NET 19.8
type: docs
weight: 50
url: /pt/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para o Aspose.PSD para .NET 19.8

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-184|Carregar arquivos de imagem JPEG, PNG e outros em PsdImage a partir de fluxo|Recurso|
|PSDNET-134|Implementar renderização da Camada de Preenchimento: Gradiente|Recurso|
|PSDNET-166|Salvar PSD em PDF não fornece texto selecionável|Recurso|
|PSDNET-158|Suporte para salvar PSB como PDF|Recurso|
|PSDNET-189|Alto uso de memória ao carregar PSD no Modo Somente Leitura|Melhoria|
|PSDNET-171|Após a criação de nova Camada de Texto, o arquivo PSD se tornou ilegível para o PS|Bug|
|PSDNET-156|Exceção ao carregar PSD|Bug|

## **Alterações na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **APIs Removidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Exemplos de Uso:**
**PSDNET-184. Carregar arquivos de imagem JPEG, PNG e outros em PsdImage a partir de fluxo**

{{< highlight java >}}

    // Carregar arquivos de imagem JPEG, PNG e outros em PsdImage a partir de fluxo

    string outputFilePath = "ResultadoPsd.psd";

    var listaDeArquivos = new string[]

    {

        "ExemploPsd.psd",

        "ExemploBmp.bmp",

        "ExemploGif.gif",

        "ExemploJpeg2000.jpf",

        "ExemploJpeg.jpg",

        "ExemploPng.png",

        "ExemploTiff.tif",

    };

    using (var imagem = new PsdImage(200, 200))

    {

        foreach (var nomeArquivo in listaDeArquivos)

        {

            string caminhoArquivo = nomeArquivo;

            using (var fluxo = new FileStream(caminhoArquivo, FileMode.Open))

            {

                Layer camada = null;

                try

                {

                     camada = new Layer(fluxo);

                     imagem.AddLayer(camada);

                }

                catch (Exception e)

                {

                    if (camada != null)

                    {

                        camada.Dispose();

                    }

                    throw e;

                }

            }

        }

        imagem.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. Implementar renderização da Camada de Preenchimento: Gradiente**

{{< highlight java >}}

             // Implementar renderização da Camada de Preenchimento: Gradiente

            string nomeArquivo = "CamadaPreenchimentoGradiente.psd";

            GradientType[] tiposGradiente = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var imagem = Image.Load(nomeArquivo))

            {

                PsdImage imagemPsd = (PsdImage)imagem;

                FillLayer camadaPreenchimento = (FillLayer)imagemPsd.Layers[0];

                GradientFillSettings configPreenchimento = (GradientFillSettings)camadaPreenchimento.FillSettings;

                foreach (var tipoGradiente in tiposGradiente)

                {

                    configPreenchimento.GradientType = tipoGradiente;

                    camadaPreenchimento.Update();

                    imagemPsd.Save(nomeArquivo + "_" + tipoGradiente.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. Salvar PSD em PDF não fornece texto selecionável**

{{< highlight java >}}

  // Salvar PSD em PDF não fornece texto selecionável

    string nomeArquivoFonte = "texto.psd";

    using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        string nomeArquivoSaida = "texto.pdf";

        imagem.Save(nomeArquivoSaida, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Após a criação de nova Camada de Texto, o arquivo PSD se tornou ilegível para o PS**

{{< highlight java >}}

 // Após a criação de nova Camada de Texto no Servidor de Compilação, o arquivo PSD se tornou ilegível para o PS

    string nomeArquivoFonte = "UmaCamada.psd";

    string nomeArquivoSaida = "UmaCamadaComTextoAdicionado.psd";

    using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        imagem.AddTextLayer("Algum texto", new Rectangle(50, 50, 100, 100));

        PsdOptions opcoes = new PsdOptions(imagem);

        imagem.Save(nomeArquivoSaida, opcoes);

    }

{{< /highlight >}}



**PSDNET-156. Exceção ao carregar PSD**

{{< highlight java >}}

 using (var imagem = Image.Load("Cópia_isolada.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Alto uso de memória ao carregar PSD no Modo Somente Leitura**

{{< highlight java >}}

 // Alto uso de memória do Aspose.PSD ao carregar PSD no Modo Somente Leitura

            string nomeArquivoFonte = "EfeitoTexto3D_Branco.psd";

            string nomeArquivoSaida = "Exportado.png";

            LoadOptions opcoesCarregamento = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase opcoesSalvamento = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

            {

                imagem.Save(nomeArquivoSaida, opcoesSalvamento);

            }

            double memoriaUsada = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // O uso de memória deve ser inferior a 100 MB para esses exemplos

            if (memoriaUsada > 100)

            {

                throw new Exception("Uso de memória é muito alto");

            }

{{< /highlight >}}

**PSDNET-158. Suporte para salvar PSB como PDF**

{{< highlight java >}}

 // Suporte para salvar PSB como PDF

    string nomeArquivoFonte = "exemplo.psb";

    using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        string nomeArquivoSaida = "exemplo.pdf";

        imagem.Save(nomeArquivoSaida, new PdfOptions());

    }

{{< /highlight >}}
