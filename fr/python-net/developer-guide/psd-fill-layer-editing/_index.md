---
title: Mise à jour de la couche de remplissage PSD en utilisant Python
weight: 100
type: docs
description: Exemples d'utilisation de tous les types de calques d'ajustement, y compris Color Fill, Gradient Fill et Pattern Fill
keywords: [calque de remplissage, Color Fill, Gradient Fill, Pattern Fill, psd api, python, exemple de code]
url: fr/python-net/psd-remplissage-couche-edition/
---

## **Aperçu**

Pour créer un calque régulier, vous pouvez utiliser la fonction create_regular_layer fournie dans le code. Cette fonction prend les paramètres left, top, width et height pour définir la position et la taille du calque. Elle crée un nouveau calque, définie ses limites, et le remplit avec une couleur spécifiée.

Pour créer un calque de remplissage de couleur, vous pouvez utiliser la méthode FillLayer.create_instance avec le paramètre FillType.COLOR. Après avoir créé le calque de remplissage, vous pouvez accéder à ses réglages de remplissage en utilisant la propriété fill_settings et définir la couleur en utilisant la propriété color de la classe ColorFillSettings. Dans le code fourni, la couleur est définie comme Color.coral. La propriété de rognage (clipping) du calque de remplissage est définie sur 1, ce qui fait que le calque agit comme un masque de rognage.

Pour créer un calque de remplissage de dégradé, vous pouvez utiliser la méthode FillLayer.create_instance avec le paramètre FillType.GRADIENT. De manière similaire au calque de remplissage de couleur, vous pouvez accéder aux réglages de remplissage en utilisant la propriété fill_settings et définir les points de couleur de dégradé et les points de transparence. Dans le code fourni, les points de couleur de dégradé sont définis en utilisant la classe GradientColorPoint, et les points de transparence sont définis en utilisant la classe GradientTransparencyPoint. La propriété de rognage du calque de remplissage est également définie sur 1.

Pour créer un calque de remplissage de motif, vous pouvez utiliser la méthode FillLayer.create_instance avec le paramètre FillType.PATTERN. Encore une fois, vous pouvez accéder aux réglages de remplissage en utilisant la propriété fill_settings et définir les données du motif et d'autres propriétés. Dans le code fourni, les données du motif sont définies en utilisant la classe PatternFillSettings, et la propriété de rognage est définie sur 1.

Après avoir créé les calques de remplissage, vous pouvez les ajouter à l'image PSD en utilisant la méthode add_layer. Vous pouvez également spécifier le nom d'affichage et d'autres propriétés pour chaque calque de remplissage.

Enfin, vous pouvez enregistrer l'image PSD et l'image PNG correspondante en utilisant le code fourni. Les options PNG sont définies pour utiliser la vraie couleur avec alpha pour la transparence.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}
