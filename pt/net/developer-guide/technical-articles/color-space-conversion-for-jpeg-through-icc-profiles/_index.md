---
title: Conversão de Espaço de Cor para JPEG através de Perfis ICC
type: docs
weight: 60
url: /pt/conversao-de-espaco-cor-para-jpeg-atraves-de-perfis-icc/
---

## **Gerenciamento de Cor para Formato JPEG**

Este artigo discute o uso dos perfis ICC para realizar o gerenciamento de espaço de cor ao lidar com o formato JPEG usando as APIs Aspose.PSD. O espaço de cor interno do JPEG é YCbCr, no entanto, esse [formato](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) também pode acomodar espaços de cor em Escala de Cinza, RGB, CMYK e YCCK para armazenar os metadados da imagem. As APIs Aspose.PSD operam principalmente no espaço RGB, sendo necessário que a API realize conversões de e para o espaço de cor a fim de lidar adequadamente com os arquivos JPEG. As conversões de Escala de Cinza para RGB e de YCbCr para RGB podem ser feitas com transformações matemáticas, mas os espaços CMYK e YCCK não podem ser facilmente convertidos para o espaço RGB.

As APIs Aspose.PSD devem realizar a transformação direta de cor RGB para CMYK em imagens JPEG que possuem espaço de cor CMYK. Por outro lado, as imagens com espaço de cor YCCK exigem uma transformação de cor RGB para CMYK para YCCK, sendo que a transformação de CMYK para YCCK utiliza a conversão [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) aplicada aos três primeiros canais, deixando o canal k intocado. Em resumo, as APIs Aspose.PSD devem realizar a interconversão de espaços de cor RGB e CMYK para ambas as imagens CMYK e YCCK, e tais transformações são feitas com a ajuda de perfis ICC, que são essencialmente tabelas de pesquisa descrevendo as propriedades de uma cor e ajudando nas transformações de cor.

## **Perfis ICC**
O mecanismo de conversão ICC usa "Perfis" que mapeiam o espaço de cor de origem para os espaços de cor CIELAB ou CIEXYZ independentes do dispositivo. O Aspose.PSD pode converter dados em espaço de cor conforme necessário ao usar esses dois espaços de cor com perfis adicionais. Portanto, para a conversão ICC, o usuário precisa fornecer dois perfis: um perfil RGB para chegar ao espaço de cor CIE interno e um perfil CMYK para obter as características de cor CMYK. Para realizar a conversão de CMYK para RGB, é necessário trocar os perfis, ou seja, usar o perfil CMYK como perfil de origem e o perfil RGB como perfil de destino.

## **Conversão de Cor para JPEG através de Perfis ICC**
As APIs Aspose.PSD ocultam os detalhes, fornecendo um mecanismo fácil de usar para especificar perfis ICC via classe [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Além disso, o Aspose.PSD usa os perfis de exemplo SWOP, CMYK e sRGB incorporados em seu núcleo, portanto, na maioria dos casos de uso comuns, o usuário não precisa procurar por perfis específicos. Há uma desvantagem de tais correções, ou seja, tais conversões de espaço de cor são irreversíveis, pois não podemos esperar obter a mesma cor após a conversão de RGB para CMYK para RGB devido a espaços de cor incompatíveis e perfis de cor diferentes. O trecho de código a seguir demonstra o uso do Aspose.PSD para a API .NET para especificar os perfis de cor RGB e CMYK para a imagem JPEG YCCK. No exemplo abaixo, os perfis de cor RGB e CMYK são alterados e a imagem é salva no espaço de cor YCCK. Observe que as propriedades [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) e [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) funcionarão para alterar os dados de pixel para o espaço de cor YCCK. Todos os outros espaços de cor não obtêm os perfis de cor para atualização dos dados de cor.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

Se nenhum perfil for definido, a API Aspose.PSD para .NET usará os perfis padrão. O exemplo abaixo usa as propriedades de perfis de destino que alteram o espaço de cor de destino para a maioria das imagens JPEG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
