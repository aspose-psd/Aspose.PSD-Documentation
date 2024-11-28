---
title: Aspose.PSD pour .NET 19.3 - Notes de version
type: docs
weight: 100
url: /fr/net/aspose-psd-pour-net-19-3-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version de Aspose.PSD pour .NET 19.3

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-104|Rendu des calques de texte tournés par TransformMatrix|Fonctionnalité|
|PSDNET-96|Mise en œuvre du rendu de l'effet de contour avec remplissage coloré pour l'exportation|Fonctionnalité|
|PSDNET-112|Les transformateurs InnerData corrompent certains calques avec des masques vectoriels|Erreur|
|PSDNET-113|La mise à jour du calque de texte pour une image PSD génère une erreur lors de l'ouverture dans Photoshop|Erreur|

## **Changements de l'API publique**
# **APIs ajoutées :**
- Aucune
# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**
**PSDNET-104. Rendu des calques de texte tournés par TransformMatrix**

{{< highlight java >}}

 string nomFichierSource = "TexteTransformé.psd";

string cheminExportation = "ExportTexteTransformé.psd";

string cheminExportPng = "ExportTexteTransformé.png";

var im = (PsdImage) Image.Load(nomFichierSource);

using(im) {

 im.Save(cheminExportation);

 im.Save(cheminExportPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Mise en œuvre du rendu de l'effet de contour avec remplissage coloré pour l'exportation**

{{< highlight java >}}

  // Mise en œuvre du rendu de l'effet de contour avec remplissage coloré pour l'exportation

 string nomFichierSource = "ContourComplexe.psd";

 string cheminExportation = "RenduContourComplexe.psd";

 string cheminExportPng = "RenduContourComplexe.png";

 var optionsChargement = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(nomFichierSource, optionsChargement)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var effet = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var réglages = (ColorFillSettings) effet.FillSettings;

   réglages.Color = Color.DeepPink;

  }

  // Enregistrer psd

  im.Save(cheminExportation, new PsdOptions());

  // Enregistrer png

  im.Save(cheminExportPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Les transformateurs InnerData corrompent certains calques avec des masques vectoriels**

{{< highlight java >}}

 // Les transformateurs InnerData corrompent certains calques avec des masques vectoriels

var fichierSource = "1.psd";

var cheminPng = "TestRotationRenversement2617.png";

var cheminPsd = "TestRotationRenversement2617.psd";

var typeRotationRenversement = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(fichierSource))) {

 im.RotateFlip(typeRotationRenversement);

 im.Save(cheminPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(cheminPsd);

}

{{< /highlight >}}

**PSDNET-113. La mise à jour du calque de texte pour une image PSD génère une erreur lors de l'ouverture dans Photoshop**

{{< highlight java >}}

 string nomFichierSource = "Test.psd";

string cheminExportation = "Résultat.psd";

using(Image image = Image.Load(nomFichierSource)) {

 if (!(image is PsdImage)) {

  return;

 }

 PsdImage psdImage = (PsdImage) image;

 Layer[] calques = psdImage.Layers;

 for (int index = calques.Length - 1; index >= 0; index--) {

  Layer calque = calques[index];

  if (!(calque is TextLayer)) {

   continue;

  }

  TextLayer calqueTexte = (TextLayer) calque;

  calqueTexte.UpdateText("\\()");

 }

 PsdOptions optionsImage = new PsdOptions(psdImage);

 psdImage.Save(cheminExportation, optionsImage);

}

// Le fichier doit s'ouvrir sans exception et être lisible par Photoshop

using(Image image = Image.Load(cheminExportation)) {}

{{< /highlight >}}
