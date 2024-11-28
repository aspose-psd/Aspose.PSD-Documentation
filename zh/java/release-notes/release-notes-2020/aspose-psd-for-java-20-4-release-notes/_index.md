---
title: Aspose.PSD for Java 20.4 - 发行说明
type: docs
weight: 30
url: /zh/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} 本页包含了 [Aspose.PSD for Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) 的发行说明 {{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDJAVA-156|支持'Vector Origination Data'资源|特性|
|PSDJAVA-171|支持lclrResource（分页颜色设置）|特性|
|PSDJAVA-157|支持LengthRecord数据的属性。(路径操作（布尔运算），图层中形状的索引，贝塞尔结点记录的数量)|特性|
|PSDJAVA-158|支持图像部分资源 #1010 背景颜色|特性|
|PSDJAVA-161|运行时添加填充图层|特性|
|PSDJAVA-168|支持图像部分资源 #1009 边框信息|特性|
|PSDJAVA-169|支持AI格式文件中的图层|特性|
|PSDJAVA-163|支持渐变叠加图层效果的阅读和编辑|特性|
|PSDJAVA-164|渲染渐变叠加图层效果|特性|
|PSDJAVA-149|当获取文本图层的textData.items属性时，Aspose.PSD for Java错误|错误|
|PSDJAVA-166|修复使用灰度ColorMode和每通道16位的PSD图像保存为灰度PSD格式时的错误|错误|
|PSDJAVA-167|修复使用灰度ColorMode和每通道16位的PSD图像保存为PNG格式时的错误|错误|
|PSDJAVA-159|在Photoshop中未显示GradientOverlayEffect.BlendMode属性更改|错误|
# **公共 API 更改**
# **新增 API：**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **已移除 API：**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **用法示例：**

**PSDJAVA-156. 支持'Vector Origination Data'资源**

{{< highlight java >}}

 /*

一个示例，演示如何读取和修改一个Vector Origination Data资源。

*/

// 为简便起见，将方法保持在本地作用域中

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("未找到VogkResource。");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// 加载包含预定义VOGK资源的PSD文件

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // 在预定义图层的资源中查找第一个VogkResource

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // 验证预定义资源属性

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource读取错误。");

    }

    // 修改一些VogkResource属性

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // 在路径中保存已加载的PSD文件的修改副本

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. 支持lclrResource（分页颜色设置）**

{{< highlight java >}}

 /*

示例演示如何使用图层Sheet颜色来用颜色突出显示图层。例如，您可以更新PSD中的某些图层，然后通过颜色突出显示所需吸引注意的图层。

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // lcrl资源始终存在于psd文件资源列表中。

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("读取Sheet颜色错误");

                }

                // 文本颜色样式的逆转。设置图层颜色突出显示。

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// 在文件中，图层高亮颜色以这种顺序排列

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Red,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Yellow,

        SheetColorHighlightEnum.Green,

        SheetColorHighlightEnum.Blue,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gray,

        SheetColorHighlightEnum.NoColor

};

// 加载包含预定义LCRL资源的PSD文件

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// 加载刚保存的PSD文件

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // 反向颜色

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. 支持LengthRecord数据的属性。(路径操作（布尔运算），图层中形状的索引，贝塞尔结点记录的数量)**

{{< highlight java >}}

 /*

示例演示在与形状工作时更改路径操作的方式。该程序读取

一个预定义的矢量路径记录(LengthRecord)，然后更改其路径操作，然后将

修改后的文档另存为新的PSD文件。

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// 加载包含预定义VSMS资源的PSD文件

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // 在预定义图层的资源中查找第一个VsmsResource

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // 更改形状的组合方式

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // 在路径中保存已加载的PSD文件的修改副本

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. 支持图像部分资源 #1010 背景颜色**

{{< highlight java >}}

 /*

示例演示如何读取和修改背景颜色资源。

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// 加载包含预定义背景颜色资源的PSD文件

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("未找到BackgroundColorResource");

    }

    // 更新背景颜色资源的颜色

    backgroundColorResource.setColor(Color.getDarkRed());

    // 在路径中保存已加载的PSD文件的修改副本

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. 运行时添加填充图层**

{{< highlight java >}}

 /*

示例演示如何向Photoshop文档添加不同类型的填充图层。

*/

String outPsdFilePath = "output.psd";

// 创建具有空画布的Photoshop文档

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // 向PSD添加不同类型的填充图层

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Color Fill Layer");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Gradient Fill Layer");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Pattern Fill Layer");

    patternFillLayer.setOpacity((byte)50);

    psdImage.addLayer(patternFillLayer);

    // 在路径中保存已加载的PSD文件的修改副本

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-168. 支持图像部分资源 #1009 边框信息**

{{< highlight java >}}

 /*

示例演示如何读取、修改和保存包含边框信息的PSD文件。

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// 加载包含预定义图像资源的PSD文件

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    ResourceBlock[] imageResources = psdImage.getImageResources();

    // 在图像资源中查找第一个边框信息资源

    BorderInformationResource borderInfoResource = null;

    for (ResourceBlock imageResource : imageResources)

    {

        if (imageResource instanceof BorderInformationResource)

        {

            borderInfoResource = (BorderInformationResource)imageResource;

            break;

        }

    }

    // 更新边框信息资源的一些属性

    borderInfoResource.setWidth(0.1);

    borderInfoResource.setUnit(PhysicalUnit.Inches);

    // 在路径中保存已加载的PSD文件的修改副本

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-169. 支持AI格式文件中的图层**

{{< highlight java >}}

 /*

示例演示如