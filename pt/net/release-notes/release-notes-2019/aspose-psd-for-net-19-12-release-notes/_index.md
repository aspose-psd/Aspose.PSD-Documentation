---
title: Aspose.PSD para .NET 19.12 - Notas de Lançamento
type: docs
weight: 10
url: /pt/net/aspose-psd-para-net-19-12-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-11|[Suporte de Camada Linkada](/pt/psd/net/trabalhando-com-camadas/#trabalhandocomcamadas-suportedecamadaslinkadas)|Recurso|
|PSDNET-131|[Suporte de Recurso SoCo](/pt/psd/net/suporte-de-socoresource/)|Recurso|
|PSDNET-115|Quebras de Linha são adicionadas a Quebras de Linha existentes se a Camada de Texto for atualizada com uma sequência|Erro|
|PSDNET-157|Salvar PSB como PNG congela|Erro|
|PSDNET-250|Exceção ao carregar arquivo PSD CMYK sem camadas com compressão RLE|Erro|
|PSDNET-161|Exceção ao atualizar camadas de texto|Erro|
|PSDNET-222|Redimensionar alguns arquivos PSD com máscaras de camada funciona incorretamente|Erro|
|PSDNET-244|Salvar PSD com algumas Globalization.CultureInfo.CurrentCulture leva a exceções ao carregar|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **APIs Removidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Exemplos de Uso:**
**PSDNET-11. Suporte de Camada Linkada**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("exemplo.psd"))

            {

                Layer[] camadas = psd.Layers;

                // vincular todas as camadas em um grupo vinculado

                short groupIdDeCamadas = psd.LinkedLayersManager.LinkLayers(camadas);

                // obter id para uma camada

                short groupIdVinculado = psd.LinkedLayersManager.GetLinkGroupId(camadas[0]);

                if (groupIdDeCamadas != groupIdVinculado)

                {

                    throw new Exception("groupIdDeCamadas e groupIdVinculado não são iguais.");

                }

                // obter todas as camadas vinculadas pelo id do grupo de ligação.

                Layer[] camadasVinculadas = psd.LinkedLayersManager.GetLayersByLinkGroupId(groupIdVinculado);

                // desvincular cada camada do grupo

                foreach (var camadaVinculada in camadasVinculadas)

                {

                    psd.LinkedLayersManager.UnlinkLayer(camadaVinculada);

                }

                // obter NULL para um ID de grupo de link que não possui camadas no grupo.

                camadasVinculadas = psd.LinkedLayersManager.GetLayersByLinkGroupId(groupIdVinculado);

                if (camadasVinculadas != null)

                {

                    throw new Exception("O campo camadasVinculadas não é NULO.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. Suporte de Recurso SoCo**

{{< highlight java >}}

      // Suporte de Recurso SoCo

    string nomeDoArquivoFonte = "CamadaDePreenchimentoDeCor.psd";

    string caminhoExportacao = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(nomeDoArquivoFonte);

    using (im)

    {

        foreach (var camada in im.Layers)

        {

            if (camada is FillLayer)

            {

                var camadaPreenchimento = (FillLayer)camada;

                foreach (var recurso in camadaPreenchimento.Resources)

                {

                    if (recurso is SoCoResource)

                    {

                        var recursoSoCo = (SoCoResource)recurso;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), recursoSoCo.Color);

                        recursoSoCo.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(caminhoExportacao);

        }

    }

{{< /highlight >}}

**PSDNET-115. Quebras de Linha são adicionadas a Quebras de Linha existentes se a Camada de Texto for atualizada com uma sequência**

{{< highlight java >}}

           const string NovoTexto = "abcdef\rzxcvbn";

        string caminhoArquivoFonte = "ArquivoDeTesteParaCaracteresAsiáticos.psd");

        string caminhoArquivoSaida = "resultado.psd";

        using (var imagem = (PsdImage)Image.Load(caminhoArquivoFonte))

        {

            var camada = (TextLayer)imagem.Layers[0];

            var opcoesImagem = new PsdOptions(imagem);

            camada.UpdateText(NovoTexto);

            imagem.Save(caminhoArquivoSaida, opcoesImagem);

        }

        using (var imagemCriada = (PsdImage)Image.Load(caminhoArquivoSaida))

        {

            var camadaCriada = (TextLayer)imagemCriada.Layers[0];

            if (NovoTexto != camadaCriada.Text)

            {

                throw new InvalidDataException("O texto atualizado é inválido");

            }

        }

{{< /highlight >}}

**PSDNET-157. Salvar PSB como PNG congela**

{{< highlight java >}}

       // Salvar PSB como PNG

    string nomeArquivoFonte = "amostra.psb";

    string nomeArquivoSaida = "amostra.png";

    using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        PngOptions opcoes = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        imagem.Save(nomeArquivoSaida, opcoes);

    }

{{< /highlight >}}



` `**PSDNET-250. Exceção ao carregar arquivo PSD CMYK sem camada com compressão RLE**

{{< highlight java >}}

     void CarregarDadosBrutosDoPsd()

        {

            string caminhoFonte = "CyanMagentaYellowBlackComAlpha.psd";

            using (RasterImage imagem = (RasterImage)Image.Load(caminhoFonte))

            {

                var configuracoesDadosBrutos = imagem.RawDataSettings;

                RawDataTester carregador = new RawDataTester();

                imagem.LoadRawData(imagem.Bounds, configuracoesDadosBrutos, carregador);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle retângulo, byte[] pixels, Point inicio, Point fim)

            {

            }

            public void Process(Rectangle retângulo, byte[] pixels, Point inicio, Point fim, LoadOptions opçõesCarregamento)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. Exceção ao atualizar camadas de texto**

{{< highlight java >}}

      // Carregar um arquivo PSD como uma imagem e convertê-lo em PsdImage

    using (PsdImage imagemPsd = (PsdImage)Image.Load("exemplo.psd"))

    {

        foreach (var camada in imagemPsd.Layers)

        {

            if (camada is TextLayer)

            {

                TextLayer camadaTexto = camada as TextLayer;

                camadaTexto.UpdateText("atualização de teste", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        imagemPsd.Save("AtualizarCamadaDeTextoNoArquivoPSD_saida.psd");

    }

{{< /highlight >}}



**PSDNET-222. Redimensionar alguns arquivos PSD com máscaras de camada funciona incorretamente**

{{< highlight java >}}

     int escala = 2;

        string[] nomes = {

                             "UmaRegularEUmAjusteComVetorELayerMask",

                             "CamadaDeNíveisComLayerMaskRgb",

                             "CamadaDeNíveisComLayerMaskCmyk",

                             "CamadaDeAjusteBalançoDeCores"

                         };

        for (int i = 0; i < nomes.Length; i++)

        {

            string caminhoArquivoFonte = nomes[i] + ".psd";

            string caminhoArquivoSaida = "saida_" + caminhoArquivoFonte;

            string caminhoPngSaida = "saida_" + nomes[i] + ".png";

            var opcoesCarregamentoPsd = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage imagem = (PsdImage)Image.Load(caminhoArquivoFonte, opcoesCarregamentoPsd))

            {

                imagem.Resize(imagem.Width * escala, imagem.Height * escala);

                imagem.Save(caminhoArquivoSaida, new PsdOptions());

                imagem.Save(caminhoPngSaida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. Salvar PSD com algumas Globalization.CultureInfo.CurrentCulture leva a exceções ao carregar**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string nomeArquivoFonte = string.Format("exemplo-{0}.psd", i);

            var opcoesCarregamentoPsd = new PsdLoadOptions() { LoadEffectsResource = true };

            var opcoesSalvamentoPsd = new PsdOptions();

            var cultura = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultura;

            System.Threading.Thread.CurrentThread.CurrentUICulture = cultura;

            string nomeArquivoSaida = "saida-" + nomeArquivoFonte;

            // Carregar um arquivo PSD como uma imagem e convertê-lo em PsdImage

            using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte, opcoesCarregamentoPsd))

            {

                imagem.Resize(160, 120);

                imagem.Save(nomeArquivoSaida, opcoesSalvamentoPsd);

            }

            cultura = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultura;

            System.Threading.Thread.CurrentThread.CurrentUICulture = cultura;

            // Carregar um arquivo PSD como uma imagem e convertê-lo em PsdImage

            using (PsdImage imagem2 = (PsdImage)Image.Load(nomeArquivoFonte, opcoesCarregamentoPsd))

            {

                imagem2.Resize(160, 120);

                imagem2.Save(nomeArquivoSaida, opcoesSalvamentoPsd);

            }

        }

{{< /highlight >}}
