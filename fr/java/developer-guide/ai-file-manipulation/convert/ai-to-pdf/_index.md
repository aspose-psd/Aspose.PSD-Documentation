---
title: Convertir AI en PDF
weight: 100
type: docs
description: Vérifiez comment Aspose.PSD pour Java peut manipuler la conversion d'images AI en PDF
keywords: [ai en png, format ai, fichiers illustrateur, convertir illustrateur, ai en pdf, ai en jpeg, ai en tiff, ai en psd, api psd, java, exemple de code]
url: fr/java/convert/ai-to-pdf
---

## **Aperçu**
Pour convertir des fichiers AI en format PDF en utilisant Aspose.PSD pour Java, vous pouvez suivre ces étapes :

- Installer Aspose.PSD pour Java : Commencez par télécharger et installer la bibliothèque Aspose.PSD pour Java. Vous pouvez l'inclure en tant que dépendance dans votre projet en l'ajoutant à votre configuration Maven ou Gradle ou en l'incluant manuellement dans le fichier JAR.

- Importer les modules nécessaires : Une fois que vous avez ajouté la bibliothèque Aspose.PSD à votre projet, importez les classes nécessaires dans votre code Java. Ces classes comprennent celles requises pour charger et manipuler les fichiers AI, ainsi que pour les exporter au format PDF.

- Charger et manipuler les fichiers AI : Utilisez les classes fournies par Aspose.PSD pour charger vos fichiers AI dans votre application Java. Vous pouvez utiliser la classe Image pour charger le fichier AI et manipuler son contenu selon vos besoins.

- Exporter AI en PDF : Après le chargement du fichier AI, créez une instance de la classe PsdOptions pour spécifier les paramètres de l'exportation PDF. Cela inclut des paramètres tels que la qualité de l'image, le niveau de compression, etc. Configurez ces options selon vos besoins.

- Enregistrer et utiliser le PDF : Une fois que vous avez configuré les options d'exportation, utilisez la méthode Image.Save pour enregistrer le fichier AI sous forme de PDF. Spécifiez le chemin du fichier souhaité où vous souhaitez enregistrer le fichier PDF résultant.

- Utiliser le fichier PDF : Après avoir enregistré le fichier PDF, vous pouvez l'utiliser à diverses fins, telles que le partage, l'affichage sur une page web ou un traitement ultérieur. Le fichier PDF résultant contiendra tout le contenu du fichier AI d'origine, converti au format PDF.

## **Résumé**
En résumé, en utilisant Aspose.PSD pour Java, vous pouvez convertir sans difficulté des fichiers AI en format PDF, permettant la compatibilité avec diverses applications et périphériques prenant en charge le PDF. Le processus de conversion implique le chargement du fichier AI, la configuration des options d'exportation en utilisant les [PdfOptions](https://reference.aspose.com/psd/java/com.aspose.psd.imageoptions/pdfoptions/), et l'enregistrement de la sortie en tant que fichier PDF en utilisant la méthode PsdImage.save. Avec Aspose.PSD pour Java, vous pouvez réaliser des conversions précises et fiables d'AI en PDF sans effort.

## **Exemple**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-Convert-Ai-To-Pdf.java" >}}
