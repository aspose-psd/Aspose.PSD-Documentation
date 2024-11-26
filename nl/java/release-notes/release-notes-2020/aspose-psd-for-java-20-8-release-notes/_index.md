---
title: Aspose.PSD voor Java 20.8 - Release-opmerkingen
type: docs
weight: 50
url: /nl/java/aspose-psd-voor-java-20-8-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-voor-java-20.8/) {{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDJAVA-264|Ondersteuning van SoLdResource (Smart Object Layer Data resource)|Functie|
|PSDJAVA-263|Ondersteuning van PlLdResource (geplaatste laagresource voor Slim Objectlaag)|Functie|
|PSDJAVA-262|Ondersteuning toevoegen voor Structuren van Object Array en Unit Array: ObAr / UnFl handtekeningen|Functie|
|PSDJAVA-265|Onderstrepen en doorhalen verdwijnen na focus op de tekst in het bestand dat is opgeslagen met Aspose.|Fout|
|PSDJAVA-257|Oplossing voor opslaan van gewijzigde PSD-afbeelding met CMYK ColorMode 16 bit per kanaal|Fout|
|PSDJAVA-268|Regresie: Aspose.PSD 20.7.0 breekt lettergroottes voor oudere bestanden|Fout|

# **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.ImageStack
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Raster
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Unknown
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Vector
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.AntiAliasPolicyKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure.StructureKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure.StructureKey
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ClassID.#ctor(byte[],boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getAntiAliasPolicy
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getBottom
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getBounds
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getHorizontalMeshPointUnit
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getHorizontalMeshPoints
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getItems
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getLeft
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPageNumber
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPerspective
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPerspectiveOther
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPlacedLayerType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getRight
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTop
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTotalPages
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTransformMatrix
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getUOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getValue
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVerticalMeshPointUnit
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVerticalMeshPoints
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.isCustom
- M:com.aspose.	psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setAntiAliasPolicy(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setBottom(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setBounds(com.aspose.psd.Rectangle)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setCustom(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setHorizontalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setHorizontalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setItems(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setLeft(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPageNumber(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPerspective(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPerspectiveOther(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPlacedLayerType(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setRight(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setTop(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setTotalPages(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setTransformMatrix(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setUOrder(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setVOrder(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setValue(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setVerticalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setVerticalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.#ctor(java.util.UUID,boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getAntiAliasPolicy
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getBottom
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getBounds
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getHorizontalMeshPointUnit
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getHorizontalMeshPoints
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getItems
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getLeft
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPageNumber
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPerspective
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPerspectiveOther
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPlacedLayerType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getRight
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getTop
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getTotalPages
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getTransformMatrix
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getUOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getValue
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVerticalMeshPointUnit
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVerticalMeshPoints
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.get_Item(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.isCustom
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setAntiAliasPolicy(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setBottom(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setBounds(com.aspose.psd.Rectangle)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setCustom(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setHorizontalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setHorizontalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setItems(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setLeft(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPageNumber(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPerspective(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPerspectiveOther(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPlacedLayerType(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setRight(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setTop(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setTotalPages(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setTransformMatrix(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setUOrder(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVOrder(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setValue(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVerticalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVerticalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.#ctor(java.util.UUID,boolean,boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getAntiAliasPolicy
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getBottom
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getBounds
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getComp
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getCrop
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getDurationDenominator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getDurationNumerator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getFrameCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getFrameStepDenominator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getFrameStepNumerator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getHeight
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getHorizontalMeshPointUnit
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getHorizontalMeshPoints
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getItems
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getLeft
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPageNumber
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPerspective
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPerspectiveOther
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPlacedLayerType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getRight
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getTop
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getTotalPages
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getTransformMatrix
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getUOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getVOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getValue
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getVerticalMeshPointUnit
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getVerticalMeshPoints
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setHeight(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setHorizontalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setHorizontalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setItems(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setLeft(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setPageNumber(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setPerspective(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setPerspectiveOther(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setPlacedLayerType(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setRight(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setSignature(com.aspose.psd.fileformats.psd.layers.layerresources.OSType)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setTop(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setTotalPages(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setTransformMatrix(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setUOrder(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setVOrder(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setValue(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setVerticalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setVerticalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.save(com.aspose.psd.StreamContainer,int)

{{% alert color="info" %}} Aan de slag met de laatste versie van Aspose.PSD voor Java op [downloads.aspose.com](https://downloads.aspose.com/psd/java) {{% /alert %}}