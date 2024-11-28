---
title: Aspose.PSD para .NET 18.8 - Notas de Lançamento
type: docs
weight: 50
url: /pt/net/aspose-psd-para-net-18-8-notas-de-lancamento/
---

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-68|Suporte da propriedade LayerCreationDateTime.|Recurso|
|PSDNET-67|Suporte do realce da cor da camada da folha.|Recurso|
|PSDNET-66|Capacidade de mesclar camadas uma com a outra.|Recurso|
|PSDNET-65|Adicionar suporte parcial da propriedade da Caixa Delimitadora da Camada de Texto.|Recurso|
|PSDNET-64|Adicionar suporte para IopaResource.|Recurso|
|PSDNET-56|Suporte de Efeitos de Camada para formato PSD.|Recurso|
|PSDNET-55|Suporte InterruptMonitor para .Net.|Recurso|
|PSDNET-50|Tornar possível a aplanar camadas.|Recurso|
|PSDNET-49|Adicionar a renderização da propriedade de opacidade de preenchimento em camadas.|Recurso|
|PSDNET-43|Implementar a renderização de Camada de Ajuste de Curvas.|Recurso|
|PSDNET-42|Adicionar suporte da Camada de Ajuste de Curvas.|Recurso|
|PSDNET-41|Implementar a renderização de Camada de Ajuste de Níveis.|Recurso|
|PSDNET-40|Adicionar suporte da Camada de Ajuste de Níveis.|Recurso|
|PSDNET-37|Adicionar suporte da Camada de Ajuste do Canal Mixer.|Recurso|
|PSDNET-35|Adicionar suporte da Camada de Ajuste de Matiz/Saturação.|Recurso|
|PSDNET-34|Implementar a renderização de Camada de Ajuste de Exposição para exportação.|Recurso|
|PSDNET-31|Adicionar suporte de renderização para exportação da Camada de Ajuste do CanalMixer.|Recurso|
|PSDNET-26|Adicionar suporte de Máscara de Recorte.|Recurso|
|PSDNET-13|Adicionar suporte da máscara de camada.|Recurso|
|PSDNET-9|Adicionar suporte da camada de ajuste Filtro de Foto.|Recurso|
|PSDNET-8|Adicionar suporte da camada de ajuste do Canal Mixer.|Recurso|
|PSDNET-7|Adicionar suporte da camada de ajuste de Exposição.|Recurso|
|PSDNET-6|Adicionar suporte da camada de ajuste de Brilho/Contraste.|Recurso|
|PSDNET-5|Adicionar suporte parcial de camadas de ajustes.|Recurso|
|PSDNET-3|Adicionar suporte para opção de Texto NoBreak do PSD.|Recurso|
|PSDNET-2|Capacidade de adicionar Camada de Texto em tempo de execução.|Recurso|
|PSDNET-62|O Codec TIFF não pode salvar imagem de canal de 16 bits.|Melhoria|
|PSDNET-61|Salvar imagem PSD produz cores de imagem inválidas.|Melhoria|
|PSDNET-60|Coordenada do canto superior esquerdo está incorreta na atualização.|Melhoria|
|PSDNET-59|Exceção ao atualizar camadas de texto.|Melhoria|
|PSDNET-58|Expor propriedade Codec de imagem JPEG2000 publicamente.|Melhoria|
|PSDNET-57|Corrigir opções de 24bpp para exportar para BMP.|Melhoria|
|PSDNET-46|Camada de ajuste ignorada para conversão PSD CMYK para TIFF ou JPG.|Melhoria|

## **Exemplos de Uso:**

**PSDNET-68 Suporte da propriedade LayerCreationDateTime**

{{< highlight java >}}
 // Exemplo da propriedade LayerCreationDateTime
string nomeArquivoFonte = "UmaCamada.psd";
using (var imagem = (PsdImage)(Image.Load(nomeArquivoFonte)))
{
    var camada = imagem.Layers[0];
    var dataHoraCriacao = camada.LayerCreationDateTime;
    var dataHoraEsperada = new DateTime(2018, 7, 17, 8, 57, 24, 769);
    Assert.AreEqual(dataHoraEsperada, dataHoraCriacao);
    var agora = DateTime.Now;
    var camadaCriada = imagem.AddLevelsAdjustmentLayer();
    // Verificar se a Data de Criação foi atualizada em novas camadas criadas
    Assert.True(agora <= camadaCriada.LayerCreationDateTime);
}
{{< /highlight >}}

