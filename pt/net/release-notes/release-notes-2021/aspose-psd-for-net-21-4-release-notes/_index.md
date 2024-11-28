---
title: Aspose.PSD para .NET 21.4 - Notas de Lançamento
type: docs
weight: 90
url: /pt/net/aspose-psd-para-net-21-4-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para [Aspose.PSD for .NET 21.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-259|Renderização do Efeito de Camada de Sobreposição de Padrão|Recurso|
|PSDNET-861|Adicionar propriedades de recurso Vogk desconhecidas para suportar redimensionamento de camadas de forma com caminhos vetoriais na imagem PSD|Recurso|
|PSDNET-90|PSD não convertido corretamente para PDF|Erro|
|PSDNET-830|Exceção ao salvar o arquivo PSD específico com camadas de texto|Erro| (Corrigido anteriormente)

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginBoxCorners
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.Transform
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginBoxCornersPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsTransformPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Tx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Ty

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-90. PSD não convertido corretamente para PDF**

{{< highlight csharp >}}
            string srcFile = "psd_magical.psd";
            string outputJpg = "output.jpg";
            string outputPdf = "output.pdf";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                JpegOptions jpgOptions = new JpegOptions();
                PdfOptions pdfOptions = new PdfOptions();

                psdImage.Save(outputJpg, jpgOptions);
                psdImage.Save(outputPdf, pdfOptions);
            }
{{< /highlight >}}

**PSDNET-259. Renderizando o Efeito de Camada de Sobreposição de Padrão**

{{< highlight csharp >}}
            string sourceFile = "imagemComPadrao.psd";
            string outputFile = "resultado.png";

            using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-861. Adicionar propriedades de recurso Vogk desconhecidas para suportar redimensionamento de camadas de forma com caminhos vetoriais na imagem PSD**

