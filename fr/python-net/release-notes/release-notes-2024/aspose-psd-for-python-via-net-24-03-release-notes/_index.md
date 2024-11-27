---
title: Notes de publication Aspose.PSD pour Python via .NET 24.3
type: docs
weight: 10
url: /fr/net/aspose-psd-pour-python-via-net-24-3-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                          | **Catégorie**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [Format AI] Réduire le temps de chargement des grandes images AI multipages | Amélioration |
| PSDPYTHON-45 | Le fichier PSD devient illisible après la conversion de 8 bits en 16 bits |     Erreur     |
| PSDPYTHON-46 | Le fichier PSD devient illisible après la conversion de 8 bits en 32 bits |     Erreur     |
| PSDPYTHON-47 | [Format AI] Corriger le rendu de la courbe courte au fichier AI         |     Erreur     |



## **Changements d'API publique**
# **APIs ajoutées:**
- Aucune

# **APIs supprimées:**
- Aucune


## **Exemples d'utilisation:**

**PSDPYTHON-42. [Format AI] Réduire le temps de chargement des grandes images AI multipages**

{{< highlight python >}}
   # Aucun exemple
{{< /highlight >}}

**PSDPYTHON-45. Le fichier PSD devient illisible après la conversion de 8 bits à 16 bits**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # c'est bon
                pass
            else:
                raise Exception("Mauvaise ressource globale, la première ressource devrait être Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Le fichier PSD devient illisible après la conversion de 8 bits à 32 bits**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # c'est bon
                pass
            else:
                raise Exception("Mauvaise ressource globale, la première ressource devrait être Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Format AI] Corriger le rendu de la courbe courte au fichier AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