**PSDNET-67 Suporte do destaque da cor da camada da folha**

{{< highlight java >}}
 // Exemplo de propriedade SheetColorHighlight
string nomeArquivoFonte = "ExemploFolhaCorDestaque.psd";
string caminhoExportacao = "ExemploFolhaCorDestaqueAlterada.psd";
using (var imagem = (PsdImage)(Image.Load(nomeArquivoFonte)))
{
    var camada1 = imagem.Layers[0];
    Assert.AreEqual(SheetColorHighlightEnum.Violet, camada1.SheetColorHighlight);
    var camada2 = imagem.Layers[1];
    Assert.AreEqual(SheetColorHighlightEnum.Orange, camada2.SheetColorHighlight);
    camada1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;
    imagem.Save(caminhoExportacao);	
}
{{< /highlight >}}

**PSDNET-66 Capacidade de mesclar camadas uma com a outra**

{{< highlight java >}}
 // Exemplo de mesclar duas camadas
var arquivoFonte1 = "ExemploOpacidadePreenchimento.psd";
var arquivoFonte2 = "TresCamadasRegularesSemiTransparentes.psd";
var caminhoExportacao = "CamadasMescladasDeDoisPsdDiferentes.psd";
using (var imagem1 = (PsdImage)(Image.Load(arquivoFonte1)))
{
    var camada1 = imagem1.Layers[1];
    using (var imagem2 = (PsdImage)(Image.Load(arquivoFonte2)))
    {
        var camada2 = imagem2.Layers[0];
        camada1.MergeLayerTo(camada2);
	    imagem2.Save(caminhoExportacao);	
    }
}
{{< /highlight >}}

**PSDNET-65 Adicionar suporte parcial da propriedade da Caixa Delimitadora da Camada de Texto**

{{< highlight java >}}
 // Exemplo de Caixa Delimitadora de Texto
string nomeArquivoFonte = "CamadaComTexto.psd";
var tamanhoCorretoOptico = new Size(127, 45);
var tamanhoCorretoCaixaDelimitadora = new Size(172, 62);
using (var imagem = (PsdImage)(Image.Load(nomeArquivoFonte)))
{
    var camadaTexto = (TextLayer)imagem.Layers[1];
    // O tamanho da camada é o tamanho da área renderizada
    var tamanhoOtico = camadaTexto.Size;
    Assert.AreEqual(tamanhoCorretoOptico, tamanhoOtico);
    // TextBoundBox é o tamanho máximo da camada para a Camada de Texto.
    // Nesta área, PS tentará ajustar seu texto
    var caixaDelimitadora = camadaTexto.TextBoundBox;
    Assert.AreEqual(tamanhoCorretoCaixaDelimitadora, caixaDelimitadora);
}
{{< /highlight >}}

**PSDNET-64 Adicionar suporte para IopaResource**

{{< highlight java >}}
 // Alterar a propriedade de opacidade de preenchimento pela mudança de IopaResource
string nomeArquivoFonte = "AmostraOpacidadePreenchimento.psd";
string caminhoExportacao = "AmostraOpacidadePreenchimentoAlterada.psd";
using (var imagem = (PsdImage)(Image.Load(nomeArquivoFonte)))
{
    var camada = imagem.Layers[2];
    var recursos = camada.Resources;
    foreach (var recurso in recursos)
    {
        if (recurso is IopaResource)
        {
            var recursoIopa = (IopaResource)recurso;
            recursoIopa.FillOpacity = 200;
        }
    }
    imagem.Save(caminhoExportacao);	
}
{{< /highlight >}}

**PSDNET-56 Suporte de Efeitos de Camada para formato PSD**

{{< highlight java >}}
 using (
    PsdImage imagem =
        (PsdImage)
        Aspose.PSD.Image.Load(
            nomeArquivoFonte,
            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()
            {
                LoadEffectsResource = true,
                UseDiskForLoadEffectsResource = true
            }))
{
    imagem.Save(
                saida,

                new Aspose.PSD.ImageOptions.PngOptions()
                {
                    ColorType =
                            Aspose.PSD.FileFormats.Png
                            .PngColorType
                            .TruecolorWithAlpha

                });
}
{{< /highlight >}}

**PSDNET-55 Suporte InterruptMonitor para .Net**

