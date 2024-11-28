---
title: Desenho de Imagens
type: docs
weight: 10
url: /pt/java/desenho-de-imagens/
---

## **Desenhando Linhas**
Este exemplo usa a classe Graphics para desenhar formas de linha na superfície da imagem. Para demonstrar a operação, o exemplo cria uma nova Imagem e desenha linhas na superfície da Imagem usando o método DrawLine exposto pela classe Graphics. Primeiro, criaremos uma PsdImage especificando sua altura e largura.

Uma vez que a imagem tenha sido criada, usaremos o método Clear exposto pela classe Graphics para definir a cor de fundo. O método DrawLine da classe Graphics é usado para desenhar uma linha em uma imagem conectando duas estruturas de ponto. Este método tem várias sobrecargas que aceitam a instância da classe Pen e pares de coordenadas de pontos ou estruturas Point/PointF como argumentos. A classe Pen define um objeto usado para desenhar linhas, curvas e figuras. A classe Pen tem vários construtores sobrecarregados para desenhar linhas com cor, largura e pincel especificados. A classe SolidBrush é usada para desenhar continuamente com cor específica. Finalmente, a imagem é exportada para o formato de arquivo BMP. O trecho de código a seguir mostra como desenhar formas de linha na superfície da Imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}
## **Desenhando Elipse**
Exemplo de desenho de elipse é o segundo artigo na série de formas de desenho. Usaremos a classe Graphics para desenhar a forma de elipse na superfície da Imagem. Para demonstrar a operação, o exemplo cria uma nova Imagem e desenha a forma de elipse na superfície da Imagem usando o método DrawEllipse exposto pela classe Graphics. Primeiro, criamos uma PsdImage especificando sua altura e largura.

Após criar a imagem, criaremos e inicializaremos o objeto da classe Graphics e definiremos a cor de fundo da imagem usando o método Clear da classe Graphics. O método DrawEllipse da classe Graphics é usado para desenhar a forma de elipse na superfície da imagem especificada pela estrutura de retângulo delimitador. Este método tem várias sobrecargas que aceitam as instâncias das classes Pen e Rectangle/RectangleF ou pares de coordenadas, altura e largura como argumentos. A classe Pen define um objeto usado para desenhar linhas, curvas e figuras. A classe Pen tem vários construtores sobrecarregados para desenhar linhas com cor, largura e pincel especificados. A classe Rectangle armazena um conjunto de quatro inteiros que representam a localização e o tamanho de um retângulo. A classe Rectangle tem vários construtores sobrecarregados para desenhar a estrutura de retângulo com tamanho e localização específicos. A classe SolidBrush é usada para desenhar continuamente com cor específica. Finalmente, a imagem é exportada para o formato de arquivo BMP. O trecho de código a seguir mostra como desenhar a forma de elipse na superfície da Imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
## **Desenhando Retângulo**
Neste exemplo, desenharemos a forma de retângulo na superfície da Imagem. Para demonstrar a operação, o exemplo cria uma nova Imagem e desenha a forma de retângulo na superfície da imagem usando o método DrawRectangle exposto pela classe Graphics. Primeiro, criaremos uma PsdImage especificando sua altura e largura. Em seguida, definiremos a cor de fundo da Imagem usando o método Clear da classe Graphics.

O método DrawRectangle da classe Graphics é usado para desenhar a forma de retângulo em uma superfície de imagem especificada pela estrutura do retângulo. Este método tem várias sobrecargas que aceitam as instâncias das classes Pen e Rectangle/RectangleF ou par de coordenadas, largura e altura como argumentos. A classe Rectangle armazena um conjunto de quatro inteiros que representam a localização e o tamanho de um retângulo. A classe Rectangle tem vários construtores sobrecarregados para desenhar a estrutura de retângulo com tamanho e localização específicos. Finalmente, a imagem é exportada para o formato de arquivo BMP. O trecho de código a seguir mostra como desenhar a forma de retângulo na superfície da Imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}
## **Desenhando Arco**
Nesta sessão da série de formas de desenho, desenharemos a forma de Arco na superfície da Imagem. Usaremos o método DrawArc da classe Graphics para demonstrar a operação em uma imagem BMP. Primeiro, criaremos uma PsdImage especificando sua altura e largura. Uma vez que a imagem tenha sido criada, usaremos o método Clear exposto pela classe Graphics para definir sua cor de fundo.

O método DrawArc da classe Graphics é usado para desenhar a forma de Arco em uma superfície de imagem. DrawArc representa uma porção de uma elipse especificada pela estrutura de retângulo ou par de coordenadas. Este método tem várias sobrecargas que aceitam as instâncias das classes Pen e Rectangle/RectangleF ou um par de coordenadas, largura e altura como argumentos. Finalmente, a imagem é exportada para o formato de arquivo BMP. O trecho de código a seguir mostra como desenhar a forma de Arco na superfície da Imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
## **Desenhando Bezier**
Este exemplo usa a classe Graphics para desenhar a forma de Bezier na superfície da Imagem. Para demonstrar a operação, o exemplo cria uma nova Imagem e desenha a forma de Bezier na superfície da Imagem usando o método DrawBezier exposto pela classe Graphics. Primeiro, criamos uma PsdImage especificando sua altura e largura. Após a criação da imagem, usaremos o método Clear exposto pela classe Graphics para definir sua cor de fundo.

O método DrawBezier da classe Graphics é usado para desenhar a forma de Bezier spline em uma superfície de imagem definida por quatro estruturas de Point. Este método tem várias sobrecargas que aceitam as instâncias da classe Pen e quatro pares ordenados de coordenadas ou quatro estruturas Point/PointF ou array de estruturas Point/PointF. A classe Pen define um objeto usado para desenhar linhas, curvas e figuras. A classe Pen tem vários construtores sobrecarregados para desenhar linhas com cor, largura e pincel especificados. Finalmente, a imagem é exportada para o formato de arquivo BMP. O trecho de código a seguir mostra como desenhar a forma de Bezier na superfície da Imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
## **Desenhando Imagens usando a Funcionalidade Principal**
Aspose.PSD é uma biblioteca que oferece muitos recursos valiosos, incluindo a criação de imagens do zero. Desenhe usando a funcionalidade principal, como manipular as informações de bitmap de uma imagem, ou use recursos avançados como Graphics e GraphicsPath para desenhar formas na superfície da imagem com a ajuda de diferentes pincéis e canetas. Usando a classe RasterImage do Aspose.PSD, você pode recuperar as informações de pixel de uma área da imagem e manipulá-la. A classe RasterImage contém toda a funcionalidade principal de desenho, como obter e definir pixels e outros métodos para manipulação de imagem. Crie uma nova imagem usando qualquer um dos métodos descritos em Criando Arquivos e atribua-a a uma instância da classe RasterImage. Use o método LoadPixels da classe RasterImage para recuperar as informações de pixel de uma parte de uma imagem. Depois de obter uma matriz de pixels, você pode manipulá-la, por exemplo, alterando a cor de cada pixel. Depois de manipular as informações de pixel, defina-as de volta na área desejada da imagem usando o método SavePixels da classe RasterImage. O trecho de código a seguir mostra como desenhar imagens usando a funcionalidade principal.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}
