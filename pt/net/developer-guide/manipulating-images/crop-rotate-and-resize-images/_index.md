---
title: Recortar, Girar e Redimensionar Imagens
type: docs
weight: 40
url: /pt/net/recortar-girar-e-redimensionar-imagens/
---

## **Recortar Imagens**
O recorte de imagens geralmente refere-se à remoção das partes externas de uma imagem para ajudar a melhorar o enquadramento. O recorte também pode ser usado para cortar alguma parte de uma imagem e aumentar o foco em uma área específica. A API Aspose.PSD oferece dois métodos diferentes para recortar imagens: por deslocamentos e por retângulo.
### **Recortar por Deslocamentos**
A classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) fornece uma versão sobrecarregada do método Crop que aceita 4 valores inteiros que denotam Esquerda, Direita, Topo e Base. Com base nesses quatro valores, o método Crop move os limites da imagem em direção ao centro da imagem, descartando a porção externa. O trecho de código abaixo demonstra como recortar uma imagem por deslocamentos.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Recortar por Retângulo**
A classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) fornece outra versão sobrecarregada do método Crop que aceita uma instância da classe Rectangle. Você pode recortar qualquer parte de uma imagem fornecendo os limites desejados ao objeto Rectangle. O trecho de código abaixo demonstra como recortar qualquer imagem por meio de um retângulo.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Girar e Virar uma Imagem**
Aspose.PSD para .NET é uma biblioteca fácil de usar porque fornece métodos simples para realizar operações complexas. Por exemplo, o Aspose.PSD para .NET disponibiliza o método RotateFlip para a sua classe base Image se um aplicativo precisar girar uma imagem. Independentemente do formato da imagem, a biblioteca pode realizar procedimentos específicos de Rotação & Viragem nela.
### **Girar uma Imagem**
O método Image.RotateFlip pode ser usado para girar a imagem em 90/180/270 graus e virar a imagem horizontalmente ou verticalmente. O método Image.RotateFlip aceita um parâmetro do tipo RotateFlipType que especifica o tipo de rotação e viragem a ser aplicado à imagem. Os passos para realizar a Rotação & Viragem são simples, como abaixo,

1. Carregar a imagem usando o método fábrica Load exposto pela classe Image.
1. Chamar o método Image.RotateFlip especificando o RotateFlipType apropriado.
1. Salvar os resultados.

O exemplo de código a seguir demonstra como definir a propriedade RotateFlip de uma Imagem e a enumeração RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Girar uma Imagem em um Ângulo Específico**
A API Aspose.PSD para .NET expõe o método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate para facilitar seus usuários que desejam girar uma imagem em um ângulo específico. Ao contrário do método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, o método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate aceita três parâmetros:

1. Ângulo de rotação: Um parâmetro do tipo float que especifica o ângulo de rotação para o qual a imagem deve ser girada. Um valor positivo gira a imagem no sentido horário; um valor negativo realiza uma rotação antihorária.
1. Redimensionar proporcionalmente: Um parâmetro do tipo Boolean que especifica se o tamanho da imagem deve ser alterado de acordo com as projeções do retângulo rotacionado (pontos do canto). Se definido como falso, as dimensões da imagem não serão alteradas e apenas o conteúdo interno da imagem será rotacionado.
1. Cor de fundo: Um parâmetro do tipo Color que especifica a cor a ser preenchida no fundo da imagem rotacionada.

O trecho de código abaixo demonstra o uso do método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Redimensionar Imagens**
Este artigo demonstra o uso do Aspose.PSD para .NET para realizar a operação de redimensionamento em uma imagem. As APIs Aspose.PSD expuseram métodos eficazes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD para .NET expôs o método Resize para a classe Image que pode ser usado para redimensionar imagens existentes instantaneamente. Há duas sobrecargas do método Resize para atender às necessidades do aplicativo.
### **Redimensionamento Simples**
Os passos para realizar o redimensionamento são simples, como abaixo:

1. Carregar a imagem usando o método fábrica Load exposto pela classe Image.
1. Chamar o método Image.Resize especificando nova Altura & Largura.
1. Salvar os resultados.

O exemplo de código a seguir demonstra como redimensionar uma imagem.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **Redimensionar com Enumeração ResizeType**
A API Aspose.PSD expôs a enumeração ResizeType que pode ser usada com o método Image.Resize para alcançar os resultados desejados. O trecho de código fornecido abaixo demonstra o uso da enumeração ResizeType, enquanto os detalhes dos membros da enumeração ResizeType podem ser encontrados no final desta página.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



Se você deseja obter um resultado de qualidade após aplicar o redimensionamento, é recomendável usar sempre o ResizeType.LanczosResample, pois ele fornecerá resultados altamente qualitativos, mas pode funcionar mais lentamente do que o ResizeType.NearestNeighbourResample. Por outro lado, o algoritmo ResizeType.NearestNeighbourResample é especificamente usado para redimensionamento rápido, comprometendo a qualidade da imagem. Este método pode ser útil para geração de miniaturas em tempo real ou processos similares onde o desempenho é necessário.
## **Redimensionar Imagem Proporcionalmente**
Você pode redimensionar imagens passando novos valores de altura e largura como parâmetros para o método Image.Resize, mas, nesse caso, você terá que calcular a proporção você mesmo. Isso ocorre porque, quando a largura ou a altura de uma imagem é alterada, a imagem é dimensionada ou reduzida para preencher o novo tamanho. Se as alterações na largura e altura de uma imagem não estiverem em proporção, isso pode resultar em um resultado esticado e distorcido. Este artigo demonstra o uso do Aspose.PSD para .NET API para redimensionar imagens passando apenas uma nova altura ou largura, permitindo que a API calcule automaticamente o outro valor proporcional.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Enumeração ResizeType**
ResizeType determina o tipo de redimensionamento a ser realizado na imagem com base no filtro selecionado.

Membros da [Enumeração ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**Nome do Membro**|**Valor**|**Descrição**|
| :- | :- | :- |
|LeftTopToLeftTop|0|O ponto superior esquerdo da nova imagem coincidirá com o ponto superior esquerdo da imagem original. O corte ocorrerá se necessário.|
|RightTopToRightTop|1|O ponto superior direito da nova imagem coincidirá com o ponto superior direito da imagem original. O corte ocorrerá se necessário.|
|RightBottomToRightBottom|2|O ponto inferior direito da nova imagem coincidirá com o ponto inferior direito da imagem original. O corte ocorrerá se necessário.|
|LeftBottomToLeftBottom|3|O ponto inferior esquerdo da nova imagem coincidirá com o ponto inferior esquerdo da imagem original. O corte ocorrerá se necessário.|
|CenterToCenter|4|O centro da nova imagem coincidirá com o centro da imagem original. O corte ocorrerá se necessário.|
|LanczosResample|5|Resample usando o algoritmo Lanczos usando máscara 7x7.|
|NearestNeighbourResample|6|Resample usando o algoritmo de vizinho mais próximo.|

