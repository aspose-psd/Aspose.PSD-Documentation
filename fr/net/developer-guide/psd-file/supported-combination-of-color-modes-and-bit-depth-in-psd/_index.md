---
title: Combinaison de modes de couleur et de profondeur de bits pris en charge dans PSD
type: docs
weight: 80
url: /fr/combination-de-modes-de-couleur-et-de-profondeur-de-bits-pris-en-charge-dans-psd/
---

## **Description**
Aspose.PSD prend en charge l'ouverture de fichiers PSD avec n'importe quelle combinaison de mode de couleur et de profondeur de bits dans les fichiers Adobe Photoshop PSD. Vous pouvez ouvrir de tels fichiers et utiliser une API de bas niveau pour modifier le contenu du fichier. Mais pour certaines combinaisons moins populaires, des problèmes spécifiques peuvent survenir, certains d'entre eux étant liés aux limitations des modes de couleur.

## **Combinaison d'exportation prise en charge de modes de couleur et de profondeur de bits dans PSD en mode lecture seule**

| | Bitmap | Niveaux de gris | Indexé | RVB | CMJN | Multicanal | Duotone | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Profondeur 1 | Oui[](https://issue.kharkov.dynabic.com/issues/PSDNET-283) | - | - | - | - | - | - | - |
| Profondeur 8 | - | Oui | Oui | Oui | Oui | Non Q3-Q4 | Non Q3-Q4 | Oui[](https://issue.kharkov.dynabic.com/issues/PSDNET-290) |
| Profondeur 16 | - | Oui | - | Oui | Oui | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-287) | - | Non (Q3-Q4) |
| Profondeur 32 | - | Oui*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125) | - | Oui* | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-285) | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-288) | - | - |
\* Problèmes mineurs dans certains cas

## **Combinaison d'exportation prise en charge de modes de couleur et de profondeur de bits dans PSD en mode édition**

| | Bitmap | Niveaux de gris | Indexé | RVB | CMJN | Multicanal | Duotone | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Profondeur 1 | Oui | - | - | - | - | - | - | - |
| Profondeur 8 | - | Oui | Non | Oui | Oui | Non Q3-Q4 | Non Q3-Q4 | Oui* |
| Profondeur 16 | - | Oui | - | Oui | Oui* | - | - | Non (Q3-Q4) |
| Profondeur 32 | - | Non (Q3-Q4) | - | Non (Q3-Q4) | - | - | - | - |
\* Problèmes mineurs dans certains cas

Si vous avez besoin du soutien d'une combinaison spécifique de modes de couleur / profondeur de bits, vous pouvez poster sur les [forums Aspose](https://forum.aspose.com/c/psd)
