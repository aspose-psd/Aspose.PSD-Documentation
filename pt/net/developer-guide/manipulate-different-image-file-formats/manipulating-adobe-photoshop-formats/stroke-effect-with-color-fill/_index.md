---
title: Efeito de Traço com Preenchimento de Cor
type: docs
weight: 60
url: /pt/net/stroke-effect-with-color-fill/
---

## **Efeito de Traço com Preenchimento de Cor**
Este artigo demonstra como renderizar o efeito de traço com preenchimento de cor. O efeito de traço é utilizado para adicionar traços e bordas a camadas e formas. Pode ser usado para criar linhas de cor sólida, gradientes coloridos, bem como bordas padronizadas.

Os passos para renderizar o efeito de traço com preenchimento de cor são simples como abaixo:

- Definir a propriedade [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource).
- Carregar um arquivo PSD como uma imagem usando o método de fábrica `Load` exposto pela classe Image e definir as [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions).
- Definir as propriedades de configuração de [**ColorFillSettings**.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)
- Salvar os resultados.

O trecho de código a seguir mostra como renderizar o efeito de traço com preenchimento de cor.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
