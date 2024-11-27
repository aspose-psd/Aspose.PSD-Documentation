---
title: Notes de version Aspose.PSD pour .NET 23.2
type: docs
weight: 110
url: /fr/net/aspose-psd-pour-net-23-2-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-1359|Rework text rendering to improve text positioning, rendering, and support|Amélioration|
|PSDNET-1270|Ajouter la capacité de traiter l'effet de déformation via l'API publique|Fonctionnalité|
|PSDNET-1391|Ajouter la prise en charge des modes de plomb de bas en bas et de haut en haut des paramètres de paragraphe|Fonctionnalité|
|PSDNET-912|Changer la police et la couleur pour le calque de texte PSD|Bogue|
|PSDNET-1022|Export incorrect du texte dans les tests de mise à jour du texte, le texte est manquant|Bogue|
|PSDNET-1221|Le texte extrêmement petit est manquant après le redimensionnement de l'image PSD plus grande|Bogue|
|PSDNET-1301|Aspose.Psd pour .NET textLayer.UpdateText() imprime '-' (tiret) comme trait de soulignement de manière aléatoire pour différents ensembles de données|Bogue|
|PSDNET-1379|Les paramètres de résolution ne s'appliquent pas à l'exportation de PSD vers PDF|Bogue|


## **Changements de l'API publique**
# **APIs ajoutés:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **APIs supprimés:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manuel


## **Exemples d'utilisation:**

**PSDNET-912. Changer la police et la couleur pour le calque de texte PSD**

{{< highlight csharp >}}
string dossierPolices = "Fonts";
string fichierSrc = "M1PDTT26052021001.psd";
string sortiePsd = "resultat.psd";
string sortiePng = "resultat.png";

FontSettings.SetFontsFolder(dossierPolices);

using (var image = (PsdImage)Image.Load(fichierSrc))
{
    TextLayer calqueNom = (TextLayer)image.Layers[9];
    var portionTexte = calqueNom.TextData.Items[0];

    portionTexte.Text = "MODESTO SR";
    portionTexte.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    portionTexte.Style.FillColor = Color.Red;

    calqueNom.TextData.UpdateLayerData();

    image.Save(sortiePsd);
    image.Save(sortiePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Export incorrect du texte dans les tests de mise à jour du texte, le texte est manquant**

{{< highlight csharp >}}
string fichierSrc = "ComplexKerningExample.psd";
string sortiePsd = "TextUpdateComplexKerningExample_.psd";
string sortiePng = "TextUpdateComplexKerningExample_.png";

using (var image = (PsdImage)Image.Load(fichierSrc))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var calque = image.Layers[i] as TextLayer;

        if (calque != null)
        {
            calque.UpdateText("Le texte est mis à jour");
        }
    }

    image.Save(sortiePsd);
    image.Save(sortiePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Le texte extrêmement petit est manquant après le redimensionnement de l'image PSD plus grande**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Ajouter la capacité de traiter l'effet de déformation via l'API publique**

{{< highlight csharp >}}
string fichierSource = "source.psd";
string exportPngDeforme = "déformé.png";
string exportPsdDeforme = "fichierDéformé.psd";

var optionsChargementDeformation = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(fichierSource, optionsChargementDeformation))
{
    image.Save(exportPngDeforme, new PngOptions());
    image.Save(exportPsdDeforme, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd pour .NET textLayer.UpdateText() imprime '-' (tiret) comme trait de soulignement de manière aléatoire pour différents ensembles de données**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string sortie = "IMAGE_SORTIE.jpg";

using (PsdImage imagePsd = (PsdImage)Image.Load(src))
{
    foreach (var calque in imagePsd.Layers.Where(x => x.IsVisible))
    {
        if (calque is TextLayer)
        {
            TextLayer calqueTexte = calque as TextLayer;
            switch (calque.Name.Trim().ToUpper())
            {
                case "NOM":
                    calqueTexte.UpdateText("MR. JACK SMITH");
                    break;
                case "IDNO":
                    calqueTexte.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNATION":
                    calqueTexte.UpdateText("OFFICER-001");
                    break;
                case "GROUPE SANGUIN":
                    calqueTexte.UpdateText("AB-");
                    break;
                case "ADRESSE":
                    calqueTexte.UpdateText("BLOCK-A, RUE-7, APPARTEMENT N° - 047, SECTEUR-024");
                    break;
                case "ADRESSE PERMANENTE":
                    calqueTexte.UpdateText("N° MAISON - 42, RUE -025, SOCIÉTÉ DE LOGEMENT PALM GREENS VIEW, SECTEUR - 45");
                    break;
            }
        }
    }
    imagePsd.Save(sortie, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. Les paramètres de résolution ne s'appliquent pas à l'exportation de PSD vers PDF**

{{< highlight csharp >}}
string entrée = "Datensatz 1.psd";
string sortie = "Datensatz 1.pdf";

using (var image = Image.Load(entrée, new PsdLoadOptions()))
{
    ResolutionSetting paramètreResolution = new ResolutionSetting(300, 300);

    image.Save(sortie, new PdfOptions()
    {
        ResolutionSettings = paramètreResolution
    });
}
{{< /highlight >}}

**PSDNET-1391. Ajouter la prise en charge des modes de plomb de bas en bas et de haut en haut des paramètres de paragraphe**

{{< highlight csharp >}}
string entrée = "leadingMode.psd";
string sortie = "sortie_leadingMode.png";

using (var imagePsd = (PsdImage)Image.Load(entrée, new PsdLoadOptions()))
{
    IText texte1 = ((TextLayer)imagePsd.Layers[1]).TextData;
    foreach (var portionTexte in texte1.Items)
    {
        portionTexte.Paragraph.LeadingType = LeadingType.TopToTop; // Changer la valeur de LeadingType  
    }
    texte1.Items[8].Text = "TopToTop";
    texte1.Items[8].Style.FillColor = Color.ForestGreen;
    texte1.UpdateLayerData();

    IText texte2 = ((TextLayer)imagePsd.Layers[2]).TextData;
    foreach (var portionTexte in texte2.Items)
    {
        portionTexte.Paragraph.LeadingType = LeadingType.BottomToBottom; // Changer la valeur de LeadingType   
    }
    texte2.Items[8].Text = "BottomToBottom";
    texte2.Items[8].Style.FillColor = Color.ForestGreen;
    texte2.UpdateLayerData();

    imagePsd.Save(sortie, new PngOptions());
}
{{< /highlight >}}
