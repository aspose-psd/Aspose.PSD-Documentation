---
title: Catatan Rilis Aspose.PSD untuk .NET 20.12
type: dokumen
weight: 10
url: /id/net/aspose-psd-for-net-20-12-release-notes/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 20.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-757|Dukungan mengonversi lapisan ke Lapisan Objek Cerdas|Fitur|
|PSDNET-764|Metode SmartObjectLayer.ReplaceContents menghasilkan NullReferenceException jika mencoba menambahkan file PSB|Bug|
|PSDNET-773|Render CMYK 8-bit dan Gambar 16-bit CMYK tidak benar, jika lapisan lebih besar dari Kanvas|Bug|
|PSDNET-782|File PSB yang disimpan dapat dibuka dengan API kami, tetapi tidak dengan Photoshop|Bug|
|PSDNET-783|Jika mencoba mengubah Lapisan Pintar dalam PSD tertentu dengan sumber data bersama, kami mendapatkan pengecualian|Bug|
|PSDNET-172|Penggantian FileFormatVersion menjadi PsdVersion untuk menghindari kebingungan|Peningkatan|
|PSDNET-620|Hapus konfigurasi kerangka Compact dari Aspose.PSD .NET|Peningkatan|
|PSDNET-765|PsdImageException: Header sumber tidak dikenal saat mencoba membuka file PSB dengan SmartObjectLayers|Peningkatan|
|PSDNET-798|Pindahkan Hirarki Kelas Masker Vektor ke Ruang Nama Inti untuk memastikan keseragaman Produk Aspose.PSD dan Aspose.Imaging|Peningkatan|

