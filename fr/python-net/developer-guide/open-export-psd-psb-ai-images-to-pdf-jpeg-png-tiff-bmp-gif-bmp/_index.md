---
title: Ouvrir des fichiers PSD, PSB et AI et les exporter en PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Exemple d'exportation de fichiers PSD, PSB et AI vers d'autres formats
keywords: [ouvrir psd, ouvrir ai, ouvrir psb, exporter en png, exporter en pdf, exporter en jpeg, exporter en tiff, api psd, python, exemple de code]
url: fr/python-net/ouvrir-exporter-images-psd-psb-ai-en-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Aperçu**
Pour convertir des fichiers PSD, PSB et AI en différents formats, vous pouvez utiliser la bibliothèque Aspose.PSD en Python. Cette bibliothèque offre diverses options et paramètres pour personnaliser le processus de conversion.

Tout d'abord, vous devez importer les classes et modules nécessaires de la bibliothèque Aspose.PSD. Assurez-vous d'avoir installé la bibliothèque avant d'exécuter le code.

Dans ce code, nous définissons diverses options pour différents formats, tels que PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB et PSD. Ces options vous permettent de personnaliser le fichier de sortie selon vos besoins.

Ensuite, nous définissons un dictionnaire de formats qui associe les extensions de fichiers à leurs options de sauvegarde respectives.

Pour convertir un fichier PSD en d'autres formats, vous devez charger le fichier PSD en utilisant PsdImage.load() puis itérer à travers le dictionnaire des formats. Pour chaque format, spécifiez le nom du fichier de sortie et enregistrez l'image en utilisant la méthode image.save().

De même, pour convertir un fichier AI en d'autres formats, chargez le fichier AI en utilisant AiImage.load() et itérez à travers le dictionnaire de formats. Spécifiez le nom du fichier de sortie et enregistrez l'image en utilisant la méthode image.save().

Assurez-vous de fournir les bons chemins de fichiers pour les fichiers PSD et AI sources.

C'est tout! Vous pouvez maintenant utiliser ce code pour convertir des fichiers PSD, PSB et AI en différents formats en utilisant Aspose.PSD pour Python.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
