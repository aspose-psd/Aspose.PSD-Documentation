---
title: Criar Imagem PSD ou PSB do Zero usando Python
weight: 100
type: docs
description: Exemplo de como o Aspose.PSD for Python pode criar uma Imagem Psd do zero
keywords: [criar psd, criar psb, criar novo, criar camada, criar camada de texto, api psd, python, exemplo de código]
url: pt/python-net/criar-imagens-psd-psb-do-zero/
---

## **Visão Geral**
Para criar um arquivo PSD ou PSB do zero usando o Aspose.PSD for Python, você pode seguir os passos abaixo:

Importe os módulos e classes necessárias da biblioteca Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Especifique o nome e o caminho do arquivo de saída:

```python 
outputFile = "ExemploCriarArquivoDoZero.psd"
```

Crie uma imagem PSD com as dimensões desejadas:

```python 
with PsdImage(500, 500) as img:
```

Adicione uma camada PSD regular e atualize-a usando a API gráfica:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Crie uma camada de texto:
```python 
textLayer = img.add_text_layer("Texto de Exemplo", Rectangle(200, 200, 100, 100))
```

Adicione um efeito de sombra à camada de texto:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Salve o arquivo PSD:
```python 
img.save(outputFile)
```

Esse código cria uma imagem PSD com dimensões de 500x500 pixels. Ele adiciona uma camada regular e desenha uma elipse nela usando uma caneta e um pincel. Em seguida, adiciona uma camada de texto com o texto "Texto de Exemplo" e aplica um efeito de sombra a ela. Por fim, salva o arquivo PSD com o nome de saída especificado.

Observação: você precisará ter a biblioteca Aspose.PSD instalada e configurada corretamente em seu ambiente Python para que este código funcione. Você pode consultar a documentação oficial do Aspose.PSD para obter mais informações sobre como instalar e usar a biblioteca.

Confira o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentação-Python-Aspose-Psd-criar-psd-psb-imagens-do-zero.py" >}}
