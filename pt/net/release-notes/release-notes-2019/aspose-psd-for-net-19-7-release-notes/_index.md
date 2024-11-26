---
title: Notas de lançamento do Aspose.PSD para .NET 19.7
type: docs
weight: 60
url: /pt/net/aspose-psd-for-net-19-7-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para [Aspose.PSD para .NET 19.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-126|Suporte ao processamento de Máscaras de Camada Vetorial|Recurso|
|PSDNET-130|Implementar método de Redimensionamento correto para arquivos PSD|Recurso|
|PSDNET-165|Adicionar suporte para exportar PSD para PDF|Recurso|
|PSDNET-186|Adicionar suporte para exportar formato AI (Versão 2 e 3) para outros formatos|Recurso|

## **Mudanças na API pública**
# **APIs Adicionadas:**
- F:Aspose.PSD.FileFormat.Ai
- T:Aspose.PSD.FileFormats.Ai.AiDataSection
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- T:Aspose.PSD.FileFormats.Ai.AiFinalizeSection
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- T:Aspose.PSD.FileFormats.Ai.AiFormatVersion
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe20
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe30
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf14
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf15
- T:Aspose.PSD.FileFormats.Ai.AiHeader
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Creator
- P:Aspose.PSD.FileFormats.Ai.AiHeader.For
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Title
- P:Aspose.PSD.FileFormats.Ai.AiHeader.CreationDate
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcessColors
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcSets
- P:Aspose.PSD.FileFormats.Ai.AiHeader.BoundingBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.ColorUsage
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TemplateBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TileBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentPreview
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Item(System.String)
- T:Aspose.PSD.FileFormats.Ai.AiImage
- M:Aspose.PSD.FileFormats.Ai.AiImage.#ctor
- P:Aspose.PSD.FileFormats.Ai.AiImage.FileFormat
- P:Aspose.PSD.FileFormats.Ai.AiImage.Version
- P:Aspose.PSD.FileFormats.Ai.AiImage.Header
- P:Aspose.PSD.FileFormats.Ai.AiImage.SetupSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.FinalizeSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.DataSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.IsCached
- P:Aspose.PSD.FileFormats.Ai.AiImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Ai.AiImage.Width
- P:Aspose.PSD.FileFormats.Ai.AiImage.Height
- M:Aspose.PSD.FileFormats.Ai.AiImage.CacheData
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Ai.AiImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.SetPalette(Aspose.PSD.IColorPalette,System.Boolean)
- T:Aspose.PSD.FileFormats.Ai.AiSetupSection
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData
- P:Aspose.PSD.ImageOptions.PdfOptions.PageSize
# **APIs Removidas:**
- Nenhuma

## **Exemplos de uso:**
**PSDNET-126. Suporte ao processamento de Máscaras de Camada Vetorial**

{{< highlight java >}}

             string nomeArquivoOrigem = "CaminhosDiferentes_CamadaMascaras_Origem.psd";

            string caminhoExportacao = "CaminhosDiferentes_CamadaMascaras_Exportacao.psd";

            string caminhoExportacaoPng = "CaminhosDiferentes_CamadaMascaras_Exportacao.png";

            // leitura

            using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoOrigem))

            {

                // fazer alterações nos pontos do caminho vetorial

                foreach (var camada in imagem.Layers)

                {

                    foreach (var recursoCamada in camada.Resources)

                    {

                        var recurso = recursoCamada as VectorPathDataResource;

                        if (recurso != null)

                        {

                            foreach (var registroCaminho in recurso.Caminhos)

                            {

                                var registroBezier = registroCaminho as BezierKnotRecord;

                                if (registroBezier != null)

                                {

                                    Point p0 = registroBezier.Pontos[0];

                                    registroBezier.Pontos[0] = registroBezier.Pontos[2];

                                    registroBezier.Pontos[2] = p0;

                                    break;

                                }

                            }

                        }

                    }

                }

                // exportação

                imagem.Save(caminhoExportacao);

                imagem.Save(caminhoExportacaoPng, new PngOptions() { TipoCor = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-130. Implementar método de Redimensionamento correto para arquivos PSD**

{{< highlight java >}}

              // Implementar método de Redimensionamento correto para arquivos PSD.

            string nomeArquivoOrigem = "1.psd";

            string caminhoExportacaoPsd = "TesteRedimensionamento.psd";

            string caminhoExportacaoPng = "TesteRedimensionamento.png";

            using (RasterImage imagem = Image.Load(nomeArquivoOrigem) as RasterImage)

            {

                imagem.Resize(160, 120);

                imagem.Save(caminhoExportacaoPsd, new PsdOptions());

                imagem.Save(caminhoExportacaoPng, new PngOptions() { TipoCor = PngColorType.TruecolorWithAlpha });

            }           

{{< /highlight >}}

**PSDNET-165. Adicionar suporte para exportar PSD para PDF**

{{< highlight java >}}

   // Adicionar suporte de exportação PSD para PDF

    string[] arquivosOrigem = new string[]

    {

        @"1.psd",

        @"pequeno.psb",

        @"psb3.psb",

        @"emRgb16.psd",

        @"MuitosTiposdeElementos.psd",

        @"SobreposicaoCorSombrasMascara.psd",

        @"TresCamadasRegularesSemiTransparentes.psd"

    };

    for (int i = 0; i < arquivosOrigem.Length; i++)

    {

        string nomeArquivoOrigem = arquivosOrigem[i];

        using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoOrigem))

        {

           string nomeArquivoSaida = "PsdParaPdf" + i + ".pdf";

           imagem.Save(nomeArquivoSaida, new PdfOptions());

        }

    }

{{< /highlight >}}

**PSDNET-186. Adicionar suporte para exportar formato AI (Versão 2 e 3) para outros formatos**

{{< highlight java >}}

 // Adicionar suporte de exportação formato AI (Versão 2 e 3) para outros formatos

            string[] arquivosOrigem = new string[]

            {

                @"34992OStroke",

                @"retangulo2_cor",

            };

            for (int i = 0; i < arquivosOrigem.Length; i++)

            {

                string nome = arquivosOrigem[i];

                string nomeArquivoOrigem = @"dadosTeste\Imagens\Ai\" + nome + ".ai";

                ImageOptionsBase opcoes;

                string nomeArquivoSaida;

                using (AiImage imagem = (AiImage)Image.Load(nomeArquivoOrigem))

                {

                    nomeArquivoSaida = nome + ".psd";

                    opcoes = new PsdOptions();

                    imagem.Save(nomeArquivoSaida, opcoes);

                    nomeArquivoSaida = nome + ".png";

                    opcoes = new PngOptions() { TipoCor = PngColorType.TruecolorWithAlpha };

                    imagem.Save(nomeArquivoSaida, opcoes);

                    nomeArquivoSaida = nome + ".jpg";

                    opcoes = new JpegOptions() { Qualidade = 85 };

                    imagem.Save(nomeArquivoSaida, opcoes);

                    nomeArquivoSaida = nome + ".gif";

                    opcoes = new GifOptions() { CorrecaoPaleta = false };

                    imagem.Save(nomeArquivoSaida, opcoes);

                    nomeArquivoSaida = nome + ".tif";

                    opcoes = new TiffOptions(TiffExpectedFormat.TiffDeflateRgba);

                    imagem.Save(nomeArquivoSaida, opcoes);

                    nomeArquivoSaida = nome + ".psd";

                    opcoes = new PsdOptions();

                    imagem.Save(nomeArquivoSaida, opcoes);

                }

            }

{{< /highlight >}}
