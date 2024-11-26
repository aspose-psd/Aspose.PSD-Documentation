---
title: Desenho de Imagens usando Gráficos
type: docs
weight: 20
url: /pt/net/drawing-images-using-graphics/
---

## **Desenho de Imagens usando Gráficos**
Com a biblioteca Aspose.PSD, você pode desenhar formas simples como linhas, retângulos e círculos, bem como formas complexas como polígonos, curvas, arcos e formas Bezier. A biblioteca Aspose.PSD cria essas formas usando a classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) que está no namespace Aspose.PSD. Objetos Graphics são responsáveis por realizar diferentes operações de desenho em uma imagem, alterando assim a superfície da imagem. A classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) usa uma variedade de objetos auxiliares para melhorar as formas:

·         Pens, para desenhar linhas, contornos de formas ou renderizar outras representações geométricas.

·         Brushes, para definir como áreas são preenchidas.

·         Fonts, para definir a forma dos caracteres de texto.
### **Desenhar com a Classe Graphics**
Abaixo está um exemplo de código demonstrando o uso da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). O código de exemplo foi dividido em várias partes para mantê-lo simples e fácil de seguir. Passo a passo, os exemplos mostram como:

1. Criar uma imagem.
1. Criar e inicializar um objeto Graphics.
1. Limpar a superfície.
1. Desenhar uma elipse.
1. Desenhar um polígono preenchido e salvar a imagem.
### **Exemplos de Programação**
#### **Criando uma Imagem**
Comece criando uma imagem usando qualquer um dos métodos descritos em Criando Arquivos.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Criar e Inicializar um Objeto Graphics**
Em seguida, crie e inicialize um objeto Graphics passando o objeto Image para o seu construtor.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Limpar a Superfície**
Limpe a superfície da Graphics chamando o método Clear da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) e passe a cor como parâmetro. Este método preenche a superfície da Graphics com a cor passada como argumento.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Desenhar uma Elipse**
Você pode observar que a classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) expôs muitos métodos para desenhar e preencher formas. Você encontrará a lista completa de métodos na Referência da API Aspose.PSD para .NET. Há várias versões sobrecarregadas do método DrawEllipse expostas pela classe Graphics. Todos esses métodos aceitam um objeto Pen como seu primeiro argumento. Os parâmetros posteriores são passados para definir o retângulo delimitador em torno da elipse. Para este exemplo, use a versão que aceita um objeto Rectangle como segundo parâmetro para desenhar uma elipse usando o objeto Pen na cor desejada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Desenhar um Polígono Preenchido**
Em seguida, desenhe um polígono usando o LinearGradientBrush e um array de pontos. A classe Graphics expôs várias versões sobrecarregadas do método FillPolygon(). Todas elas aceitam um objeto Brush como seu primeiro argumento, definindo as características do preenchimento. O segundo parâmetro é um array de pontos. Por favor, note que a cada dois pontos consecutivos no array especificam um lado do polígono.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Desenho de Imagens usando Gráficos: Fonte Completa**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Todas as classes que implementam IDisposable e acessam recursos não gerenciados são instanciadas em uma instrução Using para garantir que sejam descartadas corretamente.

