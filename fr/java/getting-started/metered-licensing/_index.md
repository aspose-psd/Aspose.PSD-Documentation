---
title: Licence à la consommation
type: docs
weight: 70
url: /fr/java/licence-a-la-consommation/
---

{{% alert color="primary" %}}

Aspose.PSD permet aux développeurs d'appliquer une clé de licence à la consommation. Il s'agit d'un nouveau mécanisme de licence. Ce nouveau mécanisme de licence sera utilisé avec la méthode de licence existante. Les clients qui souhaitent être facturés en fonction de l'utilisation des fonctionnalités de l'API peuvent utiliser la licence à la consommation. Pour plus de détails, veuillez vous référer à la section des [FAQ sur la licence à la consommation](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Licence à la consommation**
Voici les étapes simples pour utiliser la classe Metered.

1. Créez une instance de la classe Metered.
1. Passez les clés publique et privée à la méthode setMeteredKey.
1. Effectuez un traitement (effectuez une tâche).
1. Appelez la méthode getConsumptionQuantity de la classe Metered.
1. Cela renverra la quantité d'appels d'API que vous avez consommée jusqu'à présent.

Voici un exemple de code montrant comment définir une clé publique et privée pour la consommation.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}

