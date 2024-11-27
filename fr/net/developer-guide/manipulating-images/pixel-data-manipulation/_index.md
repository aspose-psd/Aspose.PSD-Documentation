---
title: Manipulation des données de pixels en utilisant Aspose.PSD pour C#
weight: 100
type: docs
description: Exemple de comment mettre à jour rapidement et directement les données brutes des pixels en utilisant l'API C# de PSD
keywords: [modifier pixels, modifier psd, modifier calque, manipulation de données brutes, modifier données psd, api psd, C#, csharp, exemple de code]
url: fr/manipulation-des-donnees-de-pixel/
---

## Introduction

Aspose.PSD est une bibliothèque puissante qui vous permet de travailler avec des fichiers Adobe Photoshop (PSD) en C#. Dans cet article, nous allons explorer comment manipuler les données de pixels dans un fichier PSD en utilisant Aspose.PSD pour C#.

## Aperçu

Le code fourni démontre comment créer un fichier PSD, ajouter un nouveau calque, manipuler directement les données de pixels et enregistrer l'image modifiée.

### Étapes pour Manipuler les Données de Pixels

1. **Importer les modules requis**:
   Importez les modules nécessaires. Vous avez besoin d'importer les classes `PsdImage` et `Layer` de la bibliothèque Aspose.PSD.

2. **Définir les chemins des fichiers d'entrée et de sortie**:
   Spécifiez les chemins des fichiers d'entrée et de sortie.

3. **Ouvrir le fichier d'entrée en tant que flux**:
   Ouvrez le fichier d'entrée en tant que flux en utilisant la classe `FileStream` en mode lecture. Créez un objet `PsdImage` en chargeant le flux.

4. **Créer une Nouvelle Image PSD**:
   Créez une nouvelle image PSD en utilisant le constructeur `PsdImage` et fournissez la largeur et la hauteur du calque en arguments.

5. **Attribuer le Calque à l'Image PSD**:
   Attribuez le calque à la propriété `Layers` de l'image PSD.

6. **Manipuler les Données de Pixels**:
   Chargez les pixels ARGB32 du calque en utilisant la méthode `LoadArgb32Pixels`. Définissez une plage d'indices en fonction de la longueur du tableau de pixels et modifiez les valeurs des pixels selon vos besoins.

7. **Enregistrer les Données de Pixels Modifiées**:
   Enregistrez les données de pixels modifiées de nouveau sur le calque en utilisant la méthode `SaveArgb32Pixels`.

8. **Enregistrer l'Image PSD**:
   Enregistrez l'image PSD dans le fichier de sortie en utilisant la méthode `Save`.

### Exemple

Voici un exemple de code démontrant comment manipuler les données de pixels en utilisant Aspose.PSD pour C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### Résumé

Aspose.PSD pour C# offre un ensemble de fonctionnalités puissantes pour manipuler les données de pixels dans les fichiers PSD. Que vous ayez besoin de modifier des pixels en fonction de conditions spécifiques ou de créer des motifs complexes, Aspose.PSD rend ces tâches simples et efficaces.

Pour plus d'informations détaillées et d'exemples, veuillez visiter la [documentation Aspose.PSD pour C#](https://docs.aspose.com/psd/net/).
