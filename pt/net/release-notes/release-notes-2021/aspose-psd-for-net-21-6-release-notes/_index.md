---
title: Aspose.PSD para .NET 21.6 - Notas de Lançamento
type: docs
weight: 70
url: /pt/net/aspose-psd-para-net-21-6-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para [Aspose.PSD para .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-546|Máscara de recorte para um grupo não é renderizada corretamente|Erro|
|PSDNET-547|Máscara regular ou vetorial para um grupo de camadas é ignorada na renderização|Erro|
|PSDNET-647|Imagem PSD com máscaras de camada vetoriais desativadas ao salvar habilita máscaras vetoriais|Erro|
|PSDNET-786|Exceção ao criar uma TextLayer com texto maior que 255 caracteres|Erro|
|PSDNET-900|Texto da camada de texto não pode ser renderizado no Linux|Aprimoramento|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-546. Máscara de recorte para um grupo não é renderizada corretamente**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Máscara regular ou vetorial para um grupo de camadas é ignorada na renderização**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. Imagem PSD com máscaras de camada vetoriais desativadas ao salvar habilita máscaras vetoriais**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Exceção ao criar uma TextLayer com texto maior que 255 caracteres**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
