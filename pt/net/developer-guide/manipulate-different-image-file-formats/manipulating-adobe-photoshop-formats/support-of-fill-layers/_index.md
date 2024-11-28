---
title: Suporte de Camadas de Preenchimento
type: docs
weight: 90
url: /pt/net/suporte-de-camadas-de-preenchimento/
---


## **Camadas de Preenchimento Com Preenchimento de Padrão**
Este artigo demonstra como preencher a camada [PSD](https://wiki.fileformat.com/image/psd/) com preenchimento de padrão. Um padrão é uma imagem, cor, sombra ou linha que é usada para preencher uma área de uma imagem. Por favor, use a classe Aspose.PSD.FileFormats.Psd.Layers.FillLayer para adicionar um padrão na camada PSD. Os trechos de código seguintes carregam um arquivo PSD, acessam a classe [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) e definem o padrão usando as propriedades [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-CamadaPreenchimentoPadrao-CamadaPreenchimentoPadrao.cs" >}}



Aqui está outro exemplo que demonstra como o [Aspose.PSD](https://products.aspose.com/psd/net) renderiza o padrão utilizando as classes [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) e [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-ImplementarCamadaPreenchimentoPadrao-ImplementarCamadaPreenchimentoPadrao.cs" >}}
## **Camadas de Preenchimento Com Preenchimento de Gradiente**
Este artigo demonstra o uso do preenchimento de gradiente para preencher a camada PSD. As APIs Aspose.PSD expuseram métodos eficientes e fáceis de usar para alcançar este objetivo. O Aspose.PSD expôs as classes [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) e [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) para adicionar um efeito de gradiente em uma camada.

`Os passos para preencher [a camada PSD](https://wiki.fileformat.com/image/psd/) com um preenchimento de gradiente são simples como abaixo:

- Carregar um arquivo PSD como uma imagem usando o método de fábrica [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) exposto pela classe [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Configurar as propriedades de configuração do objeto [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Criar uma lista de [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) com cores necessárias e posições da cor.
- Criar uma lista de pontos de transparência com opacidade necessária e posição do ponto de transparência.
- Chamar o método [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Salvar os resultados.



O trecho de código seguinte mostra como adicionar preenchimento de gradiente em uma camada PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-CamadaPreenchimentoGradiente-CamadaPreenchimentoGradiente.cs" >}}



**Aqui está outro exemplo que utiliza a propriedade [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** para preencher a camada PSD com preenchimento de gradiente. O Aspose.PSD suporta os seguintes tipos de gradiente através da enumeração GradientType:

- **GradientType.Linear:**       Em um gradiente linear, a transição de cor vai do tom inicial ao final em linha reta.
- **GradientType.Radial:**       Em um gradiente radial, as cores se propagam a partir do ponto inicial em um padrão circular.
- **GradientType.Angle:**        Um gradiente angular varre no sentido anti-horário ao redor do ponto inicial.
- **GradientType.Reflected:** Em um gradiente refletido, a cor é espelhada em ambos os lados do ponto inicial.
- **GradientType.Diamond:**   O gradiente em forma de diamante cria uma forma de diamante a partir do ponto inicial.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-CamadasPreenchimentoGradiente-CamadasPreenchimentoGradiente.cs" >}}
## **Suporte da Propriedade de Escala para Camadas de Preenchimento de Gradiente**
Este artigo demonstra como escalar a Camada de Preenchimento com preenchimento de gradiente usando o Aspose.PSD para .NET. Para este propósito, uma nova propriedade [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) foi adicionada em [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings)**.** 

A seguir está a demonstração de código que mostra como usar a propriedade **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-SuportePropriedadeEscala-SuportePropriedadeEscala.cs" >}}
## **Camadas de Preenchimento Com Preenchimento de Cor**
Este artigo demonstra como preencher a camada [PSD](https://wiki.fileformat.com/image/psd/) com cor. Por favor, use a classe [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) para adicionar cor na camada PSD. O trecho de código seguinte carrega um arquivo PSD, acessa a classe de camada de preenchimento e define a cor usando a propriedade [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemplos-CSharp-Aspose-ModificandoEConvertendoImagens-PSD-CamadaPreenchimentoCor-CamadaPreenchimentoCor.cs" >}}



