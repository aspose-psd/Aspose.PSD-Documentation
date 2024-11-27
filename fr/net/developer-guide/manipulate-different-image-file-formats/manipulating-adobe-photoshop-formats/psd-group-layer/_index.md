---
title: Exemple d'utilisation de couches de groupe dans Aspose.PSD pour C#
weight: 100
type: docs
description: Utilisation de la couche de groupe du fichier PSD via C#
keywords: [groupe de calques, couche de groupe, ajouter une couche au groupe, api psd, C#, csharp, exemple de code]
url: fr/net/psd-groupe-de-couches/
---

## Aperçu

Les couches de groupe dans Aspose.PSD pour C# permettent une organisation et une manipulation efficaces des couches dans un fichier PSD. En utilisant des couches de dossier, vous pouvez regrouper plusieurs couches ensemble et appliquer des transformations ou des effets à l'ensemble du groupe.

Cet exemple montre comment créer une nouvelle image PSD avec `PsdImage.Create`. Ensuite, un nouvel objet `LayerGroup` est créé en utilisant `AddLayerGroup` depuis l'objet `PsdImage`. La couche de groupe est nommée "Dossier", insérée à l'index 0 et définie comme visible.

Ensuite, deux objets `Layer` sont créés avec leurs propriétés `DisplayName` définies. Ces couches sont ajoutées à la couche de groupe en utilisant `AddLayer`.

Les couches à l'intérieur du groupe peuvent être accédées via la propriété `Layers` de l'objet `LayerGroup`. L'exemple vérifie que les noms d'affichage des première et deuxième couches du groupe sont "Couche 1" et "Couche 2".

Après avoir modifié les couches de groupe, l'image PSD mise à jour est enregistrée avec la méthode `Save` de l'objet `PsdImage`.

Cet exemple de base présente le travail avec les couches de groupe en utilisant Aspose.PSD pour C#. La bibliothèque offre des fonctionnalités avancées pour manipuler et transformer des couches dans des fichiers PSD. Consultez la documentation Aspose.PSD pour C# pour plus d'exemples et de fonctionnalités détaillés.

Voici un exemple de code illustrant l'utilisation de la couche de groupe dans Aspose.PSD pour C#:

## Exemple

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Pour plus d'informations détaillées et d'exemples, veuillez visiter la [documentation Aspose.PSD pour C#](https://docs.aspose.com/psd/net/).
