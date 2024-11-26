---
title: Aspose.PSD for Java 21.5 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-21-5-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) için sürüm notlarını içerir. {{% /alert %}}

{{% alert color="info" %}}
Bu, Aspose.PSD for Java'nın ara sürümüdür.
Bazı bilinen sorunları bulunmaktadır. Bu nedenle, kararlı bir sürüm gerekiyorsa [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) sürümünü kullanmalısınız ki, Aspose.PSD 21.6 yayımlanana kadar.
Bu sürüm, 20.9 sürümünden başlayarak tüm Aspose.PSD .Net Özelliklerini (Akıllı Nesne Dahil) ve aşağıdaki özellikleri içermektedir.
{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-340|Yalnızca bir katman yeniden boyutlandırıldığında vektör yolları olan şekil katmanlarını destekleme|Özellik|
|PSDJAVA-341|Vektör yolları olan şekil katmanlarını destekleme|Özellik|
|PSDJAVA-342|Kırpılmış metin dizesi|Hata|

# **Genel API Değişiklikleri**
# **Eklenen API'lar:**
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
- F:com.aspose.psd.asynctask```
AsyncTaskProgress.Percentage
- T:com.aspose.psd.asynctask.AsyncTaskState
- M:com.aspose.psd.asynctask.AsyncTaskState.getException
- M:com.aspose.psd.asynctask.AsyncTaskState.getIsCanceled
- M:com.aspose.psd.asynctask.AsyncTaskState.getIsCompleted
- M:com.aspose.psd.asynctask.AsyncTaskState.getIsFaulted
- M:com.aspose.psd.asynctask.AsyncTaskState.getIsRunning
- T:com.aspose.psd.asynctask.IAsyncTaskState
- M:com.aspose.psd.asynctask.IAsyncTaskState.getIsCanceled
- M:com.aspose.psd.asynctask.IAsyncTaskState.getIsCompleted
- M:com.aspose.psd.asynctask.IAsyncTaskState.getIsFaulted
- M:com.aspose.psd.asynctask.IAsyncTaskState.getIsRunning
- M:com.aspose.psd.asynctask.IAsyncTaskState.setIsRunning
- T:com.aspose.psd.asynctask.NativeAsyncTask
- M:com.aspose.psd.asynctask.NativeAsyncTask.create(com.aspose.psd.asynctask.AsyncTaskAction)
- M:com.aspose.psd.asynctask.NativeAsyncTask.create(com.aspose.psd.asynctask.AsyncTaskFunc)
- M:com.aspose.psd.asynctask.NativeAsyncTask.runAsync(com.aspose.psd.asynctask.AsyncTaskAction)
- M:com.aspose.psd.asynctask.NativeAsyncTask.runAsync(com.aspose.psd.asynctask.AsyncTaskFunc)
- M:com.aspose.psd.asynctask.NativeAsyncTask.runSync(com.aspose.psd.asynctask.AsyncTaskAction)
- M:com.aspose.psd.asynctask.NativeAsyncTask.runSync(com.aspose.psd.asynctask.AsyncTaskFunc)
- T:com.aspose.psd.brushes.HatchStyle
- F:com.aspose.psd.brushes.HatchStyle.Horizontal
- F:com.aspose.psd.brushes.HatchStyle.Vertical
- F:com.aspose.psd.brushes.HatchStyle.ForwardDiagonal
- F:com.aspose.psd.brushes.HatchStyle.BackwardDiagonal
- F:com.aspose.psd.brushes.HatchStyle.Cross
- F:com.aspose.psd.brushes.HatchStyle.DiagonalCross
- M:com.aspose.psd.brushes.HatchBrush.#ctor(com.aspose.psd.brushes.HatchStyle,com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.brushes.LinearGradientBrush.#ctor(com.aspose.psd.PointF,com.aspose.psd.PointF,com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.brushes.RadialGradientBrush.#ctor(com.aspose.psd.RectangleF,com.aspose.psd.PointF,com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.brushes.TextureBrush.#ctor(com.aspose.psd.system.io.Stream,com.aspose.psd.RectangleF)
- T:com.aspose.psd.collections.Dictionary<K,V>
- M:com.aspose.psd.collections.Dictionary<K,V>.#ctor
- M:com.aspose.psd.collections.Dictionary<K,V>.add(K,V)
- M:com.aspose.psd.collections.Dictionary<K,V>.clear
- M:com.aspose.psd.collections.Dictionary<K,V>.containsKey(K)
- M:com.aspose.psd.collections.Dictionary<K,V>.containsValue(V)
- M:com.aspose.psd.collections.Dictionary<K,V>.getItem(K)
- M:com.aspose.psd.collections.Dictionary<K,V>.getKeys
- M:com.aspose.psd.collections.Dictionary<K,V>.getValues
- M:com.aspose.psd.collections.Dictionary<K,V>.remove(K)
- M:com.aspose.psd.collections.Dictionary<K,V>.tryGetValue(K,V)
- T:com.aspose.psd.commands.DoCommandCommand
- M:com.aspose.psd.commands.DoCommandCommand.execute(com.aspose.psd.Image)
- F:com.aspose.psd.converters.TextOptions.MultilineRootElement
- F:com.aspose.psd.converters.TextOptions.MultilineTextElement
- M:com.aspose.psd.layers.TextLayer.#ctor(com.aspose.psd.Color,java.lang.String,com.aspose.psd.FontSettings)
```

# **Bu Sürümde Düzeltilen Hatalar:**
- **PSDJAVA-342** - Kırpılmış metin dizesi hata raporu 

# **Bu Sürümdeki Sorunlar**
- Sürüm içeriğinin tamamını görüntülemek için [JIRA](https://asposepsd.atlassian.net/browse/PSDJAVA) takibi yapabilirsiniz.
  
# **Bu Sürümdeki Notlar**
- Bu sürümde öne çıkan değişikliklere daha detaylı bakın [Java 21.5 for Aspose.PSD Release Notes](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/).