{{< highlight java >}}
         public void TesteInterruptMonitor(string diretorio, string diretorioSaida)
        {

            ImageOptionsBase opcoesSalvamento = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker trabalhador = new SaveImageWorker(diretorio + "grande.psb", diretorio + "grande_saida.png", opcoesSalvamento, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(trabalhador.ThreadProc));

            try

            {

                thread.Start();

                // O tempo limite deve ser menor do que o tempo necessário para a conversão completa da imagem (sem interrupção).

                System.Threading.Thread.Sleep(3000);
                
                // Interromper o processo

                monitor.Interrupt();

                System.Console.WriteLine("Interrompendo a thread de salvamento #{0} em {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Aguarde a interrupção...

                thread.Join();

            }

            finally

            {

                // Se o arquivo a ser excluído não existir, nenhuma exceção é lançada.

                System.IO.File.Delete(diretorio + "grande_saida.png");

            }

        }
        
        /// <summary>

        /// Inicia a conversão da imagem e aguarda sua interrupção.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// O caminho para a imagem de entrada.

            /// </summary>

            private readonly string caminhoInput;

            /// <summary>

            /// O caminho para a imagem de saída.

            /// </summary>

            private readonly string caminhoOutput;

            /// <summary>

            /// O monitor de interrupção.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// As opções de salvamento.

            /// </summary>

            private readonly ImageOptionsBase opcoesSalvamento;

            /// <summary>

            /// Inicializa uma nova instância da classe <see cref="SaveImageWorker" />.

            /// </summary>

            /// <param name="caminhoInput">O caminho para a imagem de entrada.</param>

            /// <param name="caminhoOutput">O caminho para a imagem de saída.</param>

            /// <param name="opcoesSalvamento">As opções de salvamento.</param>

            /// <param name="monitor">O monitor de interrupção.</param>

            public SaveImageWorker(string caminhoInput, string caminhoOutput, ImageOptionsBase opcoesoesSalvamento, Multithreading.InterruptMonitor monitor)
            {
                this.caminhoInput = caminhoInput;
                this.caminhoOutput = caminhoOutput;
                this.opcoesSalvamento = opcoesSalvamento;
                this.monitor = monitor;
            }

            /// <summary>

            /// Tentar converter imagem de um formato para outro. Lida com a interrupção.

            /// </summary>

            public void ThreadProc()
            {
                using (Image imagem = Image.Load(this.caminhoInput))
                {
                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;
                    try
                    {
                        imagem.Save(this.caminhoOutput, this.opcoesSalvamento);
                        Assert.Fail("Interrupção esperada.");
                    }
                    catch (CoreExceptions.OperationInterruptedException e)
                    {
                        System.Console.WriteLine("A thread de salvamento #{0} foi concluída em {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);
                        System.Console.WriteLine(e);
                    }
                    catch (System.Exception e)
                    {
                        System.Console.WriteLine(e);
                    }
                    finally
                    {
                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;
                    }
                }
            }
        }

{{< /highlight >}}

**PSDNET-50 Tornar possível a aplanar camadas**

{{< highlight java >}}
 // Aplanar todo o PSD
string nomeArquivoFonte = "TresCamadasRegularesSemiTransparentes.psd";
string caminhoExportacao = "TresCamadasRegularesSemiTransparentesAplanadas.psd";
using (var imagem = (PsdImage)(Image.Load(nomeArquivoFonte)))
{
    imagem.FlattenImage();
    imagem.Save(caminhoExportacao);	 
}

// Mesclar uma camada em outra
string nomeArquivoFonte = "TresCamadasRegularesSemiTransparentes.psd";
string caminhoExportacao = "TresCamadasRegularesSemiTransparentesAplanadasCamadaPorCamada.psd";
using (var imagem = (PsdImage)(Image.Load(nomeArquivoFonte)))
{
    var camadaInferior = imagem.Layers[0];
    var camadaMeio = imagem.Layers[1];
    var camadaSuperior = imagem.Layers[2];
    var camada1 = imagem.MergeLayers(camadaInferior, camadaMeio);
    var camada2 = imagem.MergeLayers(camada1, camadaSuperior);
    // Configurar camadas mescladas
    imagem.Layers = new Layer[] { camada2 };
    imagem.Save(caminhoExportacao);	 
}

{{< /highlight >}}

**PSDNET-49 Adicionar a renderização da propriedade de opacidade de preenchimento em camadas**

{{< highlight java >}}
 // Alterar a propriedade de opacidade de preenchimento
string nomeArquivoFonte = "AmostraOpacidadePreenchimento.psd";
string caminhoExportacao = "AmostraOpacidadePreenchimentoAlterada.psd";
using (var imagem = (PsdImage)(Image.Load(nomeArquivoFonte)))
{
    var camada = imagem.Layers[2];
    camada.FillOpacity = 5;
    imagem.Save(caminhoExportacao);	
}
{{< /highlight >}}

**PSDNET-43 Implementar a renderização de Camada de Ajuste de Curvas**

{{< highlight java >}}
 // Edição da camada de Curvas
string nomeArquivoFonte = "CamadaDeAjusteDeCurvas";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDeCurvasAlterada";
string caminhoExportacaoPng = "CamadaDeAjusteDeCurvasAlterada";
for (int j = 1; j < 2; j++)
{
    using (var imagem = LoadFile(nomeArquivoFonte + j.ToString() + ".psd"))
    {
        foreach (var camada in imagem.Layers)
	    {
            if (camada is CurvesLayer)
            {
                 var camadaCurvas = (CurvesLayer)camada;
                 if (camadaCurvas.IsDiscreteManagerUsed)
                 {
                      var gerenciador = (CurvesDiscreteManager)camadaCurvas.GetCurvesManager();
                      for (int i = 10; i < 50; i++)
                      {
                           gerenciador.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));
                      }
                 }
                 else
                 {
                      var gerenciador = (CurvesContinuousManager)camadaCurvas.GetCurvesManager();
                      gerenciador.AddCurvePoint(0, 50, 100);
                      gerenciador.AddCurvePoint(0, 150, 130);
                 }
            }
        }
    }
    // Salvar PSD
    imagem.Save(caminhoPsdAposAlteracao + j.ToString() + ".psd");
    // Salvar PNG
    var opcoesSalvamento = new PngOptions();
    opcoesSalvamento.ColorType = PngColorType.TruecolorWithAlpha;
    imagem.Save(caminhoExportacaoPng + j.ToString() + ".png", opcoesSalvamento);
}
{{< /highlight >}}

