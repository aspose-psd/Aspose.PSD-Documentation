---
title: Notas da Versão Aspose.PSD para .NET 21.8
type: docs
weight: 50
url: /pt/net/aspose-psd-para-net-21-8-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-698|Suporte aos métodos de compressão ZipWithPrediction|Recurso|
|PSDNET-663|O espaçamento de texto está incorreto no PSD gerado|Erro|
|PSDNET-685|Exceção ao salvar PSD|Erro|
|PSDNET-927|Distância incorreta entre linhas e símbolos no Aspose.PSD quando usado sem licença|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-663. O espaçamento de texto está incorreto no PSD gerado**

{{< highlight csharp >}}
            string nomeArquivoFonte = "source.psd";
            string nomeArquivoSaida = "output.png";

            using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))
            {
                imagem.Save(nomeArquivoSaida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Exceção ao salvar PSD**

{{< highlight csharp >}}
            string nomeArquivoFonte = "File.psd";
            string nomeArquivoSaida = "File2.psd";

            using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))
            {
                var camada1 = (TextLayer)imagem.Layers[1];
                camada1.TextData.UpdateLayerData();

                imagem.Save(nomeArquivoSaida);
            }
{{< /highlight >}}

**PSDNET-698. Suporte aos métodos de compressão ZipWithPrediction**

{{< highlight csharp >}}
            string caminhoArquivoEntrada = "zipTest698.psd";

            string saidaPng = "output.png";
            string saidaRaw = "out_Raw.psd";
            string saidaZip = "out_Zip.psd";

            using (Image imagem = Image.Load(caminhoArquivoEntrada))
            {
                imagem.Save(saidaPng, new PngOptions());

                imagem.Save(saidaRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                imagem.Save(saidaZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Distância incorreta entre linhas e símbolos no Aspose.PSD quando usado sem licença**

{{< highlight csharp >}}
            bool[] estadosLicenca = new bool[] { false, true };
            for (int i = 0; i < estadosLicenca.Length; i++)
            {
                bool testeLicenca = estadosLicenca[i];
                if (testeLicenca)
                {
                    License licenca = new License();
                    licenca.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string arquivoFonte = "psdnetTest927.psd";
                string arquivoSaida = "out_" + testeLicenca.ToString() + "_psdnetTest927.png";

                using (var imagem = (PsdImage)Image.Load(arquivoFonte))
                {
                    imagem.Save(arquivoSaida, new PngOptions());
                }
            }
{{< /highlight >}}
