---
title: Desenho de Imagens usando Gráficos
type: docs
weight: 20
url: /pt/java/desenhando-imagens-usando-graficos/
---

## **Desenho de Imagens usando Gráficos**

Com a biblioteca Aspose.PSD você pode desenhar formas simples como linhas, retângulos e círculos, bem como formas complexas como polígonos, curvas, arcos e formas de Bezier. A biblioteca Aspose.PSD cria essas formas usando a classe Graphics que reside no namespace Aspose.PSD. Objetos Graphics são responsáveis por realizar diferentes operações de desenho em uma imagem, alterando assim a superfície da imagem. A classe Graphics utiliza uma variedade de objetos auxiliares para aprimorar as formas:

- Pens, para desenhar linhas, contornar formas ou representar outras representações geométricas.
- Brushes, para definir como as áreas são preenchidas.
- Fonts, para definir a forma dos caracteres de texto.

### **Desenhando com a Classe Graphics**

Abaixo está um exemplo de código demonstrando o uso da classe Graphics. O código de exemplo foi dividido em várias partes para manter simples e fácil de seguir. Passo a passo, os exemplos mostram como:

1. Criar uma imagem.
1. Criar e inicializar um objeto Graphics.
1. Limpar a superfície.
1. Desenhar uma elipse.
1. Desenhar um polígono preenchido e salvar a imagem.

### **Amostras de Programação**

#### **Criando uma Imagem**

Comece criando uma imagem usando um dos métodos descritos em Criando Arquivos.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

#### **Criar e Inicializar um Objeto Graphics**

Em seguida, crie e inicialize um objeto Graphics passando o objeto Image para seu construtor.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

#### **Limpar a Superfície**

Limpe a superfície do Graphics chamando o método Clear da classe Graphics e passando uma cor como parâmetro. Este método preenche a superfície do Graphics com a cor passada como argumento.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

#### **Desenhar uma Elipse**

Você pode notar que a classe Graphics expõe muitos métodos para desenhar e preencher formas. Você encontrará a lista completa de métodos na Referência da API do Aspose.PSD para Java. Existem várias versões sobrecarregadas do método DrawEllipse expostas pela classe Graphics. Todos esses métodos aceitam um objeto Pen como seu primeiro argumento. Os parâmetros posteriores são passados para definir o retângulo delimitador ao redor da elipse. Para este exemplo, use a versão que aceita um objeto Rectangle como segundo parâmetro para desenhar uma elipse usando o objeto Pen na cor desejada.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

#### **Desenhar um Polígono Preenchido**

Em seguida, desenhe um polígono usando o LinearGradientBrush e uma matriz de pontos. A classe Graphics expõe várias versões do método FillPolygon. Todos eles aceitam um objeto Brush como seu primeiro argumento, definindo as características do preenchimento. O segundo parâmetro é uma matriz de pontos. Observe que cada dois pontos consecutivos na matriz especificam um lado do polígono.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

### **Desenho de Imagens usando Gráficos: Código Fonte Completo**

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

Todas as classes que implementam IDisposable e acessam recursos não gerenciados são instanciadas em um bloco Using para garantir que sejam corretamente liberadas.
