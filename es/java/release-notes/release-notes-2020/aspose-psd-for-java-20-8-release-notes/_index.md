---
title: Notas de la versión de Aspose.PSD para Java 20.8
type: docs
weight: 50
url: /es/java/aspose-psd-para-java-20-8-notas-de-version/
---

{{% alert color="primary" %}} Esta página contiene notas de lanzamiento para [Aspose.PSD para Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) {{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-264|Soporte de SoLdResource (recurso de datos de capa de objeto inteligente)|Característica|
|PSDJAVA-263|Soporte de PlLdResource (recurso de capa colocada para capa de objeto inteligente)|Característica|
|PSDJAVA-262|Añadir soporte de estructuras de Array de Objetos y Array de Unidades: firmas ObAr / UnFl|Característica|
|PSDJAVA-265|Subrayado y tachado perdidos después de enfocarse en el texto en archivo guardado con Aspose.|Error|
|PSDJAVA-257|Corregir guardado de imagen PSD modificada con modo de color CMYK de 16 bits por canal|Error|
|PSDJAVA-268|Regresión: Aspose.PSD 20.7.0 rompe tamaños de fuente para archivos antiguos|Error|

# **Cambios en la API Pública**
# **APIs Añadidas:**
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
- ...

# **Ejemplos de uso:**

**PSDJAVA-264. Soporte de SoLdResource (recurso de datos de capa de objeto inteligente)**
{{< highlight java >}}
// Este ejemplo muestra cómo obtener o establecer las propiedades de datos de capa de objeto inteligente del archivo PSD.

// Definir una clase local solo para mantener código reutilizable (métodos)
clase LocalScopeExtension
{
    boolean equals(Object a, Object b)
    {
        return (a == b) || (a != null && a.equals(b));
    }

    void assertAreEqual(Object actual, Object expected)
    {
        boolean areEqual = equals(actual, expected);
        // Comparar arrays si los hay
        if (!areEqual &&
                (actual != null && actual.getClass().isArray()) &&
                (expected != null && expected.getClass().isArray()))
        {
            int length;
            // Usar Reflexión para acceder a los arrays y soportar arrays de primitivos
            if ((length = Array.getLength(actual)) == Array.getLength(expected))
            {
                for (int i = 0; i < length; i++)
                {
                    if (!equals(Array.get(actual, i), Array.get(expected, i)))
                    {
                        break;
                    }
                }

                areEqual = true;
            }
        }

        if (!areEqual)
        {
            throw new FormatException(
                    String.format("El valor actual %s no es igual al esperado %s.", actual, expected));
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();

String srcPsdPath = "LayeredSmartObjects8bit2.psd";
String dstPsdPath = "LayeredSmartObjects8bit2_output.psd";

Object[][] expectedValues = new Object[][]{...};

// Cargar un archivo PSD predefinido que contiene SoLdResource
PsdImage image = (PsdImage)Image.load(srcPsdPath);
try
{
    SoLdResource resource = null;
    int index = 0;
    for (Layer imageLayer : image.getLayers())
    {
        for (LayerResource imageResource : imageLayer.getResources())
  ...
{{< /highlight >}}

... (¡Resto del contenido omitido por brevedad!)...
            {
                if (imageResource instanceof SoLdResource)
                {
                    resource = (SoLdResource)imageResource;
                    Object[] expectedValue = expectedValues[index++];
                    $.assertAreEqual(expectedValue[0], resource.isCustom());
                    $.assertAreEqual(expectedValue[1], resource.getUniqueId().toString());
                    $.assertAreEqual(expectedValue[2], resource.getPageNumber());
                    $.assertAreEqual(expectedValue[3], resource.getTotalPages());
                    $.assertAreEqual(expectedValue[4], resource.getAntiAliasPolicy());
                    $.assertAreEqual(expectedValue[5], resource.getPlacedLayerType());
                    $.assertAreEqual(8, resource.getTransformMatrix().length);
                    $.assertAreEqual(expectedValue[6], resource.getTransformMatrix());
                    $.assertAreEqual(expectedValue[7], resource.getValue());
                    $.assertAreEqual(expectedValue[8], resource.getPerspective());
                    $.assertAreEqual(expectedValue[9], resource.getPerspectiveOther());
                    $.assertAreEqual(expectedValue[10], resource.getTop());
                    $.assertAreEqual(expectedValue[11], resource.getLeft());
                    $.assertAreEqual(expectedValue[12], resource.getBottom());
                    $.assertAreEqual(expectedValue[13], resource.getRight());
                    $.assertAreEqual(expectedValue[14], resource.getUOrder());
                    $.assertAreEqual(expectedValue[15], resource.getVOrder());

                    $.assertAreEqual(expectedValue[16], resource.getCrop());
                    $.assertAreEqual(expectedValue[17], resource.getFrameStepNumerator());
                    $.assertAreEqual(expectedValue[18], resource.getFrameStepDenominator());
                    $.assertAreEqual(expectedValue[19], resource.getDurationNumerator());
                    $.assertAreEqual(expectedValue[20], resource.getDurationDenominator());
                    $.assertAreEqual(expectedValue[21], resource.getFrameCount());
                    $.assertAreEqual(expectedValue[22], resource.getWidth());
                    $.assertAreEqual(expectedValue[23], resource.getHeight());
                    $.assertAreEqual(expectedValue[24], resource.getResolution());
                    $.assertAreEqual(expectedValue[25], resource.getResolutionUnit());
                    $.assertAreEqual(expectedValue[26], resource.getComp());
                    $.assertAreEqual(expectedValue[27], resource.getCompId());
                    $.assertAreEqual(expectedValue[28], resource.getOriginalCompId());
                    $.assertAreEqual(expectedValue[29], resource.getPlacedId().toString());
                    $.assertAreEqual(expectedValue[30], resource.getNonAffineTransformMatrix());
                    if (resource.isCustom())
                    {
                        $.assertAreEqual(expectedValue[31], resource.getHorizontalMeshPointUnit());
                        $.assertAreEqual(expectedValue[32], resource.getHorizontalMeshPoints());
                        $.assertAreEqual(expectedValue[33], resource.getVerticalMeshPointUnit());
                        $.assertAreEqual(expectedValue[34], resource.getVerticalMeshPoints());
                        double[] temp = resource.getVerticalMeshPoints();
                        resource.setVerticalMeshPoints(resource.getHorizontalMeshPoints());
                        resource.setHorizontalMeshPoints(temp);
                    }

                    resource.setPageNumber(2);
                    resource.setTotalPages(3);
                    resource.setAntiAliasPolicy(0);
                    resource.setValue(1.23456789);
                    resource.setPerspective(0.123456789);
                    resource.setPerspectiveOther(0.987654321);
                    resource.setTop(-126);
                    resource.setLeft(-215);
                    resource.setBottom(248);
                    resource.setRight(145);
                    resource.setCrop(4);
                    resource.setFrameStepNumerator(1);
                    resource.setFrameStepDenominator(601);
                    resource.setDurationNumerator(2);
                    resource.setDurationDenominator(602);
                    resource.setFrameCount(11);
                    resource.setWidth(541);
                    resource.setHeight(249);
                    resource.setResolution(144);
                    resource.setComp(21);
                    resource.setCompId(22);
                    resource.setTransformMatrix(new double[]
                            {
                                12.937922786050663,
...
{{< /highlight >}}

**PSDJAVA-263. Soporte de PlLdResource (recurso de capa colocada para capa de objeto inteligente)**
{{< highlight java >}}
// Este ejemplo muestra cómo obtener o establecer las propiedades del recurso de capa colocada del archivo PSD.

// Define una clase local solo para mantener código reutilizable (métodos)
clase LocalScopeExtension
{
    boolean equals(Object a, Object b)
    {
        return (a == b) || (a != null && a.equals(b));
    }

    void assertAreEqual(Object actual, Object expected)
    {
        boolean areEqual = equals(actual, expected);
        // Comparar arrays si los hay
        if (!areEqual &&
...
{{< /highlight >}}