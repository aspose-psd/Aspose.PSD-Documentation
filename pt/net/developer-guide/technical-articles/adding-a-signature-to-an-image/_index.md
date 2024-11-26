---
title: Adicionando uma Assinatura a uma Imagem
type: docs
weight: 70
url: /pt/net/adicionando-uma-assinatura-a-uma-imagem/
---

## **Adicionando uma Assinatura**


Adicionar uma assinatura a uma imagem é às vezes necessário para assinar digitalmente as imagens e evitar falsificações. Outra ideia poderia ser tratar a imagem mais como se ela estivesse sendo exibida em uma galeria. Qualquer que seja o motivo, as APIs Aspose.PSD fornecem a funcionalidade de adicionar uma assinatura a uma imagem usando o mecanismo mais simples conforme explicado abaixo. Por favor, observe que este exemplo faz uso da classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para desenhar outra imagem com a assinatura na superfície da imagem original. Para demonstrar a operação, iremos carregar uma imagem PSD do disco e desenhar outra imagem como assinatura na superfície da imagem original usando o método [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) da classe Graphics. Iremos salvar a imagem resultante em formato PNG usando a classe [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions). Abaixo está um exemplo de código que demonstra como adicionar uma assinatura a uma imagem. O código de exemplo foi dividido em partes para facilitar o acompanhamento. Passo a passo, o exemplo mostra como:

- Carregar as imagens primária e secundária (assinatura).
- Criar e inicializar um objeto Graphics.
- Desenhar a imagem usando o método DrawImage da classe Graphics.
- Salvar o resultado em formato PNG.
### **Exemplos do Programa**
#### **Carregando Imagens**
Primeiramente, crie instâncias da classe Image para carregar as imagens de amostra do disco.
#### **Criando e Inicializando um Objeto Gráfico**
Após carregar as imagens, crie e inicialize um objeto da classe Graphics usando o objeto da imagem primária.
#### **Desenhando a Imagem Secundária na Imagem Primária**
Em seguida, usando o método DrawImage da classe Graphics, adicione a imagem secundária na imagem primária. Existem várias sobrecargas do método DrawImage que aceitam um objeto da classe Image como primeiro parâmetro, enquanto todos os outros parâmetros correspondem ao local onde a imagem deve ser desenhada. Para efeitos de demonstração, o seguinte código utiliza a versão de sobrecarga de DrawImage que aceita um objeto da classe Point como segundo parâmetro e tenta desenhar a assinatura no canto inferior direito da imagem primária.
#### **Salvando a Imagem**
Por fim, salve a imagem de volta no disco local como um arquivo PNG usando a classe PngOptions.
#### **Código Fonte Completo**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-DrawingImages-AdicionarAssinaturaEmImagem-AdicionarAssinaturaEmImagem.cs" >}}
