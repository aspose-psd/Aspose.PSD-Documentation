---
title: Manipulation d'images TIFF
type: docs
weight: 50
url: /fr/net/manipulation-images-tiff/
---

## **Ajouter des cadres avec des paramètres différents**
TIFF est un format très flexible qui permet d'ajouter des cadres différents, avec différentes dimensions, compressions et autres paramètres. Les API Aspose.PSD vous permettent d'ajouter n'importe quel cadre TIFF de n'importe quelle taille, ce qui facilite la création de documents complexes. Si vous avez besoin d'ajuster les cadres lors du processus d'ajout pour les rendre tous égaux, suivez les étapes suivantes :

- Créez un nouveau cadre vierge avec les options désirées ou copiez le cadre source avec les options de sortie spécifiées en utilisant la méthode CreateFrameFrom.
- Redimensionnez le cadre/image source aux dimensions désirées en utilisant la méthode Resize.
- Ajoutez les pixels du cadre/image source au nouveau cadre.
- Ajoutez le nouveau cadre à l'image TIFF de sortie.

## **Exporter des calques d'une image PSD au format de fichier Tiff multi-pages**
Parfois, vous avez besoin d'exporter les calques d'une image PSD au format de fichier TIFF multi-pages. Cet article va démontrer comment réaliser cette tâche en utilisant l'API Aspose.PSD pour .NET. Tout d'abord, nous chargerons l'image PSD depuis le disque. Ensuite, nous itérerons sur les calques de l'image PSD et créerons un TiffFrame à partir des calques correspondants. Enfin, nous enregistrerons l'image Tiff résultante dans un fichier unique sur le disque.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModificationEtConversionImages-TIFF-ExporterVersTiffMultiPages-ExporterVersTiffMultiPages.cs" >}}

## **Configuration des options TiffOptions**
Les développeurs peuvent ajuster différentes propriétés de la classe [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) pour obtenir les résultats souhaités. Dans ce document, nous nous concentrerons sur 4 propriétés principales qui contrôlent les attributs de l'image résultante.

Ces propriétés sont énumérées ci-dessous.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Lorsque nous initialisons une structure TiffOptions vide, chaque option est définie sur sa valeur par défaut, par exemple la compression est définie sur Aucune, BitsPerSample est défini sur 1 et Photometric sur MinIsWhite. Enregistrer dans ce format rendra l'image finale en noir et blanc, ce qui est un comportement attendu pour cette combinaison d'options. Pour obtenir des résultats en couleur, vous devez définir toutes les propriétés mentionnées ci-dessus sur des valeurs correspondant à l'espace couleur souhaité ou vous pouvez initialiser la structure TiffOptions avec des paramètres prédéfinis comme discuté plus loin dans cet article. Ci-dessous est présentée une table décrivant les valeurs de paramètres attendues que vous pouvez définir pour obtenir les résultats souhaités. Veuillez noter que vous devez définir les 4 colonnes à travers TiffOptions pour enregistrer n'importe quelle image chargée/créée au format TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Non compressé|1/4/8/16 (palette, mode couleur) un seul canal|Aucun|
|MinIsWhite/MinIsBlack|LZW/Non compressé|1/4/8/16 (mode échelle de gris) un seul canal|Aucun|
|Palette|LZW/Non compressé|8 (palette, mode couleur) un seul canal|Horizontal (plus de compression obtenue pour LZW avec les mêmes motifs)|
|MinIsWhite/MinIsBlack|LZW/Non compressé|8 (mode échelle de gris) un seul canal|Horizontal (plus de compression obtenue pour LZW avec les mêmes motifs)|
|RVB|LZW/Non compressé|[8,8,8] (3 canaux RVB)|Aucun/Horizontal|
|RVB|LZW/Non compressé|[8,8,8,8] (3 canaux RVB et canal alpha supplémentaire pouvant être défini via TiffOptions.AlphaStorage) En fait, n'importe quel nombre de canaux supplémentaires est pris en charge mais chaque canal doit avoir une taille de 8 bits comme [8,8,8,8,8,8]|Aucun/Horizontal|
Toutes les 4 propriétés doivent être définies grâce à TiffOptions pour enregistrer n'importe quel format d'image au format Tiff. Lors de l'utilisation de différentes combinaisons, certains visualiseurs (y compris le Visualiseur de photos de Windows) peuvent refuser d'afficher l'image résultante en raison du support limité qu'ils offrent. Dans ce cas, veuillez choisir un visualiseur différent pour vos tests.
### **Paramètres prédéfinis pour la classe TiffOptions**
Pour faciliter les utilisateurs et éviter la mauvaise configuration de l'instance TiffOptions, l'API Aspose.PSD pour .NET a exposé un autre constructeur qui accepte un paramètre de type [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). En fonction de la valeur sélectionnée de l'énumération TiffExpectedFormat, l'API configure automatiquement toutes les propriétés obligatoires pour l'instance de TiffOptions afin de produire les résultats souhaités. Avant de passer au code d'exemple, voici la liste des champs de TiffExpectedFormat et leurs détails pour mieux comprendre leur utilisation.


