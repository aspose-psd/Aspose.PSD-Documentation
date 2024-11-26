---
title: Notas da Versão Aspose.PSD Adapters para .NET 24.4
type: docs
weight: 100
url: /pt/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}
Esta página contém notas de lançamento para [Aspose.PSD Adapters para .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)
{{% /alert %}}

| **Chave**    | **Resumo**                                                                     | **Categoria** |
|:------------|:-----------------------------------------------------------------------------|:------------|
| PSDNET-1985  | Publicação inicial do Aspose.PSD.Adapters.Imaging no Nuget                    | Aprimoramento |


## **Alterações na API Pública**

# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

Por favor, verifique a [página de documentação do Aspose.PSD.Adapters](/psd/pt/net/adapters)

**PSDNET-1985. Exemplo mais completo de uso dos Aspose.PSD Adapters**

{{< highlight csharp >}}
// Adicione a ativação dos adaptadores na sua configuração de inicialização
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// adicionalmente, ative os Exporters
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Para trabalhar com adaptadores, você precisa de Licenças tanto para Aspose.PSD quanto para a adaptação
// Aqui está como aplicar a Licença Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Aqui está um exemplo de como aplicar a Licença Adaptee para Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Então você pode executar qualquer código dos adaptadores ou das bibliotecas PSD ou Imaging

// Depois disso, todos esses arquivos podem ser abertos pelo Aspose.PSD sem código adicional, apenas utilize
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Após a execução deste código, você obterá o arquivo PSD criado a partir de WEBP e poderá aplicar quaisquer filtros, camadas e ajustes do Aspose.PSD, incluindo Transformação Warp
}

// Você também pode criar Adaptees de Exportação de Imagens para Formato PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Use a API Aspose.Imaging para Editar o arquivo WEBP com recursos específicos de Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Em seguida, basta usar o método ToPsdImage() e editar o arquivo como PSD com recursos semelhantes ao Photoshop, incluindo camadas, filtros inteligentes e objetos inteligentes.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Algum texto", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Salve o arquivo PSD final usando Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Se você não precisa utilizar os Loaders ou Exporters fornecidos pelos Adaptadores, simplesmente desative-os
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
