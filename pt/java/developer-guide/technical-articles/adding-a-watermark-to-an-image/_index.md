---
title: Adicionar uma marca d'água a uma imagem
type: docs
weight: 20
url: /pt/adicionar-uma-marca-dagua-a-uma-imagem/
---

## **Adicionar uma marca d'água a uma imagem**
Este documento explica como adicionar uma marca d'água a uma imagem usando o Aspose.PSD. Adicionar uma marca d'água a uma imagem é um requisito comum para aplicações de processamento de imagem. Este exemplo usa a classe Graphics para desenhar uma string na superfície da imagem.
### **Adicionar uma marca d'água**
Para demonstrar a operação, iremos carregar uma imagem BMP do disco e desenhar uma string como marca d'água na superfície da imagem usando o método DrawString da classe Graphics. Vamos salvar a imagem no formato PNG usando a classe PngOptions. Abaixo está um exemplo de código que demonstra como adicionar uma marca d'água a uma imagem. O código de exemplo foi dividido em partes para facilitar o acompanhamento. Passo a passo, os exemplos mostram como:

1. Carregar uma imagem.
1. Criar e inicializar um objeto Graphics.
1. Criar e inicializar objetos Font e SolidBrush.
1. Desenhar uma string como marca d'água usando o método DrawString da classe Graphics.
1. Salvar a imagem como PNG.

O trecho de código a seguir mostra como adicionar uma marca d'água na imagem.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Adicionar uma marca d'água diagonal**
Adicionar uma marca d'água diagonal a uma imagem é semelhante à adição de uma marca d'água horizontal como discutido acima, com algumas diferenças. Para demonstrar a operação, iremos carregar uma imagem JPG do disco, adicionar transformações usando um objeto da classe Matrix e desenhar uma string como marca d'água na superfície da imagem usando o método DrawString da classe Graphics. Abaixo está um exemplo de código que demonstra como adicionar uma marca d'água diagonal a uma imagem. O código de exemplo foi dividido em partes para facilitar o acompanhamento. Passo a passo, os exemplos mostram como:

1. Carregar uma imagem.
1. Criar e inicializar um objeto Graphics.
1. Criar e inicializar objetos Font e SolidBrush.
1. Obter o tamanho da imagem em um objeto SizeF.
1. Criar uma instância da classe Matrix e realizar uma transformação composta.
1. Atribuir a transformação ao objeto Graphics.
1. Criar e inicializar um objeto StringFormat.
1. Desenhar uma string como marca d'água usando o método DrawString da classe Graphics.
1. Salvar a imagem resultante.

O trecho de código a seguir mostra como adicionar uma marca d'água diagonal.





{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
