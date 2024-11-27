---
title: Ajout d'un filigrane à une image
type: docs
weight: 20
url: /fr/ajout-dun-filigrane-a-une-image/
---

## **Ajout d'un filigrane à une image**
Ce document explique comment ajouter un filigrane à une image en utilisant Aspose.PSD. Ajouter un filigrane à une image est une exigence courante pour les applications de traitement d'images. Cet exemple utilise la classe Graphics pour dessiner une chaîne de caractères sur la surface de l'image.
### **Ajout d'un filigrane**
Pour illustrer l'opération, nous chargerons une image BMP du disque et dessinerons une chaîne de caractères en tant que filigrane sur la surface de l'image en utilisant la méthode DrawString de la classe Graphics. Nous enregistrerons l'image au format PNG en utilisant la classe PngOptions. Voici un exemple de code qui montre comment ajouter un filigrane à une image. Le code source de l'exemple a été divisé en parties pour faciliter le suivi. Étape par étape, les exemples montrent comment:

1. Charger une image.
1. Créer et initialiser un objet Graphics.
1. Créer et initialiser des objets Font et SolidBrush.
1. Dessiner une chaîne de caractères en filigrane en utilisant la méthode DrawString de la classe Graphics.
1. Enregistrer l'image en PNG.

Le code suivant vous montre comment ajouter un filigrane à l'image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Ajout d'un filigrane diagonal**
Ajouter un filigrane diagonal à une image est similaire à l'ajout d'un filigrane horizontal comme discuté ci-dessus, avec quelques différences. Pour illustrer l'opération, nous chargerons une image JPG du disque, ajouterons des transformations en utilisant un objet de la classe Matrix et dessinerons une chaîne de caractères en tant que filigrane sur la surface de l'image en utilisant la méthode DrawString de la classe Graphics. Voici un exemple de code qui montre comment ajouter un filigrane diagonal à une image. Le code source de l'exemple a été divisé en parties pour faciliter le suivi. Étape par étape, les exemples montrent comment:

1. Charger une image.
1. Créer et initialiser un objet Graphics.
1. Créer et initialiser des objets Font et SolidBrush.
1. Obtenir la taille de l'image dans un objet SizeF.
1. Créer une instance de la classe Matrix et effectuer une transformation composite.
1. Affecter la transformation à l'objet Graphics.
1. Créer et initialiser un objet StringFormat.
1. Dessiner une chaîne de caractères en filigrane en utilisant la méthode DrawString de la classe Graphics.
1. Enregistrer l'image résultante.

Le code suivant vous montre comment ajouter un filigrane diagonal.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
