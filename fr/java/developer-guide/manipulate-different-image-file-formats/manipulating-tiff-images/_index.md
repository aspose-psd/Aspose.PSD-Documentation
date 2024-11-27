---
title: Manipulation d'images TIFF
type: docs
weight: 40
url: /fr/java/manipulation-dimages-tiff/
---

## **Ajouter des cadres avec différents paramètres**
TIFF est un format très flexible qui permet d'ajouter différents cadres avec différentes dimensions, compressions et autres paramètres. Les APIs Aspose.PSD vous permettent d'ajouter n'importe quel cadre TIFF de n'importe quelle taille, ce qui facilite la création de documents complexes. Si vous devez ajuster les cadres lors du processus d'ajout pour les rendre tous égaux, suivez les étapes suivantes :
- Créez un nouveau cadre vide avec les options souhaitées ou copiez le cadre source avec les options de sortie spécifiées en utilisant la méthode CreateFrameFrom.
- Redimensionnez le cadre/image source aux dimensions souhaitées en utilisant la méthode Resize.
- Ajoutez les pixels du cadre/image source au nouveau cadre.
- Ajoutez le nouveau cadre à l'image TIFF de sortie.

## **Exporter des calques d'image PSD au format fichier TIFF multipage**
Parfois, vous devez exporter les calques d'image PSD vers le format de fichier TIFF multipage. Cet article démontrera comment nous pouvons accomplir cette tâche en utilisant l'API Aspose.PSD pour Java. Tout d'abord, nous chargerons l'image PSD à partir du disque. Ensuite, nous itérerons sur les calques d'image PSD et créerons TiffFrame à partir des calques correspondants. Enfin, nous enregistrerons l'image TIFF résultante dans un seul fichier sur le disque.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}

## **Configuration des options TIFF**
Les développeurs peuvent ajuster différentes propriétés de la classe TiffOptions pour obtenir les résultats souhaités. Dans ce document, nous nous concentrerons sur 4 propriétés principales qui contrôlent les attributs de l'image résultante.

Ces propriétés sont listées ci-dessous.
1. ` `TiffOptions.Photometrique
1. Compression TiffOptions
1. Bits par échantillon de TiffOptions
1. Prédicteur de TiffOptions

Lorsque nous initialisons une structure TiffOptions vide, chaque option est définie sur sa valeur par défaut, par exemple, la compression est définie sur Aucun, BitsParEchantillon est défini à 1 et Photometrique sur MinIsWhite. Enregistrer dans ce format rendra l'image finale en noir et blanc et c'est le comportement attendu pour cette combinaison d'options. Pour obtenir des résultats en couleur, vous devez définir toutes les propriétés mentionnées ci-dessus sur des valeurs correspondant à l'espace couleur souhaité ou vous pouvez initialiser la structure TiffOptions avec des paramètres prédéfinis comme discuté plus loin dans cet article. Ci-dessous, un tableau décrivant les valeurs de paramètre attendues que vous pouvez définir pour obtenir les résultats souhaités. Veuillez noter que vous devez définir les 4 colonnes à travers TiffOptions afin de sauvegarder toute image chargée/créée au format de fichier TIFF.

|` `**Photometrique de TiffOptions**|Compression TiffOptions|Bits par échantillon de TiffOptions|Prédicteur de TiffOptions|
| :- | :- | :- | :- |
|Palette|LZW/Non compressé|1/4/8/16 (palette, mode couleur) un seul canal seulement|Aucun|
|MinIsWhite/MinIsBlack|LZW/Non compressé|1/4/8/16 (mode niveaux de gris) un seul canal seulement|Aucun|
|Palette|LZW/Non compressé|8 (palette, mode couleur) un seul canal seulement|Horizontal (compression accrue pour LZW mêmes motifs)|
|MinIsWhite/MinIsBlack|LZW/Non compressé|8 (mode niveaux de gris) un seul canal seulement|Horizontal (compression accrue pour LZW mêmes motifs)|
|RVB|LZW/Non compressé|[8,8,8] (3 canaux RVB)|Aucun/Horizontal|
|RVB|LZW/Non compressé|[8,8,8,8] (3 canaux RVB et canal alpha supplémentaire peut être défini via TiffOptions.AlphaStorage) En fait, tout nombre de canaux supplémentaires est pris en charge mais chaque canal doit avoir une taille de 8 bits comme [8,8,8,8,8,8]|Aucun/Horizontal|
Toutes les 4 propriétés doivent être définies via TiffOptions pour sauvegarder n'importe quel format d'image au format Tiff. En utilisant différentes combinaisons, certains visualiseurs (y compris le Visualiseur de photos Windows) peuvent refuser de rendre l'image résultante en raison du support limité qu'ils offrent. Dans ce cas, veuillez choisir un visualiseur différent pour votre test.

