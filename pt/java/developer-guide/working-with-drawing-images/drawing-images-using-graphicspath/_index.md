---
title: Desenho de Imagens usando GraphicsPath
type: docs
weight: 30
url: /pt/java/drawing-images-using-graphicspath/
---

## **Desenho de Imagens usando GraphicsPath**
A classe GraphicsPath é responsável por criar e manter um caminho de gráficos. O GraphicsPath não possui referência a uma imagem e não altera a própria imagem. Em vez disso, pode ser considerado como um objeto que contém metadados que descrevem os caminhos que podem ser desenhados pela classe Graphics. A classe GraphicsPath usa figuras; cada figura é composta por uma sequência de linhas e curvas conectadas ou uma forma primitiva geométrica. Cada forma pode ser dividida em segmentos de forma. É possível adicionar, remover e alterar diferentes figuras ou formas em um objeto GraphicsPath. Quando o GraphicsPath estiver totalmente descrito, utilize os métodos correspondentes da classe Graphics (DrawPath e Fill Paths) para desenhar sobre ou preencher os caminhos. A classe Graphics pega cada segmento de forma e o desenha para produzir a imagem final.
### **Desenho usando a Classe GraphicsPath**
A seguir está um exemplo que demonstra o uso da classe GraphicsPath. O código-fonte do exemplo foi dividido em várias partes para mantê-lo simples e fácil de seguir. Passo a passo, os exemplos mostram como:

- Criar uma imagem.
- Inicializar um objeto Graphics.
- Limpar a superfície.
- Criar uma instância de GraphicsPath.
- Criar uma figura.
- Adicionar formas à figura.
- Criar uma matriz de figuras.
- Desenhar caminhos.
- Preencher caminhos.


### **Desenho de Imagens usando GraphicsPath: Exemplos de Programação**
#### **GraphicsPath: Criar uma Imagem**
Comece criando uma imagem usando um dos métodos descritos em Criar Arquivos.
#### **GraphicsPath: Inicializar um Objeto Graphics**
Crie e inicialize um objeto Graphics passando o objeto Imagem para o seu construtor.
#### **GraphicsPath: Limpar a Superfície**
Limpe a superfície de Graphics chamando o método Clear da classe Graphics e passando uma Cor como parâmetro. Este método preenche a superfície de Graphics com a cor passada como argumento.
#### **GraphicsPath: Criar uma Instância de GraphicsPath**
Crie uma instância de GraphicsPath com GraphicsPath definido como Alternativo por padrão. Este modo determina como preencher o interior de uma figura fechada. O outro valor possível para GraphicsPath é Enrolamento.
#### **GraphicsPath: Criar uma Figura**
Crie uma instância da classe Figura. Como discutido anteriormente, Figura pode conter Formas e as formas residem no namespace Aspose.PSD.Shapes.
#### **GraphicsPath: Adicionar Formas à Figura**
O método Adicionar Formas exposto pela classe Figura permite adicionar formas à figura. Nos exemplos de código abaixo, várias formas são adicionadas a um objeto Figura.
#### **GraphicsPath: Adicionar Figuras a uma Matriz**
Múltiplas figuras podem ser adicionadas a um objeto GraphicsPath usando o método AddFigures exposto pela classe GraphicsPath. Este método aceita uma matriz de figuras como parâmetro.
#### **GraphicsPath: Desenhar os Caminhos**
Desenhe o GraphicsPath usando o método DrawPath exposto pela classe Graphics. O método aceita dois parâmetros. O primeiro parâmetro é um objeto da classe Pen, que determina a cor, largura e estilo do caminho. O segundo parâmetro é o objeto da classe GraphicsPath, representando o próprio caminho.
#### **GraphicsPath: Preencher os Caminhos**


É possível preencher um caminho passando um objeto GraphicsPath para o método Fill Paths exposto pela classe Graphics. O método Fill Paths preenche o caminho de acordo com o modo de preenchimento (alternado ou de enrolamento) atualmente definido para o caminho. Se o caminho contiver figuras abertas, o caminho será preenchido como se essas figuras estivessem fechadas.

O método Fill Paths aceita dois parâmetros. O primeiro parâmetro é um objeto de qualquer classe de pincel do namespace Aspose.PSD.Brushes. O segundo parâmetro é o próprio caminho. Para este exemplo, utilize o HatchBrush, que é um pincel retangular com um estilo hatch, uma cor de primeiro plano e uma cor de plano de fundo. Antes de passar o objeto HatchBrush para o método Fill Paths, defina suas propriedades.
### **GraphicsPath: Código-fonte Completo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



Todas as classes que implementam IDisposable são instanciadas em uma declaração Using para garantir que sejam descartadas corretamente.


