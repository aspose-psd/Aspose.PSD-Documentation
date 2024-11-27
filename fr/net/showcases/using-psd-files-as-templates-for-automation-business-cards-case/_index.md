---
title: Utiliser des fichiers PSD comme modèles pour l'automatisation - Cas des cartes de visite
type: docs
weight: 10
url: /fr/utiliser-des-fichiers-psd-comme-modeles-pour-lautomatisation-cas-des-cartes-de-visite/
---

### **Aperçu**
Cet article décrit des cas d'utilisation courants lorsque vous avez besoin de mettre à jour certaines couches dans un [fichier PSD](https://wiki.fileformat.com/image/psd/) de manière programmable, où le fichier PSD/PSB a une structure de modèle connue. Cela peut être utilisé pour créer une grande quantité de cartes de visite pour différentes personnes (Cas des cartes de visite). Ou vous devez traduire le fichier PSD dans différentes langues en remplaçant certains éléments graphiques.

Après avoir lu cet article, vous saurez comment procéder :

![à faire:texte_alt_image](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **Cas simple**
Par exemple, vous avez un modèle PSD avec des noms de calques connus. Vous devez donc changer, mettre à jour ou remplacer une couche PSD via C#. Tout d'abord, vous devez ouvrir le fichier de modèle avec Aspose.PSD.

Comment ouvrir un fichier PSD via C# ?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![à faire:texte_alt_image](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

Ensuite, nous devons trouver une couche que nous voulons remplacer par son nom. Voici une implémentation simple pour cela.

Comment trouver la couche dans le fichier PSD par son nom

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}

Lorsque la couche est trouvée, nous pouvons la mettre à jour de manière courante, en utilisant [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) :

Comment dessiner sur la couche PSD avec Graphics

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

Dans ce cas, nous dessinons une nouvelle image [PNG](https://wiki.fileformat.com/image/png/) sur la couche PSD existante, de sorte que les anciennes données seront perdues dans le nouveau fichier.

Mais que faire si nous devons également mettre à jour le texte ? Le processus sera similaire. Trouvez le [calque de texte](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) par son nom, puis mettez à jour de manière programmatique [le calque de texte du fichier Photoshop](/psd/fr/net/render-text-with-different-colors-in-text-layer/) avec C#.

Comment mettre à jour le calque de texte dans Photoshop en utilisant C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}

Enfin, nous devons enregistrer nos modifications :

Comment enregistrer le fichier PSD modifié en utilisant [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}

L'image résultante :

![à faire:texte_alt_image](using-psd-files-as-templates-for-automation-business-cards-case_3.png)

## **Cas complexe avec fonctionnalités supplémentaires**
Ci-dessus, nous avons montré la manière la plus simple de remplacer une image dans une couche d'un fichier PSD.

Mais Aspose.PSD peut offrir des fonctionnalités supplémentaires plus complexes comme l'ajout d'une nouvelle couche, la suppression d'anciennes couches et la mise à jour du calque texte en utilisant différents styles dans un texte multi-lignes.

Nous pouvons trouver la [couche ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) que nous voulons remplacer, puis nous trouvons son index dans la liste des couches, le supprimons et insérons une nouvelle couche après l'avoir créée à partir d'un [fichier Jpeg](https://wiki.fileformat.com/image/jpeg/) au même endroit.

Créer une nouvelle couche à partir du fichier et l'insérer dans l'image PSD en utilisant [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}

À la fin de ce fragment de code, nous corrigeons la position de la couche et enregistrons le nouvel ensemble de couches dans l'image Psd.

Comment copier les propriétés de la couche de [PsdImage ](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}

Et enfin, nous devons mettre à jour les calques de texte dans l'image PSD existante avec C#. Aspose.PSD prend en charge la [mise à jour du TextLayer par Portions](/psd/fr/net/working-with-text-layers/). Chaque [portion de texte](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) a une combinaison unique de propriétés de style et de paragraphe.

Comment copier les propriétés de la couche de PsdImage

{{< gist "aspose-com-gists" "8a4d34ce856d64fc7c0ce94" "Documentation-CSharp-Aspose-PsdFileAsTemplate-Snippet-8.cs" >}}

En conclusion, nous avons modifié le modèle PSD via du code en ajoutant une nouvelle couche à partir d'un fichier Jpeg, Png, J2k, Bmp, Gif ou Tiff et un texte multi-ligne avec [différents styles](https://ist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) dans chaque ligne.

![à faire:texte_alt_image](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
