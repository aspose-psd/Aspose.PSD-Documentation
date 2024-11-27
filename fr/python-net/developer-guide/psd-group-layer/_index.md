---
title: Exemple d'utilisation des calques de groupe dans Aspose.PSD pour Python
weight: 100
type: docs
description: Utilisation du calque de groupe du fichier PSD via Python
keywords: [calque de groupe, calque de groupe, ajouter un calque à un groupe, api psd, python, exemple de code]
url: fr/python-net/psd-group-layer/
---

## **Aperçu**

Travailler avec des calques de groupe dans Aspose.PSD pour Python est une fonctionnalité puissante qui vous permet d'organiser et de manipuler les calques au sein d'une image PSD. Les calques de groupe, également appelés calques de dossier, permettent de regrouper plusieurs calques et d'appliquer des transformations ou des effets à l'ensemble du groupe.

Dans cet exemple, nous créons d'abord une nouvelle image PSD en utilisant la méthode PsdImage.create. Ensuite, nous créons un nouvel objet LayerGroup en utilisant la méthode add_layer_group de l'objet PsdImage. Nous fournissons le nom du calque de groupe ("Dossier"), l'indice auquel il doit être inséré (0), et un indicateur booléen indiquant si le calque de groupe doit être visible (True).

Ensuite, nous créons deux objets Layer et définissons leurs noms d'affichage en utilisant la propriété display_name. Nous ajoutons ces calques au calque de groupe en utilisant la méthode add_layer.

Enfin, nous pouvons accéder aux calques au sein du groupe en utilisant la propriété layers de l'objet LayerGroup. Dans l'exemple, nous attestons que les noms d'affichage des premier et deuxième calques dans le groupe sont respectivement "Calque 1" et "Calque 2".

Après avoir manipulé les calques de groupe, nous pouvons enregistrer l'image PSD modifiée en utilisant la méthode save de l'objet PsdImage.

Il s'agit simplement d'un exemple de base pour vous aider à démarrer avec les calques de groupe dans Aspose.PSD pour Python. La bibliothèque propose de nombreuses fonctionnalités avancées pour la manipulation et la transformation des calques au sein des images PSD. Vous pouvez consulter la documentation Aspose.PSD pour Python pour plus de détails et d'exemples sur le travail avec les calques de groupe et d'autres fonctionnalités de la bibliothèque.

Pour travailler avec les calques de groupe dans Aspose.PSD pour Python, vous pouvez utiliser la classe LayerGroup. Voici un extrait de code d'exemple qui montre comment créer un calque de groupe, ajouter des calques et enregistrer l'image PSD modifiée.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}
