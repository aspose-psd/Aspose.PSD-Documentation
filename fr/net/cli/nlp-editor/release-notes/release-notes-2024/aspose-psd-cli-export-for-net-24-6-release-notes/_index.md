---
title: Aspose.PSD CLI Editeur NLP pour .NET 24.6 - Notes de version
type: docs
weight: 90
url: /fr/net/cli/editeur-nlp/aspose-psd-editeur-nlp-cli-pour-net-24-6-notes-de-version/
---
{{% alert color="primary" %}}

Cette page contient les notes de version de [Aspose.PSD CLI Editeur NLP pour .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                      | **Catégorie** |
|:-------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110  | Première version des applications Aspose.PSD CLI : Aspose.PSD.CLI.Export et Aspose.PSD.CLI.NLP.Editeur |  Amélioration |


## **Exemples d'utilisation:**

**PSDNET-2110. Première version de l'application Aspose.PSD CLI Editeur NLP**

## **Utilisation en ligne de commande:**

{{% alert color="primary" %}}
Commencez par installer cet outil dotnet :
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Nous recommandons de lancer la commande suivante avant la première utilisation :
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Après cette commande, vous pourrez exécuter cette application avec le nom court nlp.cli au lieu de Aspose.PSD.CLI.NLP.Editeur. Vous pouvez spécifier votre propre nom court.
{{% /alert %}}

**Exemples d'utilisation**

1. Cette commande convertira le premier fichier trouvé (pouvant être ouvert avec aspose.psd) du dossier actuel et le sauvegardera au format PNG avec transparence. De plus, la licence sera configurée. Vous devez spécifier la licence une seule fois. Les exécutions suivantes utiliseront la licence du chemin spécifié. Cette commande affichera le journal verbose du traitement NLP s'il est disponible.
{{< highlight bash >}}nlp.cli Convertir fichier de ce dossier en format png avec alpha --licence "C:\Aspose\FichierLicence.lic --verbose "{{< /highlight >}}

2. Cette commande trouvera le fichier ayant le nom le plus similaire à "smth.psd". Ensuite, elle ajustera le contraste et le sauvegardera en JPEG avec la meilleure qualité. Le nom du fichier de sortie sera affiché. Ce sera smth.jpg.
{{< highlight bash >}}Ajuster le contraste sur 10 de la couche avec le nom ellipse dans le fichier smth.psd et sauvegarder en output.jpg avec la meilleure qualité{{< /highlight >}}

3. Cette commande pivotera le fichier sur le chemin spécifié et réduira sa taille de 25 %. Le fichier de sortie sera affiché. Il sera sauvegardé dans le dossier actuel de la console.
{{< highlight bash >}}Redimensionner le fichier C:\Utilisateurs\someuser\Bureau\entrée.psd à 25%{{< /highlight >}}

4. Cette commande trouvera le fichier entrée.psd dans C:\Utilisateurs\someuser\Bureau\. Ensuite, elle trouvera la couche avec l'index 3 et la redimensionnera en largeur 50px et hauteur 100px. Ensuite, cette couche sera sauvegardée en PDF dans C:\Utilisateurs\someuser\Bureau\sortie.pdf.
{{< highlight bash >}}Redimensionner la couche avec l'index 3 de C:\Utilisateurs\someuser\Bureau\entrée.psd en largeur 50 et hauteur 100 et sauvegarder en C:\Utilisateurs\someuser\Bureau\sortie.pdf{{< /highlight >}}

5. Cette commande ouvrira smth.psd dans le dossier actuel, mais tous les effets seront désactivés. Ensuite, ce fichier sera converti au format BMP et enregistré sous le nom output.bmp dans le dossier actuel.
{{< highlight bash >}}Ouvrir smth.psd sans effets et sauvegarder en output.bmp{{< /highlight >}}

**Avis de non-responsabilité**

Il s'agit d'une application expérimentale. Veuillez l'essayer et laisser un retour. Tout retour est hautement apprécié. Nous voulons amener l'application sans code au niveau supérieur. Notre objectif est une intégration facile à tout pipeline de construction ou processus commercial.
