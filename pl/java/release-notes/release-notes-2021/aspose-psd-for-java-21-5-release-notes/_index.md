---
title: Aspose.PSD dla Java 21.5 - Notatki wydania
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-21-5-notatki-wydania/
---

{{% alert color="primary" %}} Ta strona zawiera notatki wydania dla [Aspose.PSD dla Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
To jest wydanie pośrednie Aspose.PSD dla Java.
Ma pewne znane problemy. Jeśli potrzebujesz stabilnej wersji, powinieneś używać [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) do czasu wydania Aspose.PSD 21.6.
To wydanie obejmuje wszystkie funkcje Aspose.PSD .Net (w tym Obiekt Inteligentny) od wersji 20.9 oraz wymienione poniżej funkcje.
{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDJAVA-340|Obsługa zmiany rozmiaru warstw kształtu z ścieżkami wektorowymi, gdy zmieniana jest tylko warstwa|Funkcja|
|PSDJAVA-341|Obsługa zmiany rozmiaru warstw kształtu z ścieżkami wektorowymi|Funkcja|
|PSDJAVA-342|Skrócony ciąg tekstowy|Błąd|

# **Zmiany w API publicznym**
# **Dodane API:**
- M: com.aspose.psd.CmykColor.isEquals(com.aspose.psd.CmykColor,com.aspose.psd.CmykColor)
- M: com.aspose.psd.Color.isEquals(com.aspose.psd.Color,com.aspose.psd.Color)
- M: com.aspose.psd.ColorPaletteHelper.getCloseImagePalette(com.aspose.psd.RasterImage,com.aspose.psd.Rectangle,int,boolean)
- M: com.aspose.psd.ColorPaletteHelper.hasTransparentColors(com.aspose.psd.IColorPalette)
- T: com.aspose.psd.CompositeException
- T: com.aspose.psd.CurrentThreadSettings
- M: com.aspose.psd.CurrentThreadSettings.getLocale
- M: com.aspose.psd.CurrentThreadSettings.setLocale(java.lang.String)
- M: com.aspose.psd.CurrentThreadSettings.setLocale(java.util.Locale)
- M: com.aspose.psd.DataStreamSupporter.save(java.io.RandomAccessFile)
- M: com.aspose.psd.DataStreamSupporter.saveData(com.aspose.psd.system.io.Stream)
- M: com.aspose.psd.DisposableObject.close
- M: com.aspose.psd.Font.makeFontWithGraphUnit(java.lang.String,float,int)
- M: com.aspose.psd.FontSettings.addFontsFolder(java.lang.String)
- M: com.aspose.psd.FontSettings.removeFontsFolder(java.lang.String)
- M: com.aspose.psd.FontSettings.setFontsFolders(java.lang.String[])
- M: com.aspose.psd.Image.create(com.aspose.psd.Image[])
- M: com.aspose.psd.Image.create(com.aspose.psd.Image[],boolean)
- M: com.aspose.psd.Image.getImage2Export(com.aspose.psd.ImageOptionsBase,com.aspose.psd.Rectangle)
- M: com.aspose.psd.Image.isAutoAdjustPalette
- M: com.aspose.psd.Image.isUsePalette
- M: com.aspose.psd.Image.load(java.io.RandomAccessFile)
- M: com.aspose.psd.Image.load(java.io.RandomAccessFile,com.aspose.psd.LoadOptions)
- M: com.aspose.psd.Image.save(java.io.RandomAccessFile,com.aspose.psd.ImageOptionsBase)
- M: com.aspose.psd.Image.save(java.io.RandomAccessFile,com.aspose.psd.ImageOptionsBase,com.aspose.psd.Rectangle)
- M: com.aspose.psd.ImageOptionsBase.deepClone
- M: com.aspose.psd.ImageOptionsBase.getFullFrame
- M: com.aspose.psd.ImageOptionsBase.memberwiseClone
- M: com.aspose.psd.ImageOptionsBase.setFullFrame(boolean)
- F: com.aspose.psd.Matrix.TYPE_FLIP
- F: com.aspose.psd.Matrix.TYPE_GENERAL_ROTATION
- F: com.aspose.psd.Matrix.TYPE_GENERAL_SCALE
- F: com.aspose.psd.Matrix.TYPE_GENERAL_TRANSFORM
- F: com.aspose.psd.Matrix.TYPE_IDENTITY
- F: com.aspose.psd.Matrix.TYPE_MASK_ROTATION
- F: com.aspose.psd.Matrix.TYPE_MASK_SCALE
- F: com.aspose.psd.Matrix.TYPE_QUADRANT_ROTATION
- F: com.aspose.psd.Matrix.TYPE_TRANSLATION
- F: com.aspose.psd.Matrix.TYPE_UNIFORM_SCALE
- M: com.aspose.psd.Matrix.isEquals(com.aspose.psd.Matrix,com.aspose.psd.Matrix)
- M: com.aspose.psd.Matrix.isIdentity
- M: com.aspose.psd.NonGenericDictionary.#ctor
- M: com.aspose.psd.NonGenericDictionary.getKeysTyped
- M: com.aspose.psd.NonGenericDictionary.getValuesTyped
- M: com.aspose.psd.NonGenericList.add(int,java.lang.Object)
- M: com.aspose.psd.NonGenericList.addAll(java.util.Collection)
- M: com.aspose.psd.NonGenericList.addAll(int,java.util.Collection)
- M: com.aspose.psd.NonGenericList.containsAll(java.util.Collection)
- M: com.aspose.psd.NonGenericList.get(int)
- M: com.aspose.psd.NonGenericList.getList
- M: com.aspose.psd.NonGenericList.isEmpty
- M: com.aspose.psd.NonGenericList.lastIndexOf(java.lang.Object)
- M: com.aspose.psd.NonGenericList.listIterator
- M: com.aspose.psd.NonGenericList.listIterator(int)
- M: com.aspose.psd.NonGenericList.remove(int)
- M: com.aspose.psd.NonGenericList.removeAll(java.util.Collection)
- M: com.aspose.psd.NonGenericList.retainAll(java.util.Collection)
- M: com.aspose.psd.NonGenericList.set(int,java.lang.Object)
- M: com.aspose.psd.NonGenericList.subList(int,int)
- M: com.aspose.psd.NonGenericList.toArray
- M: com.aspose.psd.NonGenericList.toArray(java.lang.Object[])
- T: com.aspose.psd.PdfComplianceVersion
- F: com.aspose.psd.PdfComplianceVersion.Pdf15
- F: com.aspose.psd.PdfComplianceVersion.PdfA1a
- F: com.aspose.psd.PdfComplianceVersion.PdfA1b
- M: com.aspose.psd.PixelDataFormat.getCieLab(int,int,int)
- M: com.aspose.psd.PixelDataFormat.getCmyk(int,int,int,int)
- M: com.aspose.psd.PixelDataFormat.getCmyka(int,int,int,int,int)
- M: com.aspose.psd.PixelDataFormat.getGrayscaleAlpha(int,int)
- M: com.aspose.psd.PixelDataFormat.getRgb(int,int,int)
- M: com.aspose.psd.PixelDataFormat.getRgbIndexed(int)
- M: com.aspose.psd.PixelDataFormat.getRgba(int,int,int,int)
- M: com.aspose.psd.PixelDataFormat.getYCbCr(int,int,int)
- F: com.aspose.psd.PixelFormat.CieLab
- M: com.aspose.psd.Point.isEquals(com.aspose.psd.Point,com.aspose.psd.Point)
- M: com.aspose.psd.PointF.isEquals(com.aspose.psd.PointF,com.aspose.psd.PointF)
- M: com.aspose.psd.RasterCachedImage.doRotate(float,boolean,com.aspose.psd.Color)
- M: com.aspose.psd.RasterCachedImage.getRotateMode
- T: com.aspose.psd.RasterCachedImage$RotateTestMode
- F: com.aspose.psd.RasterCachedImage$RotateTestMode.ByteArrayMode
- F: com.aspose.psd.RasterCachedImage$RotateTestMode.RegularMode
- F: com.aspose.psd.RasterCachedImage$RotateTestMode.StreamMode
- M: com.aspose.psd.RasterImage.isUsePalette
- M: com.aspose.psd.Rectangle.isEquals(com.aspose.psd.Rectangle,com.aspose.psd.Rectangle)
- M: com.aspose.psd.RectangleF.isEquals(com.aspose.psd.RectangleF,com.aspose.psd.RectangleF)
- M: com.aspose.psd.RectangleF.op_Division(com.aspose.psd.RectangleF,float)
- M: com.aspose.psd.RectangleF.op_Multiply(com.aspose.psd.RectangleF,float)
- M: com.aspose.psd.Region.isEquals(com.aspose.psd.Region,com.aspose.psd.Graphics)
- M: com.aspose.psd.Size.isEquals(com.aspose.psd.Size,com.aspose.psd.Size)
- M: com.aspose.psd.SizeF.isEquals(com.aspose.psd.SizeF,com.aspose.psd.SizeF)
- F: com.aspose.psd.StreamContainer.READ_WRITE_BYTES_COUNT
- F: com.aspose.psd.StreamContainer.startPosition
- M: com.aspose.psd.StreamContainer.#ctor(com.aspose.psd.system.io.Stream)
- M: com.aspose.psd.StreamContainer.#ctor(com.aspose.psd.system.io.Stream,boolean)
- T: com.aspose.psd.asynctask.AsyncTask
- M: com.aspose.psd.asynctask.AsyncTask.create(com.aspose.psd.asynctask.AsyncTaskAction)
- M: com.aspose.psd.asynctask.AsyncTask.create(com.aspose.psd.asynctask.AsyncTaskFunc)
- T: com.aspose.psd.asynctask.AsyncTaskAction
- M: com.aspose.psd.asynctask.AsyncTaskAction.run(com.aspose.psd.asynctask.IAsyncTaskState)
- T: com.aspose.psd.asynctask.AsyncTaskException
- M: com.aspose.psd.asynctask.AsyncTaskException.#ctor(java.lang.String)
- T: com.aspose.psd.asynctask.AsyncTaskFunc
- M: com.aspose.psd.asynctask.AsyncTaskFunc.#ctor
- M: com.aspose.psd.asynctask.AsyncTaskFunc.beginInvoke(com.aspose.psd.asynctask.IAsyncTaskState,com.aspose.psd.system.AsyncCallback,java.lang.Object)
- M: com.aspose.psd.asynctask.AsyncTaskFunc.endInvoke(com.aspose.psd.system.IAsyncResult)
- M: com.aspose.psd.asynctask.AsyncTaskFunc.invoke(com.aspose.psd.asynctask.IAsyncTaskState)
- T: com.aspose.psd.asynctask.AsyncTaskProgress
- F: com.aspose.psd.asynctask.AsyncTaskProgress.Duration
- F: com.aspose.psd.asynctask.AsyncTaskProgress.ProgressPercentage
- M: com.aspose.psd.as```pl
ynctask.AsyncTaskProgress.getDuration
- M: com.aspose.psd.asynctask.AsyncTaskProgress.getProgressPercentage
- M: com.aspose.psd.asynctask.AsyncTaskProgress.#ctor(long,int)
- T: com.aspose.psd.asynctask.IAsyncTaskState
- M: com.aspose.psd.asynctask.IAsyncTaskState.getData
- T: com.aspose.psd.system.AsyncCallback
- M: com.aspose.psd.system.AsyncCallback.Invoke(com.aspose.psd.system.IAsyncResult)
- T: com.aspose.psd.system.IAsyncResult
- M: com.aspose.psd.system.IAsyncResult.AsyncState
- M: com.aspose.psd.system.IAsyncResult.AsyncWaitHandle
- M: com.aspose.psd.system.IAsyncResult.CompletedSynchronously
- M: com.aspose.psd.system.IAsyncResult.IsCompleted
- T: com.aspose.psd.system.RuntimeObject
- M: com.aspose.psd.system.RuntimeObject.getBaseType
- M: com.aspose.psd.system.RuntimeObject.getFullName
- M: com.aspose.psd.system.RuntimeObject.getMethods
- M: com.aspose.psd.system.RuntimeObject.getNameSpace
- M: com.aspose.psd.system.RuntimeObject.getProperties
- M: com.aspose.psd.system.RuntimeObject.getPropertyValue(java.lang.String)
- T: com.io.placement
- F: com.io.placement.Inside
- F: com.io.placement.Outside
- T: iODisplayTextType
- F: iODisplayTextType.Bottom
- F: iODisplayTextType.Center
- F: iODisplayTextType.Top
- T: com.aspose.psd.system.io.IRandomAccessStreamProvider
- M: com.aspose.psd.system.io.IRandomAccessStreamProvider.getStream
- M: com.aspose.psd.system.io.Stream.close
- M: com.aspose.psd.system.io.Stream.getCanRead
- M: com.aspose.psd.system.io.Stream.getCanSeek
- M: com.aspose.psd.system.io.Stream.getCanWrite
- M: com.aspose.psd.system.io.Stream.getLength
- M: com.aspose.psd.system.io.Stream.getPosition
- M: com.aspose.psd.system.io.Stream.read
- M: com.aspose.psd.system.io.Stream.seek
- M: com.aspose.psd.system.io.Stream.setLength(long)
- M: com.aspose.psd.system.io.Stream.write
- M: com.aspose.psd.system.io.Stream.BeginRead(byte[],int,int,com.aspose.psd.system.AsyncCallback,java.lang.Object)
- F: com.aspose.psd.system.io.Stream.Null
- F: com.aspose.psd.system.io.Stream.Null.length
- T: com.aspose.psd.system.threading.CancellationToken
- F: com.aspose.psd.system.threading.CancellationToken.None
- M: com.aspose.psd.system.threading.CancellationToken.getCanBeCanceled
- M: com.aspose.psd.system.threading.CancellationToken.isCancellationRequested
- M: com.aspose.psd.system.threading.CancellationToken.register(com.aspose.psd.system.threading.CancellationTokenRegistration)
- M: com.aspose.psd.system.threading.CancellationToken.throwIfCancellationRequested
- T: com.aspose.psd.system.threading.CancellationTokenRegistration
- M: com.aspose.psd.system.threading.CancellationTokenRegistration.dispose
- T: com.aspose.psd.system.threading.IThreadPool
- M: com.aspose.psd.system.threading.IThreadPool.queueUserWorkItem(java.lang.Runnable)
- T: com.aspose.psd.system.threading.ManualResetEvent
- M: com.aspose.psd.system.threading.ManualResetEvent.#ctor(boolean)
- M: com.aspose.psd.system.threading.ManualResetEvent.getWaitHandle
- M: com.aspose.psd.system.threading.ManualResetEvent.reset
- M: com.aspose.psd.system.threading.ManualResetEvent.set
- M: com.aspose.psd.system.threading.ManualResetEvent.waitOne
- M: com.aspose.psd.system.threading.Thread.sleep(long)
- T: com.aspose.psd.system.threading.ThreadAbortException
- M: com.aspose.psd.system.threading.ThreadAbortException.#ctor
```