---
title: Aspose.PSD pour Java 23.6 - Notes de version
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-23-6-notes-de-version/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                                                                                      | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | Refactoriser l'API de la Chronologie                                                                                                            | Amélioration  |
| PSDJAVA-480 | Supprimer les artefacts lors du rendu de la déformation                                                                                         | Amélioration  |
| PSDJAVA-481 | Optimisation du rendu de la déformation                                                                                                         | Amélioration  |
| PSDJAVA-482 | Support de la Couche d'Ajustement de Seuil                                                                                                      | Fonctionnalité|
| PSDJAVA-483 | Support de la Couche d'Ajustement de Couleur Sélective                                                                                          | Fonctionnalité|
| PSDJAVA-484 | Possibilité d'exporter la Chronologie PSD vers le fichier Gif animé                                                                              | Fonctionnalité|
| PSDJAVA-485 | Ajout de la prise en charge des calques de texte sans bordures rectangulaires                                                                    | Fonctionnalité|
| PSDJAVA-486 | Support de la Couche de Forme                                                                                                                  | Fonctionnalité|
| PSDJAVA-487 | Le remplacement de l'image dans un objet intelligent n'est pas mis à jour                                                                        | Problème     |
| PSDJAVA-488 | Le fichier PSD ne peut pas être enregistré en PSD avec l'exception suivante: Les modes Rvb et Lab ne peuvent pas contenir moins de 3 canaux et plus de 4 canaux| Problème     |
| PSDJAVA-489 | La justification du texte est perdue si la couche de texte est ouverte en mode édition de Photoshop                                              | Problème     |
| PSDJAVA-490 | Exception de référence nulle lors de l'enregistrement d'un fichier PSD                                                                          | Problème     |
| PSDJAVA-491 | Exception lors du chargement de la couche de forme : Les points pour les limites d'origine vectorielle ne sont pas encore pris en charge              | Problème     |
| PSDJAVA-492 | Exception lors du chargement de VogkResource : Les points sont enregistrés en tant que DoubleStructures, nous les lisons en tant que UnitStructures | Problème     |
| PSDJAVA-493 | Le type de calque de la Couche de Forme est vide                                                                                               | Problème     |