- TiffExpectedFormat.Default: Définir le champ sur Default agit de manière similaire au constructeur par défaut de la classe TiffOptions sans compression définie et BitsPerPixel positionné sur 1 afin de produire un résultat en noir et blanc. Il est conseillé d'utiliser ce champ lorsque d'autres propriétés spécifiques au format doivent être définies manuellement selon les résultats souhaités.
- TiffExpectedFormat.TiffCcitRle: Spécifique à l'encodage RLE lors de l'enregistrement du résultat au format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffCcittFax3: Spécifique à l'encodage CCITT Fax3 lors de l'enregistrement du résultat au format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffCcittFax4: Spécifique à l'encodage CCITT Fax4 lors de l'enregistrement du résultat au format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffDeflateBW: Spécifique à la compression Deflate lors de l'enregistrement du résultat au format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffDeflateRGB: Spécifique à la compression Deflate lors de l'enregistrement du résultat au format TIFF RVB (couleur).
- TiffExpectedFormat.TiffJpegRGB: Spécifique à la compression Jpeg lors de l'enregistrement du résultat au format TIFF RVB (couleur).
- TiffExpectedFormat.TiffJpegYCBCR: Spécifique à la compression Deflate lors de l'enregistrement du résultat au format TIFF YCBCR (couleur).
- TiffExpectedFormat.TiffLzwBW: Spécifique à la compression LZW lors de l'enregistrement du résultat au format TIFF 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffLzwRGB: Spécifique à la compression LZW lors de l'enregistrement du résultat au format TIFF RVB (couleur).
- TiffExpectedFormat.TiffLzwRGBA: Spécifique à la compression LZW lors de l'enregistrement du résultat au format TIFF RGBA (couleur avec transparence).
- TiffExpectedFormat.TiffNoCompressionBW: Spécifique au format TIFF non compressé lors de l'enregistrement du résultat en 1 BitsPerPixel (noir et blanc).
- TiffExpectedFormat.TiffNoCompressionRGB: Spécifique au format TIFF non compressé lors de l'enregistrement du résultat en RVB (couleur).
- TiffExpectedFormat.TiffNoCompressionRGBA: Spécifique au format TIFF non compressé lors de l'enregistrement du résultat en RGBA (couleur avec transparence).

Le code suivant illustre l'utilisation des champs TiffExpectedFormat lors de la création d'une instance de la classe TiffOptions.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModificationEtConversionImages-TIFF-ConfigurationTiffOptions-TiffOptionsConfiguration.cs" >}}

## **Prise en charge de la compression Deflate et Adobe Deflate**
Le format de fichier TIFF (Tagged Image File Format) prend en charge divers types de compression, le type de compression étant stocké sous forme de tag (une valeur entière) dans le fichier. L'un de ces méthodes de compression est Adobe Deflate (anciennement connu sous le nom de Deflate). L'API Aspose.PSD pour .NET prend en charge cette méthode de compression pour l'exportation et la création d'images TIFF.
### **Enregistrement de l'image au format TIFF avec compression Deflate**
Convertir les images chargées en TIFF avec la compression Deflate/Adobe Deflate est facile comme suit.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModificationEtConversionImages-TIFF-TIFFavecCompressionDeflate-TIFFavecCompressionDeflate.cs" >}}
### **Création d'une image Tiff avec la compression Adobe Deflate**
L'exemple fourni ci-dessous illustre l'utilisation de l'API Aspose.PSD pour .NET pour créer une image à partir de zéro en utilisant la méthode de compression Adobe Deflate.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModificationEtConversionImages-TIFF-TIFFavecCompressionAdobeDeflate-TIFFavecCompressionAdobeDeflate.cs" >}}
### **Compression d'images TIFF**
L'API Aspose.PSD pour .NET peut être utilisée pour convertir des images PSD au format d'image TIFF et même changer la compression de l'image TIFF résultante. L'API peut également être utilisée pour stocker différentes images sous forme de cadres dans une image TIFF à des fins d'archivage tout en compressant les images pour obtenir la plus petite taille de données. La compression de l'image doit être effectuée en réduisant la taille des données source indépendamment de l'algorithme de compression utilisé. Afin d'obtenir le meilleur taux de compression, nous pouvons utiliser des espaces de couleurs indexés. Le code fourni ci-dessous réalise la meilleure compression en utilisant seulement 16 couleurs indexées et l'algorithme de compression LZW, cependant les couleurs sources sont légèrement truquées.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModificationEtConversionImages-TIFF-CompressionTiff-CompressionTiff.cs" >}}
