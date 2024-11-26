---
title: Edição de máscaras de camada raster em arquivo PSD via API
type: docs
weight: 20
url: /pt/net/editando-mascaras-de-camada-raster-em-arquivo-psd-via-api/
---

## **Visão geral**
**Para automatizar a edição de formatos PSD e alterar arquivos PSD sem o Adobe® Photoshop®, você pode usar a API Aspose.PSD fornecida abaixo. Existem trechos de código em C# e .NET que podem ajudá-lo a modificar arquivos PSD.**

Usando Máscaras de Camada e Vetor PSD, somos capazes de ocultar e mostrar pixels de camada sem excluí-los permanentemente. Máscaras raster também são chamadas de máscara de camada ou máscara de usuário. O acesso às máscaras raster e vetor no Aspose.PSD é fornecido por meio da propriedade de camada [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata), que pode ser uma instância das classes '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' e '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' que são subclasses abstratas da classe 'LayerMaskData'. Se uma camada tem tanto máscaras raster quanto vetor, então é fornecida uma instância de [LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull). Se uma camada tem apenas uma máscara raster ou vetor, então é fornecida uma instância de [LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort). Se a propriedade LayerMaskData for nula, então a camada não tem máscaras ou apenas uma máscara vetor desativada.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Uma máscara raster e uma máscara de vetor desativada LayerMaskDataShort</p><p>Uma máscara raster desativada LayerMaskDataShort</p><p>Uma máscara raster e uma máscara vetor LayerMaskDataFull</p><p>Uma máscara raster LayerMaskDataShort</p><p>Uma máscara vetor LayerMaskDataShort</p><p>Uma máscara de vetor desativada nula (Mas recurso de vetor está presente)</p>|
| :- | :- |
## **Como obter uma máscara raster de camada no arquivo PSD?**
Primeiramente, devemos verificar se uma camada tem tanto máscaras de vetor quanto de camada:

O código de exemplo fornecido abaixo demonstra como obter uma máscara raster de camada

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Caso contrário, o tipo da propriedade de camada LayerMaskData é LayerMaskDataShort. Nesse caso, vamos verificar se a camada tem apenas uma máscara raster verificando a propriedade Flags. Não deve conter o [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** flag, caso contrário a máscara é um cache de máscara de vetor.


Obtendo trecho de código da máscara:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Se você precisar **extrair uma máscara raster** como LayerMaskDataShort (para manipulações adicionais) mesmo quando ambas as máscaras estiverem presentes, a LayerMaskDataFull deverá ser extraída e convertida para LayerMaskDataShort. O código a seguir pode ser usado para ambos os casos:

Extraindo uma máscara raster do PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **Como verificar se uma camada no arquivo PSD tem uma máscara raster?**
O seguinte código em C# pode ajudá-lo a verificar se uma camada tem uma máscara raster:

Como saber se a máscara raster foi aplicada à [Camada PSD](/psd/pt/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **Como remover / adicionar / atualizar uma máscara raster de camada no arquivo PSD?**
Apenas remover / adicionar / atualizar o LayerMaskData não é suficiente para a correção do salvamento, pois os canais não são atualizados; embora possa fornecer uma renderização correta. Isso não altera os canais de máscara:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Devemos usar o método AddLayerMask da camada para remover / adicionar / atualizar.

Isso adiciona/atualiza tanto a máscara quanto os canais:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Isso remove tanto a máscara quanto os canais:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **Removendo uma máscara raster de camada na imagem PSD**
Primeiramente, verificamos se a máscara está no formato curto e se não é de vetor, podemos simplesmente chamar o método AddLayerMask com null para excluir a máscara raster. Mas se estiver no formato completo, precisamos convertê-la para o formato curto, deixando apenas a máscara de vetor. Para remover uma máscara de camada, o seguinte trecho de código em C# .NET pode ser usado:

Trecho de código de como remover Máscara de Camada do Arquivo PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **Atualizando uma máscara raster de camada na imagem PSD**
Isso é direto: se a máscara estiver no formato curto, devemos alterar ImageData e MaskRectangle se necessário, caso contrário [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)e [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)devem ser alterados. O seguinte trecho de código em C# .NET pode ser usado para atualizar uma máscara de camada:

Atualizar Máscara de Camada PSD com C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Aqui está um exemplo de possíveis ações que alteram uma máscara raster. Este inverte uma máscara de usuário de camada:

Atualizar Máscara de Camada PSD com C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **Atualizando uma máscara de vetor no arquivo PSD quando uma máscara raster de camada está presente**
Supõe-se que um usuário já tenha alterado um recurso de caminho de vetor. Em seguida, pode atualizar a máscara de vetor simplesmente chamando o método de camada [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask):

Atualizar [Máscara de Vetor de Camada PSD](/psd/pt/net/layer-vector-mask/) com C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **Adicionando uma máscara raster de camada no arquivo PSD**
Se uma camada não tem máscara, podemos adicionar a máscara raster fornecida simplesmente chamando o método de camada AddLayerMask.

Se a máscara não tem a flag [UserMaskFromRenderingOtherData**](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags), então ela já possui uma máscara raster e devemos atualizá-la conforme descrito acima. Caso contrário, se esta máscara estiver em um formato curto, a convertamos para o formato completo. Se não, a usamos como está. Em seguida, atualize UserMaskData, UserMaskRectangle e outras propriedades com as propriedades da máscara fornecida. O seguinte trecho de código em C# .NET pode ser usado para adicionar (atualizar) uma máscara de camada:

Adicionar nova Máscara de Camada ao PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Como verificar se uma máscara de camada está habilitada?**
Para descobrir o estado habilitado da máscara raster da camada, podemos verificar o estado da flag LayerMaskFlags.Disabled na propriedade Flags para LayerMaskDataShort ou em RealFlags para LayerMaskDataFull. O seguinte trecho de código em C# .NET pode ser usado para obter o estado habilitado da máscara da camada:

Verificar se uma máscara está habilitada:

{{< gist "aspose-com-gists" "8a4d46ce856269c7ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **Como habilitar ou desabilitar uma máscara de camada raster?**
Para habilitar ou desabilitar uma máscara de camada raster, podemos mudar o estado da flag LayerMaskFlags.Disabled na propriedade Flags para LayerMaskDataShort ou em RealFlags para LayerMaskDataFull. O seguinte trecho de código em C# .NET pode ser usado para alterar o estado habilitado de uma máscara de camada:

Habilitar ou desabilitar Máscara de Camada Raster:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}
