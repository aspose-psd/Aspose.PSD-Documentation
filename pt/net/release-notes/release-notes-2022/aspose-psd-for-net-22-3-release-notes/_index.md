---
title: Aspose.PSD para .NET 22.3 - Notas de Lançamento
type: docs
weight: 100
url: /pt/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-210|Adicionar propriedade IsOpen para o Grupo de Camadas|Recurso|
|PSDNET-643|Imagem PSD com máscaras de camada de raster descarta máscaras ao salvar em imagem PSD de 16 bits|Erro|
|PSDNET-899|O modo de mistura Dissolução não se aplica à pasta com máscara|Erro|
|PSDNET-1047|Arquivo específico não pode ser aberto pelo Photoshop após a salvamento no Aspose.PSD 21.11|Erro|
|PSDNET-1068|Renderização incorreta da camada com modo de mistura de Dodge Linear (Adicionar)|Erro|
|PSDNET-1069|A camada de Preenchimento de Padrão gera exceção na atualização após o carregamento|Erro|


## **Alterações na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-210. Adicionar propriedade IsOpen para Grupo de Camadas**

{{< highlight csharp >}}
// Exemplo de leitura e escrita da propriedade IsOpen em tempo de execução.
string nomeArquivoOrigem = "LayerGroupOpenClose.psd";
string nomeArquivoSaida = "Saída" + nomeArquivoOrigem;

using (var imagem = (PsdImage)Image.Load(nomeArquivoOrigem))
{
    foreach (var camada in imagem.Layers)
    {
        if (camada is LayerGroup && camada.Name == "Grupo 1")
        {
            bool grupo1Aberto = ((LayerGroup)camada).IsOpen;
            ((LayerGroup)camada).IsOpen = !grupo1Aberto;
        }

        if (camada is LayerGroup && camada.Name == "Grupo 2")
        {
            bool grupo2Aberto = ((LayerGroup)camada).IsOpen;           
            ((LayerGroup)camada).IsOpen = !grupo2Aberto;
        }
    }

    imagem.Save(nomeArquivoSaida);
}
{{< /highlight >}}

**PSDNET-643. Imagem PSD com máscaras de camada de raster descarta máscaras ao salvar em imagem PSD de 16 bits**

{{< highlight csharp >}}
            string caminhoArquivoOrigem = "UmaRegularEUmaRegularComMascara.psd";
            string caminhoArquivoSaida = "out_UmaRegularEUmaRegularComMascara.psd";

            using (PsdImage imagem = (PsdImage)Image.Load(caminhoArquivoOrigem))
            {
                imagem.Save(caminhoArquivoSaida, new PsdOptions(imagem)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. O modo de mistura Dissolução não se aplica à pasta com máscara**

{{< highlight csharp >}}
            string arquivoOrigem = "psdnet899.psd";
            string pngSaida = "out_psdnet899.png";

            using (PsdImage imagem = (PsdImage) Image.Load(arquivoOrigem))
            {
                imagem.Save(pngSaida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Arquivo específico não pode ser aberto pelo Photoshop após a salvamento no Aspose.PSD 21.11**

{{< highlight csharp >}}
            string arquivoOrigem = "psdnet1047.psd";
            string psdSaida = "out_psdnet1047.psd";

            using (PsdImage imagem = (PsdImage) Image.Load(arquivoOrigem))
            {
                imagem.Save(psdSaida);
            }

            // Necessário abrir manualmente o PSD de saída pelo Photoshop.

            using (PsdImage imagem = (PsdImage) Image.Load(psdSaida))
            {
                // sem exceção.
            }
{{< /highlight >}}

**PSDNET-1068. Renderização incorreta da camada com modo de mistura de Dodge Linear (Adicionar)**

{{< highlight csharp >}}
            string arquivoOrigem = "quebrado.psd";
            string pngSaida = "out_quebrado.psd.png";

            using (var imagemPsd = (PsdImage) Image.Load(arquivoOrigem))
            {
                imagemPsd.Save(pngSaida, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. A camada de Preenchimento de Padrão gera exceção na atualização após o carregamento**

{{< highlight csharp >}}
            string arquivoOrigem = "TodosOsTiposDeCamadaPsd.psd";

            using (var imagem = (PsdImage) Image.Load(arquivoOrigem))
            {
                var camadaPreenchimento = (FillLayer)imagem.Layers[9];
                camadaPreenchimento.Update();
            }
{{< /highlight >}}
