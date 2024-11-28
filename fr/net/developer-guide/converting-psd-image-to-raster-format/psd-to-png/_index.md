---
title: Convertir PSD en PNG en utilisant C#
linktitle: PSD en PNG
type: docs
weight: 30
url: /fr/net/psd-to-png/
description: L'API de manipulation C# .NET de Photoshop peut convertir du format PSD au format PNG avec le code fourni dans cet article.
---

Aspose.PSD est un SDK de format PSD et une API de manipulation de Photoshop en C# .NET, qui peut convertir du format PSD au format PNG.

Pour cette conversion de PSD, vous devez utiliser le code C# suivant :

Le code d'exemple fourni ci-dessous montre comment convertir un PSD en PNG :

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-ModificationEtConversionImages-PSD-ConvertPsdToPng-ConvertPsdToPng.cs" >}}

Vous pouvez spécifier le niveau de compression du format PNG de 0 à 9, où 9 représente la compression la plus élevée. Vous pouvez utiliser la compression progressive PNG et modifier le type de couleur du fichier PNG. Les [Options PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions) ont différentes propriétés pour chaque cas d'exportation PSD.

Il est judicieux d'utiliser un PNG semi-transparent avec un canal Alpha pour votre site ou travail. Un fichier Adobe Photoshop peut être exporté de manière pixel-parfait avec le [Mode Lecture Seule](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/readonlymode).

Voici un exemple d'un fichier PSD exporté avec le[ Masque Appliqué](https://docs.aspose.com/display/psdjava/Apply+Masking), [Calque de Texte](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer), et Calque de Remplissage Transparent [Couleur de Remplissage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.filllayers/filllayer) (Aspose.PSD prend en charge tous les types de [Calques de Remplissage Adobe Photoshop](https://docs.aspose.com/display/psdjava/Support+of+Fill+Layers)). De plus, vous pouvez voir l'[effet d'ombre](/fr/net/effets-d-ombre-dans-le-fichier-psd/) sur le Calque de Forme PSD.

![à faire:texte_alt_de_l_image](psd-to-png_1.png)
