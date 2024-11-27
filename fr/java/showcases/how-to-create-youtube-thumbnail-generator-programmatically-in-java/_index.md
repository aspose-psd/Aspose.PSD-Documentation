---
title: Comment créer un générateur de miniatures YouTube de manière programmative en Java
type: docs
weight: 10
url: /fr/java/comment-creer-un-generateur-de-miniatures-youtube-de-maniere-programmative-en-java/
---

## **Introduction**
Le but de ce document est de démontrer l'utilisation de l'API de certains outils composés d'[Aspose.PSD pour Java](https://products.aspose.com/psd/java) sur un exemple réel. Dans cet article, **un simple programme Java qui génère des miniatures YouTube** pour la chaîne [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q) sera écrit et expliqué. Cette chaîne a été choisie de la vie réelle car ses miniatures sont assez standards, et elles illustrent l'utilisation de quelques outils composés populaires d'Aspose.PSD pour Java (par exemple, l'effet [d'ombre portée](/psd/fr/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), le remplissage de dégradé radial, le dessin de texte et de formes) :

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)
## **Fonctionnement en bref**
Un simple programme Java prend en entrée deux arguments : une légende et une image. Un **document Photoshop (PSD) en mémoire est généré** à partir de cette entrée en utilisant Aspose.PSD pour Java. Ensuite, le programme **convertit le document du format PSD au format de fichier PNG** pour obtenir une miniature YouTube avec une taille de 1280x720 pixels. L'image de sortie ressemble à ce qui suit :

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)
## **Exigences techniques**
Les technologies suivantes sont nécessaires pour réussir à exécuter le code de cet article :

- Java 6+
- [Aspose.PSD pour Java](/psd/fr/java/installation/) (la dernière version)
## **Pour commencer**
Comme il a été mentionné, le programme utilise un PSD en mémoire pour générer une miniature. Alors, commençons par **créer un document PSD** :

PsdImage psdImage = new PsdImage(1280, 720);

Si vous examinez de plus près la miniature YouTube ci-dessus, vous pouvez remarquer que **elle est composée de plusieurs composants** :

1. une image de fond (masque imprimé)
1. un dégradé radial PSD (met en valeur la zone dans le coin supérieur droit)
1. un logotype avec un effet d'ombre portée
1. une légende et un dessin simple (rectangle bleu)

Plongeons plus profondément pour voir comment implémenter chacun de ces composants en utilisant Aspose.PSD pour Java dans les prochaines sections.
## **1. Ajouter une image de fond**
L'ordre des calques est important. Par conséquent, une image de fond doit être ajoutée en premier pour ne pas chevaucher les autres calques. Faites attention que seuls les [formats de fichiers raster sont pris en charge](/psd/fr/java/supported-file-formats/) pour le moment.
### **1.1. Ajouter une image de fond à un calque Photoshop**
Pour **ajouter une image raster dans un PSD**, un flux d'entrée doit être passé en argument lors de la construction du calque (voir plus d'[exemples de chargement d'images raster](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)) :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}



1.2. Adapter l'image de fond à la toile

Les 2 actions suivantes (redimensionnement, positionnement) sont utiles pour les cas où **la taille de l'image diffère de la taille de la toile**, bien que l'image dans cet article ait la même taille que la toile (supposez que ce ne sera pas toujours le cas).

Assurez-vous que l'image chargée **s’adapte à la taille de la toile** (voir plus d'[exemples de redimensionnement](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)) :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}



Après le redimensionnement, la position de l'image est modifiée. Par conséquent, pour **réinitialiser la position de l'image**, déplacez l'image redimensionnée dans le coin supérieur gauche :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
## **2. Ajouter un dégradé radial**
Il y a **deux façons d'ajouter un dégradé radial**, en utilisant :

- un [effet de superposition de dégradé](/psd/fr/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) sur un calque existant (un effet de dégradé qui se lie au calque actuel et s'applique à son contenu)
- un nouveau [calque de remplissage de dégradé](/psd/fr/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (un calque séparé qui conserve une configuration autonome du dégradé)

Il suffit d'utiliser l'effet de superposition de dégradé pour cet exemple. Cependant, pour rendre cet article plus intéressant et utile, **le calque de remplissage de dégradé est utilisé** car tous les effets de calque s'appliquent de manière similaire et un autre effet de calque sera utilisé dans la prochaine section.
### **2.1. Ajouter un calque de remplissage de dégradé radial**
Le processus d'ajout d'un nouveau calque de remplissage de dégradé se compose des 2 étapes suivantes :

\1. Il est nécessaire de **déclarer les paramètres de remplissage de dégradé** car il n'en existe pas de prédéfinis. La configuration minimale requise ressemble à ce qui suit (ce qui signifie que le type de dégradé, l'échelle, la couleur et les points de transparence sont des propriétés requises) :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}



