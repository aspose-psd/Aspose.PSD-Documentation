---
title: Licenciamento Medido
type: docs
weight: 80
url: /pt/net/licenciamento-medido/
description: A PSD Photoshop C# Library permite que os desenvolvedores apliquem uma chave medido que é um novo mecanismo de licenciamento e será usado juntamente com o método de licenciamento existente.
---

{{% alert color="primary" %}} 

O Aspose.PSD permite que os desenvolvedores apliquem uma chave medido. É um novo mecanismo de licenciamento. O novo mecanismo de licenciamento será usado juntamente com o método de licenciamento existente. Os clientes que desejam ser cobrados com base no uso das funcionalidades da API podem usar o licenciamento medido. Para mais detalhes, consulte a seção de [Perguntas Frequentes sobre Licenciamento Medido](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 
## **Licenciamento Medido**
Aqui estão os passos simples para usar a classe Metered.

1. Crie uma instância da classe Metered.
1. Passe as chaves pública e privada para o método setMeteredKey.
1. Realize o processamento (execute a tarefa).
1. Chame o método getConsumptionQuantity da classe Metered.
1. Ele retornará a quantidade de solicitações da API que você consumiu até o momento.

A seguir está o código de exemplo demonstrando como configurar a chave pública e privada medida.

{{< highlight java >}}

 // Crie uma instância da classe Metered do PSD

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Acesse a propriedade setMeteredKey e passe as chaves pública e privada como parâmetros

metered.SetMeteredKey("*****", "*****");



// Obtenha a quantidade de dados medidos antes de chamar a API

decimal quantidadeAntes = Aspose.PSD.Metered.GetConsumptionQuantity();



// Exiba informações

Console.WriteLine("Quantidade Consumida Antes: " + quantidadeAntes.ToString());

// Obtenha a quantidade de dados medidos depois de chamar a API

decimal quantidadeDepois = Aspose.PSD.Metered.GetConsumptionQuantity();



// Exiba informações

Console.WriteLine("Quantidade Consumida Depois: " + quantidadeDepois.ToString());

{{< /highlight >}}
