---
title: Prise en charge des grandes images
type: docs
weight: 60
url: /fr/java/prise-en-charge-des-grand-images/
---

## **Prise en charge des grandes images**
Étant donné que la bibliothèque Java standard présente certaines limitations en termes de taille d'image qu'elle peut traiter, nous avons introduit un nouveau mécanisme de prise en charge des grandes images. La nouvelle approche surmonte les limitations, mais en raison des limitations de taille des données, les dimensions maximales prises en charge pour la création et le chargement sont de 2 147 483 647 x 2 147 483 647 pixels.
### **Travailler avec de grandes images**
Aspose.PSD a amélioré les performances et la prise en charge des grandes images. Les images de plusieurs centaines de mégaoctets ne posent plus de problème, vous pouvez donc créer, charger et dessiner sur ces images. Cependant, en raison du traitement partiel et de la gestion des exceptions OutOfMemoryException, les performances peuvent être très faibles sur des images très grandes. En effet, Aspose.PSD essaie de réallouer une petite quantité de données pour le traitement, et chaque étape de réallocation est très coûteuse. Les avantages de la nouvelle architecture sont évidents :

- Il n'y a aucune limitation à la taille de l'image.
- Vous n'êtes pas limité par la mémoire disponible sur votre PC.

Si vous rencontrez des problèmes de traitement lent, il est conseillé d'augmenter la quantité totale de RAM pour adapter tous vos pixels en mémoire. Dans le cas contraire, le traitement est toujours possible mais plus lent. L'approche est la suivante :

- Appelez la méthode LoadPartialPixels avec le rectangle désiré et déléguez pour recevoir les pixels chargés spécifiés.

Aspose.PSD essaie de charger l'ensemble du rectangle.

- S'il y a suffisamment de mémoire pour adapter tous les pixels, alors tous les pixels sont simplement renvoyés à l'appelant.
- S'il n'y a pas assez de mémoire, l'appelant reçoit un sous-ensemble de pixels à l'intérieur du rectangle spécifié. Lorsque ces pixels ont été traités, l'appelant reçoit le rectangle suivant. Le traitement se termine lorsque l'ensemble du rectangle est traité.

Aspose.PSD essaie d'extraire autant de lignes que possible. S'il n'y a pas assez de mémoire pour adapter une seule ligne de pixels, alors une seule ligne est divisée en parties conformes aux rectangles ayant 1 hauteur. Vous pouvez également dessiner sur de grandes images. Le processus de dessin essaie d'affecter l'ensemble du rectangle désiré. S'il n'y a pas assez de mémoire, le dessin est effectué sur des rectangles partiels jusqu'à ce que toute la zone soit dessinée. De plus, Aspose.PSD prend en charge l'enregistrement et l'exportation de grandes images. Enregistrez l'image source sur le disque ou exportez-la vers un autre format de fichier. Le processus de sauvegarde ou d'exportation est effectué en utilisant des rectangles partiels si nécessaire.
### **Formats d'image pris en charge**
Les formats suivants sont pris en charge pour le traitement des grandes images :

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Les formats ci-dessus peuvent être traités en toute sécurité par la création, la modification, l'application d'opérations de dessin, l'enregistrement sur le disque ou l'exportation, quel que soit la taille de l'image.

. 
