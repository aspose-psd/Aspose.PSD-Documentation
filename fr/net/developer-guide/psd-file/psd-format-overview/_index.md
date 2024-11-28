---
title: Aperçu du format PSD
type: docs
weight: 60
url: /fr/net/psd-format-overview/
---

## **Description**
PSD, Document Photoshop, représente le format de fichier natif d'Adobe Photoshop utilisé pour la conception graphique et le développement.

## **Spécifications du format de fichier**
Les données dans un fichier PSD sont stockées dans l'ordre des octets big-endian. Cela implique d'échanger les entiers courts et longs lors de la lecture ou de l'écriture sur la plateforme Windows. Le format de fichier Photoshop est divisé en cinq grandes parties. Il a de nombreux indicateurs de longueur qui peuvent être utilisés pour passer d'une section à la suivante. Les indicateurs de longueur sont généralement rembourrés avec des octets pour arrondir à l'intervalle le plus proche de 2 ou 4 octets. Les cinq grandes parties sont :

- En-tête de fichier
- Données du mode couleur
- Ressources d'image
- Informations sur les calques et les masques
- Données d'image

Pour la conformité, les données doivent être écrites à tous ces champs dans la section, car Photoshop pourrait essayer de lire l'ensemble de la section. Cela implique également que des zéros soient écrits aux champs omis lors de l'écriture dans un fichier. Le champ de longueur dans les sections délimitées par la longueur doit être utilisé pour décider quand arrêter la lecture. Dans la plupart des cas, le champ de longueur indique le nombre d'octets, pas d'enregistrements, à suivre. Les points suivants doivent être retenus lors de la lecture d'un fichier.

- Les valeurs dans la colonne "Longueur" de toutes les tables sont en octets.
- Toutes les valeurs définies comme chaîne Unicode se composent de :
- Un champ de longueur de 4 octets, représentant le nombre de caractères dans la chaîne (pas d'octets).
- La chaîne de valeurs Unicode, deux octets par caractère.

## **Caractéristiques du format**
Les fichiers PSD peuvent inclure des calques d'image, des calques d'ajustement, des masques de calque, des annotations, des informations de fichier, des mots-clés et d'autres éléments spécifiques à Photoshop. Les fichiers Photoshop ont l'extension par défaut.PSD et ont une hauteur et une largeur maximales de 30 000 pixels, et une limite de longueur de deux gigaoctets.

## **Comment cela peut être utilisé**
1. Un instrument pour le Découpage de PSD.
1. [Conversion de PSD](/psd/fr/net/converting-psd-image-to-raster-format/) en HTML
1. Utilisation de [PSD comme modèle](/psd/fr/net/using-psd-files-as-templates-for-automation-business-cards-case/) pour l'Email
1. PSD vers HTML CMS spécifique
1. Identikit dans un fichier PSD (Portrait-robot)
1. Créer des images d'aperçu pseudo-3D à l'aide d'Objets intelligents pour des biens tels que des bouteilles, des tasses, des t-shirts, etc.
1. Édition rapide de PSD : Corrections automatiques, Préréglages, Objet intelligent, Découpe d'image de calque de texte

Et bien plus encore. Si vous avez réalisé quelque chose d'exceptionnel avec Aspose.PSD, veuillez partager avec nous votre étude de cas en utilisant les [Forums Aspose](https://forum.aspose.com/).

Des exemples supplémentaires dont vous pouvez vous inspirer :

- [Études de cas](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Exemples](/psd/fr/net/showcases-html/)
