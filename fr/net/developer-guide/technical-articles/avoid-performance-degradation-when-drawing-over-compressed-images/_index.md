---
title: Évitez la dégradation des performances lors du dessin sur des images compressées
type: docs
weight: 10
url: /fr/net/evitez-la-degradation-des-performances-lors-du-dessin-sur-des-images-compressees/
---

## **Évitez la dégradation des performances lors du dessin sur des images compressées**
Il arrive parfois que vous vouliez effectuer des opérations graphiques extrêmement étendues sur une image compressée. Lorsque Aspose.PSD doit compresser et décompresser des images à la volée, une dégradation des performances peut se produire. Le dessin sur des images compressées peut également entraîner une pénalité en termes de performances.
### **Solution**
Pour éviter la dégradation des performances, nous recommandons de convertir l'image vers un format non compressé, ou brut, avant d'effectuer des opérations graphiques.
### **Utilisation du chemin du fichier**
Dans l'exemple suivant, une image PSD est convertie en format brut (sans compression) et enregistrée sur disque. L'image non compressée est ensuite rechargée avant que des opérations graphiques ne soient effectuées dessus. La même technique s'applique aux fichiers BMP et GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImageNonCompresséeUtilisationCheminFichier-ImageNonCompresséeUtilisationCheminFichier.cs" >}}
### **Utilisation d'un objet Stream**
Le code suivant vous montre comment une image PSD est convertie en format brut (sans compression) et enregistrée sur disque en utilisant MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImageNonCompresséeUtilisationObjetStream-ImageNonCompresséeUtilisationObjetStream.cs" >}}
