---
title: Évitez la dégradation des performances lors du dessin sur des images compressées
type: docs
weight: 40
url: /fr/java/evitez-la-degradation-des-performances-lors-du-dessin-sur-des-images-compressees/
---

## **Évitez la dégradation des performances lors du dessin sur des images compressées**
Il arrive parfois que vous souhaitiez effectuer des opérations graphiques extrêmement vastes sur une image compressée. Lorsque Aspose.PSD doit compresser et décompresser des images à la volée, une dégradation des performances peut se produire. Le fait de dessiner sur des images compressées peut également entraîner une pénalité en termes de performances.
### **Solution**
Pour éviter la dégradation des performances, nous vous recommandons de convertir l'image dans un format non compressé, c'est-à-dire brut, avant d'effectuer des opérations graphiques.
### **Utilisation du chemin de fichier**
Dans l'exemple suivant, une image PSD est convertie en format brut (sans compression) et enregistrée sur le disque. L'image non compressée est ensuite chargée à nouveau avant d'effectuer des opérations graphiques dessus. La même technique s'applique aux fichiers BMP et GIF.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Utilisation d'un objet de flux**
Le bout de code suivant vous montre comment convertir une image PSD en format brut (sans compression) et l'enregistrer sur le disque en utilisant un flux.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
