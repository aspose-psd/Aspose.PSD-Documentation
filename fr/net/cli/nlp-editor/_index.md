---
title: Application Aspose.PSD CLI NLP pour .NET
type: docs
weight: 10
url: /fr/net/cli/editeur-nlp/
is_root: false
keywords: Outil CLI Photoshop NLP Traitement en langage naturel Fichiers PSD Console Bibliothèque C# API PSD
description: Application Aspose.PSD CLI NLP Editor basée sur NLP pour formats de fichier PSD, PSB et AI. Automatisation CI/CD sans code. Prend en charge le traitement en langage naturel pour l'édition de fichiers PSD. Il vous suffit d'écrire votre demande en langage naturel pour effectuer diverses opérations telles que la conversion, l'ajustement, le redimensionnement, et plus encore. Il n'est pas nécessaire d'installer Adobe Photoshop ou Adobe Illustrator et peut être exécuté depuis la console sans code supplémentaire.
---

**![Logo du produit Aspose.PSD pour .NET](home_1.png)**

**Bienvenue dans l'application Aspose.PSD NLP Editor CLI pour .NET**

L'application Aspose.PSD CLI NLP Editor est un utilitaire console léger pour éditer des fichiers PSD en utilisant des commandes en langage naturel. Intégration facile dans les pipelines CI/CD.

**Avis de non-responsabilité**

Il s'agit d'une application expérimentale. Veuillez l'essayer et laisser vos commentaires. Tout retour d'information est grandement apprécié. Nous souhaitons amener l'application sans code au niveau supérieur. Notre objectif est une intégration facile dans n'importe quel pipeline de construction ou processus métier.

**Fonctionnalités principales de l'application Aspose.PSD NLP Editor CLI pour .NET**

1. Effectuer des opérations sur les fichiers PSD, PSB, AI en utilisant des commandes en langage naturel.
2. Prend en charge diverses opérations comme la conversion, l'ajustement, le redimensionnement, et plus encore.
3. Automatisation CI/CD sans code.
4. Prend en charge l'écriture des demandes en langage naturel pour l'édition des fichiers PSD.

## **Utilisation en ligne de commande:**

{{% alert color="primary" %}}
Installez d'abord cet outil dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Nous recommandons de lancer la commande suivante avant la première utilisation :
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Après cette commande, vous pourrez exécuter cette application avec le nom court nlp.cli au lieu de Aspose.PSD.CLI.NLP.Editor. Vous pouvez spécifier votre propre nom court.
{{% /alert %}}

**Paramètres disponibles pour l'application Aspose.PSD.CLI.Crop**

| **Argument** | **Description**                         |
|:-------------|:----------------------------------------|
| tout texte   | Requis. Commande en langage naturel pour mettre à jour le fichier PSD ou PSB      |
| licence      | Chemin d'accès à la licence.                    |
| verbose      | Afficher plus d'informations sur une commande spécifique. |
| setup        | Crée un fichier bat dans le dossier des outils pour un appel rapide depuis la console. Exemple : --setup psd.nlp. Ensuite, vous pouvez appeler l'outil avec la commande psd.nlp |

**Exemples d'utilisation**

1. Cette commande convertira le premier fichier trouvé (qui peut être ouvert avec aspose.psd) du dossier actuel et l'enregistrera en format png avec transparence. De plus, la licence sera configurée. Vous devez spécifier la licence une seule fois. Les exécutions suivantes utiliseront la licence à partir du chemin spécifié. Cette commande affichera le journal verbose du traitement NLP s'il est disponible.
{{< highlight bash >}}
  nlp.cli Convertir le fichier de ce dossier en format png avec alpha --licence "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. Cette commande trouvera le fichier avec le nom le plus similaire à "smth.psd". Ensuite, elle ajustera le contraste et l'enregistrera en jpeg avec la meilleure qualité. Le nom du fichier de sortie sera affiché. Il sera smth.jpg.
{{< highlight bash >}}
Ajuster le contraste sur 10 de la couche avec le nom ellipse dans le fichier smth.psd et enregistrer le tout en output.jpg avec la meilleure qualité
{{< /highlight >}}

3. Cette commande windera le fichier sur le chemin spécifié, et réduira sa taille à 25%. Le fichier de sortie sera affiché. Il sera enregistré dans le dossier actuel de la console.
{{< highlight bash >}}
Redimensionner le fichier C:\Users\someuser\Desktop\input.psd à 25%
{{< /highlight >}}

4. Cette commande trouvera le fichier input.psd dans C:\Users\someuser\Desktop\. Puis elle trouvera la couche avec l'index 3 et la redimensionnera à une largeur de 50px et une hauteur de 100px. Ensuite, cette couche sera enregistrée en PDF dans C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
 Redimensionner la couche avec l'index 3 de C:\Users\someuser\Desktop\input.psd à une largeur de 50 et une hauteur de 100 et l'enregistrer dans C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. Cette commande ouvrira smth.psd dans le dossier actuel, mais tous les effets seront désactivés. Ensuite, ce fichier sera converti au format BMP et enregistré en output.bmp dans le dossier actuel.
 {{< highlight bash >}}
 Ouvrir smth.psd sans effets et l'enregistrer en output.bmp
  {{< /highlight >}}

**Veuillez consulter d'autres [Applications CLI Aspose.PSD](https://docs.aspose.com/psd/net/cli) pour .NET si vous avez besoin de prendre en charge les formats PSD, PSB et AI dans votre flux de travail**

1. [Aspose.PSD CLI Convertir](/psd/fr/fr/net/cli/convertir)
2. [Aspose.PSD CLI Recadrer](/psd/fr/fr/net/cli/recadrer)
3. [Aspose.PSD CLI Redimensionner](/psd/fr/fr/net/cli/redimensionner)
4. [Aspose.PSD CLI Exporter](/psd/fr/fr/net/cli/exporter)
5. [Aspose.PSD CLI Editeur NLP](/psd/fr/fr/net/cli/editeur-nlp)

**Vérifiez également Aspose.PSD pour .NET ou [d'autres plates-formes]**

Les applications CLI Aspose.PSD sont une solution prête à l'emploi pour les opérations populaires. Si vous avez besoin d'une solution flexible, veuillez consulter la version complète de Aspose.PSD

1. [Aspose.PSD pour .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD pour Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD pour Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Ressources Aspose.PSD pour .NET**

Voici les liens vers certaines ressources utiles dont vous pourriez avoir besoin pour accomplir vos tâches.

- [Documentation en ligne des Applications CLI Aspose.PSD pour .NET](/psd/fr/fr/net/cli/conversion)
- [Notes de version Aspose.PSD pour Applications CLI pour .NET](/psd/fr/fr/net/cli/conversion/notes-de-version/)
- [Page Produit d'Aspose.PSD pour Applications CLI .NET](https://products.aspose.com/psd/net/cli)
- [Guide de référence API Aspose.PSD pour .NET](https://reference.aspose.com/net/psd)
- [Téléchargez des exemples sur le dépôt GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Forum d'assistance gratuit Aspose.PSD pour .NET](https://forum.aspose.com/c/psd)
- [Service d'assistance payant Aspose.PSD pour .NET Helpdesk](https://helpdesk.aspose.com/)

