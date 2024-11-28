---
title: Aspose.PSD for .NET 18.8 - Notes de publication
type: docs
weight: 50
url: /fr/net/aspose-psd-for-net-18-8-release-notes/
---

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-68|Prise en charge de la propriété LayerCreationDateTime.|Fonctionnalité|
|PSDNET-67|Prise en charge de la mise en évidence de SheetColor|Fonctionnalité|
|PSDNET-66|Possibilité de fusionner des calques entre eux|Fonctionnalité|
|PSDNET-65|Ajouter la prise en charge partielle de la propriété Text Layer BoundBox|Fonctionnalité|
|PSDNET-64|Ajouter la prise en charge pour IopaResource|Fonctionnalité|
|PSDNET-56|Prise en charge des effets de calque pour le format PSD|Fonctionnalité|
|PSDNET-55|Support InterruptMonitor pour .Net|Fonctionnalité|
|PSDNET-50|Permettre l'aplatissement des calques|Fonctionnalité|
|PSDNET-49|Ajouter le rendu de la propriété d'opacité de remplissage dans les calques.|Fonctionnalité|
|PSDNET-43|Mise en œuvre du rendu de la couche d'ajustement des courbes|Fonctionnalité|
|PSDNET-42|Ajouter la prise en charge de la couche d'ajustement des courbes|Fonctionnalité|
|PSDNET-41|Mise en œuvre du rendu de la couche d'ajustement des niveaux|Fonctionnalité|
|PSDNET-40|Ajouter la prise en charge de la couche d'ajustement des niveaux|Fonctionnalité|
|PSDNET-37|Ajouter la prise en charge de la couche d'ajustement du mélangeur de canaux|Fonctionnalité|
|PSDNET-35|Ajouter la prise en charge de la couche d'ajustement de teinte/saturation|Fonctionnalité|
|PSDNET-34|Mise en œuvre du rendu de la couche d'ajustement d'exposition pour l'exportation.|Fonctionnalité|
|PSDNET-31|Ajouter la prise en charge du rendu pour exportation de la couche d'ajustement du mélangeur de canaux|Fonctionnalité|
|PSDNET-26|Ajouter la prise en charge du masque d'écrêtage|Fonctionnalité|
|PSDNET-13|Ajouter la prise en charge du masque de calque|Fonctionnalité|
|PSDNET-9|Ajouter la prise en charge de la couche d'ajustement du filtre photo|Fonctionnalité|
|PSDNET-8|Ajouter la prise en charge de la couche d'ajustement du mélangeur de canaux|Fonctionnalité|
|PSDNET-7|Ajouter la prise en charge de la couche d'ajustement de l'exposition|Fonctionnalité|
|PSDNET-6|Ajouter la prise en charge de la couche d'ajustement de luminosité/contraste|Fonctionnalité|
|PSDNET-5|Ajouter la prise en charge partielle des calques d'ajustement|Fonctionnalité|
|PSDNET-3|Ajouter la prise en charge de l'option de texte PSD NoBreak|Fonctionnalité|
|PSDNET-2|Possibilité d'ajouter des calques de texte à l'exécution|Fonctionnalité|
|PSDNET-62|Le Codec TIFF ne peut pas enregistrer une image de canal 16 bits|Amélioration|
|PSDNET-61|L'enregistrement de l'image PSD produit des couleurs invalides|Amélioration|
|PSDNET-60|La coordonnée du coin supérieur gauche est incorrecte lors de la mise à jour|Amélioration|
|PSDNET-59|Exception lors de la mise à jour des calques de texte|Amélioration|
|PSDNET-58|Exposer la propriété Codec de l'image JPEG2000 au public|Amélioration|
|PSDNET-57|Correction des options 24 bpp pour l'exportation vers BMP|Amélioration|
|PSDNET-46|La couche d'ajustement est ignorée pour la conversion PSD CMJN en TIFF ou JPG|Amélioration|

## **Exemples d'utilisation :**
**PSDNET-68 Prise en charge de la propriété LayerCreationDateTime**

{{< highlight java >}}

 // Exemple d'utilisation de la propriété LayerCreationDateTime