La configuration ci-dessus déclare un dégradé radial qui est transparent sur les bords et bleu foncé au centre. La position du dégradé est au milieu de la toile par défaut.

Pour inverser le remplissage de dégradé et le déplacer légèrement vers le coin supérieur droit, utilisez les propriétés facultatives correspondantes :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}


\2. Lorsque la configuration est terminée, ajoutez un calque de remplissage de dégradé avec ses paramètres dans le PSD :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
## **Ajouter un logotype avec une ombre**
L'**ombre portée** est un effet qui permet d'ajouter une ombre personnalisée le long du contour de l'objet (image, texte, etc.).
### **3.1. Ajouter un logotype à un calque Photoshop**
La même approche que dans la section 1.1. peut être utilisée pour **ajouter un logotype dans un PSD** :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
### **3.2. Positionner le logotype**
L'image chargée est étroitement collée au coin supérieur gauche par défaut. Cependant, des **marges doivent être ajoutées** pour ressembler à la miniature YouTube originale sur la chaîne. Par conséquent, la position de l'image doit être éloignée des bords du calque :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
### **3.3. Ajouter un effet d'ombre portée au logotype**
Le logotype peut être invisible si une image d'arrière-plan claire est utilisée. Par conséquent, il est souhaitable d'**ajouter un effet d'ombre portée** à un logotype à travers la propriété d'options de fusion (voir plus d'[exemples d'ombres](/psd/fr/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)) :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}

L'effet d'ombre portée n'a pas les propriétés requises en raison de la configuration par défaut (il ressemble à celui de Photoshop). Cependant, l'ombre ci-dessus est modifiée pour ressembler à une bordure translucide floue sur les bords.        
## **4. Ajouter un dessin de texte et de forme**
### **3.1. Créer un calque graphique**
Le dessin n'est pas pris en charge directement par un calque régulier. Par conséquent, le moteur graphique est utilisé à côté du calque pour **fournir une API de dessin** (voir plus d'[exemples de dessin](/psd/fr/java/drawing-images-using-graphics/)) :

Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
### **3.2. Dessiner un texte multiligne**
Un lecteur astucieux pourrait demander : pourquoi ne pas utiliser un calque de texte pour ajouter un texte ? Eh bien, il y a quelques raisons : l'édition de texte n'est pas requise dans ce cas car le PSD est généré à partir de zéro à chaque fois ; la personnalisation de la police n'est pas prise en charge par l'API [texte](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) (v20.6 au moment de l'écriture).

Il est facile de **dessiner du texte avec une police personnalisée** : il suffit d'instancier une police désirable et d'appeler la méthode correspondante du moteur graphique. Cependant, pour créer un rectangle (voir les détails dans la prochaine section) dont la hauteur change automatiquement en fonction du nombre de lignes de texte est un peu plus difficile. La hauteur exacte de toutes les lignes doit d'abord être calculée :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}

Où 1,15 est la hauteur de la ligne, 3 est le rembourrage de texte.
### **3.3. Dessiner un rectangle**
Un rectangle est également facile à dessiner même avec une brosse dégradée (il suffit de définir une zone à dessiner et une plage de couleurs). Lorsque la hauteur du texte est connue, la taille et la position du rectangle se calculent. Pour **dessiner un rectangle rempli** **dans le psd** (pas seulement un cadre), appelez la méthode correspondante du moteur graphique avec tout cela :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}

` `Où 40, 15, 25 sont les retraits.
## **Résultat**
Ainsi, la mise en forme de la miniature est terminée. Par conséquent, il est temps d'**exporter la miniature dans un format de fichier raster** (par exemple, PNG) pour une distribution ultérieure :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}
## **Conclusion**
Dans cet article, nous avons créé un générateur de miniatures YouTube pour la chaîne DW Documentary et expliqué comment utiliser certains des outils composés les plus populaires tels que l'effet d'ombre portée, le remplissage de dégradé radial, le dessin de texte et de formes.
## **Exemple complet**
Vous pouvez [télécharger le SDK Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
