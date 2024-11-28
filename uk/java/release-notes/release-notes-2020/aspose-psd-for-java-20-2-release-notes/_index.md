---
title: Aspose.PSD для Java 20.2 - Примітки до випуску
type: docs
weight: 20
url: /uk/java/aspose-psd-for-java-20-2-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до випуску для [Aspose.PSD для Java 20.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-96|Покращення можливості відображення тексту різних кольорів у шарі тексту|Функція|
|PSDJAVA-97|Підтримка ресурсу clbl (ресурс шару містить інформацію про елементи обрізання переходу)|Функція|
|PSDJAVA-100|Підтримка ресурсу blwh (ресурс містить дані про шар налаштувань чорного та білого)|Функція|
|PSDJAVA-101|Можливість експорту групи шарів у форматах Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Функція|
|PSDJAVA-105|Підтримка ресурсу lspf (Містить налаштування щодо захищеного налаштування шару)|Функція|
|PSDJAVA-106|Підтримка ресурсу infx (Містить дані про злиття внутрішніх елементів)|Функція|
|PSDJAVA-99|Рефакторинг PsdImage та Layer для зміни поведінки трансформації (Правильне змінення розміру/обертання/обрізання для масок шарів, якщо ми трансформуємо один шар окремо)|Покращення|
|PSDJAVA-98|В деяких налаштуваннях глобалізації растровий зображення AI не може бути відкрито|Помилка|
|PSDJAVA-102|Після виконання операції FlipRotate на шарі, зображення PSD стає нечитабельним|Помилка|
|PSDJAVA-103|System.ArgumentException під час завантаження файлу PSD|Помилка|
|PSDJAVA-104|Після використання методу трансформації лише для шару, збережений шар має неправильні межі або маску|Помилка|
# **Зміни в публічному API**
# **Це API тимчасово вимкнено і буде ввімкнено у наступному випуску:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)

` `**Тимчасово використовуйте v19.4, якщо у вас є відповідна залежність.**
# **Додані API:**
- M:com.aspose.psd.Color.op_Equality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.Color.op_Inequality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.CustomLineCap.getStrokeCaps(int[],int[])
- M:com.aspose.psd.DisposableObject.finalize
- F:com.aspose.psd.FileFormat.Otg
- M:com.aspose.psd.FileStreamContainer.to_FileStream(com.aspose.psd.FileStreamContainer)
- M:com.aspose.psd.FileStreamContainer.to_Stream(com.aspose.psd.FileStreamContainer)
- M:com.aspose.psd.Font.#ctor
- M:com.aspose.psd.Image.doAfterCreate(long[],long)
- M:com.aspose.psd.Image.doAfterLoad(long[],java.io.InputStream)
- M:com.aspose.psd.Image.getProgressEventHandler
- M:com.aspose.psd.Image.getProgressEventHandlerInfo
- M:com.aspose.psd.ImageOptionsBase.getProgressEventHandler
- M:com.aspose.psd.ImageOptionsBase.setProgressEventHandler(com.aspose.psd.ProgressEventHandler)
- T:com.aspose.psd.InterpolationMode
- F:com.aspose.psd.InterpolationMode.Bicubic
- F:com.aspose.psd.InterpolationMode.Bilinear
- F:com.aspose.psd.InterpolationMode.Default
- F:com.aspose.psd.InterpolationMode.High
- F:com.aspose.psd.InterpolationMode.HighQualityBicubic
- F:com.aspose.psd.InterpolationMode.HighQualityBilinear
- F:com.aspose.psd.InterpolationMode.Invalid
- F:com.aspose.psd.InterpolationMode.Low
- F:com.aspose.psd.InterpolationMode.NearestNeighbor
- M:com.aspose.psd.LoadOptions.getProgressEventHandler
- M:com.aspose.psd.LoadOptions.setProgressEventHandler(com.aspose.psd.ProgressEventHandler)
- F:com.aspose.psd.Matrix.TypeFlip
- F:com.aspose.psd.Matrix.TypeGeneralRotation
- F:com.aspose.psd.Matrix.TypeGeneralScale
- F:com.aspose.psd.Matrix.TypeGeneralTransform
- F:com.aspose.psd.Matrix.TypeIdentity
- F:com.aspose.psd.Matrix.TypeMaskRotation
- F:com.aspose.psd.Matrix.TypeMaskScale
- F:com.aspose.psd.Matrix.TypeQuadrantRotation
- F:com.aspose.psd.Matrix.TypeTranslation
- F:com.aspose.psd.Matrix.TypeUniformScale
- M:com.aspose.psd.Matrix.#ctor(com.aspose.psd.Matrix)
- M:com.aspose.psd.Matrix.#ctor(com.aspose.psd.Rectangle,com.aspose.psd.Point[])
- M:com.aspose.psd.Matrix.#ctor(com.aspose.psd.RectangleF,com.aspose.psd.PointF[])
- M:com.aspose.psd.Matrix.#ctor(float,float,float,float,float,float)
- M:com.aspose.psd.Matrix.equals(com.aspose.psd.Matrix,com.aspose.psd.Matrix)
- M:com.aspose.psd.Matrix.getElements
- M:com.aspose.psd.Matrix.getM11
- M:com.aspose.psd.Matrix.getM12
- M:com.aspose.psd.Matrix.getM21
- M:com.aspose.psd.Matrix.getM22
- M:com.aspose.psd.Matrix.getM31
- M:com.aspose.psd.Matrix.getM32
- M:com.aspose.psd.Matrix.multiply(com.aspose.psd.Matrix)
- M:com.aspose.psd.Matrix.multiply(com.aspose.psd.Matrix,int)
- M:com.aspose.psd.Matrix.reset
- M:com.aspose.psd.Matrix.rotate(float)
- M:com.aspose.psd.Matrix.rotate(float,int)
- M:com.aspose.psd.Matrix.rotateAt(float,com.aspose.psd.PointF)
- M:com.aspose.psd.Matrix.rotateAt(float,com.aspose.psd.PointF,int)
- M:com.aspose.psd.Matrix.scale(float,float)
- M:com.aspose.psd.Matrix.scale(float,float,int)
- M:com.aspose.psd.Matrix.transformPoints(com.aspose.psd.PointF[])
- M:com.aspose.psd.Matrix.translate(float,float)
- M:com.aspose.psd.Matrix.translate(float,float,int)
- M:com.aspose.psd.Metered.equals(java.lang.Object)
- M:com.aspose.psd.NonGenericDictionary.copyTo(com.aspose.psd.internal.aL.g,int)
- M:com.aspose.psd.NonGenericList.copyTo(com.aspose.psd.internal.aL.g,int)
- M:com.aspose.psd.PixelDataFormat.op_Equality(com.aspose.psd.PixelDataFormat,com.aspose.psd.PixelDataFormat)
- M:com.aspose.psd.PixelDataFormat.op_Inequality(com.aspose.psd.PixelDataFormat,com.aspose.psd.PixelDataFormat)
- M:com.aspose.psd.Point.op_Addition(com.aspose.psd.Point,com.aspose.psd.Size)
- M:com.aspose.psd.Point.op_Equality(com.aspose.psd.Point,com.aspose.psd.Point)
- M:com.aspose.psd.Point.op_Inequality(com.aspose.psd.Point,com.aspose.psd.Point)
- M:com.aspose.psd.Point.op_Subtraction(com.aspose.psd.Point,com.aspose.psd.Size)
- M:com.aspose.psd.Point.to_PointF(com.aspose.psd.Point)
- M:com.aspose.psd.Point.to_Size(com.aspose.psd.Point)
- M:com.aspose.psd.PointF.op_Addition(com.aspose.psd.PointF,com.aspose.psd.Size)
- M:com.aspose.psd.PointF.op_Addition(com.aspose.psd.PointF,com.aspose.psd.SizeF)
- M:com.aspose.psd.PointF.op_Equality(com.aspose.psd.PointF,com.aspose.psd.PointF)
- M:com.aspose.psd.PointF.op_Inequality(com.aspose.psd.PointF,com.aspose.psd.PointF)
- M:com.aspose.psd.PointF.op_Subtraction(com.aspose.psd.PointF,com.aspose.psd.Size)
- M:com.aspose.psd.PointF.op_Subtraction(com.aspose.psd.PointF,com.aspose.psd.SizeF)
- T:com.aspose.psd.ProgressEventHandler
- M:com.aspose.psd.ProgressEventHandler.#ctor
- M:com.aspose.psd.ProgressEventHandler.beginInvoke(com.aspose.psd.progressmanagement.ProgressEventHandlerInfo,com.aspose.psd.system.AsyncCallback,java.lang.Object)
- M:com.aspose.psd.ProgressEventHandler.endInvoke(com.aspose.psd.system.IAsyncResult)
- M:com.aspose.psd.ProgressEventHandler.invoke(com.aspose.psd.progressmanagement.ProgressEventHandlerInfo)
- M:com.aspose.psd.RasterImage.getSkewAngle
- M:com.aspose.psd.RasterImage.normalizeAngle
- M:com.aspose.psd.RasterImage.normalizeAngle(boolean,com.aspose.psd.Color)
- M:com.aspose.psd.RawDataSettings.getColorPalette
- M:com.aspose.psd.RawDataSettings.getCustomColorConverter
- M:com.aspose.psd.RawDataSettings.getDitheringMethod
- M:com.aspose.psd.RawDataSettings.getFallbackIndex
- M:com.aspose.psd.RawDataSettings.getIndexedColorConverter
- M:com.aspose.psd.RawDataSettings.getLineSize
- M:com.aspose.psd.RawDataSettings.getPixelDataFormat
- M:com.aspose.psd.RawDataSettings.setColorPalette(com.aspose.psd.IColorPalette)
- M:com.aspose.psd.RawDataSettings.setCustomColorConverter(com.aspose.psd.IColorConverter)
- M:com.aspose.psd.RawDataSettings.setDitheringMethod(int)
- M:com.aspose.psd.RawDataSettings.setFallbackIndex(int)
- M:com.aspose.psd.RawDataSettings.setIndexedColorConverter(com.aspose.psd.IIndexedColorConverter)
- M:com.aspose.psd.RawDataSettings.setLineSize(int)
- M:com.aspose.psd.RawDataSettings.setPixelDataFormat(com.aspose.psd.PixelDataFormat)
- M:com.aspose.psd.Rectangle.op_Equality(com.aspose.psd.Rectangle,com.aspose.psd.Rectangle)
- M:com.aspose.psd.Rectangle.op_Inequality(com.aspose.psd.Rectangle,com.aspose.psd.Rectangle)
- M:com.aspose.psd.RectangleF.op_Equality(com.aspose.psd.RectangleF,com.aspose.psd.RectangleF)
- M:com.aspose.psd.RectangleF.op_Inequality(com.aspose.psd.RectangleF,com.aspose.psd.RectangleF)
- M:com.aspose.psd.RectangleF.to_RectangleF(com.aspose.psd.Rectangle)
- M:com.aspose.psd.Size.op_Addition(com.aspose.psd.Size,com.aspose.psd.Size)
- M:com.aspose.psd.Size.op_Equality(com.aspose.psd.Size,com.aspose.psd.Size)
- M:com.aspose.psd.Size.op_Inequality(com.aspose.psd.Size,com.aspose.psd.Size)
- M:com.aspose.psd.Size.op_Subtraction(com.aspose.psd.Size,com.aspose.psd.Size)
- M:com.aspose.psd.Size.to_Point(com.aspose.psd.Size)
- M:com.aspose.psd.Size.to_SizeF(com.aspose.psd.Size)
- M:com.aspose.psd.SizeF.op_Addition(com.aspose.psd.SizeF,com.aspose.psd.SizeF)
- M:com.aspose.psd.SizeF.op_Equality(com.aspose.psd.SizeF,com.aspose.psd.SizeF)
- M:com.aspose.psd.SizeF.op_Inequality(com.aspose.psd.SizeF,com.aspose.psd.SizeF)
- M:com.aspose.psd.SizeF.op_Subtraction(com.aspose.psd.SizeF,com.aspose.psd.SizeF)
- M:com.aspose.psd.SizeF.to_PointF(com.aspose.psd.SizeF)
- M:com.aspose.psd.StreamContainer.to_Stream(com.aspose.psd.StreamContainer)
- T:com.aspose.psd.coreexceptions.IndexOutOFRangeException
- M:com.aspose.psd.coreexceptions.IndexOutOFRangeException.#ctor(java.lang.String)
- M:com.aspose.psd.coreexceptions.IndexOutOFRangeException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.fileformats.ai.AiDataSection.releaseManagedResources
- T:com.aspose.psd.fileformats.jpeg2000.Jpeg2000CustomException
- M:com.aspose.psd.fileformats.jpeg2000.Jpeg2000CustomException.#ctor(java.lang.String)
- M:com.aspose.psd.fileformats.psd.PsdImage.addRegularLayer
- M:com.aspose.psd.fileformats.psd.ResourceBlock.getID
- M:com.aspose.psd.fileformats.psd.ResourceBlock.setID(short)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getHeight
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getWidth
- M:com.aspose.psd.fileformats.psd.layers.LayerMaskDataFull.getUserMaskRectangle
- M:com.aspose.psd.fileformats.psd.layers.LayerMaskDataFull.setUserMaskRectangle(com.aspose.psd.Rectangle)
- T:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry
- M:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry.#ctor
- M:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry.getFirstSupportedDescriptor(java.io.InputStream,int)
- M:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry.getFirstSupportedDescriptorByTypeName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry.getRegisteredDescriptors
- M:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry.loadResourceByFirstSupportedDescriptor(java.io.InputStream,int)
- M:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry.registerOpener(com.aspose.psd.fileformats.psd.layers.ILayerResourceLoader)
- M:com.aspose.psd.fileformats.psd.layers.LayerResourcesRegistry.unregisterOpener(com.aspose.psd.fileformats.psd.layers.ILayerResourceLoader)
- T:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getBlackAndWhitePresetFileName
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getBlues
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getBwPresetKind
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getCyans
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getGreens
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getMagentas
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getReds
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getTintColor
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getTintColorBlue
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.getTintColorGreen
-**Баги:**
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.setTintColorRed(double)
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.setTintColorGreen(double)
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.setTintColorBlue(double)
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.setUseTint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BlackWhiteAdjustmentLayer.setYellows(int)
- F:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType.Angle
- T:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource
- F:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getBlackAndWhitePresetFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getBlues
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getBwPresetKind
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getCyans
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getGreens
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getMagentas
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getReds
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getTintColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getUseTint
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.getYellows
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.setBlackAndWhitePresetFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.setBlues(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.BlwhResource.setBwPresetKind(int)

**Видалені API:**
- F:com.aspose.psd.xmp.types.derived.RenditionClass.DefinedValues
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.#ctor(int)
- T:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.#ctor
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuides
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGuides(com.aspose.psd.fileformats.psd.resources.GuideResource[])
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGuideCount
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getHeaderVersion
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setHeaderVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleX
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleX(int)
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.getGridCycleY
- M:com.aspose.psd.fileformats.psd.resources.GridAndGuidesResouce.setGridCycleY(int)
- M:com.aspose.psd