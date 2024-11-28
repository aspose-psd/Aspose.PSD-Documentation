---
title: Notas de Lançamento do Aspose.PSD para .NET 20.10
type: docs
weight: 30
url: /pt/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para [Aspose.PSD para .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-565|Exceção ao salvar o arquivo PSD específico com camadas de texto|Erro|
|PSDNET-680|Fontes são perdidas após idas e vindas com Aspose.PSD|Erro|
|PSDNET-704|Renderização da Camada do Objeto Inteligente|Recurso|
|PSDNET-707|Suporte para transformações não destrutivas do Objeto Inteligente|Recurso|
|PSDNET-711|A Camada de Texto é Deslocada Após salvar sem quaisquer alterações|Erro|
|PSDNET-720|Aspose.PSD 20.8: Exceção de conversão de Psd para Tiff|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- Nenhuma
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-565. Exceção ao salvar o arquivo PSD específico com camadas de texto**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Fontes são perdidas após idas e vindas com Aspose.PSD**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void AreEqual(int expected, int actual)
            {
                if (expected != actual)
                {
                    throw new Exception("Os valores não são iguais.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-704. Renderização da Camada do Objeto Inteligente**
{{< highlight csharp >}}
            // Este exemplo demonstra como substituir o conteúdo da camada de objeto inteligente do Adobe® Photoshop® e sua correta renderização.
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // Este exemplo demonstra como atualizar o cache de imagem das camadas de objeto inteligente do Adobe® Photoshop® e sua correta renderização.
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-707. Suporte para transformações não destrutivas do Objeto Inteligente**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Estes exemplos demonstram transformações não destrutivas do arquivo PSD com SmartObjectLayer.
            // Podemos redimensionar, rotacionar, inclinar, distorcer, transformar em perspectiva ou distorcer uma camada sem
            // perder os dados ou qualidade da imagem original, pois as transformações não afetam os dados originais.

            // Este exemplo demonstra como redimensionar a imagem do Adobe® Photoshop® com camadas de objetos inteligentes:
            ExemploDeSuporteDeRedimensionamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            ExemploDeSuporteDeRedimensionamentoDeImagemDeObjetoInteligente("picture-frame-4-linked3");
            ExemploDeSuporteDeRedimensionamentoDeImagemDeObjetoInteligente("gorilla");

            // Este exemplo demonstra como redimensionar o arquivo PSD com camadas de objetos inteligentes.
            void ExemploDeSuporteDeRedimensionamentoDeImagemDeObjetoInteligente(string fileName)
            {
                const int escala = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Redimensionar_" + fileName + ".psd";
                string outputPngPath = outputDir + "Redimensionar_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int novaLargura = image.Width * escala;
                    int novaAltura = image.Height * escala;
                    image.Resize(novaLargura, novaAltura);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este exemplo demonstra como redimensionar a camada de objeto inteligente do Adobe® Photoshop®.
            ExemploDeSuporteDeRedimensionamentoDeCamadaDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            ExemploDeSuporteDeRedimensionamentoDeCamadaDeObjetoInteligente("gorilla");

            // Este exemplo demonstra como redimensionar uma camada de objeto inteligente no arquivo PSD.
            void ExemploDeSuporteDeRedimensionamentoDeCamadaDeObjetoInteligente(string fileName)
            {
                const double escala = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "RedimensionarUltimo_" + fileName + ".psd";
                string outputPngPath = outputDir + "RedimensionarUltimo_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var camadaObjetoInteligente = image.Layers[image.Layers.Length - 1];
                    int novaLargura = (int)(camadaObjetoInteligente.Width * escala);
                    int novaAltura = (int)(camadaObjetoInteligente.Height * escala);
                    camadaObjetoInteligente.Resize(novaLargura, novaAltura);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este exemplo demonstra como cortar a camada de objeto inteligente do Adobe® Photoshop®.
            ExemploDeSuporteDeCorteDeCamadaDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            ExemploDeSuporteDeCorteDeCamadaDeObjetoInteligente("gorilla");

            // Este exemplo demonstra como cortar uma camada de objeto inteligente no arquivo PSD.
            void ExemploDeSuporteDeCorteDeCamadaDeObjetoInteligente(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "CortarUltimo_" + fileName + ".psd";
                string outputPngPath = outputDir + "CortarUltimo_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var camadaObjetoInteligente = image.Layers[image.Layers.Length - 1];
                    camadaObjetoInteligente.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este exemplo demonstra como cortar a camada de objeto inteligente do Adobe® Photoshop®:
            ExemploDeSuporteDeCorteDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked");
            ExemploDeSuporteDeCorteDeImagemDeObjetoInteligente("gorilla");

            // Este exemplo demonstra como cortar o arquivo PSD com camadas de objetos inteligentes.
            void ExemploDeSuporteDeCorteDeImagemDeObjetoInteligente(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Cortar_" + fileName + ".psd";
                string outputPngPath = outputDir + "Cortar_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Crop(25, 10, 30, 5);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este exemplo demonstra como rotacionar e espelhar a imagem do Adobe® Photoshop® com camadas de objetos inteligentes:
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("gorilla", RotateFlipType.Rotate90FlipNone);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Este exemplo demonstra como rotacionar e espelhar o arquivo PSD com camadas de objetos inteligentes.
            void ExemploDeSuporteDeRotacaoEEspelhamentoDeImagemDeObjetoInteligente(string fileName, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + rotateFlipType + "_" + fileName + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este exemplo demonstra como rotacionar e espelhar a camada de objeto inteligente do Adobe® Photoshop®.
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("gorilla", RotateFlipType.Rotate90FlipNone);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            ExemploDeSuporteDeRotacaoEEspelhamentoDeCamadaDeObjetoInteligente("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Este exemplo demonstra como rotacionar a camada de objeto inteligente do Adobe® Photoshop® por qualquer ângulo:
            const string FormatoAngulo = "+#;-#;+0";
            ExemploDeRotacaoDeCamadaDeObjetoInteligente("gorilla", 45, false);
            ExemploDeRotacaoDeCamadaDeObjetoInteligente("gorilla", 45, true);
            ExemploDeRotacaoDeCamadaDeObjetoInteligente("r3-embedded-transform2", -30, true);
            ExemploDeRotacaoDeCamadaDeObjetoInteligente("r3-embedded-transform2", -30, false);
            ExemploDeRotacaoDeCamadaDeObjetoInteligente("new_panama-papers-8-trans4-linked", 190, false);
            ExemploDeRotacaoDeCamadaDeObjetoInteligente("new_panama-papers-8-trans4-linked", 190, true);

            // Este exemplo demonstra como rotacionar uma camada de objeto inteligente no arquivo PSD por qualquer ângulo.
            void ExemploDeRotacaoDeCamadaDeObjetoInteligente(string fileName, float angle, bool resizeProportionally)
            {
                string prefixo = "RotacionarUltimo" +  angle.ToString(FormatoAngulo) + (resizeProportionally ? "RedimensionarProporcionalmente" : "") + "_";
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + prefixo + fileName + ".psd";
                string outputPngPath = outputDir + prefixo + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var camadaObjetoInteligente = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    camadaObjetoInteligente.Rotate(angle, resizeProportionally, Color.Empty);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Este exemplo demonstra como rotacionar a imagem do Adobe® Photoshop® com camada de objeto inteligente por qualquer ângulo
            ExemploDeRotacaoDeImagemDeObjetoInteligente("gorilla", 45, false);
            ExemploDeRotacaoDeImagemDeObjetoInteligente("new_panama-papers-8-trans4-linked", -30, false);

            // Este exemplo demonstra como rotacionar o arquivo PSD com camadas de objetos inteligentes por qualquer ângulo.
            void ExemploDeRotacaoDeImagemDeObjetoInteligente(string fileName, float angle, bool resizeProportionally)
            {
                string prefix