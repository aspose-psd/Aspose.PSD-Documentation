---
title: Aspose.PSD para .NET 20.2 - Notas de Lançamento
type: docs
weight: 110
url: /pt/net/aspose-psd-para-net-20-2-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para  [Aspose.PSD para .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-206|Melhoria da capacidade de renderizar texto de cores diferentes na Camada de Texto|Recurso|
|PSDNET-369|Suporte para recurso clbl (Recurso da Camada contém informações sobre elementos de clipe de mistura)|Recurso|
|PSDNET-274 |Suporte para recurso blwh (Recurso contém Dados da Camada de Ajuste de Preto e Branco)|Recurso|
|PSDNET-230|Capacidade de exportar Grupo de Camadas para Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Recurso|
|PSDNET-372|Suporte para recurso lspf (Contém configurações sobre configuração de Camada Protegida)|Recurso|
|PSDNET-370|Suporte para recurso infx (Contém dados sobre Mistura de elementos interiores)|Recurso|
|PSDNET-251|Refatoração de PsdImage e Camada para alterar o comportamento de Transformação (Redimensionamento/Rotação/Corte corretos para máscaras de camada se transformarmos uma camada separadamente)|Aprimoramento|
|PSDNET-276 |Em algumas configurações de globalização, a imagem raster AI não pode ser aberta|Erro|
|PSDNET-194|Após realizar a operação FlipRotate na Camada, a Imagem PSD se torna ilegível|Erro|
|PSDNET-177. |System.ArgumentException durante o carregamento do arquivo PSD|Erro|
|PSDNET-249|Após usar um método de transformação apenas para uma camada, a camada salva tem limites incorretos ou uma máscara|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykColor.Equals(System.Object)
- T:Aspose.PSD.CompositeException
- T:Aspose.PSD.CoreExceptions.IndexOutOFRangeException
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String)
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String,System.Exception)
- F:Aspose.PSD.FileFormat.Otg
- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000CustomException
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.IsDataStoredDiscretely
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetChannelData(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey
- T:Aspose.PSD.ImageOptions.TiffOptionsUtils
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])
- P:Aspose.PSD.ImageOptionsBase.ProgressEventHandler
- P:Aspose.PSD.LoadOptions.ProgressEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Metered.Equals(System.Object)
- T:Aspose.PSD.ProgressEventHandler
- T:Aspose.PSD.ProgressManagement.EventType
- F:Aspose.PSD.ProgressManagement.EventType.RelativeProgress
- F:Aspose.PSD.ProgressManagement.EventType.StageChange
- F:Aspose.PSD.ProgressManagement.EventType.Initialization
- F:Aspose.PSD.ProgressManagement.EventType.PreProcessing
- F:Aspose.PSD.ProgressManagement.EventType.Processing
- F:Aspose.PSD.ProgressManagement.EventType.Finalization
- T:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Description
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.EventType
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.MaxValue
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Value
- M:Aspose.PSD.RasterImage.GetSkewAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Color)
# **APIs Removidas:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues

## **Exemplos de uso:**
**PSDNET-206. Melhoria da capacidade de renderizar texto de cores diferentes na Camada de Texto**

{{< highlight java >}}

  using (var imagemPsd = (PsdImage)Image.Load("texto_etalon_cores_diferentes.psd"))

{

    var camadaTexto = (TextLayer)imagemPsd.Layers[1];

    camadaTexto.TextData.UpdateLayerData();

    imagemPsd.Save("saida.png", new PngOptions());

}

{{< /highlight >}}

**PSDNET-369. Suporte para recurso clbl (Recurso da Camada contém informações sobre elementos de clipe de mistura)**

{{< highlight java >}}

        void AssertIsTrue(bool condicao, string mensagem)

        {

            if (!condicao)

            {

                throw new FormatException(mensagem);

            }

        }

        string arquivoFonte = "AmostraParaRecurso.psd";

        string arquivoDestino = "Saída" + arquivoFonte;

        ClblResource GetClblResource(PsdImage im)

        {

            foreach (var camada in im.Layers)

            {

                foreach (var recursoCamada in camada.Resources)

                {

                    if (recursoCamada is ClblResource)

                    {

                        return (ClblResource)recursoCamada;

                    }

                }

            }

            throw new Exception("O ClblResource especificado não foi encontrado");

        }

        using (PsdImage im = (PsdImage)Image.Load(arquivoFonte))

        {

            var recurso = GetClblResource(im);

            AssertIsTrue(recurso.BlendClippedElements, "O ClblResource.BlendClippedElements deve ser verdadeiro");

            // Teste de edição e salvamento

            recurso.BlendClippedElements = false;

            im.Save(arquivoDestino);

        }

        using (PsdImage im = (PsdImage)Image.Load(arquivoDestino))

        {

            var recurso = GetClblResource(im);

            AssertIsTrue(!recurso.BlendClippedElements, "O ClblResource.BlendClippedElements deve mudar para falso");

        }