string sourceFileName = "UnCalque.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var calque = im.Calques[0];

    var creationDateTime = calque.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var maintenant = DateTime.Now;

    var calqueCree = im.AjouterCalqueAjustementNiveaux();

    // Vérifier si la date de création est mise à jour sur les nouveaux calques créés

    Assert.True(maintenant <= calqueCree.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Prise en charge de la mise en évidence de SheetColor**

{{< highlight java >}}

 // Exemple d'utilisation de la propriété SheetColorHighlight

string sourceFileName = "ExempleMiseEnAvantSheetColor.psd";

string exportPath = "ExempleMiseEnAvantSheetColorModifie.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var calque1 = im.Calques[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, calque1.SheetColorHighlight);

    var calque2 = im.Calques[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, calque2.SheetColorHighlight);



    calque1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 Possibilité de fusionner des calques entre eux**

{{< highlight java >}}

 // Exemple de fusion de deux calques

var sourceFile1 = "ExempleOpaciteDeRemplissage.psd";

var sourceFile2 = "TroisCalquesReguliersSemiTransparent.psd";

var exportPath = "CalquesFusionnesAPartirDeDeuxPsdDifferents.psd";

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var calque1 = im1.Calques[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var calque2 = im2.Calques[0];

        calque1.FusionnerCalqueAvec(calque2);

	im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 Ajouter la prise en charge partielle de la propriété Text Layer BoundBox**

{{< highlight java >}}

 // Exemple de Boîte de texte

string sourceFileName = "CalqueAvecTexte.psd";

var tailleOptiqueCorrecte = new Taille(127, 45);

var boiteCorrecte = new Taille(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var calqueTexte = (CalqueTexte)im.Calques[1];

    // La taille du calque est la taille de la zone de rendu

    var tailleOptique = calqueTexte.Taille;

    Assert.AreEqual(tailleOptiqueCorrecte, tailleOptique);

    // TextBoundBox est la taille maximale du calque pour le calque de texte. 

    // Dans cette zone, PS essaiera de adapter votre texte

    var boiteTexte = calqueTexte.TextBoundBox;

    Assert.AreEqual(boiteCorrecte, boiteTexte);

}

{{< /highlight >}}

**PSDNET-64 Ajouter la prise en charge pour IopaResource**

{{< highlight java >}}

 // Modifier la propriété d'opacité de remplissage en changeant IopaResource

string sourceFileName = "ExempleOpaciteDeRemplissage.psd";

string exportPath = "ExempleOpaciteDeRemplissageModifie.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var calque = im.Calques[2];



    var ressources = calque.Ressources;

    foreach (var ressource in ressources)

    {

        if (ressource est IopaResource)

        {

            var ressourceIopa = (IopaResource)ressource;

            ressourceIopa.OpaciteRemplissage = 200;

        }

    }



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-56 Prise en charge des effets de calque pour le format PSD**

{{< highlight java >}}

 using (

    PsdImage image =

        (PsdImage)

        Aspose.PSD.Image.Load(

            sourceFileName,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                output,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    TypeCouleur =

                            Aspose.PSD.FormatsFichier.Png

                            .TypeCouleurPng

                            .VraiCouleurAvecAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 Support InterruptMonitor pour .Net**

{{< highlight java >}}

         public void TestInterrupteurMonitor(string dir, string ouputDir)

        {

            OptionsImageBase saveOptions = new OptionsImage.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            TravailleurEnregistrerImage worker = new TravailleurEnregistrerImage(dir + "grand.psb", dir + "sortie_grande.png", saveOptions, monitor);

            Fil thread = new Fil(new ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // Le délai d'attente doit être inférieur au temps nécessaire pour la conversion complète de l'image (sans interruption).

                FilSommeil(3000);

                // Interrompre le processus

                monitor.Interrompre();

                System.Console.WriteLine("Interruption du fil d'enregistrement #{0} à {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Attendre l'interruption...

                thread.Join();

            }

            finally

            {

                // Si le fichier à supprimer n'existe pas, aucune exception n'est levée.

                System.IO.File.Delete(dir + "sortie_grande.png");

            }

        }

        /// <summary>

        /// Initie la conversion d'image et attend son interruption.

        /// </summary>

        private class TravailleurEnregistrerImage

        {

            /// <summary>

            /// Le chemin de l'image d'entrée.

            /// </summary>

            private readonly string cheminEntree;

            /// <summary>

            /// Le chemin de l'image de sortie.

            /// </summary>

            private readonly string cheminSortie;

            /// <summary>

            /// Le moniteur d'interruption.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Les options d'enregistrement.

            /// </summary>

            private readonly OptionsImageBase optionsEnregistrement;

            /// <summary>

            /// Initialise une nouvelle instance de la classe TravailleurEnregistrerImage.

            /// </summary>

            /// <param name="cheminEntree">Le chemin de l'image d'entrée.</param>

            /// <param name="cheminSortie">Le chemin de l'image de sortie.</param>

            /// <param name="optionsEnregistrement">Les options d'enregistrement.</param>

            /// <param name="monitor">Le moniteur d'interruption.</param>

            public TravailleurEnregistrerImage(string cheminEntree, string cheminSortie, OptionsImageBase optionsEnregistrement, Multithreading.InterruptMonitor monitor)

            {

                this.cheminEntree = cheminEntree;

                this.cheminSortie = cheminSortie;

                this.optionsEnregistrement = optionsEnregistrement;

                this.monitor = monitor;

            }

            /// <summary>

            /// Essaye de convertir une image d'un format à un autre. Gère l'interruption.

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.cheminEntree))

                {

                    Multithreading.InterruptMonitor.ThreadInstanceLocale = this.monitor;

                    try

                    {

                        image.Save(this.cheminSortie, this.optionsEnregistrement);

                        Asserter.Fails("Interruption attendue.");

                    }

                    attraper (CoreExceptions.OperationInterruptionException e)

                    {

                        System.Console.WriteLine("Fin du fil d'enregistrement #{0} à {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    attraper (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    enfin

                    {

                        Multithreading.InterruptMonitor.ThreadInstanceLocale = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 Prise en charge de l'aplatir des calques**

{{< highlight java >}}

 // Aplatir tout le PSD

string sourceFileName = "TroisCalquesReguliersSemiTransparent.psd";

string exportPath = "TroisCalquesReguliersSemiTransparentAplatis.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.AplatirImage();

    im.Save(exportPath);	 

}

// Fusionner un calque dans un autre

string sourceFileName = "TroisCalquesReguliersSemiTransparent.psd";

string exportPath = "TroisCalquesReguliersSemiTransparentAplatisCalqueParCalque.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var calqueInferieur = im.Calques[0];

    var calqueIntermediaire = im.Calques[1];

    var calqueSuperieur = im.Calques[2];

    var calque1 = im.FusionnerCalques(calqueInferieur, calqueIntermediaire);

    var calque2 = im.FusionnerCalques(calque1, calqueSuperieur);

    // Configurer les calques fusionnés

    im.Calques = new Calque[] { calque2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 Ajouter le rendu de la propriété d'opacité de remplissage dans les calques**

{{< highlight java >}}

 // Changer la propriété d'opacité de remplissage

string sourceFileName = "ExempleOpaciteDeRemplissage.psd";

string exportPath = "ExempleOpaciteDeRemplissageModifie.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var calque = im.Calques[2];

    calque.OpaciteRemplissage = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 Mise en œuvre du rendu de la couche d'ajustement des courbes**

{{< highlight java >}}

 // Édition de la couche de courbes

string sourceFileName = "CoucheAjustementCourbes";

string cheminPsdApresChangement = "CoucheAjustementCourbesModif";

string cheminementExportPng = "CoucheAjustementCourbesModif";

pour (int j = 1; j < 2; j++)

{

    en utilisant (var im = ChargementFichier(sourceFileName + j.ToString() + ".psd"))

    {

        foreach (var calque in im.Calques)

	{

            if (calque est CoucheCourbes)

            {

                 var calqueCourbes = (CoucheCourbes)calque;

                 si (calqueCourbes.IsDiscreteManagerUsed)

                 {

                      var gestionnaire = (GestionnaireDiscreteCourbes)calqueCourbes.GetGestionnaireCourbes();

                      pour (int i = 10; i < 50; i++)

                      {

                           gestionnaire.DefinirValeurAPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 autre

                 {

                      var gestionnaire = (GestionnaireContinuCourbes)calqueCourbes.GetGestionnaireCourbes();

                      gestionnaire.AjouterPointCourbe(0, 50, 100);

                      gestionnaire.AjouterPointCourbe(0, 150, 130);

                 }

            }

        }

    }



    // Enregistrer le PSD

    im.Save(cheminPsdApresChangement + j.ToString() + ".psd");



    // Enregistrer le PNG

    var optionsEnregistrement = new OptionsPng();

    optionsEnregistrement.TypeCouleur = TypeCouleurPng.VraiCouleurAvecAlpha;

    im.Save(cheminementExportPng + j.ToString() + ".png", optionsEnregistrement);

}

{{< /highlight >}}

**PSDNET-42 Ajouter la prise en charge de la couche d'ajustement des courbes**

{{< highlight java >}}

 // Édition de la couche de courbes

string sourceFileName = "CoucheAjustementCourbes";

string cheminPsdApresChangement = "CoucheAjustementCourbesModif";

pour (int j = 1; j < 2; j++)

{

    en utilisant (var im = ChargementFichier(sourceFileName + j.ToString() + ".psd"))

    {

         foreach (var calque in im.Calques)

	 {

            if (calque est CoucheCourbes)

            {

                 var calqueCourbes = (CoucheCourbes)calque;

                 si (calqueCourbes.IsDiscreteManagerUsed)

                 {

                      var gestionnaire = (GestionnaireDiscreteCourbes)calqueCourbes.GetGestionnaireCourbes();

                      pour (int i = 10; i < 50; i++)

                      {

                           gestionnaire.DefinirValeurAPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 autre

                 {

                      var gestionnaire = (GestionnaireContinuCourbes)calqueCourbes.GetGestionnaireCourbes();

                      gestionnaire.AjouterPointCourbe(0, 50, 100);

                      gestionnaire.AjouterPointCourbe(0, 150, 130);

                 }

	 }

    }



    // Save PSD

    im.Save(cheminPsdApresChangement + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 Mise en œuvre du rendu de la couche d'ajustement des niveaux**

{{< highlight java >}}

 // Édition de la couche de niveaux

string sourceFileName = "CoucheAjustementNiveaux.psd";

string cheminPsdApresChangement = "CoucheAjustementNiveauxModif.psd";

string cheminementExportPng = "CoucheAjustementNiveauxModif.png";

utilisation (var im = ChargementFichier(sourceFileName))

{

    pour chaque (var calque dans im.Calques)

    {

        if (calque est CoucheNiveaux)

        {

            var calqueNiveaux = (CoucheNiveaux)calque;

            var canal = calqueNiveaux.ObtenirCanal(0);

            canal.NiveauMilieuEntree = 2.0f;

            canal.NiveauOmbreEntree = 10;

            canal.NiveauHighlightEntree = 230;

            canal.NiveauOmbreSortie = 20;

            canal.NiveauHighlightSortie = 200;

        }

    }



    // Enregistrer PSD

    im.Save(cheminPsdApresChangement);



    // Enregistrer PNG

    var optionsEnregistrement = new OptionsPng();

    optionsEnregistrement.TypeCouleur = TypeCouleurPng.VraiCouleurAvecAlpha;

    im.Save(cheminementExportPng, optionsEnregistrement);

}

{{< /highlight >}}

**PSDNET-40 Ajouter la prise en charge de la couche d'ajustement des niveaux**

{{< highlight java >}}

 // Édition de la couche de niveaux

string sourceFileName = "CoucheAjustementNiveaux.psd";

string cheminPsdApresChangement = "CoucheAjustementNiveauxModif.psd";

utilisation (var im = ChargementFichier(sourceFileName))

{

    pour chaque (var calque dans im.Calques)

    {

        if (calque est CoucheNiveaux)

        {

            var calqueNiveaux = (CoucheNiveaux)calque;

            var canal = calqueNiveaux.ObtenirCanal(0);

            canal.NiveauMilieuEntree = 2.0f;

            canal.NiveauOmbreEntree = 10;

            canal.NiveauHighlightEntree = 230;

            canal.NiveauOmbreSortie = 20;

            canal.NiveauHighlightSortie = 200;

        }

    }



    // Enregistrer PSD

    im.Save(cheminPsdApresChangement);

}

{{< /highlight >}}

**PSDNET-37 Ajouter la prise en charge de la couche d'ajustement du mélangeur de canaux**

{{< highlight java >}}



// Mélangeur de canaux Rvb

string sourceFileName = "CoucheAjustementMélangeurCanauxRvb.psd";

string cheminPsdApresChangement = "CoucheAjustementMélangeurCanauxRvbModif.psd";

utilisation (var im = ChargementFichier(sourceFileName))

{

    pour chaque (var calque dans im.Calques)

    {

         if (calque est CoucheMélangeurCanauxRvb)

         {

              var calqueRgb = (CoucheMélangeurCanauxRvb)calque;

              calqueRgb.CanalRouge.Bleu = 100;

              calqueRgb.CanalBleu.Vert = -100;

              calqueRgb.CanalVert.Constante = 50;

         }

    }



    im.Save(cheminPsdApresChangement);

}

// Mélangeur de canaux Cmyk

string sourceFileName = "CoucheAjustementMélangeurCanauxCmyk.psd";

string cheminPsdApresChangement = "CoucheAjustementMélangeurCanauxCmykModif.psd";

utilisation (var im = ChargementFichier(sourceFileName))

{

    pour chaque (var calque dans im.Calques)

    {

         if (calque est CoucheMélangeurCanauxCmyk)

         {

             var calqueCmyk = (CoucheMélangeurCanauxCmyk)calque;

             calqueCmyk.CanalCyan.Noir = 20;

             calqueCmyk.CanalMagenta.Jaune = 50;

             calqueCmyk.CanalJaune.Cyan = -25;

             calqueCmyk.CanalNoir.Jaune = 25;

         }

    }



    im.Save(cheminPsdApresChangement);

}





// Ajout du nouveau calque (Cmyk pour cet exemple)

string sourceFileName = "CmykAvecAlpha.psd";

string cheminPsdApresChangement = "CoucheAjustementMélangeurCanauxCmykModif.psd";

utilisation (var im = ChargementFichier(sourceFileName))

{

    var nouveauCalque = im.AjouterCoucheAjustementMélangeurCanaux();

    nouveauCalque.ObtenirCanalParIndice(2).Constante = 50;

    nouveauCalque.ObtenirCanalParIndice(0).Constante = 50;



    im.Save(cheminPsdApresChangement);

}		

{{< /highlight >}}

**PSDNET-35 Ajouter la prise en charge de la couche d'ajustement de teinte/saturation**

{{< highlight java >}}

 // Édition de la couche de teinte/saturation

string sourceFileName = "CoucheAjustementTeinteSaturation.psd";

string cheminPsdApresChangement = "CoucheAjustementTeinteSaturationModif.psd";

utilisation (var im = ChargementFichier(sourceFileName))

{

     pour chaque (var calque dans im.Calques)

     {

           if (calque est CoucheTeinteSaturation)

           {

                var calqueTeinte = (CoucheTeinteSaturation)calque;

                calqueTeinte.Teinte = -25;

                calqueTeinte.Saturation = -12;

                calqueTeinte.Luminosite = 67;

                var plageCouleurs = calqueTeinte.ObtenirPlage(2);

                plageCouleurs.Teinte = -40;

                plageCouleurs.Saturation = 50;

                plageCouleurs.Luminosite = -20;

                plageCouleurs.BordureLaPlusAGauche = 300;

           }

      }

      im.Save(cheminPsdApresChangement);

}



// Ajout de la couche de teinte/saturation

string sourceFileName = "ExemplePhoto.psd";

string cheminPsdApresChangement = "ExemplePhotoAjoutTeinteSaturation.psd";



utilisation (PsdImage im = ChargementFichier(sourceFileName))

{

     this.EnregistrerPourTestVisuel(im, this.CheMin, prefix + fichier, "avant");

     var calqueTeinte = im.AjouterCoucheAjustementTeinteSaturation();

     calqueTeinte.Teinte = -25;

     calqueTeinte.Saturation = -12;

     calqueTeinte.Luminosite = 67;

     var plageCouleurs = calqueTeinte.ObtenirPlage(2);

     plageCouleurs.Teinte = -160;

     plageCouleurs.Saturation = 100;

     plageCouleurs.Luminosite = 20;

     plageCouleurs.BordureLaPlusAGauche = 300;



     im.Save(cheminPsdApresChangement);

}

{{< /highlight >}}