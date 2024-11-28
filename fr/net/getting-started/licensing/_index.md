---
title: Licences
type: docs
weight: 70
url: /fr/net/licensing/
description: Évaluer la bibliothèque PSD Photoshop C# depuis NuGet et appliquer la licence en utilisant un fichier ou un flux pour supprimer toutes les restrictions de l'évaluation installée.
---

## **Limitations de la Version d'Évaluation**
Vous pouvez télécharger une version d'évaluation de Aspose.PSD pour .NET depuis le [NuGet](https://www.nuget.org/packages/Aspose.psd/). La version d'évaluation fournit les mêmes fonctionnalités que la version entièrement sous licence du composant avec quelques restrictions. Lorsque vous achetez Aspose.PSD, l'application de la licence supprime toutes les restrictions de l'évaluation installée. La version d'évaluation de Aspose.PSD pour .NET offre une fonctionnalité complète du produit, avec seulement deux limitations:

- **Un filigrane sur chaque image**: Toute image que vous enregistrez, modifiez ou exportez comporte un filigrane avec la mention "Évaluation seulement. Créé avec Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". Les petites images, où le filigrane complet ne tient pas, ont deux lignes diagonales à travers l'image à la place.
- **Pas de prise en charge de la fonctionnalité de dessin de base**: En mode d'évaluation, les pixels d'image ne peuvent pas être chargés ou enregistrés dans l'image. Pour dessiner des images, utilisez plutôt la fonctionnalité de dessin avancée. Cette limitation affecte les fonctionnalités qui dépendent de la fonctionnalité de dessin de base. Aspose.PSD for .NET vous permet d'enregistrer votre propre format de fichier. Cependant, cette fonctionnalité dépend de la fonctionnalité de dessin de base, il n'a donc pas de sens de l'utiliser en mode d'évaluation car vous ne pouvez pas modifier le contenu de ces fichiers.

