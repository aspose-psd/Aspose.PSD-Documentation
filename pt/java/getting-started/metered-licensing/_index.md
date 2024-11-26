---
title: Licenciamento Medido
type: docs
weight: 70
url: /pt/java/licenciamento-medido/
---

{{% alert color="primary" %}}

O Aspose.PSD permite aos desenvolvedores aplicar uma chave medida. Esta é um novo mecanismo de licenciamento. O novo mecanismo de licenciamento será utilizado juntamente com o método de licenciamento existente. Os clientes que desejam ser cobrados com base no uso dos recursos da API podem usar o licenciamento medido. Para mais detalhes, consulte a seção [FAQ sobre Licenciamento Medido](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Licenciamento Medido**
Aqui estão os passos simples para usar a classe Medido.

1. Crie uma instância da classe Medido.
1. Passe as chaves pública e particular para o método setMeteredKey.
1. Faça o processamento (realize a tarefa).
1. Chame o método getConsumptionQuantity da classe Medido.
1. Ele retornará a quantidade de solicitações de API que você consumiu até agora.

Aqui está o código de exemplo que demonstra como definir a chave pública e privada medida.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}