{{< /highlight >}}

**PSDNET-274. Suporte para recurso blwh (Recurso contém Dados da Camada de Ajuste de Preto e Branco)**

{{< highlight java >}}

         const string MensagemValorAtualIncorreto = "O valor da propriedade esperado não é igual ao valor atual";

        void AssertIsTrue(bool condicao, string mensagem)

        {

            if (!condicao)

            {

                throw new FormatException(mensagem);

            }

        }

        void ExemploSuporteDeRecursoBlwh(

            string arquivoFonte,

            int vermelhos,

            int amarelos,

            int verdes,

            int cianos,

            int azuis,

            int magentas,

            bool usarTonalidade,

            int tipoPresetPretoBranco,

            string nomePresetPretoBranco,

            double tonalidadeVermelha,

            double tonalidadeVerde,

            double tonalidadeAzul,

            int tonalidade,

            int novaTonalidade)

        {

            string arquivoDestino = "Saída" + arquivoFonte;

            bool recursoRequeridoEncontrado = false;

            using (PsdImage im = (PsdImage)Image.Load(arquivoFonte))

            {

                foreach (var camada in im.Layers)

                {

                    foreach (var recursoCamada in camada.Resources)

                    {

                        if (recursoCamada is BlwhResource)

                        {

                            var recursoBlwh = (BlwhResource)recursoCamada;

                            var camadaBlwh = (BlackWhiteAdjustmentLayer)camada;

                            recursoRequeridoEncontrado = true;

                            AssertIsTrue(recursoBlwh.Reds == vermelhos, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Yellows == amarelos, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Greens == verdes, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Cyans == cianos, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Blues == azuis, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Magentas == magentas, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.UseTint == usarTonalidade, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.TintColor == tonalidade, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.BwPresetKind == tipoPresetPretoBranco, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.BlackAndWhitePresetFileName == nomePresetPretoBranco, MensagemValorAtualIncorreto);

                            AssertIsTrue(Math.Abs(camadaBlwh.TintColorRed - tonalidadeVermelha) < 1e-6, MensagemValorAtualIncorreto);

                            AssertIsTrue(Math.Abs(camadaBlwh.TintColorGreen - tonalidadeVerde) < 1e-6, MensagemValorAtualIncorreto);

                            AssertIsTrue(Math.Abs(camadaBlwh.TintColorBlue - tonalidadeAzul) < 1e-6, MensagemValorAtualIncorreto);

                            // Teste de edição e salvamento

                            recursoBlwh.Reds = vermelhos - 15;

                            recursoBlwh.Yellows = amarelos - 15;

                            recursoBlwh.Greens = verdes + 15;

                            recursoBlwh.Cyans = cianos + 15;

                            recursoBlwh.Blues = azuis - 15;

                            recursoBlwh.Magentas = magentas - 15;

                            recursoBlwh.UseTint = !usarTonalidade;

                            recursoBlwh.BwPresetKind = 4;

                            recursoBlwh.BlackAndWhitePresetFileName = "nomePresetPretoBranco";

                            camadaBlwh.TintColorRed = tonalidadeVermelha - 60;

                            camadaBlwh.TintColorGreen = tonalidadeVerde - 60;

                            camadaBlwh.TintColorBlue = tonalidadeAzul - 60;

                            im.Save(arquivoDestino);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(recursoRequeridoEncontrado, "O BlwhResource especificado não foi encontrado");

            recursoRequeridoEncontrado = false;

            using (PsdImage im = (PsdImage)Image.Load(arquivoDestino))

            {

                foreach (var camada in im.Layers)

                {

                    foreach (var recursoCamada in camada.Resources)

                    {

                        if (recursoCamada is BlwhResource)

                        {

                            var recursoBlwh = (BlwhResource)recursoCamada;

                            var camadaBlwh = (BlackWhiteAdjustmentLayer)camada;

                            recursoRequeridoEncontrado = true;

                            AssertIsTrue(recursoBlwh.Reds == vermelhos - 15, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Yellows == amarelos - 15, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Greens == verdes + 15, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Cyans == cianos + 15, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Blues == azuis - 15, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.Magentas == magentas - 15, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.UseTint == !usarTonalidade, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.TintColor == novaTonalidade, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.BwPresetKind == 4, MensagemValorAtualIncorreto);

                            AssertIsTrue(recursoBlwh.BlackAndWhitePresetFileName == "nomePresetPretoBranco", MensagemValorAtualIncorreto);

                                                       AssertIsTrue(Math.Abs(camadaBlwh.TintColorRed - tonalidadeVermelha + 60) < 1e-6, MensagemValorAtualIncorreto);

                            AssertIsTrue(Math.Abs(camadaBlwh.TintColorGreen - tonalidadeVerde + 60) < 1e-6, MensagemValorAtualIncorreto);

                            AssertIsTrue(Math.Abs(camadaBlwh.TintColorBlue - tonalidadeAzul + 60) < 1e-6, MensagemValorAtualIncorreto);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(recursoRequeridoEncontrado, "O BlwhResource especificado não foi encontrado");

        }

        ExemploSuporteDeRecursoBlwh(

            "CamadaAjustePretoBrancoListrasMascara.psd",

            0x28,

            0x3c,

            0x28,

            0x3c,

            0x14,

            0x50,

            false,

            1,

            "\0",

            225.00045776367188,

            211.00067138671875,

            179.00115966796875,

            -1977421,

            -5925001);

        ExemploSuporteDeRecursoBlwh(

            "CamadaAjustePretoBrancoListrasMascara2.psd",

            0x80,

            0x40,

            0x20,

            0x10,

            0x08,

            0x04,

            true,

            4,

            "\0",

            239.996337890625,

            127.998046875,

            63.9990234375,

            -1015744,

            -4963324);

        Console.WriteLine("A atualização de BlwhResource funciona como esperado. Pressione qualquer tecla.");

{{< /highlight >}}

**PSDNET-230. Capacidade de exportar Grupo de Camadas para Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

  using (var imagemPsd = (PsdImage)Image.Load("1.psd"))

            {

                // pasta com o fundo

                LayerGroup pastaFundo = (LayerGroup)imagemPsd.Layers[0];

                // pasta com o conteúdo

                LayerGroup pastaConteudo = (LayerGroup)imagemPsd.Layers[4];

                pastaFundo.Save("fundo.png", new PngOptions());

                pastaConteudo.Save("conteudo.png", new PngOptions());

            }

{{< /highlight >}}

` `**PSDNET-372. Suporte para recurso lspf (Contém configurações sobre configuração de Camada Protegida)**

{{< highlight java >}}

         const string MensagemValorAtualIncorreto = "O valor da propriedade esperado não é igual ao valor atual";

        void AssertIsTrue(bool condicao, string mensagem)

        {

            if (!condicao)

            {

                throw new FormatException(mensagem);

            }

        }

        string arquivoFonte = "AmostraParaRecurso.psd";

        string arquivoDestino = "Saída" + arquivoFonte;

        bool recursoRequeridoEncontrado = false;

        using (PsdImage im = (PsdImage)Image.Load(arquivoFonte))

        {

            foreach (var camada in im.Layers)

            {

                foreach (var recursoCamada in camada.Resources)

                {

                    if (recursoCamada is LspfResource)

                    {

                        var recurso = (LspfResource)recursoCamada;

                        recursoRequeridoEncontrado = true;

                        AssertIsTrue(false == recurso.IsCompositeProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(false == recurso.IsPositionProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(false == recurso.IsTransparencyProtected, MensagemValorAtualIncorreto);

                        // Teste de edição e salvamento

                        recurso.IsCompositeProtected = true;

                        AssertIsTrue(true == recurso.IsCompositeProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(false == recurso.IsPositionProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(false == recurso.IsTransparencyProtected, MensagemValorAtualIncorreto);

                        recurso.IsCompositeProtected = false;

                        recurso.IsPositionProtected = true;

                        AssertIsTrue(false == recurso.IsCompositeProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(true == recurso.IsPositionProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(false == recurso.IsTransparencyProtected, MensagemValorAtualIncorreto);

                        recurso.IsPositionProtected = false;

                        recurso.IsTransparencyProtected = true;

                        AssertIsTrue(false == recurso.IsCompositeProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(false == recurso.IsPositionProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(true == recurso.IsTransparencyProtected, MensagemValorAtualIncorreto);

                        recurso.IsCompositeProtected = true;

                        recurso.IsPositionProtected = true;

                        recurso.IsTransparencyProtected = true;

                        im.Save(arquivoDestino);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(recursoRequeridoEncontrado, "O LspfResource especificado não foi encontrado");

        recursoRequeridoEncontrado = false;

        using (PsdImage im = (PsdImage)Image.Load(arquivoDestino))

        {

            foreach (var camada in im.Layers)

            {

                foreach (var recursoCamada in camada.Resources)

                {

                    if (recursoCamada is LspfResource)

                    {

                        var recurso = (LspfResource)recursoCamada;

                        recursoRequeridoEncontrado = true;

                        AssertIsTrue(recurso.IsCompositeProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(recurso.IsPositionProtected, MensagemValorAtualIncorreto);

                        AssertIsTrue(recurso.IsTransparencyProtected, MensagemValorAtualIncorreto);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(recursoRequeridoEncontrado, "O LspfResource especificado não foi encontrado");

        Console.WriteLine("A atualização de LspfResource funciona como esperado. Pressione qualquer tecla.");

{{< /highlight >}}

` `**PSDNET-370. Suporte para recurso infx (Contém dados sobre Mistura de elementos interiores)**

{{< highlight java >}}

         void AssertIsTrue(bool condicao, string mensagem)

        {

            if (!condicao)

            {

                throw new FormatException(mensagem);

            }

        }

        string arquivoFonte = "AmostraParaRecurso.psd";

        string arquivoDestino = "Saída" + arquivoFonte;

        bool recursoRequeridoEncontrado = false;

        using (PsdImage im = (PsdImage)Image.Load(arquivoFonte))

        {

            foreach (var camada in im.Layers)

            {

                foreach (var recursoCamada in camada.Resources)

                {

                    if (recursoCamada is InfxResource)

                    {

                        var recurso = (InfxResource)recursoCamada;

                        recursoRequeridoEncontrado = true;

                        AssertIsTrue(!recurso.BlendInteriorElements, "O InfxResource.BlendInteriorElements deve ser falso");

                        // Teste de edição e salvamento

                        recurso.BlendInteriorElements = true;

                        im.Save(arquivoDestino);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(recursoRequeridoEncontrado, "O InfxResource especificado não foi encontrado");

        recursoRequeridoEncontrado = false;

        using (PsdImage im = (PsdImage)Image.Load(arquivoDestino))

        {

            foreach (var camada in im.Layers)

            {

                foreach (var recursoCamada in camada.Resources)

                {

                    if (recursoCamada is InfxResource)

                    {

                        var recurso = (InfxResource)recursoCamada;

                        recursoRequeridoEncontrado = true;

                        AssertIsTrue(recurso.BlendInteriorElements, "O InfxResource.BlendInteriorElements deve mudar para verdadeiro");

                        break;

                    }

                }

            }

        }

        AssertIsTrue(recursoRequeridoEncontrado, "O InfxResource especificado não foi encontrado");

{{< /highlight >}}

**PSDNET-251. Refatoração de PsdImage e Camada para alterar o comportamento de Transformação (Redimensionamento/Rotação/Corte corretos para máscaras de camada se transformarmos uma camada separadamente)**

{{< highlight java >}}

             var enums = (RotateFlipType[])Enum.GetValues(typeof(RotateFlipType));

            var fileNames = new string[]

            {

                "UmaRegularEUmaAjustadaComVetorELayerMask",

                "UmaRegularEUmaAjustadaComLayerMask", 

                "CamadaTexto",

                "FormasVinculadasComTexto"

            };

            foreach (string nomeArquivo in fileNames)

            {

                foreach (RotateFlipType rotateFlipType in enums)

                {

                    string arquivoFonte = nomeArquivo + ".psd";

                    string arquivoDestino = nomeArquivo + "_" + rotateFlipType;

                    var opcoesCarregamentoPsd = new PsdLoadOptions() { LoadEffectsResource = true };

                    using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte, opcoesCarregamentoPsd))

                    {

                        imagem.RotateFlip(rotateFlipType);

                        imagem.Save(arquivoDestino);

                    }

                }

            }

{{< /highlight >}}

**PSDNET-276. Em algumas configurações de globalização, a imagem raster AI não pode ser aberta**

{{< highlight java >}}

        string arquivoFonte = "form_raster_8.ai";

        System.Threading.Thread.CurrentThread.CurrentCulture = new System.Globalization.CultureInfo("ru_RU");

        System.Threading.Thread.CurrentThread.CurrentUICulture = System.Threading.Thread.CurrentThread.CurrentCulture;

        using (AiImage imagem = (AiImage)Image.Load(arquivoFonte))

        {

            // não deve lançar exceção

        }

{{< /highlight >}}

**PSDNET-194. Após realizar a operação FlipRotate na Camada, a Imagem PSD se torna ilegível**

{{< highlight java >}}

             string arquivoFonte = GetFileInCustomFolderRelativeToBase(@"testdata\Issues\IMAGINGNET-2617\1.psd");

            var tipoRotacao = RotateFlipType.Rotate90FlipNone;

            var arquivoSaidaPsd = this.GetFileInOutputFolder("RotateFlipTest2617.psd");

            try

            {

                using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))

                {

                    for (int i = 0; i < imagem.Layers.Length; i++)

                    {

                        var camada = imagem.Layers[i];

                        if (!camada.Bounds.IsEmpty)

                        {

                            camada.RotateFlip(tipoRotacao);

                        }

                    }

                    string arquivoSaidaPng = this.GetFileInOutputFolder("RotateFlipTest2617.png");

                    imagem.Save(arquivoSaidaPsd);

                }

            // Aqui lançamos exceção. Para o PhotoShop esse arquivo também é ilegível,

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoSaidaPsd)) // Lança uma exceção

            {

                // Não faz nada

            }

{{< /highlight >}}

**PSDNET-177. System.ArgumentException durante o carregamento do arquivo PSD**

{{< highlight java >}}

         string caminhoFonte = "1.psd";

        string caminhoPsd = "RotateFlipTest2617.psd";

        RotateFlipType tipoFlip = RotateFlipType.Rotate270FlipXY;

        using (var im = (PsdImage)(Image.Load(caminhoFonte)))

        {

            im.RotateFlip(tipoFlip);

            im.Save(caminhoPsd);

        }

        using (var im = (PsdImage)(Image.Load(caminhoPsd))) // Aqui não devemos receber exceções

        {

            // não fazer nada

        }

{{< /highlight >}}

**PSDNET-249. Após usar um método de transformação apenas para uma camada, a camada salva tem limites incorretos ou uma máscara**

{{< highlight java >}}

         void AssertIsTrue(bool condicao, string mensagem)

        {

            if (!condicao)

            {

                throw new FormatException(mensagem);

            }

        }

        const double Tolerancia = 1e-6;

        int novaLargura = 132;

        int novaAltura = 247;

        double xEscala = novaLargura / 48.0;

        double yEscala = novaAltura / 19.0;

        string arquivoFonte = "CamadaTexto.psd";

        string arquivoSaida = "CamadaTextoRedimensionada" + novaLargura + "_" + novaAltura;

        var opcoesCarregamentoPsd = new PsdLoadOptions() { LoadEffectsResource = true };

        using (PsdImage imagem = (PsdImage) Image.Load(arquivoFonte, opcoesCarregamentoPsd))

        {

            var camada = imagem.Layers[1] as TextLayer;

            var novoLeft = camada.Left - (novaLargura - camada.Width) / 2;

            var novoTop = camada.Top - (novaAltura - camada.Height) / 2;

            camada.Resize(novaLargura, novaAltura);

            AssertIsTrue(camada.Left == novoLeft, "A propriedade Left da camada deve ser " + novoLeft);

            AssertIsTrue(camada.Top == novoTop, "A propriedade Top da camada deve ser " + novoTop);

            AssertIsTrue(camada.Width == novaLargura, "A propriedade Width da camada deve ser " + novaLargura);

            AssertIsTrue(camada.Height == novaAltura, "A propriedade Height da camada deve ser " + novaAltura);

            AssertIsTrue(Math.Abs(camada.TransformMatrix[0] - xEscala) <= Tolerancia, "A propriedade TransformMatrix[0] da camada deve ser " + xEscala);

            AssertIsTrue(Math.Abs(camada.TransformMatrix[3] - yEscala) <= Tolerancia, "A propriedade TransformMatrix[3] da camada deve ser " + yEscala);

            AssertIsTrue(Math.Abs(camada.TransformMatrix[4] - novoLeft) <= Tolerancia, "A propriedade TransformMatrix[4] da camada deve ser " + novoLeft);

            AssertIsTrue(Math.Abs(camada.TransformMatrix[5] - novoTop) <= Tolerancia, "A propriedade TransformMatrix[5] da camada deve ser " + novoTop);

            imagem.Save(arquivoSaida + ".psd", new PsdOptions());

            imagem.Save(arquivoSaida + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

        }

{{< /highlight >}}