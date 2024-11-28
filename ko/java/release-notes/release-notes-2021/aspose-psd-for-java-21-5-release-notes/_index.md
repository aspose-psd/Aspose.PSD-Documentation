---
title: Aspose.PSD for Java 21.5 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-21-5-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 21.5]의 릴리스 노트가 포함되어 있습니다. (https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
이것은 Aspose.PSD for Java의 중간 릴리스입니다.
일부 알려진 문제점이 있습니다. 따라서 안정적인 버전이 필요한 경우 [Aspose.PSD 20.9] (https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/)를 사용하십시오. Aspose.PSD 21.6이 출시될 때까지 이 릴리스는 모든 Aspose.PSD .Net 기능 (스마트 객체 포함)을 포함하며 아래 기능을 추가로 제공합니다.
{{% /alert %}} 

|**키**|**요약**|**범주**|
| :- | :- | :- |
|PSDJAVA-340|레이어가 리사이징 될 때 벡터 경로를 포함하는 모양 레이어 크기 조정 지원|기능|
|PSDJAVA-341|벡터 경로를 포함하는 모양 레이어 크기 조정 지원|기능|
|PSDJAVA-342|잘린 텍스트 문자열|버그|

# **공개 API 변경**
# **추가된 API:**
- M:com.aspose.psd.CmykColor.isEquals(com.aspose.psd.CmykColor,com.aspose.psd.CmykColor)
- M:com.aspose.psd.Color.isEquals(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.ColorPaletteHelper.getCloseImagePalette(com.aspose.psd.RasterImage,com.aspose.psd.Rectangle,int,boolean)
- M:com.aspose.psd.ColorPaletteHelper.hasTransparentColors(com.aspose.psd.IColorPalette)
- T:com.aspose.psd.CompositeException
- T:com.aspose.psd.CurrentThreadSettings
- M:com.aspose.psd.CurrentThreadSettings.getLocale
- M:com.aspose.psd.CurrentThreadSettings.setLocale(java.lang.String)
- M:com.aspose.psd.CurrentThreadSettings.setLocale(java.util.Locale)
- M:com.aspose.psd.DataStreamSupporter.save(java.io.RandomAccessFile)
- M:com.aspose.psd.DataStreamSupporter.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.DisposableObject.close
- M:com.aspose.psd.Font.makeFontWithGraphUnit(java.lang.String,float,int)
- M:com.aspose.psd.FontSettings.addFontsFolder(java.lang.String)
- M:com.aspose.psd.FontSettings.removeFontsFolder(java.lang.String)
- M:com.aspose.psd.FontSettings.setFontsFolders(java.lang.String[])
- M:com.aspose.psd.Image.create(com.aspose.psd.Image[])
- M:com.aspose.psd.Image.create(com.aspose.psd.Image[],boolean)
- M:com.aspose.psd.Image.getImage2Export(com.aspose.psd.ImageOptionsBase,com.aspose.psd.Rectangle)
- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.Image.isUsePalette
- M:com.aspose.psd.Image.load(java.io.RandomAccessFile)
- M:com.aspose.psd.Image.load(java.io.RandomAccessFile,com.aspose.psd.LoadOptions)
- M:com.aspose.psd.Image.save(java.io.RandomAccessFile,com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.save(java.io.RandomAccessFile,com.aspose.psd.ImageOptionsBase,com.aspose.psd.Rectangle)
- M:com.aspose.psd.ImageOptionsBase.deepClone
- M:com.aspose.psd.ImageOptionsBase.getFullFrame
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- M:com.aspose.psd.ImageOptionsBase.setFullFrame(boolean)
- F:com.aspose.psd.Matrix.TYPE_FLIP
- F:com.aspose.psd.Matrix.TYPE_GENERAL_ROTATION
- F:com.aspose.psd.Matrix.TYPE_GENERAL_SCALE
- F:com.aspose.psd.Matrix.TYPE_GENERAL_TRANSFORM
- F:com.aspose.psd.Matrix.TYPE_IDENTITY
- F:com.aspose.psd.Matrix.TYPE_MASK_ROTATION
- F:com.aspose.psd.Matrix.TYPE_MASK_SCALE
- F:com.aspose.psd.Matrix.TYPE_QUADRANT_ROTATION
- F:com.aspose.psd.Matrix.TYPE_TRANSLATION
- F:com.aspose.psd.Matrix.TYPE_UNIFORM_SCALE
- M:com.aspose.psd.Matrix.isEquals(com.aspose.psd.Matrix,com.aspose.psd.Matrix)
- M:com.aspose.psd.Matrix.isIdentity
- M:com.aspose.psd.NonGenericDictionary.#ctor
- M:com.aspose.psd.NonGenericDictionary.getKeysTyped
- M:com.aspose.psd.NonGenericDictionary.getValuesTyped
- M:com.aspose.psd.NonGenericList.add(int,java.lang.Object)
- M:com.aspose.psd.NonGenericList.addAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.addAll(int,java.util.Collection)
- M:com.aspose.psd.NonGenericList.containsAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.get(int)
- M:com.aspose.psd.NonGenericList.getList
- M:com.aspose.psd.NonGenericList.isEmpty
- M:com.aspose.psd.NonGenericList.lastIndexOf(java.lang.Object)
- M:com.aspose.psd.NonGenericList.listIterator
- M:com.aspose.psd.NonGenericList.listIterator(int)
- M:com.aspose.psd.NonGenericList.remove(int)
- M:com.aspose.psd.NonGenericList.removeAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.retainAll(java.util.Collection)
- M:com.aspose.psd.NonGenericList.set(int,java.lang.Object)
- M:com.aspose.psd.NonGenericList.subList(int,int)
- M:com.aspose.psd.NonGenericList.toArray
- M:com.aspose.psd.NonGenericList.toArray(java.lang.Object[])
- T:com.aspose.psd.PdfComplianceVersion
- F:com.aspose.psd.PdfComplianceVersion.Pdf15
- F:com.aspose.psd.PdfComplianceVersion.PdfA1a
- F:com.aspose.psd.PdfComplianceVersion.PdfA1b
- M:com.aspose.psd.PixelDataFormat.getCieLab(int,int,int)
- M:com.aspose.psd.PixelDataFormat.getCmyk(int,int,int,int)
- M:com.aspose.psd.PixelDataFormat.getCmyka(int,int,int,int,int)
- M:com.aspose.psd.PixelDataFormat.getGrayscaleAlpha(int,int)
- M:com.aspose.psd.PixelDataFormat.getRgb(int,int,int)
- M:com.aspose.psd.PixelDataFormat.getRgbIndexed(int)
- M:com.aspose.psd.PixelDataFormat.getRgba(int,int,int,int)
- M:com.aspose.psd.PixelDataFormat.getYCbCr(int,int,int)
- F:com.aspose.psd.PixelFormat.CieLab
- M:com.aspose.psd.Point.isEquals(com.aspose.psd.Point,com.aspose.psd.Point)
- M:com.aspose.psd.PointF.isEquals(com.aspose.psd.PointF,com.aspose.psd.PointF)
- M:com.aspose.psd.RasterCachedImage.doRotate(float,boolean,com.aspose.psd.Color)
- M:com.aspose.psd.RasterCachedImage.getRotateMode
- T:com.aspose.psd.RasterCachedImage$RotateTestMode
- F:com.aspose.psd.RasterCachedImage$RotateTestMode.ByteArrayMode
- F:com.aspose.psd.RasterCachedImage$RotateTestMode.RegularMode
- F:com.aspose.psd.RasterCachedImage$RotateTestMode.StreamMode
- M:com.aspose.psd.RasterImage.isUsePalette
- M:com.aspose.psd.Rectangle.isEquals(com.aspose.psd.Rectangle,com.aspose.psd.Rectangle)
- M:com.aspose.psd.RectangleF.isEquals(com.aspose.psd.RectangleF,com.aspose.psd.RectangleF)
- M:com.aspose.psd.RectangleF.op_Division(com.aspose.psd.RectangleF,float)
- M:com.aspose.psd.RectangleF.op_Multiply(com.aspose.psd.RectangleF,float)
- M:com.aspose.psd.Region.isEquals(com.aspose.psd.Region,com.aspose.psd.Graphics)
- M:com.aspose.psd.Size.isEquals(com.aspose.psd.Size,com.aspose.psd.Size)
- M:com.aspose.psd.SizeF.isEquals(com.aspose.psd.SizeF,com.aspose.psd.SizeF)
- F:com.aspose.psd.StreamContainer.READ_WRITE_BYTES_COUNT
- F:com.aspose.psd.StreamContainer.startPosition
- M:com.aspose.psd.StreamContainer.#ctor(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.StreamContainer.#ctor(com.aspose.psd.system.io.Stream,boolean)
- T:com.aspose.psd.asynctask.AsyncTask
- M:com.aspose.psd.asynctask.AsyncTask.create(com.aspose.psd.asynctask.AsyncTaskAction)
- M:com.aspose.psd.asynctask.AsyncTask.create(com.aspose.psd.asynctask.AsyncTaskFunc)
- T:com.aspose.psd.asynctask.AsyncTaskAction
- M:com.aspose.psd.asynctask.AsyncTaskAction.run(com.aspose.psd.asynctask.IAsyncTaskState)
- T:com.aspose.psd.asynctask.AsyncTaskException
- M:com.aspose.psd.asynctask.AsyncTaskException.#ctor(java.lang.String)
- T:com.aspose.psd.asynctask.AsyncTaskFunc
- M:com.aspose.psd.asynctask.AsyncTaskFunc.#ctor
- M:com.aspose.psd.asynctask.AsyncTaskFunc.beginInvoke(com.aspose.psd.asynctask.IAsyncTaskState,com.aspose.psd.system.AsyncCallback,java.lang.Object)
- M:com.aspose.psd.asynctask.AsyncTaskFunc.endInvoke(com.aspose.psd.system.IAsyncResult)
- M:com.aspose.psd.asynctask.AsyncTaskFunc.invoke(com.aspose.psd.asynctask.IAsyncTaskState)
- T:com.aspose.psd.asynctask.AsyncTaskProgress
- F:com.aspose.psd.asynctask.AsyncTaskProgress.Duration
- F:com.aspose.psd.asynctask.AsyncTaskProgress```ko
컬러는 다음의 값을 가질 수 있습니다.

피엘 데이터 형식

RGB
CMYK
CMYKA
색조 알파
그레이스케일 알파
RGB 인덱스
RGBA
YC bCr

더 이상의 자세한 정보는 아래의 페이지를 참조하십시오:
https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/
```