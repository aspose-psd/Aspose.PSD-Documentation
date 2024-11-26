---
title: Como criar um gerador de miniaturas do YouTube programaticamente em Java
type: docs
weight: 10
url: /pt/java/como-criar-um-gerador-de-miniaturas-youtube-programaticamente-em-java/
---

## **Introdução**
O objetivo deste documento é demonstrar o uso da API de algumas ferramentas compostas do [Aspose.PSD para Java](https://products.aspose.com/psd/java) em um exemplo do mundo real. Neste artigo, **um programa Java simples que gera miniaturas do YouTube** para o canal [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q) será escrito e explicado. Este canal foi escolhido do mundo real porque suas miniaturas são bastante padrão e ilustram o uso de algumas ferramentas compostas populares do Aspose.PSD para Java (por exemplo, efeito de [sombra (shadow effect)](/psd/pt/java/manipulando-formatos-photoshop/#manipulando-formatos-photoshop-suporte-efeito-sombra), preenchimento radial de gradiente, desenho de texto e formas):

![todo:image_alt_text](como-criar-um-gerador-de-miniaturas-youtube-programaticamente-em-java_1.png)

## **Como funciona em poucas palavras**
Um programa Java simples recebe como entrada dois argumentos: uma legenda e uma imagem. Um **documento Photoshop (PSD) em memória é gerado** a partir dessa entrada usando o Aspose.PSD para Java. Em seguida, o programa **converte o documento de PSD para o formato de arquivo PNG** para obter uma miniatura do YouTube com o tamanho de 1280x720 pixels. A imagem de saída se parece com a seguinte:

![todo:image_alt_text](como-criar-um-gerador-de-miniaturas-youtube-programaticamente-em-java_2.png)

## **Requisitos técnicos**
As seguintes tecnologias são necessárias para ter sucesso na execução do código deste artigo:

- Java 6+
- [Aspose.PSD para Java](/psd/pt/java/installation/) (mais recente)

## **Iniciando**
Como já mencionado, o programa usa PSD em memória para gerar uma miniatura. Portanto, vamos **criar um documento PSD**, para começar:

PsdImage psdImage = new PsdImage(1280, 720);

Se observar mais de perto a miniatura do YouTube acima, pode-se notar que **ela é composta por vários componentes**:

1. uma imagem de fundo (máscara impressa)
1. um gradiente radial de PSD (destaca a área no canto superior direito)
1. um logotipo com efeito de sombra
1. uma legenda e um desenho simples (retângulo azul)

Vamos explorar detalhadamente como implementar cada um desses componentes usando o Aspose.PSD para Java nas próximas seções.

## **1. Adicionar uma imagem de fundo**
A ordem das camadas é importante. Portanto, uma imagem de fundo deve ser adicionada primeiro para não sobrepôr outras camadas. Preste atenção que apenas [formatos de arquivo raster são suportados](/psd/pt/java/formatos-de-arquivo-suportados/) no momento.
### **1.1. Adicionar uma imagem de fundo a uma camada do Photoshop**
Para **adicionar uma imagem raster ao PSD**, é necessário passar um fluxo de entrada como argumento durante a construção da camada (veja mais [exemplos de carregamento de imagens raster](https://docs.aspose.com/display/psdnet/Criar%2C+Abrir+e+Salvar+Images)):

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```

1.2. Ajuste a imagem de fundo para o canvas

As seguintes 2 ações (redimensionamento, posicionamento) são úteis para os casos em que **o tamanho da imagem difere do tamanho do canvas**, embora a imagem neste artigo tenha o mesmo tamanho que o canvas (assuma que nem sempre será assim).

Certifique-se de que a imagem carregada **se ajusta ao tamanho do canvas** (veja mais [exemplos de redimensionamento](https://docs.aspose.com/display/psdnet/Cortar%2C+Rotacionar+e+Redimensionar+Images#Cortar,RotacionarRedimensionarImages-RedimensionarImages)):

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

Após o redimensionamento, a posição da imagem é alterada. Portanto, para **redefinir a posição da imagem**, mova a imagem redimensionada para o canto superior esquerdo:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
```

## **2. Adicionar um gradiente radial**
Há **duas maneiras de adicionar um gradiente radial**, usando:

- um [efeito de sobreposição de gradiente](/psd/pt/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) em uma camada existente (um efeito de gradiente que se liga à camada atual e se aplica ao seu conteúdo)
- uma nova [camada de preenchimento de gradiente](/psd/pt/java/suporte-de-camadas-de-preenchimento/#suportedecamadasdepreenchimento-suportedecamadasdepreenchimentocompreenchedorgradiente) (uma camada separada que mantém uma configuração independente do gradiente)

É suficiente usar o efeito de sobreposição de gradiente para este exemplo. No entanto, para tornar este artigo mais interessante e útil, **a camada de preenchimento de gradiente é usada**, uma vez que todos os efeitos de camada se aplicam de maneira semelhante e outro efeito de camada será usado na próxima seção.
### **2.1. Adicionar uma camada de preenchimento de gradiente radial**
O processo de adicionar uma nova camada de preenchimento de gradiente consiste nos seguintes 2 passos:

\1. É necessário **declarar as configurações de preenchimento de gradiente**, uma vez que não existem predefinições. A configuração mínima necessária se parece com a seguinte (significa que o tipo de gradiente, escala, cor e pontos de transparência são propriedades obrigatórias):

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

A configuração acima declara um gradiente radial que é transparente nas bordas e azul escuro no centro. A posição do gradiente é no meio do canvas por padrão.

Para inverter o preenchimento de gradiente e deslocá-lo ligeiramente para o canto superior direito, use propriedades opcionais correspondentes:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```

\2. Quando a configuração estiver pronta, adicione uma camada de preenchimento de gradiente juntamente com suas configurações no PSD:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
```

## **Adicionar um logotipo com sombra**
A **sombra (drop shadow)** é um efeito que permite adicionar uma sombra personalizada ao longo do contorno do objeto (imagem, texto etc.).
### **3.1. Adicionar um logotipo a uma camada do Photoshop**
A mesma abordagem da seção 1.1. pode ser usada para **adicionar um logotipo ao PSD**:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
```

### **3.2. Posicionar o logotipo**
A imagem carregada está aderida de perto ao canto superior esquerdo por padrão. No entanto, algumas **margens precisam ser adicionadas** para se parecer com a miniatura original do YouTube no canal. Portanto, a posição da imagem deve ser afastada das bordas da camada:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
```

### **3.3. Adicionar um efeito de sombra (drop shadow) ao logotipo**
O logotipo pode ficar invisível se uma imagem de fundo clara for usada. Portanto, é desejável **adicionar um efeito de sombra (drop shadow)** a um logotipo através da propriedade de opções de mistura (veja mais [exemplos de sombreamento](/psd/pt/java/manipulando-formatos-photoshop/#manipulando-formatos-photoshop-suportar-efeito-sombra)):

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}
```

O efeito de sombra não possui as propriedades necessárias devido à configuração padrão (parece como a do Photoshop). No entanto, a sombra acima é modificada para se parecer com uma borda translúcida borrada nas bordas.

## **4. Adicionar um desenho de texto e uma forma**
### **3.1. Criar uma camada de gráficos**
O desenho não é suportado diretamente por uma camada regular. Portanto, o mecanismo gráfico é utilizado ao lado da camada para **fornecer uma API para desenho** (veja mais [exemplos de desenho](/psd/pt/java/desenhando-imagens-usando-gráficos/)):

```
Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
```

### **3.2. Desenhar texto multi-linha**
Um leitor experiente pode perguntar: por que não usar uma camada de texto para adicionar um texto? Bem, existem algumas razões: a edição de texto não é necessária neste caso porque o PSD é gerado do zero a cada vez; a personalização da fonte não é suportada pela [API de texto](https://docs.aspose.com/display/psdnet/Trabalhando+Com+Camadas+De+Texto) ainda (v20.6 no momento da escrita).

É fácil **desenhar algum texto com uma fonte personalizada**, basta instanciar uma fonte desejada e invocar o método correspondente do mecanismo gráfico. No entanto, para fazer um retângulo (veja detalhes na próxima seção) que mude sua altura automaticamente com base no número de linhas de texto é um pouco mais difícil. A altura exata de todas as linhas deve ser calculada primeiro:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}
```

Onde 1.15 é a altura da linha, 3 é o preenchimento do texto.

### **3.3. Desenhar um retângulo**
Um retângulo também é fácil de desenhar até mesmo com um pincel de gradiente (basta definir uma área para desenhar e uma faixa de cores). Quando a altura do texto é conhecida, o tamanho e a posição do retângulo são calculados. Para **desenhar um retângulo preenchido** **no psd** (não apenas um quadro), chame o método correspondente do mecanismo gráfico com tudo isso:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}
```

` `Onde 40, 15, 25 são recuos.

## **Resultado**
Assim, a modelagem da miniatura está concluída. Portanto, é hora de **exportar a miniatura para um formato de arquivo raster** (por exemplo, PNG) para distribuição posterior:

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}
```

## **Conclusão**
Neste artigo, criamos um gerador de miniaturas do YouTube para o canal DW Documentary e explicamos como usar algumas das ferramentas compostas mais populares, como efeito de sombra, preenchimento de gradiente radial, desenho de texto e formas.

## **Exemplo Completo**
Você pode [baixar o SDK do Aspose.PSD](https://products.aspose.com/psd/net)

```
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentação-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
```