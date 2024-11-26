---
title: Desenhar Imagens usando GraphicsPath
type: docs
weight: 30
url: /pt/net/desenhar-imagens-usando-graphicspath/
---

## **Desenhar Imagens usando GraphicsPath**
A classe [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) é responsável por criar e manter um caminho gráfico. O GraphicsPath não possui referência a uma imagem e não modifica a imagem em si; em vez disso, ele pode ser considerado como um objeto que contém metadados que descrevem os caminhos que a classe Graphics pode desenhar. A classe GraphicsPath usa figuras; cada figura é composta por uma sequência de linhas e curvas conectadas ou por uma forma primitiva geométrica. Cada forma pode ser dividida em segmentos de forma. Você pode adicionar, remover e alterar diferentes figuras ou formas em um objeto GraphicsPath. Quando o GraphicsPath estiver totalmente descrito, use os métodos correspondentes da classe Graphics (DrawPath e Fill Paths) para desenhar sobre ou preencher os caminhos. A classe Graphics pega cada segmento da forma e o desenha para produzir a imagem final.
### **Desenho usando a Classe GraphicsPath**
Abaixo está um exemplo demonstrando o uso da classe [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath). O código-fonte do exemplo foi dividido em várias partes para mantê-lo simples e fácil de seguir. Passo a passo, os exemplos mostram como:

- Criar uma imagem.
- Inicializar um objeto Graphics.
- Limpar a superfície.
- Criar uma instância de [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Criar uma figura.
- Adicionar formas à figura.
- Criar um array de figuras.
- Desenhar caminhos.
- Preencher caminhos.


### **Desenhar Imagens usando GraphicsPath: Exemplos de Programação**
#### **GraphicsPath: Criar uma Imagem**
Comece criando uma imagem usando um dos métodos descritos em Criando Arquivos.
#### **GraphicsPath: Inicializar um Objeto Graphics**
Crie e inicialize um objeto Graphics passando a imagem para seu construtor.
#### **GraphicsPath: Limpar a Superfície**
Limpe a superfície do Graphics chamando o método Clear da classe Graphics e passando uma Cor como parâmetro. Este método preenche a superfície do Graphics com a cor passada como argumento.
#### **GraphicsPath: Criar uma Instância da GraphicsPath**
Crie uma instância do GraphicsPath com GraphicsPath definido como Alternado por padrão. Este modo determina como preencher o interior de uma figura fechada. O outro valor possível de GraphicsPath é Winding.
#### **GraphicsPath: Criar uma Figura**
Crie uma instância da classe Figure. Como discutido anteriormente, Figure pode conter Shapes e shapes residem no namespace Aspose.PSD.Shapes.
#### **GraphicsPath: Adicionar Formas à Figura**
O método Add Shapes exposto pela classe Figure permite adicionar formas à figura. Nos exemplos de código abaixo, várias formas são adicionadas a um objeto Figure.
#### **GraphicsPath: Adicionar Figuras a um Array**
Múltiplas figuras podem ser adicionadas a um objeto GraphicsPath usando o método AddFigures exposto pela classe GraphicsPath. Este método aceita um array de figuras como parâmetro.
#### **GraphicsPath: Desenhar os Caminhos**
Desenhe o GraphicsPath usando o método DrawPath exposto pela classe Graphics. O método aceita dois parâmetros. O primeiro parâmetro é um objeto da classe Pen, que determina a cor, largura e estilo do caminho. O segundo parâmetro é o objeto da classe GraphicsPath, representando o próprio caminho.
#### **GraphicsPath: Preencher os Caminhos**


Você pode preencher um caminho passando um objeto GraphicsPath para o método Fill Paths exposto pela classe Graphics. O método Fill Paths preenche o caminho de acordo com o modo de preenchimento (alternado ou em curvas) atualmente definido para o caminho. Se o caminho tiver figuras abertas, o caminho é preenchido como se aquelas figuras estivessem fechadas.

O método Fill Paths aceita dois parâmetros. O primeiro parâmetro é um objeto de qualquer classe de brush do namespace Aspose.PSD.Brushes. O segundo parâmetro é o caminho em si. Para este exemplo, use o HatchBrush que é um brush retangular com um estilo de hachura, uma cor de primeiro plano e uma cor de fundo. Antes de passar o objeto HatchBrush para o método Fill Paths, defina suas propriedades.
### **GraphicsPath: Código Fonte Completo**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Todas as classes que implementam IDisposable são instanciadas em uma instrução Using para garantir que sejam descartadas corretamente.
