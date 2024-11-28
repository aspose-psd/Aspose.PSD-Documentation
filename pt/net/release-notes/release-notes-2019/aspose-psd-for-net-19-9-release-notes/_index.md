---
title: Aspose.PSD para .NET 19.9 - Notas de Lançamento
type: docs
weight: 40
url: /pt/net/aspose-psd-para-net-19-9-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para [Aspose.PSD para .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-160|Nome da camada extraído incorretamente|Recurso|
|PSDNET-175|Obtenção de propriedades de texto de uma parte diferente de texto dentro da camada de texto PSD|Recurso|
|PSDNET-190|Suporte para Adicionar grupo de camadas|Recurso|
|PSDNET-192|Suporte da Propriedade de Escala para Camada de Preenchimento Gradiente|Recurso|
|PSDNET-162|Ajustando o Brilho|Melhoria|
|PSDNET-174|IndexOutOfRangeException ao salvar imagem PSD como JPEG|Erro|
|PSDNET-180|Atualização de texto da camada de texto gera uma exceção|Erro|
|PSDNET-182|Salvar imagem PSD após operação RotateFlip produz um arquivo corrompido que não pode ser aberto|Erro|

## **Alterações na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-160. Nome da camada extraído incorretamente**

Para exibir corretamente o nome da camada, use a propriedade **DisplayName**. Um setter foi adicionado para esta propriedade e a propriedade pode ser modificada. Quando o Photoshop está salvando o nome da camada usando a propriedade Nome, os caracteres coreanos são armazenados como byte 63'?' em ASCII. Use a propriedade **DisplayName** porque a propriedade Nome não suporta caracteres coreanos.

{{< highlight java >}}

             // faça alterações nos nomes das camadas e salve

            using (var image = (PsdImage)Image.Load("camadas_com_nomes.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var camada = image.Layers[i];

                    // define novo valor na propriedade DisplayName

                    camada.DisplayName += "_alterado";

                }

                image.Save("saida.psd");

            }

{{< /highlight >}}

**PSDNET-175. Obtendo propriedades de texto de uma parte diferente de texto dentro da camada de texto PSD**

{{< highlight java >}}

            const double Tolerancia = 0.0001;

            var caminhoArquivo = "ParagrafosTresCores.psd";

            var caminhoSaida = "ParagrafosTresCores_saida.psd";

            using (var im = (PsdImage)Image.Load(caminhoArquivo))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var camada = im.Layers[i] as TextLayer;

                    if (camada != null)

                    {

                        var porcoes = camada.TextData.Items;

                        if (porcoes.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Verificando o texto de cada parte

                        if (porcoes[0].Text != "Antigo " ||

                            porcoes[1].Text != "cor" ||

                            porcoes[2].Text != " texto\r" ||

                            porcoes[3].Text != "Segundo parágrafo\r")

                        {

                            throw new Exception();

                        }

                        // Verificando dados de parágrafos

                        // Parágrafos possuem justificação diferente

                        if (

                            porcoes[0].Paragraph.Justification != 0 ||

                            porcoes[1].Paragraph.Justification != 0 ||

                            porcoes[2].Paragraph.Justification != 0 ||

                            porcoes[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // Todas as outras propriedades do primeiro e segundo parágrafo são iguais

                        for (int j = 0; j < porcoes.Length; j++)

                        {

                            var paragrafo = porcoes[j].Paragraph;

                            if (Math.Abs(paragrafo.AutoLeading - 1.2) > Tolerancia ||

                                paragrafo.AutoHyphenate != false ||

                                paragrafo.Burasagari != false ||

                                paragrafo.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragrafo.StartIndent) > Tolerancia ||

                                Math.Abs(paragrafo.EndIndent) > Tolerancia ||

                                paragrafo.EveryLineComposer != false ||

                                Math.Abs(paragrafo.FirstLineIndent) > Tolerancia ||

                                paragrafo.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragrafo.GlyphSpacing[0] - 1) > Tolerancia ||

                                Math.Abs(paragrafo.GlyphSpacing[1] - 1) > Tolerancia ||

                                Math.Abs(paragrafo.GlyphSpacing[2] - 1) > Tolerancia ||

                                paragrafo.Hanging != false ||

                                paragrafo.HyphenatedWordSize != 6 ||

                                paragrafo.KinsokuOrder != 0 ||

                                paragrafo.LetterSpacing.Length != 3 ||

                                Math.Abs(paragrafo.LetterSpacing[0]) > Tolerancia ||

                                Math.Abs(paragrafo.LetterSpacing[1]) > Tolerancia ||

                                Math.Abs(paragrafo.LetterSpacing[2]) > Tolerancia ||

                                paragrafo.LeadingType != LeadingMode.Auto ||

                                paragrafo.PreHyphen != 2 ||

                                paragrafo.PostHyphen != 2 ||

                                Math.Abs(paragrafo.SpaceBefore) > Tolerancia ||

                                Math.Abs(paragrafo.SpaceAfter) > Tolerancia ||

                                paragrafo.WordSpacing.Length != 3 ||

                                Math.Abs(paragrafo.WordSpacing[0] - 0.8) > Tolerancia ||

                                Math.Abs(paragrafo.WordSpacing[1] - 1.0) > Tolerancia ||

                                Math.Abs(paragrafo.WordSpacing[2] - 1.33) > Tolerancia ||

                                Math.Abs(paragrafo.Zone - 36.0) > Tolerancia)

                            {

                                throw new Exception();

                            }

                        }

                        // Verificando dados de estilos

                        // Estilos possuem cores e tamanhos de fonte diferentes

                        if (Math.Abs(porcoes[0].Style.FontSize - 12) > Tolerancia ||

                            Math.Abs(porcoes[1].Style.FontSize - 12) > Tolerancia ||

                            Math.Abs(porcoes[2].Style.FontSize - 12) > Tolerancia ||

                            Math.Abs(porcoes[3].Style.FontSize - 10) > Tolerancia)

                        {

                            throw new Exception();

                        }

                        if (porcoes[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            porcoes[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            porcoes[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            porcoes[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < porcoes.Length; j++)

                        {

                            var estilo = porcoes[j].Style;

                            if (estilo.AutoLeading != false ||

                                estilo.HindiNumbers != false ||

                                estilo.Kerning != 0 ||

                                estilo.Leading != 0 ||

                                estilo.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                estilo.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Exemplo de edição de texto

                        porcoes[0].Text = "Olá ";

                        porcoes[1].Text = "Mundo";

                        // Exemplo de remoção de porções de texto

                        camada.TextData.RemovePortion(3);

                        camada.TextData.RemovePortion(2);

                        // Exemplo de adicionar nova porção de texto

                        var porcaoCriada = camada.TextData.ProducePortion();

                        porcaoCriada.Text = "!!!\r";

                        camada.TextData.AddPortion(porcaoCriada);

                        porcoes = camada.TextData.Items;

                        // Exemplo de edição de parágrafo e estilo para porções

                        // Definir justificação à direita

                        porcoes[0].Paragraph.Justification = 1;

                        porcoes[1].Paragraph.Justification = 1;

                        porcoes[2].Paragraph.Justification = 1;

                        // Cores diferentes para cada estilo. Serão alteradas, mas a renderização não é totalmente suportada

                        porcoes[0].Style.FillColor = Color.Aquamarine;

                        porcoes[1].Style.FillColor = Color.Violet;

                        porcoes[2].Style.FillColor = Color.LightBlue;

                        // Fonte diferente. Serão alteradas, mas a renderização não é totalmente suportada

                        porcoes[0].Style.FontSize = 6;

                        porcoes[1].Style.FontSize = 8;

                        porcoes[2].Style.FontSize = 10;

                        camada.TextData.UpdateLayerData();

                        im.Save(caminhoSaida, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Suporte para Adicionar grupo de camadas**

{{< highlight java >}}

             // -Grupo 1

            // --Camada 1

            // --Grupo 2

            // ---Camada 2

            // ---Camada 3

            // --Camada 4

            string diretorioDados = "teste_psdnet190.psd";

            var opcoesCriar = new PsdOptions();

            opcoesCriar.Source = new FileCreateSource(diretorioDados, false);

            opcoesCriar.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var imagemPSD = (PsdImage)Image.Create(opcoesCriar, 500, 500))

            {

                LayerGroup grupo1 = imagemPSD.AddLayerGroup("Grupo 1", 0, true);

                Layer camada1 = new Layer(imagemPSD);

                camada1.Name = "Camada 1";

                grupo1.AddLayer(camada1);

                LayerGroup grupo2 = grupo1.AddLayerGroup("Grupo 2", 1);

                Layer camada2 = new Layer(imagemPSD);

                camada2.Name = "Camada 2";

                grupo2.AddLayer(camada2);

                Layer camada3 = new Layer(imagemPSD);

                camada3.Name = "Camada 3";

                grupo2.AddLayer(camada3);

                Layer camada4 = new Layer(imagemPSD);

                camada4.Name = "Camada 4";

                grupo1.AddLayer(camada4);

                imagemPSD.Save();

            }

{{< /highlight >}}

**PSDNET-192. Suporte da Propriedade de Escala para Camada de Preenchimento Gradiente**

{{< highlight java >}}

            using (var imagem = (PsdImage)Image.Load("CamadaPreenchimentoGradiente.psd"))

            {

                // obtendo uma camada de preenchimento

                FillLayer camadaPreenchimento = null;

                foreach (var camada in imagem.Layers)

                {

                    camadaPreenchimento = camada as FillLayer;

                    if (camadaPreenchimento != null)

                    {

                        break;

                    }

                }

                var configuracoes = camadaPreenchimento.FillSettings as IGradientFillSettings;

                // atualizar valor de escala

                configuracoes.Scale = 200;

                camadaPreenchimento.Update(); // Atualiza dados de pixels

                imagem.Save("imagem_escalonada.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-174. IndexOutOfRangeException ao salvar imagem PSD como JPEG**

{{< highlight java >}}

         using (var imagem = Aspose.PSD.Image.Load("AmostraPSD.psd"))

        {

            imagem.Save("amostraJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}

**PSDNET-180. Atualização de texto na camada de texto gera uma exceção**

{{< highlight java >}}

           // Atualização de texto na camada de texto gera uma exceção

            string caminhoArquivo = "InverterVerticalmente.psd";

