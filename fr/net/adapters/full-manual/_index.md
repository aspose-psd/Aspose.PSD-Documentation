---
title: Manuel complet des adaptateurs Aspose.PSD pour .NET
type: docs
weight: 10
url: /fr/net/adapters/full-manual
keywords: Adapters Manuel complet PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP guide de démarrage rapide
description: Manuel complet des adaptateurs Aspose.PSD.
---

## Aperçu

Il s'agit d'un manuel complet sur la façon de travailler avec les adaptateurs Aspose.PSD pour élargir les fonctionnalités d'Aspose.PSD.
Les adaptateurs sont des packages NuGet spéciaux qui permettent une intégration transparente d'Aspose.PSD avec d'autres produits Aspose, vous permettant d'exporter vos fichiers vers divers formats non pris en charge sans effort supplémentaire d'écriture de code d'intégration.

## Application des licences

Veuillez consulter l'[article complet sur l'application des licences](/psd/fr/net/adapters/license) pour les adaptateurs.

{{% alert color="primary" %}}
Veuillez noter que pour utiliser les adaptateurs, vous avez besoin des licences d'Aspose.PSD et des adaptés.
{{% /alert %}}

La licence peut être appliquée en utilisant cet exemple :
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-License.cs" >}}

Il est préférable d'appliquer la licence une fois dans le module d'initialisation de votre projet.

## Référence des adaptateurs Aspose.PSD

Tout d'abord, vous devez faire référence à Aspose.PSD.Adapters.Imaging depuis [Nuget](https://www.nuget.org/aspose.psd.adapters.imaging) ou les télécharger depuis [la page de publication d'Aspose](https://releases.aspose.com/psd/net/) (les adaptateurs sont inclus dans l'artefact de publication principal pour le moment en tant que binaire séparé) pour votre projet.

![Références nécessaires](references.png)

Il est possible que vous deviez également faire référence à d'autres packages supplémentaires.

## Activation des chargeurs et exportateurs des adaptés

### Activation des adaptateurs
Lorsque vous avez besoin d'utiliser des adaptateurs, utilisez simplement le code suivant :
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Enable-Adapters.cs" >}}


### Désactivation des adaptateurs
Dans le processus de développement, vous pouvez être confronté à la situation où les adaptateurs doivent être désactivés. C'est courant si vous avez besoin, dans une partie du code, d'utiliser les chargeurs d'Aspose.PSD et d'utiliser les chargeurs des adaptés dans une autre partie. Dans ce cas, utilisez simplement le code suivant :
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Disable-Adapters.cs " >}}

## Chargement des images en utilisant des adaptateurs

En utilisant des adaptateurs, vous pouvez [charger des formats populaires non pris en charge par Aspose.PSD](/fr/net/adapters/load-unsupported-formats) comme SVG ou WebP.

### Utilisation simple
Utilisez simplement le code suivant pour le chargement :
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Loading-Unsupported-Formats.cs" >}}

### Utilisation avancée pour le traitement d'images complexe
Si vous devez spécifier des options supplémentaires fournies par l'adapté, veuillez consulter l'exemple suivant :
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-Full-Manual-Complex-Loading.cs" >}}

Vous pouvez travailler avec une image SVG en utilisant toutes les fonctionnalités d'Imaging, puis l'exporter avec un seul appel de méthode.

## Exportation des images en utilisant des adaptateurs

Il y a de nombreuses situations où vous n'avez pas besoin d'[ouvrir un format non pris en charge](/fr/net/adapters/load-unsupported-formats), mais d'[exporter vers celui-ci](/fr/net/adapters/export-to-unsupported-formats). Dans ces cas, vous devez activer les exportateurs et utiliser le code suivant :
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Exporting-to-Unsupported-Formats.cs" >}}

## Conclusion

L'utilisation des adaptateurs Aspose.PSD pour le chargement et l'exportation de fichiers est un véritable atout pour les développeurs. Ces puissants packages NuGet permettent une intégration transparente d'Aspose.PSD avec d'autres produits Aspose, simplifiant plus que jamais l'ouverture et le travail avec des formats de fichiers non pris en charge sans avoir à écrire de code d'intégration supplémentaire. Avec les adaptateurs Aspose.PSD, vous pouvez gagner du temps et des efforts en éliminant le besoin de code supplémentaire et de processus de conversion manuelle. Que vous chargiez ou exportiez des fichiers, les adaptateurs Aspose.PSD offrent une solution pratique et efficace qui ouvre de nouvelles possibilités pour vos projets. Découvrez la puissance des adaptateurs Aspose.PSD et faites passer votre processus de développement au niveau supérieur.
