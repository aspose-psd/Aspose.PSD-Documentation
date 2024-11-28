---
title: Notas da Versão de Aspose.PSD para Java 21.6
type: docs
weight: 40
url: /pt/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} Esta página contém as notas de lançamento para [Aspose.PSD para Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-351|Máscara de recorte para um grupo não é renderizada corretamente|Bug|
|PSDJAVA-352|Máscara regular ou vetorial para um grupo de camadas é ignorada na renderização|Bug|
|PSDJAVA-353|Imagem PSD com máscaras de camada vetoriais desativadas ao salvar habilita as máscaras vetoriais|Bug|
|PSDJAVA-354|Exceção ao criar uma TextLayer com texto maior que 255 caracteres|Bug|

# **Alterações na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

# **Exemplos de Uso:**

**PSDJAVA-351. Máscara de recorte para um grupo não é renderizada corretamente**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Máscara regular ou vetorial para um grupo de camadas é ignorada na renderização**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. Imagem PSD com máscaras de camada vetoriais desativadas ao salvar habilita as máscaras vetoriais**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Exceção ao criar uma TextLayer com texto maior que 255 caracteres**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
