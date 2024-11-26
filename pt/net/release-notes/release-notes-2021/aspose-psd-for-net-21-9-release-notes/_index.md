---
title: Notas de Lançamento do Aspose.PSD para .NET 21.9
type: docs
weight: 40
url: /pt/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para o [Aspose.PSD para .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Sumário**|**Categoria**|
| :- | :- | :- |
|PSDNET-574|Tornar a Compressão RLE padrão para Salvar PSD a fim de evitar PSD de saída enorme|Recurso|
|PSDNET-747|Suporte aos Efeitos da Camada de Padrão de Sobreposição com o modo de cores multicanal no arquivo PSD|Recurso|
|PSDNET-951|Após a criação da nova camada, sua propriedade de Recursos é nula, o que impede manipulações (Redimensionar, por exemplo)|Erro|
|PSDNET-955|Não suportado dos métodos de compressão ZipWithPrediction para 8 bits|Erro|

## **Alterações na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-574. Tornar a Compressão RLE Padrão para Salvar PSD a fim de evitar PSD de saída enorme**

{{< highlight csharp >}}
            string inputFilePath = "arquivo.psd";
            string output1 = "saída_original.psd";
            string output2 = "saída_opções_psd.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Suporte aos Efeitos da Camada de Padrão de Sobreposição com o modo de cores multicanal no arquivo PSD**

{{< highlight csharp >}}
            var fileName = "TodosOsEfeitos.psd";
            var outputFile = "TodosOsEfeitos_saida.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Não deve lançar exceção
            using (var im = Image.Load(fileName, loadOptions))
            {
                // Não deve lançar exceção
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. Após a criação da nova camada, sua propriedade de Recursos é nula, o que impede manipulações (Redimensionar, por exemplo)**

{{< highlight csharp >}}
            string PSDFile = "Camada1.psd";
            string arquivoCamada1 = "Camada2.png";
            string arquivoCamada2 = "Camada3.png";
            string arquivoFinal = "saídaFinal.psd";

            void SubstituirCor(RasterImage image, Color corAntiga, int diferenca, Color novaCor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var comprimento = pixels.Length;

                var rAntigo = corAntiga.R;
                var gAntigo = corAntiga.G;
                var bAntigo = corAntiga.B;
                var novoValorCor = novaCor.ToArgb();

                for (int i = 0; i < comprimento; i++)
                {
                    // Vermelho
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Verde
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // Azul
                    var b = (byte)(pixels[i] & 0xff);

                    int diferencaAtual = Math.Abs(r - rAntigo) + Math.Abs(g - gAntigo) + Math.Abs(b - bAntigo);

                    if (diferencaAtual <= diferenca)
                    {
                        pixels[i] = novoValorCor;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Camada2 = null;
            Layer Camada3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region Adicionando Camada 1

                using (var stream = new FileStream(arquivoCamada1, FileMode.Open))
                {
                    Camada2 = new Layer(stream);

                    Camada2.Redimensionar(image.Width, image.Height);
                    var largura = Camada2.Width;
                    var altura = Camada2.Height;

                    Camada2.Esquerda = 675;
                    Camada2.Topo = 0;

                    Camada2.Direita = Camada2.Esquerda + largura;
                    Camada2.Fundo = Camada2.Topo + altura;

                    image.AdicionarCamada(Camada2);
                }

                #endregion

                using (var stream = new FileStream(arquivoCamada2, FileMode.Open))
                {
                    Camada3 = new Layer(stream);
                    // Substituindo a cor Branca por Transparente
                    SubstituirCor(Camada3, Color.Branco, 256, Color.Transparent);
                    Camada2.DesenharImagem(new Point(0, 0), Camada3);
                }

                image.Save(arquivoFinal, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Não suportado dos métodos de compressão ZipWithPrediction para 8 bits**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string saídaZip8 = "saída_Zip8bits.psd";
            string saídaZip16 = "saída_Zip16bits.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(saídaZip8, new PsdOptions() { MétodoDeCompressão = CompressionMethod.ZipWithPrediction, ContagemDeBitsDoCanal = 8 });
                image.Save(saídaZip16, new PsdOptions() { MétodoDeCompressão = CompressionMethod.ZipWithPrediction, ContagemDeBitsDoCanal = 16 });
            }
{{< /highlight >}}