Si vous souhaitez tester Aspose.PSD pour .NET sans les limitations de l'évaluation, demandez une licence temporaire de 30 jours. Veuillez vous référer à [Comment obtenir une licence temporaire ?](https://purchase.aspose.com/temporary-license) pour plus d'informations.
## **À propos du Fichier de Licence**
Une fois que vous êtes satisfait de votre évaluation de Aspose.PSD, vous pouvez acheter une licence sur le [site web d'Aspose](https://purchase.aspose.com/default.aspx). Familiarisez-vous avec les différents types d'abonnements proposés. Si vous avez des questions, n'hésitez pas à contacter [l'équipe commerciale d'Aspose](https://company.aspose.com/contact). Chaque licence Aspose est assortie d'un abonnement d'un an pour les mises à jour logicielles. Après la première année, renouvelez vos abonnements pour continuer à obtenir les dernières fonctionnalités et corrections. Le support technique est gratuit et illimité et est fourni à la fois aux utilisateurs sous licence et aux utilisateurs en phase d'évaluation via nos [Forums de Support](https://forum.aspose.com/). La licence est un fichier XML qui contient des détails tels que le nom du produit, le nombre de développeurs autorisés, la date d'expiration de l'abonnement, etc. Le fichier est signé numériquement, alors ne le modifiez pas : même ajouter involontairement un saut de ligne supplémentaire invalide le fichier. Après l'achat de Aspose.PSD, vous devez appliquer la licence avant de créer, éditer ou manipuler des images. Si vous oubliez d'appliquer la licence, toutes les images de sortie auront un filigrane d'évaluation. Vous devez définir la licence une seule fois par application ou processus que vous développez.
## **Où Appliquer une Licence dans Votre Application**
Où vous appliquez une licence dépend du type d'application que vous développez. Suivez ces règles simples:

- Appliquez la licence une seule fois par domaine d'application. Appeler plusieurs fois License.SetLicense n'est pas nocif mais gaspille du temps processeur.
- Appliquer la licence avant d'appeler des classes Aspose.PSD pour .NET.
- **Applications Windows Forms ou Console**: appelez License.SetLicense dans le code de démarrage, avant d'utiliser des classes Aspose.PSD pour .NET.
- **Applications ASP.NET**: appelez License.SetLicense depuis le fichier Global.asax.cs (Global.asax.vb), dans la méthode protégée Application_Start. De cette manière, elle est appelée une fois au démarrage de l'application. Ne pas appeler License.SetLicense depuis les méthodes Page_Load ou la licence sera chargée à chaque chargement d'une page web.
- **Applications Silverlight**: appelez License.SetLicense à partir de l'événement Application_Startup dans le fichier App.xaml.cs (App.xaml.vb).
- **Bibliothèque de classes**: appelez License.SetLicense depuis un constructeur statique de la classe qui utilise Aspose.PSD. Le constructeur statique s'exécute avant la création d'une instance de votre classe, s'assurant que la licence Aspose.PSD est correctement configurée.
## **Application d'une Licence**
Vous pouvez facilement télécharger une version d'évaluation de Aspose.PSD depuis le [page de téléchargement](https://www.nuget.org/packages/Aspose.psd/). La version d'évaluation offre exactement les mêmes fonctionnalités que la version sous licence de Aspose.PSD. De plus, la version d'évaluation devient simplement sous licence lorsque vous achetez une licence et ajoutez quelques lignes de code pour appliquer la licence.
### **Utilisation d'un Fichier ou d'un Flux**
Si vous voulez éviter de travailler avec les limitations de l'évaluation, vous devez définir une licence avant d'utiliser Aspose.PSD. Vous devez définir une licence une seule fois par application (ou processus).
### **Application d'une licence à partir d'un fichier**
La manière la plus simple d'appliquer une licence est de placer le fichier de licence dans le même dossier que Aspose.PSD.dll. Ensuite, vous pouvez spécifier le nom du fichier dans le code au lieu d'un chemin complet.



{{< highlight java >}}

 // Instancier une instance de licence et appliquer la licence en utilisant un chemin complet

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Lorsque vous appelez la méthode SetLicense, le nom de la licence doit être le même que celui de votre fichier de licence. Par exemple, si vous changez le nom du fichier de licence en "Aspose.PSD.lic.xml", vous devez utiliser ce nom de licence pour la méthode SetLicense.
### **Application d'une licence en utilisant un flux**
Il est également possible de charger une licence à partir d'un flux comme démontré ci-dessous.



{{< highlight java >}}



// Instancier une instance de licence et appliquer la licence en utilisant un flux

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **Vérification du statut de la licence**
La classe Aspose.PSD.License dispose de la propriété IsLicensed qui renverra true si la licence a été correctement définie.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("La licence est définie !");

}

{{< /highlight >}}
### **Utilisation d'une Ressource Embarquée**
Une façon pratique d'emballer la licence avec votre application et de vous assurer qu'elle n'est pas perdue, est de l'inclure en tant que ressource embarquée dans l'une des assemblies qui appellent Aspose.PSD. Pour inclure le fichier de licence en tant que ressource embarquée:

1. Dans Visual Studio .NET, cliquez sur le menu **Fichier** et sélectionnez **Ajouter un élément existant**.
1. Incluez le fichier de licence (extension .lic) dans le projet.
1. Sélectionnez le fichier dans l'Explorateur de solutions.
1. Dans la fenêtre Propriétés, définissez l'**Action de génération** sur **Ressource embarquée**.

Il n'est pas nécessaire d'appeler les méthodes GetExecutingAssembly ou GetManifestResourceStream de la classe System.Reflection.Assembly dans le cadre du Microsoft .NET Framework pour accéder à une licence embarquée. Au lieu de cela, incorporez le fichier en tant que ressource dans le projet, puis transmettez le nom du fichier de licence à la méthode SetLicense. La classe Licence trouve automatiquement le fichier de licence dans les ressources embarquées. L'exemple ci-dessous montre comment inclure la licence en tant que ressource embarquée et l'appliquer à votre application.



{{< highlight java >}}

 // Instancier la classe Licence

Aspose.PSD.License license = new Aspose.PSD.License();



// Passer le nom du fichier de licence intégré

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Vérification du statut de la licence**
La classe Aspose.PSD.License dispose de la propriété IsLicensed qui renverra true si la licence a été correctement définie.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("La licence est définie !");

}

{{< /highlight >}}
