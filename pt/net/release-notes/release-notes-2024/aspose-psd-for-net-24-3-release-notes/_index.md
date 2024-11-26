---
title: Aspose.PSD para .NET 24.3 - Notas da versão
type: docs
weight: 100
url: /pt/net/aspose-psd-para-net-24-3-notas-da-versao/
---

{{% alert color="primary" %}}

Esta página contém notas de versão para [Aspose.PSD para .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Sumário**                                                          | **Categoria** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI Format] Reduza o tempo de carregamento de imagens AI multipágina grandes |     Melhoria     |
| PSDNET-1905 | Arquivo PSD após a conversão de 8 bits para 16 bits tornou-se ilegível |     Bug     |
| PSDNET-1906 | Arquivo PSD após a conversão de 8 bits para 32 bits tornou-se ilegível |     Bug     |
| PSDNET-1921 | [AI Format] Corrija a renderização da Curva Curta no arquivo AI       |     Bug     |

## **Mudanças na API pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de uso:**

**PSDNET-1905. Arquivo PSD após a conversão de 8 bits para 16 bits tornou-se ilegível**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // está correto
    }
    else
    {
        throw new Exception("Recurso global incorreto, o primeiro recurso deve ser Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. Arquivo PSD após a conversão de 8 bits para 32 bits tornou-se ilegível**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // está correto
    }
    else
    {
        throw new Exception("Recurso global incorreto, o primeiro recurso deve ser Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI Format] Corrija a renderização da Curva Curta no arquivo AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
