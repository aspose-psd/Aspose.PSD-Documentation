---
title: Comment exécuter les exemples
type: docs
weight: 90
url: /fr/net/comment-executer-les-exemples/
description: Apprenez comment exécuter les exemples relatifs à la bibliothèque de format de fichier PSD hébergés sur GitHub.
---

## **Configuration requise du logiciel**
Veuillez vous assurer de remplir les exigences suivantes avant de télécharger et d'exécuter les exemples.

1. Visual Studio 2010 ou version ultérieure.
1. Gestionnaire de packages NuGet installé dans Visual Studio. Assurez-vous que la dernière version de l'API NuGet est installée dans Visual Studio. Pour plus de détails sur l'installation du gestionnaire de packages NuGet, veuillez consulter [http://docs.nuget.org/ndocs/guides/install-nuget](http://docs.nuget.org/ndocs/guides/install-nuget).
1. Allez dans Outils->Options->Gestionnaire de packages NuGet->Sources de packages et assurez-vous que l'option **nuget.org** est cochée.
1. Le projet d'exemple utilise la fonction de restauration automatique des packages NuGet, assurez-vous donc d'avoir une connexion Internet active. Si vous n'avez pas de connexion Internet active sur la machine où les exemples doivent être exécutés, veuillez consulter [l'installation](/psd/fr/net/installation/) pour ajouter une référence à Aspose.Imaging.dll dans le projet d'exemple.

## **Téléchargement à partir de GitHub**
Tous les exemples d'Aspose.PSD pour .NET sont hébergés sur [GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET).

- Vous pouvez soit cloner le dépôt à l'aide de votre client GitHub préféré, soit télécharger le fichier ZIP à partir de [ici](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip).
- Extrayez le contenu du fichier ZIP dans un dossier quelconque sur votre ordinateur. Tous les exemples se trouvent dans le dossier **Exemples**.
- Il y a un fichier de solution Visual Studio pour C#.
- Les projets sont créés dans Visual Studio 2013, mais les fichiers de solution sont compatibles avec Visual Studio 2010 SP1 et versions ultérieures.
- Ouvrez le fichier de solution dans Visual Studio et générez le projet.
- Lors du premier démarrage, les dépendances seront automatiquement téléchargées via NuGet.
- Le dossier **Données** à la racine du dossier **Exemples** contient les fichiers d'entrée utilisés par les exemples CSharp. Il est obligatoire de télécharger le dossier **Données** avec le projet des exemples.
- Ouvrez le fichier RunExamples.cs, tous les exemples sont appelés à partir d'ici.
- Décommentez les exemples que vous souhaitez exécuter à partir du projet.

N'hésitez pas à nous contacter via nos forums si vous rencontrez des problèmes lors de la configuration ou de l'exécution des exemples.

## **Contribuer**
Si vous souhaitez ajouter ou améliorer un exemple, nous vous encourageons à contribuer au projet. Tous les exemples et projets de démonstration de ce dépôt sont open source et peuvent être librement utilisés dans vos propres applications.

Pour contribuer, vous pouvez forker le dépôt, modifier le code source et créer une pull request. Nous passerons en revue les changements et les inclurons dans le dépôt s'ils sont jugés utiles.
