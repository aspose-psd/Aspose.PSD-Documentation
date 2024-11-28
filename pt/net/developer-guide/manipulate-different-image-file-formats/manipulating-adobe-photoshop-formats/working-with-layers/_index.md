---
title: Trabalhando com Camadas
type: docs
weight: 150
url: /pt/net/trabalhando-com-camadas/
---

## **Criar um Grupo de Camadas**
Um grupo de camadas consiste em uma ou mais camadas e ajuda a organizar camadas semelhantes ou relacionadas. Usando Aspose.PSD para .NET, você pode criar um grupo de camadas. Para isso, um novo método [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) foi adicionado na classe **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** para adicionar o grupo de camadas.

Os passos para criar grupos de camadas são simples:

- Crie uma instância de uma imagem usando a classe PsdImage com largura, altura e opções de imagem especificadas.
- Crie um [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) com o nome e índice do grupo especificados.
- Crie uma instância da classe Layer e atribua a imagem PSD a ela.
- Adicione a camada criada ao grupo de camadas usando o método AddLayer exposto pela classe LayerGroup.
- Salve os resultados.

O trecho de código a seguir mostra como criar um grupo de camadas.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CriarGruposDeCamadas-CriarGruposDeCamadas.cs" >}}


## **Renomear uma Camada**
Você pode usar qualquer nome que desejar, mas a prática típica é usar uma descrição geral do objeto ou elemento que está naquela camada. Este artigo demonstra como você pode alterar o nome de uma camada usando Aspose.PSD para .NET. Para isso, uma nova propriedade [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) foi adicionada na classe Layer para exibir corretamente um nome de camada. Foi observado que quando o Photoshop salva um nome de camada usando a propriedade [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), então caracteres coreanos são armazenados como byte 63'?' em ASCII. Portanto, se você deseja exibir corretamente um nome de camada, use a propriedade **DisplayName**, porque a propriedade **Name** não suporta caracteres coreanos.

O exemplo de código a seguir mostra como você pode renomear uma camada.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenomearCamada-RenomearCamada.cs" >}}
## **Suporte a Camadas Linkadas**
Linkar camadas é como agrupar as camadas. Se você estiver linkando duas ou mais camadas, permitirá fazer determinadas alterações em ambas as camadas vinculadas. Por exemplo, se você aplicar transformações a uma camada, elas serão aplicadas a todas as outras camadas vinculadas. Este artigo demonstra como você pode obter e desvincular camadas linkadas usando [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SuporteDeCamadaLinkada-SuporteDeCamadaLinkada.cs" >}}
