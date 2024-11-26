---
title: Adicionar uma Marca d'água a uma Imagem
type: docs
weight: 30
url: /pt/net/adicionar-uma-marca-dagua-a-uma-imagem/
---

## **Adicionar uma Marca d'água a uma Imagem**
Este documento explica como adicionar uma marca d'água a uma imagem usando Aspose.PSD. Adicionar uma marca d'água a uma imagem é um requisito comum para aplicações de processamento de imagem. Este exemplo utiliza a classe Graphics para desenhar uma string na superfície da imagem.
### **Adicionando uma Marca d'água**
Para demonstrar a operação, vamos carregar uma imagem BMP do disco e desenhar uma string como marca d'água na superfície da imagem usando o método DrawString da classe Graphics. Vamos salvar a imagem no formato PNG usando a classe PngOptions. Abaixo está um exemplo de código que demonstra como adicionar uma marca d'água a uma imagem. O código de exemplo foi dividido em partes para facilitar o acompanhamento. Passo a passo, os exemplos mostram como:

1. [Carregar](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) uma imagem.
1. Criar e inicializar um objeto [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Criar e inicializar objetos Font e [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Desenhar uma string como marca d'água usando o método [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) da classe Graphics.
1. Salvar imagem em PNG.

O trecho de código a seguir mostra como adicionar uma marca d'água na imagem.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Adicionando uma Marca d'água Diagonal**
Adicionar uma marca d'água diagonal a uma imagem é semelhante a adicionar uma marca d'água horizontal, conforme discutido acima, com algumas diferenças. Para demonstrar a operação, vamos carregar uma imagem JPG do disco, adicionar transformações usando um objeto da classe [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) e desenhar uma string como marca d'água na superfície da imagem usando o método DrawString da classe Graphics. Abaixo está um exemplo de código que demonstra como adicionar uma marca d'água diagonal a uma imagem. O código de exemplo foi dividido em partes para facilitar o acompanhamento. Passo a passo, os exemplos mostram como:

1. Carregar uma imagem.
1. Criar e inicializar um objeto Graphics.
1. Criar e inicializar objetos [Font](https://reference.aspose.com/psd/net/aspose.psd/font) e SolidBrush.
1. Obter o tamanho da imagem em um objeto [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Criar uma instância da classe Matrix e realizar uma transformação composta.
1. Atribuir a transformação ao objeto Graphics.
1. Criar e inicializar um objeto [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Desenhar uma string como marca d'água usando o método DrawString da classe Graphics.
1. Salvar a imagem resultante.

O trecho de código a seguir mostra como adicionar uma marca d'água diagonal.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
