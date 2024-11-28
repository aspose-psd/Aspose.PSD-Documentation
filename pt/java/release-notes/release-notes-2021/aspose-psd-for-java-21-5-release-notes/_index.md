---
title: Aspose.PSD para Java 21.5 - Notas de Lançamento
type: docs
weight: 40
url: /pt/java/aspose-psd-para-java-21-5-notas-de-lancamento/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para [Aspose.PSD para Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Este é um lançamento intermediário do Aspose.PSD para Java.
Possui alguns problemas conhecidos. Portanto, se você precisar de uma versão estável, deve usar [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) até que o Aspose.PSD 21.6 seja lançado.
Este lançamento inclui todos os recursos do Aspose.PSD .Net (incluindo Smart Object) desde a versão 20.9 e os recursos listados abaixo.
{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-340|Suporte ao redimensionamento de camadas de forma com caminhos vetoriais quando apenas uma camada é redimensionada|Recurso|
|PSDJAVA-341|Suporte ao redimensionamento de camadas de forma com caminhos vetoriais|Recurso|
|PSDJAVA-342|Cadeia de texto truncada|Erro|

# **Alterações na API Pública**
# **APIs Adicionadas:**
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
- M:com.aspose.psd.RasterCachedImage.getRotateMode
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
- F:com.aspose.psd.asynctask.AsyncTaskProgress.ProgressPercentage
- M:com.aspose.psd.asynctask.AsyncTaskProgress.#ctor(int,long)
- T:com.aspose.psd.asynctask.CompleteCallback
- M:com.asaspose.psd.asynctask.CompleteCallback.#ctor(com.aspose.psd.asynctask.CompleteCallback,com.aspose.psd.system.AsyncCallback,java.lang.Object)
- T:com.aspose.psd.asynctask.IAsyncTaskState
- M:com.aspose.psd.asynctask.IAsyncTaskState.getAsyncException
- M:com.aspose.psd.asynctask.IAsyncTaskState.getAsyncExceptionOccurred
- M:com.aspose.psd.asynctask.IAsyncTaskState.getIsComplete
- M:com.aspose.psd.asynctask.IAsyncTaskState.getIsFaulted
- M:com.aspose.psd.asynctask.IAsyncTaskState.getIsInProgress
- M:com.aspose.psd.asynctask.IAsyncTaskState.getProgress
- M:com.aspose.psd.asynctask.IAsyncTaskState.getState
- M:com.aspose.psd.asynctask.IAsyncTaskState.onAsyncExceptionOccurred(com.aspose.psd.asynctask.IAsyncTaskState)
- M:com.aspose.psd.asynctask.IAsyncTaskState.onComplete(com.aspose.psd.asynctask.IAsyncTaskState)
- M:com.aspose.psd.asynctask.IAsyncTaskState.onEndInvoke(com.aspose.psd.system.IAsyncResult)
- M:com.aspose.psd.asynctask.IAsyncTaskState.setResult(java.lang.Object)
- T:com.aspose.psd.asynctask.ProgressCallback
- M:com.aspose.psd.asynctask.ProgressCallback.#ctor(com.aspose.psd.asynctask.ProgressCallback,com.aspose.psd.asynctask.ProgressCallback,java.lang.Object,com.aspose.psd.system.AsyncCallback,java.lang.Object)
- M:com.aspose.psd.asynctask.ProgressCallback.invoke(com.aspose.psd.asynctask.AsyncTaskProgress)
- T:com.aspose.psd.asynctask.TaskResult
- M:com.aspose.psd.asynctask.TaskResult.#ctor(java.lang.Object,com.aspose.psd.asynctask.AsyncState)
- M:com.aspose.psd.asynctask.TaskResult.getAsyncResult
- M:com.aspose.psd.asynctask.TaskResult.getAsyncState
- T:com.aspose.psd.asynctask.Tasks
- M:com.aspose.psd.asynctask.Tasks.processTask(com.aspose.psd.asynctask.AsyncTask)
- F:com.aspose.psd.asynctask.Tasks.DefaultTimeLimit
- F:com.aspose.psd.asynctask.Tasks.MaxTimeLimit
- M:com.aspose.psd.asynctask.Tasks.set_TaskUsing(com.aspose.psd.asynctask.Tasks.TaskUsageType,com.aspose.psd.asynctask.IAsyncTaskState)
- T:com.aspose.psd.brushes.HatchStyle
- F:com.aspose.psd.brushes.HatchStyle.BACKWARD_DIAGONAL
- F:com.aspose.psd.brushes.HatchStyle.CROSS
- F:com.aspose.psd.brushes.HatchStyle.DARK_DOWNWARD_DIAGONAL
- F:com.aspose.psd.brushes.HatchStyle.DARK_HORIZONTAL
- F:com.aspose.psd.brushes.HatchStyle.DARK_UPWARD_DIAGONAL
- F:com.aspose.psd.brushes.HatchStyle.DARK_VERTICAL
- F:com.aspose.psd.brushes.HatchStyle.DIAGONAL_CROSS
- F:com.aspose.psd.brushes.HatchStyle.DIVOT
- F:com.aspose.psd.brushes.HatchStyle.FOREWARD_DIAGONAL
- F:com.aspose.psd.brushes.HatchStyle.HORIZONTAL
- F:com.aspose.psd.brushes.HatchStyle.HORIZONTAL_BRICK
- F:com.aspose.psd.brushes.HatchStyle.LARGECheckerBoard 
- F:com.aspose.psd.brushes.HatchStyle.LightDownwardDiagonal
- F:com.aspose.psd.brushes.HatchStyle.LightHorizontal
- F:com.aspose.psd.brushes.HatchStyle.LightUpwardDiagonal
- F:com.aspose.psd.brushes.HatchStyle.LightVertical
- F:com.aspose.psd.brushes.HatchStyle.MaxHatch
- F:com.aspose.psd.brushes.HatchStyle.MinHatch
- F:com.aspose.psd.brushes.HatchStyle.NARROW_HORIZONTAL
- F:com.aspose.psd.brushes.HatchStyle.OUTLINED_DIAMOND
- F:com.aspose.psd.brushes.HatchStyle.SparseDot
- F:com.aspose.psd.brushes.HatchStyle.SQUARE
- F:com.aspose.psd.brushes.HatchStyle.ThickCross
- F:com.aspose.psd.brushes.HatchStyle.ThickDownwardDiagonal
- F:com.aspose.psd.brushes.HatchStyle.ThickForwardDiagonal
- F:com.aspose.psd.brushes.HatchStyle.ThickHorizontal
- F:com.aspose.psd.brushes.HatchStyle.ThickUpwardDiagonal
- F:com.aspose.psd.brushes.HatchStyle.ThickVertical
- M:com.aspose.psd.brushes.HatchBrush.getBackgroundColor()
- M:com.aspose.psd.brushes.HatchBrush.setForegroundColor()