**PSDNET-42 Adicionar suporte da Camada de Ajuste de Curvas**

{{< highlight java >}}
 // Edição da camada de Curvas
string nomeArquivoFonte = "CamadaDeAjusteDeCurvas";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDeCurvasAlterada";
for (int j = 1; j < 2; j++)
{
    using (var imagem = LoadFile(nomeArquivoFonte + j.ToString() + ".psd"))
    {
         foreach (var camada in imagem.Layers)
	 {
            if (camada is CurvesLayer)
            {
                 var camadaCurvas = (CurvesLayer)camada;
                 if (camadaCurvas.IsDiscreteManagerUsed)
                 {
                      var gerenciador = (CurvesDiscreteManager)camadaCurvas.GetCurvesManager();
                      for (int i = 10; i < 50; i++)
                      {
                           gerenciador.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));
                      }
                 }
                 else
                 {
                      var gerenciador = (CurvesContinuousManager)camadaCurvas.GetCurvesManager();
                      gerenciador.AddCurvePoint(0, 50, 100);
                      gerenciador.AddCurvePoint(0, 150, 130);
                 }
            }
	}
    }
    // Salvar PSD
    imagem.Save(caminhoPsdAposAlteracao + j.ToString() + ".psd");
}
{{< /highlight >}}

**PSDNET-41 Implementar a renderização de Camada de Ajuste de Níveis**

{{< highlight java >}}
 // Edição da camada de Níveis
string nomeArquivoFonte = "CamadaDeAjusteDeNiveis.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDeNiveisAlterada.psd";
string caminhoExportacaoPng = "CamadaDeAjusteDeNiveisAlterada.png";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    foreach (var camada in imagem.Layers)
    {
        if (camada is LevelsLayer)
        {
            var camadaNiveis = (LevelsLayer)camada;
            var canal = camadaNiveis.GetChannel(0);
            canal.InputMidtoneLevel = 2.0f;
            canal.InputShadowLevel = 10;
            canal.InputHighlightLevel = 230;
            canal.OutputShadowLevel = 20;
            canal.OutputHighlightLevel = 200;
        }
    }
    // Salvar PSD
    imagem.Save(caminhoPsdAposAlteracao);
    // Salvar PNG
    var opcoesSalvamento = new PngOptions();
    opcoesSalvamento.ColorType = PngColorType.TruecolorWithAlpha;
    imagem.Save(caminhoExportacaoPng, opcoesSalvamento);
}
{{< /highlight >}}

