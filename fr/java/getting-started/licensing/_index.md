---
title: Licences
type: docs
weight: 60
url: /fr/java/licensing/
---

## **Limitations de la version d'évaluation**
Vous pouvez télécharger une version d'évaluation d'Aspose.PSD pour Java depuis la [page de téléchargement](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). La version d'évaluation fournit les mêmes fonctionnalités que la version entièrement sous licence du composant, avec quelques restrictions. Lorsque vous achetez Aspose.PSD, simplement appliquer la licence supprime toutes les restrictions de la version d'évaluation installée.

La version d'évaluation d'Aspose.PSD pour Java offre la pleine fonctionnalité du produit, avec seulement deux limitations :

- **Un filigrane sur chaque image** : Toute image que vous enregistrez, modifiez ou exportez comporte un filigrane indiquant "Evaluation Only. Créé avec Aspose.PSD. Copyright 2018-2019 Aspose Pty Ltd.". Pour les petites images où le filigrane complet ne rentre pas, deux lignes diagonales traversent l'image à la place.
- **Pas de support pour la fonctionnalité de dessin principale**: En mode d'évaluation, les pixels de l'image ne peuvent pas être chargés ou enregistrés dans l'image. Pour dessiner des images, utilisez la fonctionnalité de dessin avancée à la place. Cette limitation affecte les fonctionnalités qui dépendent de la fonctionnalité de dessin principale. Aspose.PSD pour Java vous permet d'enregistrer votre propre format de fichier. Cependant, cette fonction dépend de la fonctionnalité de dessin principale, il n'a donc pas de sens de l'utiliser en mode d'évaluation car vous ne pouvez pas modifier le contenu de ces fichiers.

{{% alert color="primary" %}} 

Si vous voulez tester Aspose.PSD pour Java sans les limitations de l'évaluation, demandez une licence temporaire de 30 jours. Veuillez consulter [Comment obtenir une licence temporaire?](https://purchase.aspose.com/temporary-license) pour plus d'informations.

{{% /alert %}} 

## **À propos du fichier de licence**
Une fois que vous êtes satisfait de votre évaluation d'Aspose.PSD, vous pouvez acheter une licence sur le [site Web d'Aspose](https://purchase.aspose.com/default.aspx). Familiarisez-vous avec les différents types d'abonnements offerts. Si vous avez des questions, n'hésitez pas à contacter [l'équipe commerciale d'Aspose](https://company.aspose.com/contact).

Chaque licence Aspose est accompagnée d'un abonnement d'un an pour les mises à jour logicielles. Après la première année, renouvelez vos abonnements pour continuer à obtenir les dernières fonctionnalités et corrections. Le support technique est gratuit et illimité et est fourni aux utilisateurs sous licence et en évaluation via nos [Forums de support](https://forum.aspose.com/).

La licence est un fichier XML qui contient des détails tels que le nom du produit, le nombre de développeurs autorisés, la date d'expiration de l'abonnement, etc. Le fichier est signé numériquement, donc ne le modifiez pas : même l'ajout accidentel d'un saut de ligne supplémentaire invalide le fichier.

Après avoir acheté Aspose.PSD, vous devez appliquer la licence avant de créer, éditer ou manipuler des images. Si vous oubliez d'appliquer la licence, toutes les images de sortie auront un filigrane d'évaluation. 
Vous n'avez besoin de définir la licence qu'une seule fois par application ou processus que vous développez.

## **Application de la licence**
Vous pouvez télécharger une version d'évaluation d'**Aspose.PSD** pour Java depuis [sa page de téléchargement](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). La version d'évaluation offre absolument les mêmes capacités que la version sous licence du produit. De plus, la version d'évaluation devient simplement sous licence lorsque vous achetez une licence et ajoutez quelques lignes de code pour l'appliquer.

Une fois que vous êtes satisfait de votre évaluation d'**Aspose.PSD**, vous pouvez [acheter une licence](http://www.aspose.com/Purchase/Components/Default.aspx) sur le site Web d'Aspose. Familiarisez-vous avec les différents types d'abonnements offerts. Si vous avez des questions, n'hésitez pas à contacter l'équipe commerciale d'Aspose.

Chaque licence Aspose comprend un abonnement d'un an pour des mises à jour gratuites vers de nouvelles versions ou correctifs qui sortent pendant cette période. Le support technique est gratuit et illimité et fourni à la fois aux utilisateurs sous licence et en évaluation.

{{% alert color="primary" %}} 

Si vous voulez tester **Aspose.PSD** sans les limitations de la version d'évaluation, demandez une licence temporaire de 30 jours. Veuillez consulter [Comment obtenir une licence temporaire?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) pour plus d'informations.

{{% /alert %}} 

### **Définition d'une licence**
La licence est un fichier XML en texte brut qui contient des détails tels que le nom du produit, le nombre de développeurs autorisés, la date d'expiration de l'abonnement, etc. Le fichier est signé numériquement, donc ne le modifiez pas ; même l'ajout involontaire d'un saut de ligne supplémentaire dans le fichier l'invalidera.

Vous devez définir une licence avant d'utiliser **Aspose.PSD** si vous voulez éviter ses limitations d'évaluation. Vous devez définir une licence une seule fois par application ou par process.

La licence peut être chargée à partir d'un flux ou d'un fichier dans les emplacements suivants :

1. Chemin explicite.
1. Le dossier contenant le fichier Aspose.PSD.jar.

Utilisez la méthode [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense pour autoriser le composant. Le moyen le plus simple de définir une licence est souvent de placer le fichier de licence dans le même dossier que Aspose.PSD.jar et de spécifier simplement le nom du fichier sans chemin comme le montre l'exemple suivant :

#### **Exemple 1**
Dans cet exemple, **Aspose.PSD** tentera de trouver le fichier de licence dans le dossier contenant les JARs de votre application.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}

#### **Exemple 2**
Initialise une licence à partir d'un flux.

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}

### **Valider la licence**
Il est possible de vérifier si la licence a été correctement définie ou non. La classe License a le champ isLicensed qui renverra true si la licence a été correctement définie.

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("La licence est définie!");

}

{{< /highlight >}}

## **Où Appliquer une Licence dans votre Application**
L'endroit où vous appliquez une licence dépend du type d'application que vous développez. Suivez ces règles simples :

- La licence doit être définie une seule fois par domaine d'application. Appeler License.setLicense plusieurs fois n'est pas nuisible mais gaspille du temps processeur.
- Appliquez la licence avant d'appeler les classes Aspose.PSD.
- **Applications Java**: appelez License.SetLicense dans le code de démarrage.
- **Bibliothèque de classes**: appelez License.setLicense depuis un constructeur statique de la classe qui utilise Aspose.PSD. Le constructeur statique s'exécute avant la création d'une instance de votre classe, garantissant que la licence Aspose.PSD est correctement définie.

## **Utilisation de Plusieurs Produits Aspose**
Si vous utilisez plus d'un produit Aspose dans votre application, par exemple Aspose.PSD et Aspose.Cells, voici quelques conseils utiles.

- **Appliquez la licence pour chaque produit Aspose séparément**. Même si vous avez un seul fichier de licence pour tous les composants, par exemple 'Aspose.Total.lic', vous devez tout de même appeler License.setLicense séparément pour chaque produit Aspose dans votre application.
- **Utilisez un nom de classe de licence complètement qualifié**. Chaque produit Aspose a une classe License dans son espace de noms. Par exemple, Aspose.PSD a com.aspose.psd.license.License et Aspose.Cells a com.aspose.cells.License. Utiliser un nom de classe entièrement qualifié évite toute confusion sur la licence appliquée à quel produit.
