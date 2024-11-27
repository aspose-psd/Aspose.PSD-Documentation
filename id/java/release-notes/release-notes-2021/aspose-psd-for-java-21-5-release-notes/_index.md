---
title: Catatan Rilis Aspose.PSD for Java 21.5
type: docs
weight: 40
url: /id/aspose-psd-for-java-21-5-catatan-rilis/
---

{{% alert color="primary" %}} Halaman ini berisi catatan rilis untuk [Aspose.PSD for Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Ini adalah rilis perantara Aspose.PSD for Java.
Ada beberapa isu yang diketahui. Jadi, jika Anda memerlukan versi stabil, Anda harus menggunakan [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) hingga Aspose.PSD 21.6 dirilis.
Rilis ini mencakup semua Fitur Aspose.PSD .Net (Termasuk Smart Object) sejak 20.9 dan fitur yang tercantum di bawah ini.
{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-340|Dukungan pengubahbentukan lapisan bentuk dengan jalur vektor ketika hanya lapisan diubah ukurannya|Fitur|
|PSDJAVA-341|Dukungan pengubahbentukan lapisan bentuk dengan jalur vektor|Fitur|
|PSDJAVA-342|String teks terpotong|Bug|

# **Perubahan API Publik**
# **API Ditambahkan:**
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
- F:com.aspose.psd.asynctask.AsyncTaskProgress.ProgressPercentage
- M:com.aspose.psd.asynctask.AsyncTaskProgress.#ctor(int,long)
- T:com.aspose.psd.asynctask.CompleteCallback
- M:com.aspose.psd.asynctask.CompleteCallback.run(com.asposeose.psd.asynctask.IAsyncTaskResult)
- T:com.aspose.psd.asynctask.FailureCallback
- M:com.aspose.psd.asynctask.FailureCallback.run(java.lang.Throwable)
- T:com.aspose.psd.asynctask.IAsyncTaskResult
- M:com.aspose.psd.asynctask.IAsyncTaskResult.addComplete(com.aspose.psd.asynctask.CompleteCallback)
- M:com.aspose.psd.asynctask.IAsyncTaskResult.addFailure(com.aspose.psd.asynctask.FailureCallback)
- M:com.aspose.psd.asynctask.IAsyncTaskResult.getComplete()
- M:com.aspose.psd.asynctask.IAsyncTaskResult.getFailure()
- M:com.aspose.psd.asynctask.IAsyncTaskResult.getProgress()
- M:com.aspose.psd.asynctask.IAsyncTaskResult.getState()
- M:com.aspose.psd.asynctask.IAsyncTaskResult.removeComplete(com.aspose.psd.asynctask.CompleteCallback)
- M:com.aspose.psd.asynctask.IAsyncTaskResult.removeFailure(com.aspose.psd.asynctask.FailureCallback)
- M:com.aspose.psd.asynctask.IAsyncTaskResult.setComplete(java.util.List)
- M:com.aspose.psd.asynctask.IAsyncTaskResult.setFailure(java.util.List)
- M:com.aspose.psd.asynctask.IAsyncTaskResult.setProgress(int)
- M:com.aspose.psd.asynctask.IAsyncTaskResult.setState(java.lang.Object)
- T:com.aspose.psd.asynctask.IAsyncTaskState
- M:com.aspose.psd.asynctask.IAsyncTaskState.getProgress()
- M:com.aspose.psd.asynctask.IAsyncTaskState.setFailure(java.lang.Throwable)
- M:com.aspose.psd.asynctask.IAsyncTaskState.setProgress(int)
- M:com.aspose.psd.asynctask.IAsyncTaskState.setSuccess()
- M:com.aspose.psd.asynctask.IAsyncTaskState.setState(java.lang.Object)
- T:com.aspose.psd.asynctask.SuccessCallback
- M:com.aspose.psd.asynctask.SuccessCallback.run(java.lang.Object)
- T:com.aspose.psd.system.AsyncCallback
- M:com.aspose.psd.system.AsyncCallback.invoke(java.lang.Object)
- T:com.aspose.psd.system.IAsyncResult
- M:com.aspose.psd.system.IAsyncResult.getAsyncState()
- M:com.aspose.psd.system.IAsyncResult.getAsyncWaitHandle()
- M:com.aspose.psd.system.IAsyncResult.getCompletedSynchronously()
- M:com.aspose.psd.system.IAsyncResult.getIsCompleted()
- T:com.aspose.psd.system.io.Stream
- M:com.aspose.psd.system.io.Stream.close()
- M:com.aspose.psd.system.io.Stream.Dispose()
- M:com.aspose.psd.system.io.Stream.Flush()
- M:com.aspose.psd.system.io.Stream.Read([b'`byt`;'])
- M:com.aspose.psd.system.io.Stream.WriteByte(int)
- T:com.aspose.psd.system.Uri
- M:com.aspose.psd.ChannelBlackWhite.update(com.aspose.psd.ProgressEventHandler)
- T:com.aspose.psd.ChannelBlackWhite.update_Image(com.aspose.psd.RasterImage,com.aspose.psd.RasterImage,com.aspose.psd.ProgressEventHandler)
- T:com.aspose.psd.ColorConversionMode
- M:com.aspose.psd.ColorConverter.convertColor(java.awt.color,com.aspose.psd.Color)
- M:com.aspose.psd.ColorConverter.convertColor(com.aspose.psd.Color,java.awt.color)
- M:com.aspose.psd.ColorConverter.convertRgbToCmyk(int,int,int)
- M:com.aspose.psd.ColorConverter.convertRgbToYCbCr(int,int,int,com.aspose.psd.ColorChannels)
- M:com.aspose.psd.ColorConverter.convertRgbToYCbCrByte(int,int,int,java.awt.color.colorSpace)
- M:com.aspose.psd.ColorConverter.convertRgbToYCbCrByte(int,int,int,com.aspose.psd.ColorChannels,java.awt.color.colorSpace)
- M:com.aspose.psd.ColorConverter.convertRgbaToCmyk(int,int,int,int)
- M:com.aspose.psd.ColorConverter.convertRgbaToYCbCr(int,int,int,int,com.aspose.psd.ColorChannels)
- M:com.aspose.psd.ColorConverter.convertRgbaToYCbCrByte(int,int,int,int,java.awt.color.colorSpace)
- M:com.aspose.psd.ColorConverter.convertRgbaToYCbCrByte(int,int,int,int,com.aspose.psd.ColorChannels,java.awt.color.colorSpace)
- M:com.aspose.psd.Compressor.compress(java.io.InputStream,short,java.io.OutputStream)
- M:com.aspose.psd.Compressor.decompress(java.io.InputStream,java.io.OutputStream)
- M:com.aspose.psd.Compressor.decompress(com.aspose.psd.StreamContainer,java.io.OutputStream)
- M:com.aspose.psd.Compressor.decompress(com.aspose.psd.StreamContainer,com.aspose.psd.StreamContainer)
- M:com.aspose.psd.Compressor.decompress(com.aspose.psd.StreamContainer,com.aspose.psd.StreamContainer,boolean)
- M:com.aspose.psd.Compressor.getUncompressedSize(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.Compressor.isValid(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.Core487Utils.forceByteOrder(java.nio.ByteOrder)
- M:com.aspose.psd.Directory.isConsistent()
- T:com.aspose.psd.FileFormat
- F:com.aspose.psd.FileFormats.jpg
- M:com.aspose.psd.FileFormats.tiff.getExtendedFileSpecification(com.aspose.psd.TiffOptions)
- M:com.aspose.psd.FileFormats.tiff.setExtendedFileSpecification(com.aspose.psd.system.io.Stream,com.aspose.psd.TiffOptions)
- M:com.aspose.psd.FileFormats.webp.loadPixelsFromStream(com.aspose.psd.system.io.Stream)