## **Perubahan API Publik**
# **API Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.PsdVersion
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.PsdVersion
- T:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.PathPoints
- P:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.Points
- P:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.IsClosed
- P:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.IsLinked
- P:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.IsOpen
- P:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.Type
- T:Aspose.PSD.FileFormats.Core.VectorPaths.ClipboardRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.ClipboardRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.ClipboardRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Core.VectorPaths.ClipboardRecord.BoundingRect
- P:Aspose.PSD.FileFormats.Core.VectorPaths.ClipboardRecord.Resolution
- P:Aspose.PSD.FileFormats.Core.VectorPaths.ClipboardRecord.Type
- T:Aspose.PSD.FileFormats.Core.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Core.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Core.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Core.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Core.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Core.VectorPaths.IVectorPathData.IsInverted
- T:Aspose.PSD.FileFormats.Core.VectorPaths.InitialFillRuleRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.InitialFillRuleRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Core.VectorPaths.InitialFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Core.VectorPaths.InitialFillRuleRecord.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Core.VectorPaths.InitialFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.IsClosed
- P:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.IsOpen
- P:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.RecordCount
- P:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.Type
- P:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Core.VectorPaths.PathFillRuleRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.PathFillRuleRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.PathFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Core.VectorPaths.PathFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Core.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Core.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Core.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Core.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Core.VectorPaths.PathOperations.IntersectShapeAreas
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecord.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecord.Type
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.ProducePathRecord(System.Byte[])
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.ClosedSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.ClosedSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.ClosedSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.OpenSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.OpenSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.OpenSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.PathFillRuleRecord
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.ClipboardRecord
- F:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathType.InitialFillRuleRecord
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginIndex
- F:Aspose.PSD.FileFormat.Html5Canvas
- F:Aspose.PSD.FileFormat.Apng
- F:Aspose.PSD.FileFormat.Tga
- T:Aspose.PSD.FileFormats.Core.Blending.BlendMode
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Absent
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Color
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Darken
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Difference
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Dissolve
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.ColorDodge
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.DarkerColor
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Divide
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Subtract
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.HardLight
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.HardMix
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Hue
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.ColorBurn
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.LinearLight
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.LinearBurn
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.LinearDodge
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.LighterColor
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Lighten
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Luminosity
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Multiply
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Normal
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Overlay
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.PinLight
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.PassThrough
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.SoftLight
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Saturation
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Screen
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.Exclusion
- F:Aspose.PSD.FileFormats.Core.Blending.BlendMode.VividLight
- T:Aspose.PSD.AsyncTask.AsyncTask
- M:Aspose.PSD.AsyncTask.AsyncTask.Create(Aspose.PSD.AsyncTask.AsyncTaskAction)
- M:Aspose.PSD.AsyncTask.AsyncTask.Create(Aspose.PSD.AsyncTask.AsyncTaskFunc)
- T:Aspose.PSD.AsyncTask.AsyncTaskAction
- T:Aspose.PSD.AsyncTask.AsyncTaskException
- M:Aspose.PSD.AsyncTask.AsyncTaskException.#ctor(System.String)
- T:Aspose.PSD.AsyncTask.AsyncTaskFunc
- T:Aspose.PSD.AsyncTask.AsyncTaskProgress
- M:Aspose.PSD.AsyncTask.AsyncTaskProgress.#ctor(System.Int32,System.TimeSpan)
- F:Aspose.PSD.AsyncTask.AsyncTaskProgress.Duration
- F:Aspose.PSD.AsyncTask.AsyncTaskProgress.ProgressPercentage
- T:Aspose.PSD.AsyncTask.CompleteCallback
- T:Aspose.PSD.AsyncTask.IAsyncTask
- P:Aspose.PSD.AsyncTask.IAsyncTask.Progress
- P:Aspose.PSD.AsyncTask.IAsyncTask.IsBusy
- P:Aspose.PSD.AsyncTask.IAsyncTask.IsCanceled
- P:Aspose.PSD.AsyncTask.IAsyncTask.IsFaulted
- P:Aspose.PSD.AsyncTask.IAsyncTask.Error
- P:Aspose.PSD.AsyncTask.IAsyncTask.Result
- M:Aspose.PSD.AsyncTask.IAsyncTask.RunAsync
- M:Aspose.PSD.AsyncTask.IAsyncTask.RunAsync(System.Threading.ThreadPriority)
- M:Aspose.PSD.AsyncTask.IAsyncTask.Cancel
- M:Aspose.PSD.AsyncTask.IAsyncTask.Abort
- M:Aspose.PSD.AsyncTask.IAsyncTask.SetProgressCallback(Aspose.PSD.AsyncTask.ProgressCallback)
- M:Aspose.PSD.AsyncTask.IAsyncTask.SetCompleteCallback(Aspose.PSD.AsyncTask.CompleteCallback)
- T:Aspose.PSD.AsyncTask.IAsyncTaskState
- P:Aspose.PSD.AsyncTask.IAsyncTaskState.IsCanceled
- P:Aspose.PSD.AsyncTask.IAsyncTaskState.Progress
- M:Aspose.PSD.AsyncTask.IAsyncTaskState.SetProgress(System.Int32)
- T:Aspose.PSD.AsyncTask.ProgressCallback
- M:Aspose.PSD.ColorPaletteHelper.GetCloseImagePalette(Aspose.PSD.RasterImage,Aspose.PSD.Rectangle,System.Int32,System.Boolean)
- M:Aspose.PSD.ColorPaletteHelper.HasTransparentColors(Aspose.PSD.IColorPalette)
- T:Aspose.PSD.Evalute.EvalException
- P:Aspose.PSD.Evalute.EvalException.Message
- F:Aspose.PSD.FileFormats.Bmp.BitmapCompression.Dxt1
- P:Aspose.PSD.FileFormats.Pdf.PdfCoreOptions.PdfCompliance
- F:Aspose.PSD.FileFormats.Tiff.Enums.TiffTags.PhotoshopResources
- F:Aspose.PSD.FileFormats.Tiff.Enums.TiffTags.XPTitle
- F:Aspose.PSD.FileFormats.Tiff.Enums.TiffTags.XPComment
- F:Aspose.PSD.FileFormats.Tiff.Enums.TiffTags.XPAuthor
- F:Aspose.PSD.FileFormats.Tiff.Enums.TiffTags.XPKeywords
- F:Aspose.PSD.FileFormats.Tiff.Enums.TiffTags.XPSubject
- T:Aspose.PSD.FlatArray.Exceptions.FlatArrayException
- M:Aspose.PSD.Image.GetImage2Export(Aspose.PSD.ImageOptionsBase,Aspose.PSD.Rectangle)
- P:Aspose.PSD.ImageOptions.MultiPageOptions.PageRasterizationOptions
- P:Aspose.PSD.ImageOptions.MultiPageOptions.MergeLayers
- F:Aspose.PSD.ImageOptions.PngOptions.DefaultCompressionLevel
- P:Aspose.PSD.ImageOptions.TiffOptions.CompressedQuality
- P:Aspose.PSD.ImageOptions.TiffOptions.XPTitle
- P:Aspose.PSD.ImageOptions.TiffOptions.XPComment
- P:Aspose.PSD.ImageOptions.TiffOptions.XPAuthor
- P:Aspose.PSD.ImageOptions.TiffOptions.XPKeywords
- P:Aspose.PSD.ImageOptions.TiffOptions.XPSubject
- P:Aspose.PSD.ImageOptionsBase.FullFrame
- T:Aspose.PSD.PdfComplianceVersion
- F:Aspose.PSD.PdfComplianceVersion.Pdf15
- F:Aspose.PSD.PdfComplianceVersion.PdfA1a
- F:Aspose.PSD.PdfComplianceVersion.PdfA1b
- M:Aspose.PSD.PixelDataFormat.GetGrayscaleAlpha(System.Int32,System.Int32)
- M:Aspose.PSD.PixelDataFormat.GetRgb(System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.PixelDataFormat.GetRgba(System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.PixelDataFormat.GetRgbIndexed(System.Int32)
- M:Aspose.PSD.PixelDataFormat.GetYCbCr(System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.PixelDataFormat.GetCmyk(System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.PixelDataFormat.GetCmyka(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.PixelDataFormat.GetCieLab(System.Int32,System.Int32,System.Int32)
- F:Aspose.PSD.PixelFormat.CieLab
- M:Aspose.PSD.RasterImage.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase,Aspose.PSD.Rectangle)
- M:Aspose.PSD.RectangleF.op_Multiply(Aspose.PSD.RectangleF,System.Single)
- M:Aspose.PSD.RectangleF.op_Division(Aspose.PSD.RectangleF,System.Single)

# **API Dihapus:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- T:Aspose.PSD.FileFormats.Psd.Layers.BlendMode
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Color
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Darken
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Difference
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Dissolve
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.ColorDodge
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.DarkerColor
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Divide
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Subtract
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.HardLight
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.HardMix
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Hue
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.ColorBurn
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.LinearLight
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.LinearBurn
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.LinearDodge
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.LighterColor
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Lighten
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Luminosity
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Multiply
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Normal
- F:Aspose.PSD.FileFormats.Psd.L