**PSDNET-40 Adicionar suporte da Camada de Ajuste de Níveis**

{{< highlight java >}}
 // Edição da camada de Níveis
string nomeArquivoFonte = "CamadaDeAjusteDeNiveis.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDeNiveisAlterada.psd";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    foreach (var camada in imagem.Layers)
    {
        if (camada is LevelsLayer)
        {
            var camadaNiveis = (LevelsLayer)camada;
            var canal = camadaNiveis.GetChannel(0);
            canal.InputMidtoneLevel = 2.0f;
            canal.InputShadowLevel = 10;
            canal.InputHighlightLevel = 230;
            canal.OutputShadowLevel = 20;
            canal.OutputHighlightLevel = 200;
        }
    }
    // Salvar PSD
    imagem.Save(caminhoPsdAposAlteracao);
}
{{< /highlight >}}

**PSDNET-37 Adicionar suporte da Camada de Ajuste do Canal Mixer**

{{< highlight java >}}
// Misturador de Canal Rgb
string nomeArquivoFonte = "CamadaDeAjusteDoMisturadorDeCanalRgb.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDoMisturadorDeCanalRgbAlterada.psd";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    foreach (var camada in imagem.Layers)
    {
         if (camada is RgbChannelMixerLayer)
         {
              var camadaRgb = (RgbChannelMixerLayer)camada;
              camadaRgb.RedChannel.Blue = 100;
              camadaRgb.BlueChannel.Green = -100;
              camadaRgb.GreenChannel.Constant = 50;
         }
    }
    imagem.Save(caminhoPsdAposAlteracao);
}

// Misturador de Canal Cmyk
string nomeArquivoFonte = "CamadaDeAjusteDoMisturadorDeCanalCmyk.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDoMisturadorDeCanalCmykAlterada.psd";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    foreach (var camada in imagem.Layers)
    {
         if (camada is CmykChannelMixerLayer)
         {
             var camadaCmyk = (CmykChannelMixerLayer)camada;
             camadaCmyk.CyanChannel.Black = 20;
             camadaCmyk.MagentaChannel.Yellow = 50;
             camadaCmyk.YellowChannel.Cyan = -25;
             camadaCmyk.BlackChannel.Yellow = 25;
         }
    }
    imagem.Save(caminhoPsdAposAlteracao);
}

// Adicionando nova camada (Cmyk para este exemplo)
string nomeArquivoFonte = "CmykComAlfa.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDoMisturadorDeCanalCmykAlterada.psd";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    var novaCamada = imagem.AddChannelMixerAdjustmentLayer();
    novaCamada.GetChannelByIndex(2).Constant = 50;
    novaCamada.GetChannelByIndex(0).Constant = 50;
    imagem.Save(caminhoPsdAposAlteracao);
}		
{{< /highlight >}}

**PSDNET-35 Adicionar suporte da Camada de Ajuste de Matiz/Saturação**

{{< highlight java >}}
 // Edição da camada de Matiz/Saturação
string nomeArquivoFonte = "CamadaDeAjusteDeMatizSaturacao.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDeMatizSaturacaoAlterada.psd";
using (var imagem = LoadFile(nomeArquivoFonte))
{
     foreach (var camada in imagem.Layers)
     {
           if (camada is HueSaturationLayer)
           {
                var camadaMatiz = (HueSaturationLayer)camada;
                camadaMatiz.Hue = -25;
                camadaMatiz.Saturation = -12;
                camadaMatiz.Lightness = 67;
                var faixaDeCor = camadaMatiz.GetRange(2);
                faixaDeCor.Hue = -40;
                faixaDeCor.Saturation = 50;
                faixaDeCor.Lightness = -20;
                faixaDeCor.MostLeftBorder = 300;
           }

      }
      imagem.Save(caminhoPsdAposAlteracao);
}
{{< /highlight >}}

**PSDNET-34 Implementar a renderização de Camada de Ajuste de Exposição para exportação**

{{< highlight java >}}
 // Edição da camada de Exposição
