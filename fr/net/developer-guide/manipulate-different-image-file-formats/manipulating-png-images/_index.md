---
title: Manipulation d'images PNG
type: docs
weight: 40
url: /fr/net/manipulation-images-png/
---

## **Spécification de la transparence pour les images PNG**
L'un des avantages de l'enregistrement des images au format PNG est que le PNG peut avoir un arrière-plan transparent. Aspose.PSD pour .NET propose la fonctionnalité de spécifier la transparence pour les images PNG et les images raster, comme illustré dans la section ci-dessous. L'API Aspose.PSD pour .NET peut être utilisée pour définir n'importe quelle couleur comme transparente lors de la création de nouvelles images PNG ou de la conversion d'images existantes au format PNG. À cet effet, l'API Aspose.PSD pour .NET a exposé la propriété [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) et l'énumération [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) qui peuvent être définies pour spécifier une couleur à rendre transparente dans l'image PNG. Le snippet de code ci-dessous montre comment convertir une image PSD existante en image PNG en spécifiant la couleur souhaitée comme transparente.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifierEtConvertirImages-PNG-SpécifierTransparence-SpécifierTransparence.cs" >}}
## **Définition de la résolution pour les images PNG**
Aspose.PSD pour .NET expose la classe ResolutionSetting qui peut être utilisée pour définir la résolution pour tous les formats d'image, y compris le PNG. Cet article démontre l'utilisation de l'API Aspose.PSD pour .NET pour définir les paramètres de résolution horizontale et verticale pour le format d'image PNG. Le snippet de code ci-dessous charge une image PSD existante, la convertit au format PNG et modifie également la résolution.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifierEtConvertirImages-PNG-DéfinirRésolution-DéfinirRésolution.cs" >}}
## **Compression des fichiers PNG**
Le format Portable Network Graphic (PNG) est un format de compression sans perte pour transmettre une image bitmap sur des réseaux. Lorsque vous enregistrez une image au format PNG dans un programme, on peut vous demander de choisir un niveau de compression dans une plage de 0 à un niveau maximal. La définition de cette valeur compresse effectivement la taille du fichier et ne diminue pas la qualité de l'image. Cet article décrit comment les API Aspose.PSD vous permettent de contrôler la taille des fichiers PNG. Les API Aspose.PSD peuvent être utilisées pour définir les niveaux de compression pour le format de fichier PNG en utilisant la classe PngOptions qui possède une propriété int [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel). Cette propriété accepte une valeur de 0 à 9 où 9 représente la compression maximale. Le snippet de code fourni ci-dessous montre comment définir les niveaux de compression en utilisant l'API Aspose.PSD pour .NET.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifierEtConvertirImages-PNG-CompressionFichiers-CompressionFichiers.cs" >}}
## **Spécification de la profondeur de bits pour les images PNG**
La profondeur de bits en imagerie est le nombre de bits utilisés pour indiquer la couleur d'un seul pixel dans une image bitmap. Comme tous les autres formats bitmap, la profondeur de couleur PNG est également représentée en bits tels que 1-bit (2 couleurs), 2-bit (4 couleurs), 4-bit (16 couleurs) et 8-bit (256 couleurs). L'API Aspose.PSD pour .NET peut être utilisée pour définir la profondeur de bits pour les images PNG en utilisant la propriété [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) exposée par la classe PngOptions. Actuellement, la propriété BitDepth peut être définie à 1, 2, 4 ou 8 bits pour les types de couleurs en niveaux de gris et à index. Pour tous les autres types de couleurs, seuls 8 bits sont supportés. Le snippet de code fourni ci-dessous montre comment définir la profondeur de bits pour une image PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifierEtConvertirImages-PNG-SpécifierProfondeurBits-SpécifierProfondeurBits.cs" >}}
## **Application de méthodes de filtrage sur les images PNG**
La profondeur de bits en imagerie est le nombre de bits utilisés pour indiquer la couleur d'un seul pixel dans une image bitmap. Comme tous les autres formats bitmap, la profondeur de couleur PNG est également représentée en bits tels que 1-bit (2 couleurs), 2-bit (4 couleurs), 4-bit (16 couleurs) et 8-bit (256 couleurs). L'API Aspose.PSD pour .NET peut être utilisée pour définir la profondeur de bits pour les images PNG en utilisant la propriété BitDepth exposée par la classe PngOptions. Actuellement, la propriété BitDepth peut être définie à 1, 2, 4 ou 8 bits pour les types de couleur en niveaux de gris et à index. Pour tous les autres types de couleur, seuls 8 bits sont supportés. Le snippet de code fourni ci-dessous montre comment définir la profondeur de bits pour une image PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifierEtConvertirImages-PNG-ApplicationMéthodeFiltre-ApplicationMéthodeFiltre.cs" >}}
## **Changement de la couleur d'arrière-plan d'une image PNG transparente**
Les images au format PNG peuvent avoir un arrière-plan transparent. Aspose.PSD pour .NET permet de changer la couleur d'arrière-plan d'une image PNG possédant un arrière-plan transparent. L'API Aspose.PSD pour .NET peut être utilisée pour définir/changer la couleur d'une image PNG transparente. Le snippet de code fourni ci-dessous montre comment définir/changer la couleur d'arrière-plan d'une image PNG transparente.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModifierEtConvertirImages-PNG-ChangerCouleurArrièrePlan-ChangerCouleurArrièrePlan.cs" >}}
