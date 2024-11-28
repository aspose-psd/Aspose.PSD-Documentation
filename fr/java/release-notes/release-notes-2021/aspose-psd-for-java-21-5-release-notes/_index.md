---
title: Aspose.PSD pour Java 21.5 - Notes de publication
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-21-5-notes-de-publication/
---

{{% alert color="primary" %}} Cette page contient les notes de publication pour [Aspose.PSD pour Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-pour-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Il s'agit d'une version intermédiaire de Aspose.PSD pour Java.
Il y a quelques problèmes connus. Donc, si vous avez besoin d'une version stable, vous devriez utiliser [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-pour-java-20.9/) jusqu'à ce que Aspose.PSD 21.6 soit publié.
Cette version inclut toutes les fonctionnalités Aspose.PSD .Net (y compris les objets intelligents) depuis 20.9 et les fonctionnalités répertoriées ci-dessous.
{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-340|Prise en charge du redimensionnement des calques de forme avec des chemins vectoriels lorsque seul un calque est redimensionné|Fonctionnalité|
|PSDJAVA-341|Prise en charge du redimensionnement des calques de forme avec des chemins vectoriels|Fonctionnalité|
|PSDJAVA-342|Chaîne de texte tronquée|Bogue|

# **Changements de l'API publique**
# **API ajoutées :**
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
- T:com.aspose.psd---

asynctask.AsyncTaskProgress.ReportProgress(com.aspose.psd.asynctask.AsyncTaskProgress)
- T:com.aspose.psd.asynctask.IAsyncTaskState
- M:com.aspose.psd.asynctask.IAsyncTaskState.get_Cancel
- M:com.aspose.psd.asynctask.IAsyncTaskState.get_Percentage
- M:com.aspose.psd.asynctask.IAsyncTaskState.set_Percentage(int)
- T:com.aspose.psd.brushes.LinearGradientBrush
- F:com.aspose.psd.brushes.LinearGradientBrush.alphaFactors
- F:com.aspose.psd.brushes.LinearGradientBrush.alphaPositions
- F:com.aspose.psd.brushes.LinearGradientBrush.colors
- F:com.aspose.psd.brushes.LinearGradientBrush.positions
- M:com.aspose.psd.brushes.TextureBrush.rotationAngle
- M:com.aspose.psd.brushes.TextureBrush.setTextureTransform(com.aspose.psd.system.drawing.DrawingMatrix)
- T:com.aspose.psd.brushes.TransformMode
- F:com.aspose.psd.brushes.TransformMode.FILL_TO_BORDER
- F:com.aspose.psd.brushes.TransformMode.NONE
- F:com.aspose.psd.brushes.TransformMode.REPEAT
- T:com.aspose.psd.CompressionMethod
- F:com.aspose.psd.CompressionMethod.Deflate
- F:com.aspose.psd.CompressionMethod.None
- T:com.aspose.psd.FileFormats.Psd.BlrResource.ResourceType
- F:com.aspose.psd.FileFormats.Psd.BlrResource.ResourceType.ShapeMetaData
- F:com.aspose.psd.FileFormats.Psd.BlrResource.ResourceType.VectorMetaData
- T:com.aspose.psd.Fonts.FontSettingsSubstitution
- F:com.aspose.psd.Fonts.FontSettingsSubstitution.None
- F:com.aspose.psd.Fonts.FontSettingsSubstitution.SystemDefault
- T:com.aspose.psd.GraphicsBlend
- F:com.aspose.psd.GraphicsBlend.lhsAlpha
- F:com.aspose.psd.GraphicsBlend.lhsColor
- F:com.aspose.psd.GraphicsBlend.rhsAlpha
- F:com.aspose.psd.GraphicsBlend.rhsColor
- T:com.aspose.psd.GraphicsLineCap
- F:com.aspose.psd.GraphicsLineCap.Round
- F:com.aspose.psd.GraphicsLineCap.Square
- T:com.aspose.psd.GraphicsLineJoin
- F:com.aspose.psd.GraphicsLineJoin.Bevel
- F:com.aspose.psd.GraphicsLineJoin.Miter
- T:com.aspose.psd.GraphicsPath
- F:com.aspose.psd.GraphicsPath.PathTypes
- F:com.aspose.psd.GraphicsPath.Points
- F:com.aspose.psd.GraphicsPath.StartFigure
- M:com.aspose.psd.GraphicsPath.addEllipse(com.aspose.psd.Rectangle)
- M:com.aspose.psd.GraphicsPath.closeFigure
- M:com.aspose.psd.GraphicsPath.startFigure
- T:com.aspose.psd.GraphicsPathAddMode
- F:com.aspose.psd.GraphicsPathAddMode.Add
- F:com.aspose.psd.GraphicsPathAddMode.Override
- T:com.aspose.psd.GraphicsPolygonOffsetMode
- F:com.aspose.psd.GraphicsPolygonOffsetMode.None
- F:com.aspose.psd.GraphicsPolygonOffsetMode.Offset
- M:com.aspose.psd.GraphicsPolygonOffsetOffset(com.aspose.psd.Color,double,double)
- T:com.aspose.psd.Points
- F:com.aspose.psd.Points.point
- F:com.aspose.psd.Points.tension
- F:com.aspose.psd.Points.type
- T:com.aspose.psd.PointsCurveFlag
- F:com.aspose.psd.PointsCurveFlag.Bezier
- F:com.aspose.psd.PointsCurveFlag.None
- M:com.aspose.psd.Points.contains(com.aspose.psd.Point)
- M:com.aspose.psd.Points.get_Item(int)
- M:com.aspose.psd.Points.get_Length
- M:com.aspose.psd.Points.set_Item(int,com.aspose.psd.Point)

# **Modifications de l'API :**
# **Propriétés ajoutées :**
- couleur : com.aspose.psd.brushes.LinearGradientBrush.coefficientsAlpha
- couleur : com.aspose.psd.brushes.LinearGradientBrush.positionsAlpha
- couleur : com.aspose.psd.brushes.LinearGradientBrush.colors
- couleur : com.aspose.psd.brushes.LinearGradientBrush.positifs
- méthode com.aspose.psd.brushes.TextureBrush.angleRotation
- méthode com.aspose.psd.brushes.TextureBrush.set_TransformTexture(com.aspose.psd.system.drawing.DrawingMatrix)
- valeur énumérée com.aspose.psd.brushes.TransformMode.REMPLI_AVEC_BORDURE
- valeur énumérée com.aspose.psd.brushes.TransformMode.AUCUN
- valeur énumérée com.aspose.psd.brushes.TransformMode.REPETITION
- valeur énumérée com.aspose.psd.CompressionMethod.Deflate
- valeur énumérée com.aspose.psd.CompressionMethod.None
- valeur énumérée com.aspose.psd.FileFormats.Psd.BlrResource.TypeRessource.MetaDonnéesForme
- valeur énumérée com.aspose.psd.FileFormats.Psd.BlrResource.TypeRessource.MetaDonnéesVectorielles

Début de la partie modifiée du fichier...