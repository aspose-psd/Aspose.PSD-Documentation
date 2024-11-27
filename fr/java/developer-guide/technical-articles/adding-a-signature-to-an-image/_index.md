---
title: Ajouter une signature à une image
type: docs
weight: 10
url: /fr/ajouter-une-signature-a-une-image/
---

## **Ajouter une Signature**

Ajouter une signature à une image est parfois nécessaire pour signer numériquement les images afin d'éviter les contrefaçons. Une autre réflexion pourrait être de traiter l'image comme si elle était exposée dans une galerie. Quelle que soit la raison, les API Aspose.PSD fournissent la fonctionnalité pour ajouter une signature à une image en utilisant le mécanisme le plus simple comme expliqué ci-dessous. Veuillez noter que cet exemple utilise la classe Graphics pour dessiner une autre image avec une signature sur la surface de l'image d'origine. Pour illustrer l'opération, nous chargerons une image PSD depuis le disque et dessinerons une autre image comme signature sur la surface de l'image d'origine en utilisant la méthode DrawImage de la classe Graphics. Nous enregistrerons l'image résultante au format PNG en utilisant la classe PngOptions. Ci-dessous se trouve un exemple de code qui montre comment ajouter une signature à une image. Le code source de l'exemple a été divisé en parties pour le rendre facile à suivre. Étape par étape, l'exemple montre comment :

- Charger les images principale et secondaire (signature).
- Créer et initialiser un objet Graphics.
- Dessiner une image en utilisant la méthode DrawImage de la classe Graphics.
- Enregistrer le résultat au format PNG.
### **Exemples de Programme**
#### **Chargement des Images**
Tout d'abord, créez des instances de la classe Image pour charger les images d'exemple depuis le disque.
#### **Création et Initialisation d'un Objet Graphique**
Après le chargement des images, créez et initialisez un objet de la classe Graphics tout en utilisant l'objet de l'image principale.
#### **Dessiner une Image Secondaire sur l'Image Principale**
Ensuite, en utilisant la méthode DrawImage de la classe Graphics, ajoutez l'image secondaire à l'image principale. Il existe plusieurs surcharges de la méthode DrawImage qui acceptent un objet de la classe Image comme premier paramètre, tandis que tous les autres paramètres correspondent à l'emplacement où l'image doit être dessinée. Pour l'exemple, le code suivant utilise la version de la surcharge de DrawImage qui accepte un objet de la classe Point comme deuxième paramètre et tente de dessiner la signature dans le coin inférieur droit de l'image principale.
#### **Enregistrer l'Image**
Enfin, enregistrez l'image de nouveau sur le disque local en tant que fichier PNG en utilisant la classe PngOptions.
#### **Code Source Complet**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}
