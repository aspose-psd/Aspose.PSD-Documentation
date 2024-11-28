---
title: Aspose.PSD для Java 20.8 - Примечания к выпуску
type: docs
weight: 50
url: /ru/java/aspose-psd-for-java-20-8-release-notes/
---

{{% alert color="primary" %}} Эта страница содержит примечания к выпуску [Aspose.PSD для Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) {{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDJAVA-264|Поддержка SoLdResource (ресурс данных умного объектного слоя)|Функция|
|PSDJAVA-263|Поддержка PlLdResource (размещенный ресурс слоя для умного объектного слоя)|Функция|
|PSDJAVA-262|Добавлена поддержка массива объектов и структур массива единиц: сигнатуры ObAr / UnFl|Функция|
|PSDJAVA-265|Подчеркивание и перечеркивание теряются после фокусировки на тексте в файле, сохраненном с помощью Aspose.|Ошибка|
|PSDJAVA-257|Исправление сохранения измененного изображения PSD с цветовым режимом CMYK 16 бит на канал|Ошибка|
|PSDJAVA-268|Регрессия: Aspose.PSD 20.7.0 нарушает размеры шрифтов для старых файлов|Ошибка|

# **Изменения в общем API**
# **Добавленные API:**
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setAntiAliasPolicy(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setBottom(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setBounds(com.aspose.psd.Rectangle)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setHorizontalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setHorizontalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setItems(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[])
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPageNumber
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPerspective
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPerspectiveOther
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPlacedId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPlacedLayerType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getResolution
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getResolutionUnit
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.getWidth
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.isCustom
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setAntiAliasPolicy(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setBottom(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setBounds(com.aspose.psd.Rectangle)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setComp(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setCrop(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setCustom(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setDurationDenominator(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setDurationNumerator(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setFrameCount(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setFrameStepDenominator(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setFrameStepNumerator(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setHeight(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setHorizontalMeshPointUnit(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setHorizontalMeshPoints(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setItems(com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setLeft(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setNonAffineTransformMatrix(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.setPageNumber(int)
- M:com.aspose.psd.fileformats. ...

**Примеры использования:**

**PSDJAVA-264. Поддержка SoLdResource (ресурс данных умного объектного слоя)**
{{< highlight java >}}
// Этот пример показывает, как получить или установить свойства ресурса данных умного объектного слоя файла PSD.

// Определение локального класса для хранения повторно используемого кода (методов)
class LocalScopeExtension
{
    boolean equals(Object a, Object b)
    {
        return (a == b) || (a != null && a.equals(b));
    }

    void assertAreEqual(Object actual, Object expected)
    {
        boolean areEqual = equals(actual, expected);
        // Сравнить массивы, если они есть
        if (!areEqual &&
                (actual != null && actual.getClass().isArray()) &&
                (expected != null && expected.getClass().isArray()))
        {
            int length;
            // Использовать Reflection для доступа к массивам для поддержки массивов примитивов
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
                    String.format("Фактическое значение %s не равно ожидаемому %s.", actual, expected));
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();

String srcPsdPath = "LayeredSmartObjects8bit2.psd";
String dstPsdPath = "LayeredSmartObjects8bit2_output.psd";

Object[][] expectedValues = new Object[][]...
...
{{< /highlight >}}

**PSDJAVA-263. Поддержка PlLdResource (размещенный ресурс слоя для умного объектного слоя)**
{{< highlight java >}}
// Этот пример показывает, как получить или установить свойстваразмещенного ресурса слоя для умного объектного слоя файла PSD.

// Создайте объект изображения
com.aspose.psd.Image image = new com.aspose.psd.Image(200, 200);

// Сделайте слой заполнения
com.aspose.psd.fileformats.psd.layers.FillLayer fillLayer = (com.aspose.psd.fileformats.psd.layers.FillLayer)image.getLayers().add(com.aspose.psd.fileformats.psd.layers.LayerType.FillLayer);

// Установите цвет заливки
fillLayer.getColor().setRgb(new com.aspose.psd.Color(255, 0, 0));

// Cработаем с PlLdResource
com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource plLdResource = new com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource(true);

// Задаем образ
plLdResource.setImages(new com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdImageResource[]{
    new com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdImageResource(new com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure(), com.aspose.psd.StreamContainer.createFileInstance("src\\plldImage.psd"))
});

//Задаем метатеги
plLdResource.setMetaData(toString(new Object[][]{
    new Object[] { "Transform", "1.000000,0.000000,0.000000,0.000000,1.000000,0.000000,0.000000,0.000000,1.000000"},
    new Object[] { "Comp", 65535},
    new Object[] { "FrameStepDenominator", 1},
    new Object[] { "FrameStepNumerator", 1},
    new Object[] { "DurationDenominator", 25},
    new Object[] { "DurationNumerator", 1},
    new Object[] { "PlacedID", 2109610677}
}));

fillLayer.getLayerResources().add(plLdResource);

// Сохраните изображение в формате PNG
image.save("output.png", new com.aspose.psd.imageoptions.PngOptions());

{{< /highlight >}}

**PSDJAVA-262. Добавлена поддержка массива объектов и структур массива единиц: сигнатуры ObAr / UnFl**
{{< highlight java >}}
// Этот пример показывает, как работать с массивом объектов и структурами массива единиц
com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure objectArrayStructure = 
    new com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure();
objectArrayStructure.setSize(4);

com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[] osTypeStructures = new com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[]
{
    new com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure(),
    new com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure()
};

objectArrayStructure.setArray(osTypeStructures);
objectArrayStructure.setVersion(1);

com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure unitArrayStructure = new com.asjson.java.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure();
unitArrayStructure.setSize(4);

com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[] unitOSTypeStructures = new com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure[]
{
    new com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure(),
    new com.aspose.psd.fileformats.psd.layers.layerresources.OSTypeStructure()
};

unitArrayStructure.setArray(unitOSTypeStructures);
unitArrayStructure.setVersion(1);
{{< /highlight >}}