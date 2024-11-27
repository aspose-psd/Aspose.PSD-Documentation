---
title: Notes de publication Aspose.PSD pour Java 21.6
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-21-6-notes-de-version/
---

{{% alert color="primary" %}} Cette page contient les notes de publication d'[Aspose.PSD pour Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-351|Le masque d'écrêtage pour un groupe ne se rend pas correctement|Bogue|
|PSDJAVA-352|Le masque régulier ou vectoriel pour un groupe de calques est ignoré lors du rendu|Bogue|
|PSDJAVA-353|L'image PSD avec des masques de calque vectoriels désactivés lors de l'enregistrement active les masques vectoriels|Bogue|
|PSDJAVA-354|Exception lors de la création d'un TextLayer avec un texte de plus de 255 caractères|Bogue|

# **Changements apportés à l'API publique**
# **API ajoutées:**
- Aucune

# **API supprimées:**
- Aucune

# **Exemples d'utilisation:**

**PSDJAVA-351. Le masque d'écrêtage pour un groupe ne se rend pas correctement**

{{< highlight java >}}
        String nomFichierSource = "AppleClip.psd";
        String nomFichierSortie = "result.png";

        PsdImage image = (PsdImage) Image.load(nomFichierSource);
        try
        {
            image.save(nomFichierSortie, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Le masque régulier ou vectoriel pour un groupe de calques est ignoré lors du rendu**

{{< highlight java >}}
        String nomFichierSource = "Stripes3Mask.psd";
        String nomFichierSortie = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage) Image.load(nomFichierSource);
        try
        {
            image.save(nomFichierSortie, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. L'image PSD avec des masques de calque vectoriels désactivés lors de l'enregistrement active les masques vectoriels**

{{< highlight java >}}
        String nomFichierSource = "FourWithMasksVd.psd";
        String nomFichierSortie = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(nomFichierSource);
        try
        {
            image.save(nomFichierSortie);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Exception lors de la création d'un TextLayer avec un texte de plus de 255 caractères**

{{< highlight java >}}
        String sortie = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String texte = new String(chars);
            image.addTextLayer(texte, Rectangle.getEmpty());

            image.save(sortie);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