## **Changements d'API publique**
# **APIs ajoutées :**
- M:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat,short)
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorMode
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.getSubResources
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.getPointsUnitType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.setPointsUnitType(int)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Horizontal
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Vertical
- M:com.aspose.psd.imageoptions.PsdOptions.isColorModeSet
- T:com.aspose.psd.fileformats.psd.layers.animation.Frame
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.#ctor
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getDelay
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getDisposalMethod
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getFrGA
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getId
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getLayerStates
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setDelay(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setDisposalMethod(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setFrGA(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setId(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setLayerStates(com.aspose.psd.fileformats.psd.layers.animation.LayerState[])
- T:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Dispose
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.DoNotDispose
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Automatic
- T:com.aspose.psd.fileformats.psd.layers.animation.LayerState
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.#ctor
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getBlendMode
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getFillOpacity
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getHorizontalFXRf
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getId
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getOpacity
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getPositionOffset
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getStateEffects
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getVerticalFXRf
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setFillOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setHorizontalFXRf(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setId(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setPositionOffset(com.aspose.psd.Point)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setVerticalFXRf(double)
- T:com.aspose.psd.fileformats.psd.layers.animation.Timeline
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.#ctor
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getAFSt
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getActiveFrameIndex
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrame(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrames
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFramesList
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFsID
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getLoopesCount
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getPsdImage
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(java.lang.String,com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(com.aspose.psd.system.io.Stream,com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setAFSt(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFrames(com.aspose.psd.fileformats.psd.layers.animation.Frame[])
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFsID(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setLoopesCount(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setPsdImage(com.aspose.psd.fileformats.psd.PsdImage)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.switchActiveFrame(int)
- T:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addColorOverlay
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addDropShadow
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addGradientOverlay
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addInnerShadow
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOuterGlow
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOrReplaceEffect(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addPatternOverlay
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getEffects
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getLayerStyleFX
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getScale
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setScale(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setVisible(boolean)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.clearLayerStyle
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.removeEffectAt(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.isVisible
- T:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getBlendMode
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getEffectType
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getIntensity
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getJitter
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getNoise
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getOpacity
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getRange
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSpread
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isAntiAliasing
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isSoftBlend
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isVisible
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setAntiAliasing(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setFillColor(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setIntensity(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setJitter(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setNoise(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setOpacity(byte)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setRange(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSpread(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSoftBlend(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setVisible(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

# **APIs supprimées :**

- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor(int)															   
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getKey																	  
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getPsdVersion																			 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

## **Exemples d'utilisation :**

**PSDJAVA-482. Support de la Couche d'Ajustement de Seuil**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String fichierSourceAvecCoucheSeuil = "fleurs_seuil_source.psd";
    String fichierPsdAvecCoucheSeuil = "fleurs_seuil_sortie.psd";
    String fichierPngAvecCoucheSeuil = "fleurs_seuil_sortie.png";

    String fichierSourceSansCoucheSeuil = "fleurs_source.psd";
    String fichierPsdSansCoucheSeuil = "fleurs_sortie.psd";
    String fichierPngSansCoucheSeuil = "fleurs_sortie.png";

    // Obtenir, vérifier et changer la couche d'ajustement du seuil de l'image.
    try (PsdImage image = (PsdImage) Image.load(fichierSourceAvecCoucheSeuilLayer thrsLayer = (ThresholdLayer) layer;
                short niveau = thrsLayer.getNiveau();
                
                // Vérifier les paramètres des calques.
                assertAreEqual(niveau, (short) 115);
                
                // Définir les paramètres des calques.
                thrsLayer.setNiveau((short) 50);
                
                image.save(fichierPsdAvecCoucheSeuil);
                image.save(fichierPngAvecCoucheSeuil, new PngOptions());
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
        
        // Ajouter et définir la couche d'ajustement du seuil à l'image.
        try (PsdImage image = (PsdImage) Image.load(fichierSourceSansCoucheSeuil)) {
            // Ajouter une couche d'ajustement du seuil.
            ThresholdLayer seuilLayer = image.addThresholdAdjustmentLayer();
            
            // Définir les paramètres des calques.
            seuilLayer.setNiveau((short) 115);
            
            image.save(fichierPsdSansCoucheSeuil);
            image.save(fichierPngSansCoucheSeuil, new PngOptions());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}

static void assertAreEqual(Object attendu, Object actuel) {
    assertAreEqual(attendu, actuel, "Les objets ne sont pas égaux.");
}
{{< /highlight >}}

**PSDJAVA-483. Support de la Couche d'Ajustement de Couleur Sélective**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String fichierSourceAvecCoucheCouleurSelective = "maisons_couleurSelective_source.psd";
    String fichierPsdAvecCoucheCouleurSelective = "maisons_couleurSelective_sortie.psd";
    String fichierPngAvecCoucheCouleurSelective = "maisons_couleurSelective_sortie.png";

    String fichierSourceSansCoucheCouleurSelective = "maisons_source.psd";
    String fichierPsdSansCoucheCouleurSelective = "maisons_sortie.psd";
    String fichierPngSansCoucheCouleurSelective = "maisons_sortie.png";

    // Obtenir, vérifier et changer la couche d'ajustement de couleur sélective de l'image.
    try (PsdImage image = (PsdImage) Image.load(fichierSourceAvecCoucheCouleurSelective)) {
        for (Layer layer : image.getLayers()) {
            if (layer instanceof SelectiveColorLayer) {
                // Obtenir la couche d'ajustement des couleurs sélectives.
                SelectiveColorLayer selcLayer = (SelectiveColorLayer) layer;
                CorrectionCmyk correctionRouge = selcLayer.getCorrectionCmyk(SelectiveColorsTypes.Rouges);
                CorrectionCmyk correctionJaune = selcLayer.getCorrectionCmyk(SelectiveColorsTypes.Jaunes);
                CorrectionCmyk correctionVert = selcLayer.getCorrectionCmyk(SelectiveColorsTypes.Vertes);
                CorrectionCmyk correctionBleu = selcLayer.getCorrectionCmyk(SelectiveColorsTypes.Bleues);

                // Vérifier les paramètres des calques.
                assertAreEqual(CorrectionMethodTypes.Absolu, selcLayer.getMethodeCorrection());

                assertAreEqual(correctionRouge.getCyan(), (short) -31);
                assertAreEqual(correctionRouge.getMagenta(), (short) -12);
                assertAreEqual(correctionRouge.getJaune(), (short) 27);
                assertAreEqual(correctionRouge.getNoir(), (short) 33);
                // Continuer ainsi pour les autres corrections...

                // Changer les paramètres des calques.
                selcLayer.setMethodeCorrection(CorrectionMethodTypes.Relatif);
                CorrectionCmyk correctionsRougesCmyk = new CorrectionCmyk();
                correctionsRougesCmyk.setCyan((short) 12);
                correctionsRougesCmyk.setMagenta((short) -20);
                correctionsRougesCmyk.setJaune((short) 10);
                correctionsRougesCmyk.setNoir((short) -15);
                selcLayer.setCorrectionCmyk(SelectiveColorsTypes.Rouges, correctionsRougesCmyk);

                // Enregistrer les images.
                image.save(fichierPsdAvecCoucheCouleurSelective);
                image.save(fichierPngAvecCoucheCouleurSelective, new PngOptions());
            }
        }
    } catch (Exception e) {
        e.printStackTrace();
    }

    // Ajouter et définir la couche d'ajustement de couleur sélective à l'image.
    try (PsdImage image = (PsdImage) Image.load(fichierSourceSansCoucheCouleurSelective)) {
        // Ajouter une couche d'ajustement de couleur sélective.
        SelectiveColorLayer coucheCouleurSelective = image.addSelectiveColorAdjustmentLayer();

        // Définir les paramètres des calques.
        coucheCouleurSelective.setMethodeCorrection(CorrectionMethodTypes.Absolu);

        // Continuer ainsi pour les autres corrections...

        image.save(fichierPsdSansCoucheCouleurSelective);
        image.save(fichierPngSansCoucheCouleurSelective, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}

static void assertAreEqual(Object attendu, Object actuel) {
    assertAreEqual(attendu, actuel, "Les objets ne sont pas égaux.");
}
{{< /highlight >}}