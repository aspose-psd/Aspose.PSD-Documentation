---
title: Manipulation des données de pixels en utilisant Aspose.PSD pour Python
weight: 100
type: docs
description: Exemple de la façon de mettre à jour rapidement et directement les données brutes de pixels en utilisant l'API Python PSD d'Aspose
keywords: [modifier les pixels, modifier psd, modifier calque, manipulation de données brutes, modifier les données psd, api psd, python, exemple de code]
url: fr/python-net/manipulation-des-donnees-de-pixels/
---

## **Introduction**
Aspose.PSD est une bibliothèque puissante qui vous permet de travailler avec des fichiers Adobe Photoshop (PSD) en Python. Dans cet article, nous explorerons comment manipuler les données de pixels dans un fichier PSD en utilisant Aspose.PSD.

## **Aperçu**
Le code fourni démontre comment créer un fichier PSD, ajouter le nouveau calque et ensuite manipuler directement les données de pixels, puis enregistrer l'image modifiée.

Importation des modules requis : La première étape consiste à importer les modules nécessaires. Nous importons le module BytesIO de la bibliothèque io, ainsi que les classes PsdImage et Layer des modules aspose.psd.fileformats.psd et aspose.psd.fileformats.psd.layers respectivement.

Ensuite, nous définissons les chemins des fichiers d'entrée et de sortie.

Ouverture du fichier d'entrée en tant que flux : Nous ouvrons le fichier d'entrée en tant que flux en utilisant la fonction open et le mode "rb". L'argument de mise en mémoire tampon est défini sur 0 pour désactiver la mise en mémoire tampon. Le contenu du fichier est lu dans un flux BytesIO et le flux est positionné au début en utilisant stream.seek(0).

Nous créons un objet de calque PSD en passant le flux au constructeur de la classe Layer.

Nous créons une nouvelle image PSD en utilisant le constructeur de la classe PsdImage et fournissons la largeur et la hauteur du calque en tant qu'arguments.

Nous attribuons le calque à la propriété layers de l'image PSD en utilisant l'opérateur d'assignation (=).

Pour manipuler les données de pixels, nous chargeons d'abord les pixels ARGB32 du calque en utilisant la méthode load_argb_32_pixels. Nous stockons le résultat dans la variable pixels.

Ensuite, nous définissons une plage d'indices (pixelsRange) basée sur la longueur du tableau de pixels. Nous itérons sur les indices et vérifions si un indice est divisible par 5. Si c'est le cas, nous définissons la valeur du pixel à cet indice sur 500000. Ainsi, nous voulons simplement créer un motif répétitif. Vous pouvez changer les données des pixels comme vous le souhaitez.

Ensuite, nous enregistrons les données de pixels modifiées dans le calque en utilisant la méthode save_argb_32_pixels.

Enfin, nous enregistrons l'image PSD dans le fichier de sortie en utilisant la méthode save.

Dans cet article, nous avons exploré comment manipuler les données de pixels dans un fichier PSD en utilisant Aspose.PSD pour Python. En comprenant le code fourni, vous pouvez effectuer diverses opérations au niveau des pixels, telles que modifier les pixels en fonction de certaines conditions. Aspose.PSD offre un ensemble complet de fonctionnalités pour travailler avec des fichiers PSD de manière programmatique, en faisant un outil précieux pour les tâches de manipulation d'images en Python.

Veuillez noter que le code fourni suppose que vous avez déjà installé la bibliothèque Aspose.PSD et ses dépendances. Vous pouvez trouver plus d'informations sur l'installation et l'utilisation d'Aspose.PSD pour Python dans la documentation officielle.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-pixel-data-manipulation.py" >}}