### **Paramètres prédéfinis pour la classe TiffOptions**
Afin de faciliter les utilisateurs et d'éviter la mauvaise configuration de l'instance TiffOptions, l'API Aspose.PSD pour Java a exposé un autre constructeur qui accepte un paramètre de type TiffExpectedFormat. Selon la valeur sélectionnée dans l'énumération TiffExpectedFormat, l'API configure automatiquement toutes les propriétés obligatoires pour l'instance TiffOptions afin de produire les résultats souhaités. Avant de passer au code d'exemple, voici la liste des champs de TiffExpectedFormat et leurs détails pour une meilleure compréhension de l'utilisation.

- TiffExpectedFormat.Default : Définir le champ sur Default agit de manière similaire au constructeur par défaut de la classe TiffOptions avec aucune compression définie et BitsPerPixel défini à 1 pour produire un résultat en noir et blanc. Il est conseillé d'utiliser ce champ lorsque d'autres propriétés spécifiques au format doivent être définies manuellement selon les résultats souhaités.
- TiffExpectedFormat.TiffCcitRle : Spécifique à l'encodage RLE lors de l'enregistrement du résultat dans le format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffCcittFax3 : Spécifique à l'encodage CCITT Fax3 lors de l'enregistrement du résultat dans le format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffCcittFax4 : Spécifique à l'encodage CCITT Fax4 lors de l'enregistrement du résultat dans le format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffDeflateBW : Spécifique à la compression Deflate lors de l'enregistrement du résultat dans le format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffDeflateRGB : Spécifique à la compression Deflate lors de l'enregistrement du résultat dans le format TIFF RVB (couleur).
- TiffExpectedFormat.TiffJpegRGB : Spécifique à la compression Jpeg lors de l'enregistrement du résultat dans le format TIFF RVB (couleur).
- TiffExpectedFormat.TiffJpegYCBCR : Spécifique à la compression Jpeg lors de l'enregistrement du résultat dans le format TIFF YCBCR (couleur).
- TiffExpectedFormat.TiffLzwBW : Spécifique à la compression LZW lors de l'enregistrement du résultat dans le format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffLzwRGB : Spécifique à la compression LZW lors de l'enregistrement du résultat dans le format TIFF RVB (couleur).
- TiffExpectedFormat.TiffLzwRGBA : Spécifique à la compression LZW lors de l'enregistrement du résultat dans le format TIFF RGBA (couleur avec transparence).
- TiffExpectedFormat.TiffNoCompressionBW : Spécifique au format TIFF non compressé lors de l'enregistrement du résultat en 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffNoCompressionRGB : Spécifique au format TIFF non compressé lors de l'enregistrement du résultat en RVB (couleur).
- TiffExpectedFormat.TiffNoCompressionRGBA : Spécifique au format TIFF non compressé lors de l'enregistrement du résultat en RGBA (couleur avec transparence).

Le snippet de code suivant illustre l'utilisation des champs TiffExpectedFormat lors de la création d'une instance de la classe TiffOptions.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}

## **Prise en charge de la compression Deflate et Adobe Deflate**
Le format de fichier TIFF (Tagged Image File Format) prend en charge différents types de compression, la méthode de compression étant stockée sous forme de tag (une valeur entière) dans le fichier. L'une de ces méthodes de compression est Adobe Deflate (précédemment connue sous le nom de Deflate). L'API Aspose.PSD pour Java prend en charge cette méthode de compression pour l'exportation et la création d'images TIFF.

### **Enregistrement d'une image en TIFF avec compression Deflate**
Convertir les images chargées en TIFF avec compression Deflate/Adobe Deflate est simple comme suit.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}

### **Création d'une image TIFF avec compression Adobe Deflate**
L'exemple fourni ci-dessous illustre l'utilisation de l'API Aspose.PSD pour Java pour créer une image à partir de zéro en utilisant la méthode de compression Adobe Deflate.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}

### **Compression d'images TIFF**
L'API Aspose.PSD pour Java peut être utilisée pour convertir des images PSD au format d'image TIFF et même changer la compression de l'image TIFF résultante. L'API peut également être utilisée pour stocker différentes images en tant que cadres dans une image TIFF à des fins d'archivage tout en compressant les images à la plus petite taille de données. La compression de l'image doit être effectuée en réduisant la taille des données source indépendamment de l'algorithme de compression utilisé. Pour obtenir le meilleur taux de compression, nous pouvons utiliser des espaces de couleur indexés. Le snippet de code fourni ci-dessous effectue la meilleure compression en utilisant seulement 16 couleurs indexées et l'algorithme de compression LZW, cependant, les couleurs sources sont légèrement broyées.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
