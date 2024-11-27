---
title: Exemple de l'utilisation des calques de groupe dans Aspose.PSD pour Java
weight: 100
type: docs
description: Utilisation du calque de groupe du fichier PSD via Java
keywords: [groupe de calques, calque de groupe, ajouter un calque au groupe, api psd, java, exemple de code]
url: fr/java/psd-group-layer/
---

## **Vue d'ensemble**

L'utilisation des calques de groupe dans Aspose.PSD pour Java améliore votre capacité à gérer et organiser les calques au sein d'une image PSD de manière efficace. Les calques de groupe, également appelés calques de dossier, vous permettent de regrouper plusieurs calques et d'appliquer des transformations ou des effets de manière collective.

Pour commencer, créez une nouvelle image PSD en utilisant la méthode PsdImage.create(). Ensuite, initialisez un nouvel objet LayerGroup via la méthode addLayerGroup de l'objet PsdImage. Fournissez le nom souhaité pour le calque de groupe ("Dossier"), spécifiez l'indice d'insertion (0) et définissez un indicateur booléen indiquant sa visibilité (Vrai).

Ensuite, créez deux objets Layer et définissez leurs noms d'affichage à l'aide de la méthode setDisplayName. Ajoutez ces calques au calque de groupe en utilisant la méthode addLayer.

Pour accéder aux calques à l'intérieur du groupe, utilisez la propriété layers de l'objet LayerGroup. Vérifiez que les noms d'affichage des premier et deuxième calques du groupe sont respectivement "Calque 1" et "Calque 2".

Une fois que vous avez manipulé les calques de groupe, enregistrez l'image PSD modifiée en utilisant la méthode save de l'objet PsdImage.

Ceci est un exemple fondamental pour vous familiariser avec la manipulation des calques de groupe avec Aspose.PSD pour Java. La bibliothèque offre une multitude de fonctionnalités avancées pour la manipulation de calques et la transformation au sein d'images PSD. Pour plus de détails et d'exemples sur l'utilisation des calques de groupe et d'autres fonctionnalités de la bibliothèque, consultez la documentation Aspose.PSD pour Java.

Pour travailler avec les calques de groupe dans Aspose.PSD pour Java, utilisez la classe LayerGroup. Voici un extrait de code illustrant comment créer un calque de groupe, ajouter des calques et enregistrer l'image PSD modifiée.

Veuillez vous référer à l'exemple complet fourni.

## **Exemple**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}
