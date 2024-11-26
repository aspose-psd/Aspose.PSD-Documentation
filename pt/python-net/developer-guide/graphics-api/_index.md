---
title: Utilizando a API de Gráficos para editar Camadas em arquivos PSD
weight: 100
type: docs
description: Exemplo de uso da API de Gráficos no Aspose.PSD para Python
keywords: [atualizar camada, desenhar círculo, desenhar elipse, desenhar círculo preenchido, gráficos, api psd, python, exemplo de código]
url: pt/python-net/graphics-api/
---

## **Visão Geral**
Primeiramente, você precisa carregar o arquivo PSD usando o método Image.load() ou criar uma imagem Psd do zero. No exemplo, a variável inputFile representa o caminho do seu arquivo PSD, e loadOpt representa as opções de carregamento (se houver).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Em seguida, você pode acessar a primeira camada da imagem PSD usando a sintaxe psdImage.layers[0]. Isso lhe dá uma referência ao objeto de camada que você pode manipular.

```python 
layer = psdImage.layers[0]
```
Para editar a camada, você precisa criar um objeto Graphics passando a camada como parâmetro. Esse objeto fornece vários métodos para desenhar formas e aplicar pincéis.

```python 
graphics = Graphics(layer)
```
No exemplo de código, um objeto Pen é criado para definir a cor e a espessura do contorno da forma de elipse. A constante Color.alice_blue representa a cor, e você pode ajustar a espessura conforme necessário.

```python 
pen = Pen(Color.alice_blue)
```
Da mesma forma, um objeto LinearGradientBrush é criado para definir a cor de preenchimento da forma de elipse. O Rectangle(250, 250, 150, 100) representa a posição e o tamanho da forma de elipse, e Color.red e Color.aquamarine representam as cores de início e fim do gradiente.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Para desenhar a forma de elipse na camada, você pode usar o método graphics.draw_ellipse(). O Rectangle(100, 100, 200, 200) representa a posição e o tamanho da forma de elipse.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Para preencher a forma de elipse com o pincel gradiente, você pode usar o método graphics.fill_ellipse(). O Rectangle(250, 250, 150, 100) representa a posição e o tamanho da forma de elipse.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Após fazer as alterações desejadas na camada, você pode salvar a imagem PSD modificada usando o método psdImage.save(). No exemplo, a variável psdName representa o caminho para salvar o arquivo PSD modificado.

```python 
psdImage.save(psdName)
```
Além disso, você também pode salvar a imagem modificada em outros formatos, como PNG, usando a classe PngOptions. A variável pngName representa o caminho para salvar o arquivo PNG.

```python 
psdImage.save(pngName, PngOptions())
```
É isso! Você utilizou com sucesso a API de Gráficos do Aspose.PSD para Python para editar camadas em um arquivo PSD. Sinta-se à vontade para explorar mais recursos e funcionalidades da biblioteca Aspose.PSD para aprimorar suas capacidades de edição de imagens.

Por favor, verifique o exemplo completo.

## **Exemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}
