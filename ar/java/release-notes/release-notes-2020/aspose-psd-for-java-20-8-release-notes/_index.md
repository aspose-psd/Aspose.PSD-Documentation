---
title: تحديثات Aspose.PSD for Java 20.8
type: docs
weight: 50
url: /ar/java/aspose-psd-for-java-20-8-release-notes/
---

{{% alert color="primary" %}} هذه الصفحة تحتوي على تحديثات إصدار [Aspose.PSD for Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) {{% /alert %}} 

| **المفتاح** | **الملخص** | **الفئة** |
| :- | :- | :- |
| PSDJAVA-264 | دعم SoLdResource (بيانات مصدر طبقة الكائن الذكية) | ميزة |
| PSDJAVA-263 | دعم PlLdResource (مصدر طبقة المكان) لطبقة الكائن الذكي | ميزة |
| PSDJAVA-262 | إضافة دعم لهياكل الـ Object Array و Unit Array: توقيعات ObAr / UnFl | ميزة |
| PSDJAVA-265 | فقد النُقَط والتشطيب بعد التركيز على النص في الملف المحفوظ باستخدام Aspose | خطأ |
| PSDJAVA-257 | إصلاح حفظ صورة PSD المعدّلة بنمط الألوان CMYK و16 بت لكل قناة | خطأ |
| PSDJAVA-268 | تراجع: Aspose.PSD 20.7.0 يعطل أحجام الخط لملفات أقدم | خطأ |

# **تغييرات الواجهة البرمجية العامة**
# **الواجهات الجديدة:**
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.TypeToolKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.ImageStack
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Raster
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Unknown
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Vector
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.AntiAliasPolicyKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.TypeToolKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure.StructureKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure.StructureKey
- M: com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.ClassID.#ctor(byte[],boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getAntiAliasPolicy
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getBottom
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getBounds
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getHorizontalMeshPointUnit
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getHorizontalMeshPoints
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getItems
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getLeft
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPageNumber
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPerspective
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPerspectiveOther
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getPlacedLayerType
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getRight
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTop
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTotalPages
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTransformMatrix
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getUOrder
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getUniqueId
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVOrder
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getValue
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVerticalMeshPointUnit
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVerticalMeshPoints
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.isCustom
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setAntiAliasPolicy(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setBottom(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setBounds(com.aspose.psd.Rectangle)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setCustom(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setHorizontalMeshPointUnit(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setHorizontalMeshPoints(double[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setItems(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setLeft(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPageNumber(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPerspective(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPerspectiveOther(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setPlacedLayerType(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setRight(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setTop(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setTotalPages(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setTransformMatrix(double[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setUOrder(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setUniqueId(java.util.UUID)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setVOrder(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setValue(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setVerticalMeshPointUnit(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setVerticalMeshPoints(double[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.#ctor
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.#ctor(java.util.UUID,boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getAntiAliasPolicy
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getBottom
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getBounds
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getHorizontalMeshPointUnit
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getHorizontalMeshPoints
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getItems
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getKey
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getLeft
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getLength
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPageNumber
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPerspective
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPerspectiveOther
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPlacedLayerType
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getPsdVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getRight
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getSignature
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getTop
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getTotalPages
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getTransformMatrix
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getUOrder
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getUniqueId
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVOrder
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getValue
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVerticalMeshPointUnit
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.getVerticalMeshPoints
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.get_Item(java.lang.String)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.isCustom
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.save(com.aspose.psd.StreamContainer,int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setAntiAliasPolicy(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setBottom(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setBounds(com.aspose.psd.Rectangle)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setCustom(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setHorizontalMeshPointUnit(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setHorizontalMeshPoints(double[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setItems(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setLeft(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPageNumber(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPerspective(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPerspectiveOther(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setPlacedLayerType(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setRight(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setTop(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setTotalPages(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setTransformMatrix(double[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setUOrder(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setUniqueId(java.util.UUID)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVOrder(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setValue(double)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVersion(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVerticalMeshPointUnit(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.setVerticalMeshPoints(double[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.#ctor
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.#ctor(java.util.UUID,boolean,boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getAntiAliasPolicy
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getBottom
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getBounds
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getComp
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getCompId
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getCrop
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getDurationDenominator
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources