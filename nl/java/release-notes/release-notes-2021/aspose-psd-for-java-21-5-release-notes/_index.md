---
title: Aspose.PSD voor Java 21.5 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-21-5-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Dit is een tussenliggende release van Aspose.PSD voor Java.
Het heeft enkele bekende problemen. Als u een stabiele versie nodig heeft, moet u [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) gebruiken totdat Aspose.PSD 21.6 wordt uitgebracht.
Deze release bevat alle Aspose.PSD .Net-functies (inclusief Smart Object) sinds 20.9 en de hieronder vermelde functies.
{{% /alert %}}

| **Belangrijk** | **Samenvatting** | **Categorie** |
| :- | :- | :- |
| PSDJAVA-340 | Ondersteuning voor het verkleinen van vormlagen met vectorpaden wanneer alleen een laag wordt verkleind | Functie |
| PSDJAVA-341 | Ondersteuning voor het verkleinen van vormlagen met vectorpaden | Functie |
| PSDJAVA-342 | Afgekapte tekstreeks | Bug |

# **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
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
- M:com.aspose.psd.asyn{% alert color="info" %}
Deze release van Aspose.PSD voor Java bevat de toegevoegde API's en wijzigingen in de openbare API zoals hieronder vermeld:

## **Toegevoegde API's:**
- `CmykColor.isEquals(CmykColor, CmykColor)`
- `Color.isEquals(Color, Color)`
- `ColorPaletteHelper.getCloseImagePalette(RasterImage, Rectangle, int, boolean)`
- `ColorPaletteHelper.hasTransparentColors(IColorPalette)`
- `CompositeException`
- `CurrentThreadSettings`
- `CurrentThreadSettings.getLocale`
- `CurrentThreadSettings.setLocale(String)`
- `CurrentThreadSettings.setLocale(Locale)`
- `DataStreamSupporter.save(RandomAccessFile)`
- `DataStreamSupporter.saveData(Stream)`
- `DisposableObject.close`
- `Font.makeFontWithGraphUnit(String, float, int)`
- `FontSettings.addFontsFolder(String)`
- `FontSettings.removeFontsFolder(String)`
- `FontSettings.setFontsFolders(String[])`
- `Image.create(Image[])`
- `Image.create(Image[], boolean)`
- `Image.getImage2Export(ImageOptionsBase, Rectangle)`
- `Image.isAutoAdjustPalette`
- `Image.isUsePalette`
- `Image.load(RandomAccessFile)`
- `Image.load(RandomAccessFile, LoadOptions)`
- `Image.save(RandomAccessFile, ImageOptionsBase)`
- `Image.save(RandomAccessFile, ImageOptionsBase, Rectangle)`
- `ImageOptionsBase.deepClone`
- `ImageOptionsBase.getFullFrame`
- `ImageOptionsBase.memberwiseClone`
- `ImageOptionsBase.setFullFrame(boolean)`
- `Matrix.TYPE_FLIP`
- `Matrix.TYPE_GENERAL_ROTATION`
- `Matrix.TYPE_GENERAL_SCALE`
- `Matrix.TYPE_GENERAL_TRANSFORM`
- `Matrix.TYPE_IDENTITY`
- `Matrix.TYPE_MASK_ROTATION`
- `Matrix.TYPE_MASK_SCALE`
- `Matrix.TYPE_QUADRANT_ROTATION`
- `Matrix.TYPE_TRANSLATION`
- `Matrix.TYPE_UNIFORM_SCALE`
- `Matrix.isEquals(Matrix, Matrix)`
- `Matrix.isIdentity`
- `NonGenericDictionary.#ctor`
- `NonGenericDictionary.getKeysTyped`
- `NonGenericDictionary.getValuesTyped`
- `NonGenericList.add(int, Object)`
- `NonGenericList.addAll(Collection)`
- `NonGenericList.addAll(int, Collection)`
- `NonGenericList.containsAll(Collection)`
- `NonGenericList.get(int)`
- `NonGenericList.getList`
- `NonGenericList.isEmpty`
- `NonGenericList.lastIndexOf(Object)`
- `NonGenericList.listIterator`
- `NonGenericList.listIterator(int)`
- `NonGenericList.remove(int)`
- `NonGenericList.removeAll(Collection)`
- `NonGenericList.retainAll(Collection)`
- `NonGenericList.set(int, Object)`
- `NonGenericList.subList(int, int)`
- `NonGenericList.toArray`
- `NonGenericList.toArray(Object[])`
- `PdfComplianceVersion`
- `PdfComplianceVersion.Pdf15`
- `PdfComplianceVersion.PdfA1a`
- `PdfComplianceVersion.PdfA1b`
- `PixelDataFormat.getCieLab(int, int, int)`
- `PixelDataFormat.getCmyk(int, int, int, int)`
- `PixelDataFormat.getCmyka(int, int, int, int, int)`
- `PixelDataFormat.getGrayscaleAlpha(int, int)`
- `PixelDataFormat.getRgb(int, int, int)`
- `PixelDataFormat.getRgbIndexed(int)`
- `PixelDataFormat.getRgba(int, int, int, int)`
- `PixelDataFormat.getYCbCr(int, int, int)`
- `PixelFormat.CieLab`
- `Point.isEquals(Point, Point)`
- `PointF.isEquals(PointF, PointF)`
- `RasterCachedImage.doRotate(float, boolean, Color)`
- `RasterCachedImage.getRotateMode`
- `RasterCachedImage$RotateTestMode`
- `RasterCachedImage$RotateTestMode.ByteArrayMode`
- `RasterCachedImage$RotateTestMode.RegularMode`
- `RasterCachedImage$RotateTestMode.StreamMode`
- `RasterImage.isUsePalette`
- `Rectangle.isEquals(Rectangle, Rectangle)`
- `RectangleF.isEquals(RectangleF, RectangleF)`
- `RectangleF.op_Division(RectangleF, float)`
- `RectangleF.op_Multiply(RectangleF, float)`
- `Region.isEquals(Region, Graphics)`
- `Size.isEquals(Size, Size)`
- `SizeF.isEquals(SizeF, SizeF)`
- `StreamContainer.READ_WRITE_BYTES_COUNT`
- `StreamContainer.startPosition`
- `StreamContainer.#ctor(Stream)`
- `StreamContainer.#ctor(Stream, boolean)`
- `AsyncTask`
- `AsyncTask.create(AsyncTaskAction)`
- `AsyncTask.create(AsyncTaskFunc)`
- `AsyncTaskAction`
- `AsyncTaskAction.run(IAsyncTaskState)`
- `AsyncTaskException`
- `AsyncTaskException.#ctor(String)`
- `AsyncTaskFunc`
- `AsyncTaskFunc.#ctor`
- `AsyncTaskFunc.beginInvoke(IAsyncTaskState, AsyncCallback, Object)`
- `AsyncTaskFunc.endInvoke(IAsyncResult)`
- `AsyncTaskFunc.invoke(IAsyncTaskState)`
- `AsyncTaskProgress`
- `AsyncTaskProgress.Duration`
- `AsyncTaskProgress.ProgressPercentage`
- `AsyncTaskProgress.#ctor(int, long)`
- `CompleteCallback`
{% endalert %}