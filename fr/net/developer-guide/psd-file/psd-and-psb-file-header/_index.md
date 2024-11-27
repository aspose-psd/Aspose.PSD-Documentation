---
title: En-tête du fichier PSD et PSB
type: docs
weight: 40
url: /fr/net/psd-and-psb-file-header/
---

## **Description**
L'en-tête du fichier Adobe Photoshop contient des informations sur la version du fichier (1 pour PSD et 2 pour PSB), le nombre de canaux, le mode couleur et la profondeur de bits.

Vous pouvez apprendre les combinaisons prises en charge par Aspose.PSD du mode couleur et de la profondeur de bits à partir de l'article associé.

L'en-tête du fichier contient les propriétés de base de l'image.

|**Longueur**|**Description**|
| :- | :- |
|4|Signature : toujours égale à *"8BPS"*|
|2|[Version PSD](https://reference.aspose.com/psd/fr/aspose.psd.fileformats.psd/fileformatversion) : toujours égale à 1 pour les fichiers PSD et 2 pour les fichiers PSB. Aspose.PSD peut détecter une version du format de fichier et la lire correctement.|
|6|Réservé : doit être zéro.|
|2|Le nombre de canaux dans l'image, y compris tout canal alpha. La plage prise en charge est de 1 à 56.|
|4|La hauteur de l'image en pixels. La plage prise en charge est de 1 à 30 000. PSB File prend en charge une hauteur allant jusqu'à 300 000 pixels. Les fichiers PSB sont également pris en charge par Aspose.PSD.|
|4|La largeur de l'image en pixels. La plage prise en charge est de 1 à 30 000. Le fichier PSB prend en charge une largeur allant jusqu'à 300 000 pixels. Le traitement par lots de gros fichiers PSD/PSB est également pris en charge par Aspose.PSD.|
|2|Profondeur : le nombre de bits par canal. Les valeurs prises en charge sont 1, 8, 16 et 32. Mais tous les modes couleur ne fonctionnent pas avec toutes les profondeurs.|
|2|Le [mode couleur PSD](https://reference.aspose.com/psd/fr/com.aspose.psd.fileformats.psd/ColorModes) du fichier. Les valeurs prises en charge sont : Bitmap = 0; Niveaux de gris = 1; Indexé = 2; RVB = 3; CMJN = 4; Multicanal= 7; Duotone = 8; Lab = 9.|
Vous pouvez consulter notre [Référence de l'API PSD](https://reference.aspose.com/psd) à ce sujet.