string nomeArquivoFonte = "CamadaDeAjusteDeExposicao.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDeExposicaoAlterada.psd";
string caminhoExportacaoPng = "CamadaDeAjusteDeExposicaoAlterada.png";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    foreach (var camada in imagem.Layers)
    {
        if (camada is ExposureLayer)
        {
	    var camadaExp = (ExposureLayer)camada;
            camadaExp.Exposure = 2;
            camadaExp.Offset = -0.25f;
            camadaExp.GammaCorrection = 0.5f;
        }
    }
    // Salvar PSD
    imagem.Save(caminhoPsdAposAlteracao);
    // Salvar PNG
    var opcoesSalvamento = new PngOptions();
    opcoesSalvamento.ColorType = PngColorType.TruecolorWithAlpha;
    imagem.Save(caminhoExportacaoPng, opcoesSalvamento);
}

// Adição da camada de Exposição
string nomeArquivoFonte = "ExemploFoto.psd";
string caminhoPsdAposAlteracao = "ExemploFotoAdicionadaExposicao.psd";
string caminhoExportacaoPng = "ExemploFotoAdicionadaExposicao.png";
using (PsdImage imagem = LoadFile(nomeArquivoFonte))
{
     var novaCamada = imagem.AddExposureAdjustmentLayer();
     novaCamada.Exposure = 2;
     novaCamada.Offset = -0.25f;
     novaCamada.GammaCorrection = 2f;
     // Salvar PSD
     imagem.Save(caminhoPsdAposAlteracao);
     // Salvar PNG
     var opcoesSalvamento = new PngOptions();
     opcoesSalvamento.ColorType = PngColorType.TruecolorWithAlpha;
    imagem.Save(caminhoExportacaoPng, opcoesSalvamento);
}

{{< /highlight >}}

**PSDNET-31 Adicionar suporte de renderização para exportação da Camada de Ajuste do CanalMixer**

{{< highlight java >}}
// Misturador de Canal Rgb
string nomeArquivoFonte = "CamadaDeAjusteDoMisturadorDeCanalRgb.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDoMisturadorDeCanalRgbAlterada.psd";
string caminhoExportacaoPng = "CamadaDeAjusteDoMisturadorDeCanalRgbAlterada.png";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    foreach (var camada in imagem.Layers)
    {
         if (camada is RgbChannelMixerLayer)
         {
              var camadaRgb = (RgbChannelMixerLayer)camada;
              camadaRgb.RedChannel.Blue = 100;
              camadaRgb.BlueChannel.Green = -100;
              camadaRgb.GreenChannel.Constant = 50;
         }
    }
    // Salvar PSD
    imagem.Save(caminhoPsdAposAlteracao);
    // Salvar PNG
    var opcoesSalvamento = new PngOptions();
    opcoesSalvamento.ColorType = PngColorType.TruecolorWithAlpha;
    imagem.Save(caminhoExportacaoPng, opcoesSalvamento);
}

// Misturador de Canal Cmyk
string nomeArquivoFonte = "CamadaDeAjusteDoMisturadorDeCanalCmyk.psd";
string caminhoPsdAposAlteracao = "CamadaDeAjusteDoMisturadorDeCanalCmykAlterada.psd";
string caminhoExportacaoPng = "CamadaDeAjusteDoMisturadorDeCanalCmykAlterada.png";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    foreach (var camada in imagem.Layers)
    {
         if (camada is CmykChannelMixerLayer)
         {
             var camadaCmyk = (CmykChannelMixerLayer)camada;
             camadaCmyk.CyanChannel.Black = 20;
             camadaCmyk.MagentaChannel.Yellow = 50;
             camadaCmyk.YellowChannel.Cyan = -25;
             camadaCmyk.BlackChannel.Yellow = 25;
         }
    }
    // Salvar PSD
    imagem.Save(caminhoPsdAposAlteracao);
    // Salvar PNG
    var opcoesSalvamento = new PngOptions();
    opcoesSalvamento.ColorType = PngColorType.TruecolorWithAlpha;
    imagem.Save(caminhoExportacaoPng, opcoesSalvamento);
}


{{< /highlight >}}

**PSDNET-26 Adicionar suporte de Máscara de Recorte**

{{< highlight java >}}
 // Exportar o psd com uma máscara de recorte complexa
string nomeArquivoFonte = "MascaraDeRecorteComplexa.psd";
string caminhoExportacao = "MascaraDeRecorteComplexa.png";
using (var imagem = LoadFile(nomeArquivoFonte))
{
    // Exportar para PNG