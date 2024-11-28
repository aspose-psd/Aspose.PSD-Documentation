---
title: Cortar, Girar e Redimensionar Imagens
type: docs
weight: 40
url: /pt/java/cortar-girar-e-redimensionar-imagens/
---

## **Cortar Imagens**
O corte de imagens geralmente se refere à remoção das partes externas de uma imagem para ajudar a melhorar o enquadramento. O corte também pode ser usado para recortar alguma parte de uma imagem a fim de aumentar o foco em uma área específica. A API Aspose.PSD suporta duas abordagens diferentes para cortar imagens: por deslocamentos e por retângulo.
### **Cortando por Deslocamentos**
A classe RasterImage fornece uma versão sobrecarregada do método Crop que aceita 4 valores inteiros denotando Esquerda, Direita, Topo e Inferior. Com base nesses quatro valores, o método Crop move as bordas da imagem em direção ao centro da imagem, descartando a parte externa. O trecho de código abaixo demonstra como cortar uma imagem por deslocamentos.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Cortando por Retângulo**
A classe RasterImage fornece outra versão sobrecarregada do método Crop que aceita uma instância da classe Rectangle. Você pode recortar qualquer parte de uma imagem fornecendo os limites desejados ao objeto Rectangle. O trecho de código abaixo demonstra como cortar qualquer imagem por Retângulo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Girar e Inverter uma Imagem**
O Aspose.PSD para Java é uma biblioteca fácil de usar pois fornece métodos simples para realizar operações complexas. Por exemplo, o Aspose.PSD para Java fornece o método RotateFlip para sua classe base Image se uma aplicação requer a rotação de uma imagem. Independentemente do formato da imagem, a biblioteca pode executar um procedimento específico de Rotação e Inversão nela.
### **Rotacionando uma Imagem**
O método Image.RotateFlip pode ser usado para girar a imagem em 90/180/270 graus e inverter a imagem horizontal ou verticalmente. O método Image.RotateFlip aceita um parâmetro RotateFlipType que especifica o tipo de rotação e inversão a ser aplicado à imagem. Os passos para realizar a Rotação e Inversão são simples como abaixo,

1. Carregar a imagem usando o método de fábrica Load exposto pela classe Image.
1. Chamar o método Image.RotateFlip especificando o RotateFlipType apropriado.
1. Salvar os resultados.

O exemplo de código a seguir demonstra como definir a propriedade RotateFlip de uma imagem e a enumeração RotateFlipType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Rotacionar uma Imagem em um Ângulo Específico**
O Aspose.PSD para Java API expõe o método RasterImage.Rotate para facilitar seus usuários que desejam rotacionar uma imagem em um ângulo específico. Ao contrário do método RasterImage.RotateFlip, o método RasterImage.Rotate aceita três parâmetros:

1. Ângulo de rotação: Um parâmetro do tipo float que especifica o ângulo de rotação no qual a imagem deve ser girada. Um valor positivo gira a imagem no sentido horário; um valor negativo realiza uma rotação no sentido anti-horário.
1. Redimensionar proporcionalmente: Um parâmetro do tipo Boolean que especifica se o tamanho da imagem deve ser alterado de acordo com as projeções do retângulo rotacionado (pontos de canto). Se definido como false, as dimensões da imagem não seriam modificadas e apenas o conteúdo interno da imagem seria girado.
1. Cor de fundo: Um parâmetro do tipo Color que especifica a cor a ser preenchida no fundo da imagem girada.

O trecho de código abaixo demonstra o uso do método RasterImage.Rotate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Redimensionar Imagens**
Este artigo demonstra o uso do Aspose.PSD para Java para realizar a operação de redimensionamento em uma imagem. As APIs Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar esse objetivo. O Aspose.PSD para Java expôs o método Resize para a classe Image que pode ser usado para redimensionar imagens existentes dinamicamente. Existem duas sobrecargas do método Resize para atender às necessidades da aplicação.
### **Redimensionamento Simples**
Os passos para realizar o redimensionamento são simples como abaixo:

1. Carregar a imagem usando o método de fábrica Load exposto pela classe Image.
1. Chamar o método Image.Resize especificando a nova Altura e Largura.
1. Salvar os resultados.

O exemplo de código a seguir demonstra como redimensionar uma imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Redimensionando com Enumeração ResizeType**
A API Aspose.PSD expôs a enumeração ResizeType que pode ser usada com o Image.Resize para alcançar os resultados desejados. O trecho de código fornecido abaixo demonstra o uso da enumeração ResizeType, enquanto os detalhes dos membros da enumeração ResizeType podem ser encontrados na parte inferior desta página.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



Se você pretende obter um resultado de qualidade após aplicar o redimensionamento, é sugerido que você sempre use o ResizeType.LanczosResample pois ele fornecerá resultados altamente qualitativos, porém pode funcionar mais lentamente do que o ResizeType.NearestNeighbourResample. Por outro lado, o algoritmo ResizeType.NearestNeighbourResample é especificamente usado para redimensionamento rápido, comprometendo a qualidade da imagem. Este método pode ser útil para geração de miniaturas em tempo real ou processos semelhantes onde o desempenho é necessário.
## **Redimensionar Imagem Proporcionalmente**
Você pode redimensionar imagens passando novos valores de altura e largura como parâmetros para o método Image.Resize, mas nesse caso você terá que calcular a proporção aspecto. Isso ocorre porque quando a largura ou altura de uma imagem é alterada, a imagem é escalada ou reduzida para preencher o novo tamanho. Se as alterações na largura e altura de uma imagem não estiverem em proporção, isso pode levar a um resultado esticado e distorcido. Este artigo demonstra o uso do Aspose.PSD para API Java para redimensionar imagens passando apenas a nova altura ou largura, permitindo que a API calcule automaticamente o outro valor proporcional.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **Enumeração ResizeType**
ResizeType determina o tipo de redimensionamento a ser realizado na imagem com base no filtro selecionado.

Membros da Enumeração ResizeType

|**Nome do Membro**|**Valor**|**Descrição**|
| :- | :- | :- |
|LeftTopToLeftTop|0|O ponto superior esquerdo da nova imagem coincidirá com o ponto superior esquerdo da imagem original. O corte ocorrerá se necessário.|
|RightTopToRightTop|1|O ponto superior direito da nova imagem coincidirá com o ponto superior direito da imagem original. O corte ocorrerá se necessário.|
|RightBottomToRightBottom|2|O ponto inferior direito da nova imagem coincidirá com o ponto inferior direito da imagem original. O corte ocorrerá se necessário.|
|LeftBottomToLeftBottom|3|O ponto inferior esquerdo da nova imagem coincidirá com o ponto inferior esquerdo da imagem original. O corte ocorrerá se necessário.|
|CenterToCenter|4|O centro da nova imagem coincidirá com o centro da imagem original. O corte ocorrerá se necessário.|
|LanczosResample|5|Redimensionar usando o algoritmo Lanczos usando máscara 7x7.|
|NearestNeighbourResample|6|Redimensionar usando o algoritmo do vizinho mais próximo.|
