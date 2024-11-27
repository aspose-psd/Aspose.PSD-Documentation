---
title: Ajouter un filigrane à une image
type: docs
weight: 30
url: /fr/net/ajouter-un-filigrane-a-une-image/
---

## **Ajouter un filigrane à une image**
Ce document explique comment ajouter un filigrane à une image en utilisant Aspose.PSD. Ajouter un filigrane à une image est une exigence courante pour les applications de traitement d'images. Cet exemple utilise la classe Graphics pour dessiner une chaîne de caractères sur la surface de l'image.

### **Ajouter un filigrane**
Pour illustrer l'opération, nous chargerons une image BMP depuis le disque et dessinerons une chaîne de caractères en tant que filigrane sur la surface de l'image en utilisant la méthode DrawString de la classe Graphics. Nous sauvegarderons l'image au format PNG en utilisant la classe PngOptions. Voici un exemple de code qui montre comment ajouter un filigrane à une image. Le code de l'exemple a été divisé en parties pour en faciliter la compréhension. Étape par étape, les exemples montrent comment :

1. [Charger](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) une image.
2. Créer et initialiser un objet [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
3. Créer et initialiser des objets Font et [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
4. Dessiner une chaîne de caractères en tant que filigrane en utilisant la méthode [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) de la classe Graphics.
5. Sauvegarder l'image au format PNG.

Le code suivant vous montre comment ajouter un filigrane à l'image.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **Ajouter un filigrane diagonal**
Ajouter un filigrane diagonal à une image est similaire à l'ajout d'un filigrane horizontal comme discuté ci-dessus, avec quelques différences. Pour illustrer l'opération, nous chargerons une image JPG depuis le disque, ajouterons des transformations en utilisant un objet [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) et dessinerons une chaîne de caractères en tant que filigrane sur la surface de l'image en utilisant la méthode DrawString de la classe Graphics. Voici un exemple de code qui montre comment ajouter un filigrane diagonal à une image. Le code de l'exemple a été divisé en parties pour en faciliter la compréhension. Étape par étape, les exemples montrent comment :

1. Charger une image.
2. Créer et initialiser un objet Graphics.
3. Créer et initialiser des objets [Font](https://reference.aspose.com/psd/net/aspose.psd/font) et SolidBrush.
4. Obtenir la taille de l'image dans un objet [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
5. Créer une instance de la classe Matrix et effectuer une transformation composite.
6. Assigner la transformation à l'objet Graphics.
7. Créer et initialiser un objet [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
8. Dessiner une chaîne de caractères en tant que filigrane en utilisant la méthode DrawString de la classe Graphics.
9. Sauvegarder l'image résultante.

Le code suivant vous montre comment ajouter un filigrane diagonal.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
