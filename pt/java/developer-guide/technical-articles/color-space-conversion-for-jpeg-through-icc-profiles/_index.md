---
title: Conversão de Espaço de Cor para JPEG através de Perfis ICC
type: docs
weight: 50
url: /pt/java/conversao-de-espaco-de-cor-para-jpeg-atraves-de-perfis-icc/
---

## **Gestão de Cor para o Formato JPEG**

Este artigo discute o uso de perfis ICC para realizar a gestão do espaço de cor ao lidar com o formato JPEG com APIs Aspose.PSD. O espaço de cor interno do JPEG é YCbCr, no entanto, este formato também pode acomodar espaços de cor Escala de Cinza, RGB, CMYK e YCCK para armazenar os metadados da imagem. As APIs Aspose.PSD operam principalmente no espaço RGB, portanto, a API precisa realizar a conversão de espaço de cor de e para a fim de manipular corretamente os arquivos JPEG. Conversões de Escala de Cinza para RGB e de YCbCr para RGB podem ser feitas com transformações matemáticas, mas os espaços CMYK e YCCK não podem ser facilmente convertidos para o espaço RGB.

As APIs Aspose.PSD precisam realizar a transformação direta de cor de RGB para CMYK para imagens JPEG com espaço de cor CMYK. Por outro lado, as imagens com espaço de cor YCCK requerem a transformação de cor de RGB para CMYK para YCCK, onde a transformação de CMYK para YCCK usa a conversão ITU-R BT.601 aplicada aos três primeiros canais, deixando o canal k intocado. Em resumo, as APIs Aspose.PSD precisam realizar a interconversão dos espaços de cor RGB e CMYK para ambas as imagens CMYK e YCCK, e essas transformações são feitas com a ajuda de perfis ICC, que são basicamente tabelas de pesquisa descrevendo as propriedades de uma cor e ajudando nas transformações de cor.

## **Perfis ICC**

O mecanismo de conversão ICC usa "Perfis" que mapeiam o espaço de cor de origem para os espaços de cor CIELAB ou CIEXYZ independentes do dispositivo. Aspose.PSD pode converter dados para o espaço de cor conforme necessário ao usar esses dois espaços de cor com perfis adicionais. Portanto, para a conversão ICC, o usuário precisa fornecer dois perfis - um perfil RGB para chegar ao espaço de cor CIE interno e um perfil CMYK para ter as características de cor CMYK. Para obter a conversão de CMYK para RGB, é necessário trocar os perfis, ou seja, usar o perfil CMYK como perfil de origem e o perfil RGB como perfil de destino.

## **Conversão de Cor para JPEG através de Perfis ICC**

As APIs Aspose.PSD ocultam os detalhes, fornecendo um mecanismo fácil de usar para especificar perfis ICC via classe JpegOptions. Além disso, o Aspose.PSD usa os perfis de exemplo SWOP CMYK e sRGB embutidos em seu núcleo, portanto, na maioria dos casos de uso comuns, o usuário não precisa procurar por perfis específicos. Existe uma desvantagem dessas correções, ou seja, tais conversões de espaço de cor são irreversíveis, porque não podemos esperar obter a mesma cor após a conversão de RGB para CMYK para RGB devido aos espaços de cor incompatíveis e perfis de cor diferentes. O trecho de código a seguir demonstra o uso do Aspose.PSD para a API Java para especificar perfis de cor RGB e CMYK para a imagem JPEG YCCK. No exemplo abaixo, os perfis de cor RGB e CMYK são alterados e a imagem é salva no espaço de cor YCCK. Observe que as propriedades RgbColorProfile e CmykColorProfile funcionarão para alterar os dados de pixel para o espaço de cor YCCK. Todos os outros espaços de cor não recuperam perfis de cor para atualizar os dados de cor.

`{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}`

Se nenhum perfil for definido, a API Java Aspose.PSD usará os perfis padrão. O exemplo abaixo utiliza as propriedades de perfis de destino que alteram o espaço de cor de destino para a maioria das JpegImages.

`{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}`
