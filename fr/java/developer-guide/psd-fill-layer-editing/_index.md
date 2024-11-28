---
title: Mise à jour de la couche de remplissage PSD en utilisant Java
weight: 100
type: docs
description: Exemples d'utilisation de tous les types de calques d'ajustement, y compris le remplissage de couleur, le remplissage de dégradé et le remplissage de motif
keywords: [calque de remplissage, remplissage de couleur, remplissage de dégradé, remplissage de motif, api psd, java, exemple de code]
url: fr/java/psd-fill-layer-editing/
---

## **Aperçu**

La création d'une couche régulière implique d'utiliser la fonction createRegularLayer, qui nécessite des paramètres pour définir la position et la taille de la couche. Cette fonction crée une nouvelle couche, définit ses limites et la remplit avec une couleur spécifiée.

Pour une couche de remplissage de couleur, vous utilisez la méthode FillLayer.createInstance avec le paramètre FillType.Color. Une fois la couche de remplissage créée, accédez à ses paramètres de remplissage via la propriété fill_settings et définissez la couleur souhaitée en utilisant la propriété de couleur de la classe ColorFillSettings. Dans ce contexte, la couleur est définie sur Color.getCoral(). De plus, la propriété de rognage de la couche de remplissage est définie sur 1, ce qui la fait fonctionner comme un masque d'écrêtage.

Les couches de remplissage de dégradé sont créées de manière similaire en utilisant la méthode FillLayer.create_instance, mais avec le paramètre FillType.Gradient. Comme pour les couches de remplissage de couleur, vous accédez aux paramètres de remplissage via fill_settings et définissez les points de couleur du dégradé et les points de transparence. Dans cet exemple, les points de couleur du dégradé sont définis avec la classe GradientColorPoint et les points de transparence avec la classe GradientTransparencyPoint. La propriété de rognage de la couche de remplissage est également définie sur 1.

Les couches de remplissage de motif sont créées en utilisant FillLayer.createInstance avec le paramètre FillType.Pattern. Encore une fois, accédez aux paramètres de remplissage via fill_settings et définissez les données du motif et d'autres propriétés. Dans ce code, les données du motif sont définies en utilisant la classe PatternFillSettings et la propriété de rognage est définie sur 1.

Une fois les couches de remplissage créées, ajoutez-les à l'image PSD en utilisant la méthode addLayer, en spécifiant le nom d'affichage et d'autres propriétés pour chaque couche de remplissage.

Enfin, enregistrez l'image PSD et son image PNG correspondante avec le code fourni. Les options PNG sont configurées pour utiliser une vraie couleur avec de l'alpha pour la transparence.

Veuillez vous référer à l'exemple complet pour plus de détails.

## **Exemple**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}
