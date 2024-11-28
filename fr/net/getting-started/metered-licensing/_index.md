---
title: Licence mesurée
type: docs
weight: 80
url: /fr/net/licence-mesuree/
description: La bibliothèque C# Photoshop PSD permet aux développeurs d'appliquer une clé mesurée, qui est un nouveau mécanisme de licence et sera utilisée en combinaison avec la méthode de licence existante.
---

{{% alert color="primary" %}}

Aspose.PSD permet aux développeurs d'appliquer une clé mesurée. Il s'agit d'un nouveau mécanisme de licence. Ce nouveau mécanisme de licence sera utilisé en combinaison avec la méthode de licence existante. Les clients qui souhaitent être facturés en fonction de l'utilisation des fonctionnalités de l'API peuvent utiliser la licence mesurée. Pour plus de détails, veuillez consulter la section [FAQ sur la Licence Mesurée](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Licence Mesurée**
Voici les étapes simples pour utiliser la classe Mesurée.

1. Créez une instance de la classe Mesurée.
1. Passez les clés publiques et privées à la méthode setMeteredKey.
1. Effectuez le traitement (effectuez la tâche).
1. Appelez la méthode getConsumptionQuantity de la classe Mesurée.
1. Elle renverra la quantité de requêtes API que vous avez consommées jusqu'à présent.

Voici un exemple de code illustrant comment définir la clé publique et privée mesurée.

{{< highlight java >}}

// Créer une instance de la classe Mesurée PSD

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Accéder à la propriété setMeteredKey et passer les clés publiques et privées en tant que paramètres

metered.SetMeteredKey("*****", "*****");



// Obtenir la quantité de données mesurées avant d'appeler l'API

decimal quantiteAvant = Aspose.PSD.Metered.GetConsumptionQuantity();



// Afficher les informations

Console.WriteLine("Quantité consommée avant : " + quantiteAvant.ToString());

// Obtenir la quantité de données mesurées après avoir appelé l'API

decimal quantiteApres = Aspose.PSD.Metered.GetConsumptionQuantity();



// Afficher les informations

Console.WriteLine("Quantité consommée après : " + quantiteApres.ToString());

{{< /highlight >}}
