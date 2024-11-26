---
title: Desenho de Imagens
type: docs
weight: 10
url: /pt/net/drawing-images/
---

## **Desenho de Linhas**
Este exemplo utiliza a classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para desenhar formas de linha na superfície da imagem. Para demonstrar a operação, o exemplo cria uma nova imagem e desenha linhas na superfície da imagem usando o método [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) exposto pela classe Graphics. Primeiramente, criaremos um PsdImage especificando sua altura e largura.

Após a criação da imagem, usaremos o método Clear exposto pela classe Graphics para definir a cor de fundo. O método [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) é utilizado para desenhar uma linha em uma imagem conectando duas estruturas de ponto. Este método possui várias sobrecargas que aceitam a instância da classe Pen e pares de coordenadas de pontos ou estruturas Point/PointF como argumentos. A classe Pen define um objeto usado para desenhar linhas, curvas e figuras. A classe Pen possui vários construtores sobrecarregados para desenhar linhas com cor, largura e pincel especificados. A classe SolidBrush é utilizada para desenhar continuamente com uma cor específica. Finalmente, a imagem é exportada no formato de arquivo bmp. O trecho de código a seguir mostra como desenhar formas de linha na superfície da imagem.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoImagens-DesenhoLinhas-DesenhoLinhas.cs" >}}
## **Desenho de Elipse**
O exemplo de desenho de elipse é o segundo artigo na série de desenho de formas. Utilizaremos a classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para desenhar a forma de elipse na superfície da imagem. Para demonstrar a operação, o exemplo cria uma nova imagem e desenha a forma de elipse na superfície da imagem usando o método DrawEllipse exposto pela classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Primeiramente, criaremos um PsdImage especificando sua altura e largura.

Após a criação da imagem, criaremos e inicializaremos um objeto da classe Graphics e definiremos a cor de fundo da imagem usando o método Clear da classe Graphics. O método DrawEllipse da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) é utilizado para desenhar a forma de elipse em uma superfície de imagem especificada pela estrutura de retângulo limitante. Este método possui várias sobrecargas que aceitam as instâncias das classes Pen e Rectangle/RectangleF ou um par de coordenadas, uma altura e uma largura como argumentos. A classe Pen define um objeto usado para desenhar linhas, curvas e figuras. A classe Pen possui vários construtores sobrecarregados para desenhar linhas com cor, largura e pincel especificados. A classe Rectangle armazena um conjunto de quatro inteiros que representam a localização e o tamanho de um retângulo. A classe Rectangle possui vários construtores sobrecarregados para desenhar a estrutura de retângulo com tamanho e localização especificados. A classe SolidBrush é utilizada para desenhar continuamente com uma cor específica. Finalmente, a imagem é exportada no formato de arquivo bmp. O trecho de código a seguir mostra como desenhar a forma de elipse na superfície da imagem.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoImagens-DesenhoElipse-DesenhoElipse.cs" >}}
## **Desenho de Retângulo**
Neste exemplo, desenharemos a forma de retângulo na superfície da imagem. Para demonstrar a operação, o exemplo cria uma nova imagem e desenha a forma de retângulo na superfície da imagem usando o método DrawRectangle exposto pela classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Primeiramente, criaremos um PsdImage especificando sua altura e largura. Em seguida, definiremos a cor de fundo da imagem usando o método Clear da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).

O método DrawRectangle da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) é utilizado para desenhar a forma de retângulo em uma superfície de imagem especificada pela estrutura de retângulo. Este método possui várias sobrecargas que aceitam as instâncias das classes Pen e Rectangle/RectangleF ou um par de coordenadas, uma largura e uma altura como argumentos. A classe Rectangle armazena um conjunto de quatro inteiros que representam a localização e o tamanho de um retângulo. A classe Rectangle possui vários construtores sobrecarregados para desenhar a estrutura de retângulo com tamanho e localização especificados. Finalmente, a imagem é exportada no formato de arquivo bmp. O trecho de código a seguir mostra como desenhar a forma de retângulo na superfície da imagem.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoImagens-DesenhoRetangulo-DesenhoRetangulo.cs" >}}
## **Desenho de Arco**
Nesta sessão da série de formas de desenho, desenharemos a forma de arco na superfície da imagem. Utilizaremos o método DrawArc da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para demonstrar a operação em uma imagem BMP. Primeiramente, criaremos um PsdImage especificando sua altura e largura. Após a criação da imagem, utilizaremos o método Clear exposto pela classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para definir a sua cor de fundo.

O método DrawArc da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) é usado para desenhar a forma de arco em uma superfície de imagem. DrawArc representa uma porção de uma elipse especificada pela estrutura de retângulo ou par de coordenadas. Este método possui várias sobrecargas que aceitam as instâncias das classes Pen e estruturas Rectangle/RectangleF ou um par de coordenadas, uma largura e uma altura como argumentos. Finalmente, a imagem é exportada no formato de arquivo bmp. O trecho de código a seguir mostra como desenhar a forma de arco na superfície da imagem.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoImagens-DesenhoArco-DesenhoArco.cs" >}}
## **Desenho de Bezier**
Este exemplo utiliza a classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para desenhar a forma de Bezier na superfície da imagem. Para demonstrar a operação, o exemplo cria uma nova imagem e desenha a forma de Bezier na superfície da imagem usando o método DrawBezier exposto pela classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Primeiramente, criaremos um PsdImage especificando sua altura e largura. Após a criação da imagem, utilizaremos o método Clear exposto pela classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para definir a sua cor de fundo.

O método DrawBezier da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) é utilizado para desenhar a forma de spline Bezier em uma superfície de imagem definida por quatro estruturas de Ponto. Este método possui várias sobrecargas que aceitam as instâncias da classe Pen e quatro pares ordenados de coordenadas ou quatro estruturas de Point/PointF ou array de estruturas de Point/PointF. A classe Pen define um objeto usado para desenhar linhas, curvas e figuras. A classe Pen possui vários construtores sobrecarregados para desenhar linhas com cor, largura e pincel especificados. Finalmente, a imagem é exportada no formato de arquivo bmp. O trecho de código a seguir mostra como desenhar a forma de Bezier na superfície da imagem.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoImagens-DesenhoBezier-DesenhoBezier.cs" >}}
## **Desenhando Imagens usando Funcionalidades Principais**
Aspose.PSD é uma biblioteca que oferece muitos recursos valiosos, incluindo a criação de imagens a partir do zero. Desenhe usando a funcionalidade principal, como a manipulação das informações do bitmap da imagem, ou use recursos avançados como [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) e [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) para desenhar formas na superfície da imagem com a ajuda de diferentes pincéis e canetas. Usando a classe RasterImage do Aspose.PSD, você pode recuperar as informações de pixel de uma área da imagem e manipulá-la. A classe RasterImage contém toda a funcionalidade principal de desenho, como obter e definir pixels e outros métodos para manipulação de imagem. Crie uma nova imagem usando qualquer um dos métodos descritos em Criando Arquivos e atribua-a a uma instância da classe RasterImage. Use o método LoadPixels da classe RasterImage para recuperar as informações dos pixels de uma parte de uma imagem. Depois de ter um array de pixels, você pode manipulá-lo, por exemplo, alterando a cor de cada pixel. Após manipular as informações dos pixels, defina-as de volta para a área desejada na imagem usando o método SavePixels da classe RasterImage. O trecho de código a seguir mostra como desenhar imagens usando funcionalidades principais.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DesenhoImagens-FuncionalidadesPrincipais-FuncionalidadesPrincipais.cs" >}}

