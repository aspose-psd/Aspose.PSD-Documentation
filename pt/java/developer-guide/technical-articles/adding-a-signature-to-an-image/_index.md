---
title: Adicionando uma Assinatura a uma Imagem
type: docs
weight: 10
url: /pt/java/adicionando-uma-assinatura-a-uma-imagem/
---

## **Adicionando uma Assinatura**


Adicionar uma assinatura a uma imagem é às vezes necessário para assinar digitalmente as imagens e evitar a falsificação. Outra ideia poderia ser tratar a imagem como se estivesse sendo exibida em uma galeria. Seja qual for o motivo, as APIs Aspose.PSD fornecem o recurso de adicionar uma assinatura a uma imagem usando o mecanismo mais simples, conforme explicado abaixo. Por favor, observe que este exemplo utiliza a classe Graphics para desenhar outra imagem com uma assinatura na superfície da imagem original. Para demonstrar a operação, carregaremos uma imagem PSD do disco e desenharemos outra imagem como assinatura na superfície da imagem original usando o método DrawImage da classe Graphics. Salvaremos a imagem resultante no formato PNG usando a classe PngOptions. Abaixo está um exemplo de código que demonstra como adicionar uma assinatura a uma imagem. O código do exemplo foi dividido em partes para facilitar o acompanhamento. Passo a passo, o exemplo mostra como:

- Carregar as imagens primária e secundária (assinatura).
- Criar e inicializar um objeto Graphics.
- Desenhar imagem usando o método DrawImage da classe Graphics.
- Salvar o resultado em formato PNG.
### **Exemplos de Programa**
#### **Carregando Imagens**
Primeiramente, crie instâncias da classe Image para carregar as imagens de amostra do disco.
#### **Criando e Inicializando um Objeto Gráfico**
Após carregar as imagens, crie e inicialize um objeto da classe Graphics enquanto utiliza o objeto da imagem primária.
#### **Desenhando a Imagem Secundária na Imagem Primária**
Então, utilizando o método DrawImage da classe Graphics, adicione a imagem secundária à imagem primária. Existem várias sobrecargas do método DrawImage que aceitam um objeto da Image como primeiro parâmetro, enquanto todos os outros parâmetros correspondem à localização onde a imagem deve ser desenhada. Para fins de demonstração, o código a seguir utiliza a versão da sobrecarga do DrawImage que aceita um objeto da Point como segundo parâmetro e tenta desenhar a assinatura no canto inferior direito da imagem primária.
#### **Salvando a Imagem**
Por fim, salve a imagem de volta no disco local como um arquivo PNG usando a classe PngOptions.
#### **Código Completo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemplos-src-main-java-com-aspose-psd-exemplos-DrawingImages-AdicionarAssinaturaEmImagem-AdicionarAssinaturaEmImagem.java" >}}
