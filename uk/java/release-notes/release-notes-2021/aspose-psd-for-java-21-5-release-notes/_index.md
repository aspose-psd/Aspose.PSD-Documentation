---
title: Aspose.PSD для Java 21.5 - Примітки до випуску
type: docs
weight: 40
url: /uk/java/aspose-psd-dlya-java-21-5-prymitky-do-vypusku/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до випуску [Aspose.PSD для Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Це проміжний випуск Aspose.PSD для Java.
Він має деякі відомі проблеми. Тому, якщо вам потрібна стабільна версія, ви повинні використовувати [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) до виходу Aspose.PSD 21.6.
Цей випуск включає всі функції Aspose.PSD .Net (включаючи розумний об'єкт) з версії 20.9 та нижче вказані функції.
{{% /alert %}}

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-340|Підтримка зміни розміру шарів форми з векторними шляхами, коли змінюється лише шар|Функція|
|PSDJAVA-341|Підтримка зміни розміру шарів форми з векторними шляхами|Функція|
|PSDJAVA-342|Обрізаний рядок тексту|Помилка|

# **Зміни у громадському API**
# **Додані API:**
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
- M:---
title: Aspose.PSD для Java 21.5 - Примітки до випуску
type: docs
weight: 40
url: /uk/java/aspose-psd-dlya-java-21-5-prymitky-do-vypusku/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до випуску [Aspose.PSD для Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Це проміжний випуск Aspose.PSD для Java.
Він має деякі відомі проблеми. Тому, якщо вам потрібна стабільна версія, ви повинні використовувати [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) до виходу Aspose.PSD 21.6.
Цей випуск включає всі функції Aspose.PSD .Net (включаючи розумний об'єкт) з версії 20.9 та нижче вказані функції.
{{% /alert %}}

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-340|Підтримка зміни розміру шарів форми з векторними шляхами, коли змінюється лише шар|Функція|
|PSDJAVA-341|Підтримка зміни розміру шарів форми з векторними шляхами|Функція|
|PSDJAVA-342|Обрізаний рядок тексту|Помилка|

# **Зміни у громадському API**
# **Додані API:**
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

# **Видалені API:**
- M:com.aspose.psd.Font.makeTransparent(int)
- M:com.aspose.psd.ManagedImageResource.dispose
- M:com.aspose.psd.RasterImage.isClosed
- M:com.aspose.psd.RasterImage.release
- M:com.aspose.psd.RasterImage.release(com.aspose.psd.system.OperatingSystem,boolean)
- M:com.aspose.psd.SaveOptions.getJpegQualitySetting(isaveoptions.JpegQualitySetting,boolean)
- M:com.aspose.psd.SaveOptions.setJpegQualitySetting(isaveoptions.JpegQualitySetting,int32)
- M:com.aspose.psd.SaveOptions.setJpegQualitySetting(isaveoptions.JpegQualitySetting,java.lang.Object)
- F:com.aspose.psd.SaveOptions.JpegQualitySetting.DEFAULT_JPEG_QUALITY
- M:com.aspose.psd.SaveOptions.JpegQualitySettingValue.#ctor
- M:com.aspose.psd.SaveOptions.JpegQualitySettingValue.#ctor(java.lang.String)
- F:com.aspose.psd.SaveOptions.JpegQualitySettingValue.MaxQuality
- F:com.aspose.psd.SaveOptions.JpegQualitySettingValue.MinQuality
- F:com.aspose.psd.SaveOptions.JpegQualitySettingValue.Quality100
- F:com.aspose.psd.SaveOptions.JpegQualitySettingValue.Undefined
- T:com.aspose.psd.SaveOptions.PngFilterType
- M:com.aspose.psd.SaveOptions.PngFilterTypeValue.#ctor
- F:com.aspose.psd.SaveOptions.PngFilterTypeValue.Adaptive
- F:com.aspose.psd.SaveOptions.PngFilterTypeValue.Auto
- F:com.aspose.psd.SaveOptions.PngFilterTypeValue.None
- F:com.aspose.psd.SaveOptions.PngFilterTypeValue.Paeth
- F:com.aspose.psd.SaveOptions.PngFilterTypeValue.Sub
- F:com.aspose.psd.SaveOptions.PngFilterTypeValue.Up
- F:com.aspose.psd.SaveOptions.PngFilterTypeValue.Undefined

Якщо вам необхідна допомога з Автоматизованим API, не соромтеся [звертатися до нас](https://forum.aspose.com/c/psd).