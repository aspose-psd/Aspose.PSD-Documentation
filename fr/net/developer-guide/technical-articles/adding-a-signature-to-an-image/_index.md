---
title: Ajout d'une signature à une image
type: docs
weight: 70
url: /fr/net/ajout-dune-signature-a-une-image/
---

## **Ajout d'une signature**

Ajouter une signature à une image est parfois nécessaire pour signer numériquement les images afin d'éviter la contrefaçon. Une autre réflexion pourrait être de traiter l'image plus comme si elle était présentée dans une galerie. Quelle que soit la raison, les API Aspose.PSD fournissent la fonctionnalité d'ajouter une signature sur une image en utilisant le mécanisme le plus simple comme expliqué ci-dessous. Veuillez noter que cet exemple utilise la classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) pour dessiner une autre image avec une signature sur la surface de l'image d'origine. Pour illustrer l'opération, nous chargerons une image PSD depuis le disque et dessinerons une autre image en tant que signature sur la surface de l'image d'origine en utilisant la méthode [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) de la classe Graphics. Nous enregistrerons l'image résultante au format PNG en utilisant la classe [PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions). Voici un exemple de code qui montre comment ajouter une signature à une image. Le code source de l'exemple a été divisé en parties pour le rendre facile à suivre. Étape par étape, l'exemple montre comment :

- Charger les images primaire et secondaire (signature).
- Créer et initialiser un objet Graphics.
- Dessiner une image en utilisant la méthode DrawImage de la classe Graphics.
- Enregistrer le résultat au format PNG.
### **Exemples de programme**
#### **Chargement des images**
Tout d'abord, créez des instances de la classe Image pour charger les images d'exemple depuis le disque.
#### **Création et Initialisation d'un objet Graphics**
Après le chargement des images, créez et initialisez un objet de la classe Graphics en utilisant l'objet de l'image primaire.
#### **Dessiner l'image secondaire sur l'image primaire**
Puis en utilisant la méthode DrawImage de la classe Graphics, ajoutez l'image secondaire à l'image primaire. Il existe plusieurs surcharges de la méthode DrawImage qui acceptent un objet de type Image comme premier paramètre tandis que tous les autres paramètres correspondent à l'emplacement où l'image doit être dessinée. Pour les besoins de la démonstration, le code suivant utilise la version surchargée de DrawImage qui accepte un objet de type Point comme deuxième paramètre et tente de dessiner la signature dans le coin inférieur droit de l'image primaire.
#### **Enregistrer l'image**
Enfin, enregistrez l'image sur le disque local en tant que fichier PNG en utilisant la classe PngOptions.
#### **Source complète**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