{{< highlight csharp >}}
            // Este exemplo mostra como obter e definir novas propriedades Transform e OriginBoxCorners
            // do ShapeOriginSettings no recurso Vogk da FillLayer no arquivo PSD
            string sourceFileName = Path.Combine("PSDNET861_1", "formatoVetorial_25_50.psd");
            string outputPath = Path.Combine("PSDNET861_1", "resultado.psd");

            VectorShapeOriginSettings settingOriginal;
            const int indiceCamada = 0;

            // Carregar a imagem original
            using (PsdImage imagem = (PsdImage)Image.Load(sourceFileName)) 
            {
                AssertIsTrue(indiceCamada < imagem.Layers.Length);
                var camada = imagem.Layers[indiceCamada];
                AssertIsTrue(camada is FillLayer);
                var recurso = ObterRecursoVogk((FillLayer)camada);
                AssertAreEqual(1, recurso.ShapeOriginSettings.Length);

                // Assert após leitura
                var configuracao = recurso.ShapeOriginSettings[0];
                AssertAreEqual(false, configuracao.IsShapeInvalidatedPresent);
                AssertAreEqual(false, configuracao.IsOriginRadiiRectanglePresent);
                AssertAreEqual(true, configuracao.IsOriginIndexPresent);
                AssertAreEqual(0, configuracao.OriginIndex);
                AssertAreEqual(true, configuracao.IsOriginTypePresent);
                AssertAreEqual(5, configuracao.OriginType);
                AssertAreEqual(true, configuracao.IsOriginShapeBBoxPresent);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(3, 7, 10, 22), configuracao.OriginShapeBox.Bounds);
                AssertAreEqual(true, configuracao.IsOriginResolutionPresent);
                AssertAreEqual(300d, configuracao.OriginResolution);

                // Assertar novas propriedades
                AssertAreEqual(true, configuracao.IsTransformPresent);
                AssertAreEqual(0d, configuracao.Transform.Tx);
                AssertAreEqual(0d, configuracao.Transform.Ty);
                AssertAreEqual(0.050000000000000003d, configuracao.Transform.Xx);
                AssertAreEqual(0d, configuracao.Transform.Yx);
                AssertAreEqual(0d, configuracao.Transform.Xy);
                AssertAreEqual(0.1d, configuracao.Transform.Yy);
                AssertAreEqual(true, configuracao.IsOriginBoxCornersPresent);
                AssertAreEqual(2.9000000000000004d, configuracao.OriginBoxCorners[0]);
                AssertAreEqual(7.3000000000000007d, configuracao.OriginBoxCorners[1]);
                AssertAreEqual(10.450000000000001d, configuracao.OriginBoxCorners[2]);
                AssertAreEqual(7.3000000000000007d, configuracao.OriginBoxCorners[3]);
                AssertAreEqual(10.450000000000001d, configuracao.OriginBoxCorners[4]);
                AssertAreEqual(22.400000000000002d, configuracao.OriginBoxCorners[5]);
                AssertAreEqual(2.9000000000000004d, configuracao.OriginBoxCorners[6]);
                AssertAreEqual(22.400000000000002d, configuracao.OriginBoxCorners[7]);

                // Definir novas propriedades
                settingOriginal = recurso.ShapeOriginSettings[0];
                settingOriginal.Transform.Tx = 0.2d;
                settingOriginal.Transform.Ty = 0.3d;
                settingOriginal.Transform.Xx = 0.4d;
                settingOriginal.Transform.Xy = 0.5d;
                settingOriginal.Transform.Yx = 0.6d;
                settingOriginal.Transform.Yy = 0.7d;
                settingOriginal.OriginBoxCorners = new double[8] { 9, 8, 7, 6, 5, 4, 3, 2 };

                // Salvar esta imagem PSD com as propriedades alteradas.
                imagem.Save(outputPath, new PsdOptions(imagem));
            }

            // Carregar a imagem PSD salva com as propriedades alteradas
            using (PsdImage imagem = (PsdImage)Image.Load(outputPath))
            {
                var camada = imagem.Layers[indiceCamada];
                AssertIsTrue(camada is FillLayer);
                var recurso = ObterRecursoVogk((FillLayer)camada);
                AssertAreEqual(1, recurso.ShapeOriginSettings.Length);

                // Assertar que as propriedades são salvas e carregadas corretamente
                var configuracao = recurso.ShapeOriginSettings[0];
                AssertAreEqual(true, configuracao.IsOriginIndexPresent);
                AssertAreEqual(false, configuracao.IsShapeInvalidatedPresent);
                AssertAreEqual(true, configuracao.IsOriginResolutionPresent);
                AssertAreEqual(true, configuracao.IsOriginTypePresent);
                AssertAreEqual(true, configuracao.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, configuracao.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, configuracao.OriginIndex);
                AssertAreEqual(true, configuracao.IsTransformPresent);
                AssertAreEqual(0.2d, configuracao.Transform.Tx);
                AssertAreEqual(0.3d, configuracao.Transform.Ty);
                AssertAreEqual(0.4d, configuracao.Transform.Xx);
                AssertAreEqual(0.5d, configuracao.Transform.Xy);
                AssertAreEqual(0.6d, configuracao.Transform.Yx);
                AssertAreEqual(0.7d, configuracao.Transform.Yy);
                AssertAreEqual(true, configuracao.IsOriginBoxCornersPresent);
                AssertAreEqual(settingOriginal.OriginBoxCorners[0], configuracao.OriginBoxCorners[0]);
                AssertAreEqual(settingOriginal.OriginBoxCorners[1], configuracao.OriginBoxCorners[1]);
                AssertAreEqual(settingOriginal.OriginBoxCorners[2], configuracao.OriginBoxCorners[2]);
                AssertAreEqual(settingOriginal.OriginBoxCorners[3], configuracao.OriginBoxCorners[3]);
                AssertAreEqual(settingOriginal.OriginBoxCorners[4], configuracao.OriginBoxCorners[4]);
                AssertAreEqual(settingOriginal.OriginBoxCorners[5], configuracao.OriginBoxCorners[5]);
                AssertAreEqual(settingOriginal.OriginBoxCorners[6], configuracao.OriginBoxCorners[6]);
                AssertAreEqual(settingOriginal.OriginBoxCorners[7], configuracao.OriginBoxCorners[7]);
            }

            VogkResource ObterRecursoVogk(FillLayer camada)
            {
                if (camada == null)
                {
                    throw new PsdImageArgumentException("O parâmetro layer não deve ser nulo.");
                }

                VogkResource recurso = null;
                var recursos = camada.Resources;
                for (int i = 0; i < recursos.Length; i++)
                {
                    if (recursos[i] is VogkResource)
                    {
                        recurso = (VogkResource)recursos[i];
                        break;
                    }
                }

                if (recurso == null)
                {
                    throw new PsdImageException("Recurso Vogk não encontrado.");
                }

                return recurso;
            }

            void AssertIsTrue(bool condicao)
            {
                if (!condicao)
                {
                    throw new FormatException(string.Format("Esperado verdadeiro"));
                }
            }

            void AssertAreEqual(object atual, object esperado)
            {
                if (!object.Equals(atual, esperado))
                {
                    throw new FormatException(string.Format("O valor atual {0} não é igual ao esperado {1}.", atual, esperado));
                }
            }
{{< /highlight >}}