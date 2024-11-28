---
title: Prise en charge des grandes images
type: docs
weight: 40
url: /fr/net/prise-en-charge-des-grandes-images/
---

## **Prise en charge des grandes images**
Étant donné que la bibliothèque standard .NET présente certaines limitations en ce qui concerne la taille des images qu'elle peut traiter, nous avons introduit un nouveau mécanisme de prise en charge des grandes images. La nouvelle approche surmonte les limitations mais en raison des limitations de taille des données, les dimensions maximales prises en charge pour la création et le chargement sont de 2 147 483 647 x 2 147 483 647 pixels.
### **Travailler avec de grandes images**
Aspose.PSD a amélioré ses performances et son support pour les grandes images. Les images de plusieurs centaines de mégaoctets ne posent plus de problème, vous pouvez donc créer, charger et dessiner sur ces images. Cependant, en raison du traitement partiel et de la gestion des exceptions OutOfMemoryException, les performances peuvent être très faibles sur les très grandes images. Cela est dû au fait qu'Aspose.PSD tente de réallouer une plus petite quantité de données pour le traitement et chaque étape de réallocation est très coûteuse. Les avantages de la nouvelle architecture sont évidents:

- Il n'y a pas de limite à la taille de l'image.
- Vous n'êtes pas limité par la mémoire disponible sur votre PC.

Si vous rencontrez des traitements lents, il est conseillé d'augmenter la quantité totale de RAM pour que tous vos pixels entrent en mémoire. Sinon, le traitement est toujours possible mais plus lent. L'approche est la suivante:

- Appelez la méthode [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) avec le rectangle désiré et déléguez pour recevoir les pixels chargés spécifiés.

Aspose.PSD tente de charger le rectangle entier.

- S'il y a assez de mémoire pour stocker tous les pixels, alors tous les pixels sont simplement renvoyés à l'appelant.
-S'il n'y a pas assez de mémoire, l'appelant reçoit un sous-ensemble de pixels situé à l'intérieur du rectangle spécifié. Lorsque ces pixels ont été traités, l'appelant reçoit le rectangle suivant. Le traitement se termine lorsque tout le rectangle est traité.

Aspose.PSD tente d'extraire autant de lignes que possible. S'il n'y a pas assez de mémoire pour stocker une seule ligne de pixels, alors une seule ligne est découpée en parties conformes aux rectangles ayant une hauteur de 1. Vous pouvez également dessiner sur de grandes images. Le processus de dessin tente d'affecter tout le rectangle souhaité. S'il n'y a pas assez de mémoire, le dessin est effectué sur des rectangles partiels jusqu'à ce que toute la zone soit dessinée. De plus, Aspose.PSD prend en charge l'enregistrement et l'exportation de grandes images. Enregistrez l'image source sur le disque ou exportez-la dans un autre format de fichier. Le processus d'enregistrement ou d'exportation est effectué en utilisant des rectangles partiels si nécessaire.
### **Formats d'image pris en charge**
Les formats suivants sont pris en charge pour le traitement des grandes images:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Les formats ci-dessus peuvent être traités en toute sécurité via la création, la modification, l'application d'opérations de dessin, l'enregistrement sur disque ou l'exportation, quel que soit la taille de l'image.
