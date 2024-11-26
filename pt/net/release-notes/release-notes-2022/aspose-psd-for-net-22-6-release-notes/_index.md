---
title: Notas da Versão Aspose.PSD para .NET 22.6
type: docs
weight: 70
url: /pt/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas de versão para [Aspose.PSD para .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-940|Criação de API para obter o hash único para camadas semelhantes em arquivos diferentes|Aprimoramento|
|PSDNET-678|Renderização incorreta da Camada de Preenchimento com padrão no caso em que os padrões são mais de um e a ordem das camadas é alterada|Erro|
|PSDNET-1125|Exceção ao carregar um arquivo PSD específico com modo de cor CMYK|Erro|


## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-678. Renderização incorreta da Camada de Preenchimento com padrão no caso em que os padrões são mais de um e a ordem das camadas é alterada**

{{< highlight csharp >}}
string arquivoFonte = "badPattern.psd";
string pngSaida = "out_678.png";

using (var imagemPsd = (PsdImage)Image.Load(arquivoFonte))
{
    FillLayer camada1 = (FillLayer)imagemPsd.Layers[1];
    FillLayer camada2 = (FillLayer)imagemPsd.Layers[2];

    camada1.Update();
    camada2.Update();

    imagemPsd.Save(pngSaida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Criação de API para obter o hash único para camadas semelhantes em arquivos diferentes**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    static void Main()
    {
        // Implementação do teste
    }
}
{{< /highlight >}}

**PSDNET-1125. Exceção ao carregar um arquivo PSD específico com modo de cor CMYK**

{{< highlight csharp >}}
string arquivoFonte = "02_alpha-channels.psd";
string pngSaida = "out_1125.png";

using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))
{
    imagem.Save(pngSaida, new PngOptions());
}
{{< /highlight >}}