---
title: Suporte de Camadas de Preenchimento
type: docs
weight: 50
url: /pt/java/suporte-de-camadas-de-preenchimento/
---

## **Suporte de Camadas de Preenchimento com Cor de Preenchimento**
Este artigo demonstra como preencher uma camada de PSD com Cor. Por favor, utilize a classe Aspose.PSD.FileFormats.Psd.Layers.FillLayer para adicionar Cor na camada de PSD. Os trechos de código a seguir carregam um arquivo PSD, acessam a classe FillLayer e definem a cor usando a propriedade FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Suporte de Camadas de Preenchimento com Preenchimento de Degradê**
Este artigo demonstra o uso de preenchimento de degradê para preencher uma camada de PSD. As APIs Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar esse objetivo. Aspose.PSD expôs as classes GradientColorPoint e GradientTransparencyPoint para adicionar o efeito de degradê em uma camada.

Os passos para preencher uma camada de PSD com preenchimento de degradê são simples como abaixo:

- Carregar um arquivo PSD como uma imagem usando o método de fábrica Load exposto pela classe Image.
- Definir propriedades de configurações do objeto FillLayer.
- Criar lista de ColorPoints com as cores requeridas e a posição da cor.
- Criar lista de transparencyPoints com a opacidade requerida e a posição do ponto de transparência.
- Chamar o método FillLayer.Update
- Salvar os resultados.

O trecho de código a seguir mostra como adicionar preenchimento de degradê para preencher uma camada de PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Efeito de Traçado com Preenchimento de Cor**
Este artigo demonstra como renderizar o efeito de traçado com preenchimento de cor. O efeito de traçado é usado para adicionar traços e bordas a camadas e formas. Ele pode ser usado para criar linhas de cor sólida, degradês coloridos, bem como bordas padronizadas.

Os passos para renderizar o efeito de traçado com preenchimento de cor são simples como abaixo:

- Definir a propriedade **LoadEffectsResource**.
- Carregar um arquivo PSD como uma imagem usando o método de fábrica Load exposto pela classe Image e definir **PsdLoadOptions**.
- Definir propriedades de configurações de **ColorFillSetting.**
- Salvar os resultados.

O trecho de código a seguir mostra como renderizar o efeito de traçado com preenchimento de cor.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}


