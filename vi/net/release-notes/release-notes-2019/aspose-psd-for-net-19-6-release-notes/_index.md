---
title: Aspose.PSD cho .NET 19,6 - Ghi Chú Phát Hành
type: docs
weight: 70
url: /vi/net/aspose-psd-cho-net-19-6-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 19,6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-127|Khả năng chuyển đổi tệp PSD thành PSB và ngược lại|Tính năng|
|PSDNET-154|Di dời nguồn Aspose.Imaging 19,5 sang Aspose.PSD|Cải tiến|
|PSDNET-155|Dọn dẹp API công cộng liên quan đến Aspose.PSD|Cải tiến|
|PSDNET-159|Xóa thuộc tính IsLicensed|Cải tiến|
|PSDNET-102|Chuyển đổi PSB thành JPG treo|Lỗi|
|PSDNET-150|Vị trí lớp văn bản mới thêm vào bị dời khi chỉnh sửa trong Photoshop|Lỗi|

## **Thay Đổi API Công Cộng**
# **API Thêm vào:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F:Aspose.PSD.FileFormat.Cdr
- F:Aspose.PSD.FileFormat.Cmx
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P:Aspose.PSD.Image.BufferSizeHint
- P:Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M:Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P:Aspose.PSD.LoadOptions.BufferSizeHint
- T:Aspose.PSD.MemoryManagement.Configuration
- P:Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T:Aspose.PSD.ResolutionUnit
- F:Aspose.PSD.ResolutionUnit.None
- F:Aspose.PSD.ResolutionUnit.Inch
- F:Aspose.PSD.ResolutionUnit.Cm
# **API Loại Bỏ:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapPlanes
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitsPerPixel
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapCoreHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderFullSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV2
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV3
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV4
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV5
- T:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapCompression
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapImageSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapXPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapYPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsUsed
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsImportant
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.ExtraBitMasks
- T:Aspose.PSD.FileFormats.Bmp.BitmapV4Header
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.RedMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GreenMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.BlueMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.AlphaMask
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.CSType
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.Endpoints
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GammaRed
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GammaGreen
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.GammaBlue
- T:Aspose.PSD.FileFormats.Bmp.BitmapV5Header
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.Intent
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.ProfileData
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.ProfileSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapV5Header.Reserved
- T:Aspose.PSD.FileFormats.Bmp.BmpImage
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.String)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.String,System.UInt16,Aspose.PSD.FileFormats.Bmp.BitmapCompression,System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.IO.Stream,System.UInt16,Aspose.PSD.FileFormats.Bmp.BitmapCompression,System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(Aspose.PSD.RasterImage,System.UInt16,Aspose.PSD.FileFormats.Bmp.BitmapCompression,System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.Int32,System.Int32,System.UInt16,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.#ctor(System.Int32,System.Int32,System.UInt16,Aspose.PSD.IColorPalette,Aspose.PSD.FileFormats.Bmp.BitmapCompression,System.Double,System.Double)
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.FileFormat
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.BitmapInfoHeader
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.RawDataFormat
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.RawLineSize
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.Compression
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.Width
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.Height
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.HorizontalResolution
- P:Aspose.PSD.FileFormats.Bmp.BmpImage.VerticalResolution
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.SetResolution(System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.GetDefaultOptions(System.Object[])
- M:Aspose.PSD.FileFormats.Bmp.BmpImage.ToBitmap
- T:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Units
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Reserved
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Recording
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Rendering
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Size1
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Size2
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.ColorEncoding
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Identifier
- T:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinates
- M:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinates.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinates.CieCoordinatesX
- P:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinates.CieCoordinatesY
- P:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinates.CieCoordinatesZ
- T:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinatesTriple
- M:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinatesTriple.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinatesTriple.CieXyzRed
- P:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinatesTriple.CieXyzGreen
- P:Aspose.PSD.FileFormats.Bmp.Structures.CieCoordinatesTriple.CieXyzBlue
- T:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.#ctor
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.#ctor(System.String,System.Byte[],System.Byte[])
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.ApplicationAuthenticationCode
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.ApplicationIdentifier
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.ApplicationData
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.Save(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.BlockHeaderSize
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.ExtensionLabel
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.BlockSize
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.ApplicationIdentifierSize
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifApplicationExtensionBlock.ApplicationAuthenticationCodeSize
- T:Aspose.PSD.FileFormats.Gif.Blocks.GifCommentBlock
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifCommentBlock.#ctor
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifCommentBlock.#ctor(System.String)
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifCommentBlock.Comment
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifCommentBlock.Save(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifCommentBlock.ExtensionLabel
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifCommentBlock.BlockHeaderSize
- T:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.UInt16,System.UInt16)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.UInt16,System.UInt16,System.UInt16,System.UInt16)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.UInt16,System.UInt16,System.UInt16,System.UInt16,Aspose.PSD.IColorPalette,System.Boolean,System.Boolean,System.Byte)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(Aspose.PSD.RasterImage,System.UInt16,System.UInt16)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(Aspose.PSD.RasterImage,System.UInt16,System.UInt16,System.Boolean,System.Boolean,System.Byte)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.IO.Stream,System.UInt16,System.UInt16)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.IO.Stream,System.UInt16,System.UInt16,System.Boolean,System.Boolean,System.Byte)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.String)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.String,System.UInt16,System.UInt16)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.#ctor(System.String,System.UInt16,System.UInt16,System.Boolean,System.Boolean,System.Byte)
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.FileFormat
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.Width
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.Height
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.BitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.Interlaced
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.IsPaletteSorted
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.GifFrameBitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.Left
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.Top
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.Flags
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.ControlBlock
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.HasTransparentColor
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.TransparentColor
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.GetColorPalette(Aspose.PSD.IColorPalette,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.CreateFlags(Aspose.PSD.IColorPalette,System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.ReplaceNonTransparentColors(System.Int32)
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.ExtensionLabel
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock.ImageDescriptorSize
- T:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.#ctor
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.#ctor(System.Byte,System.UInt16,System.Byte)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.#ctor(System.UInt16,System.Boolean,System.Byte,System.Boolean,Aspose.PSD.FileFormats.Gif.DisposalMethod)
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.DelayTime
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.Flags
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.TransparentColorIndex
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.DisposalMethod
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.UserInputExpected
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.HasTransparentColor
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.CreateFlags(System.Boolean,System.Boolean,Aspose.PSD.FileFormats.Gif.DisposalMethod)
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.Save(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.BlockHeaderSize
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.ExtensionLabel
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifGraphicsControlBlock.SubBlockSize
- T:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.#ctor
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.#ctor(System.UInt16,System.UInt16,System.UInt16,System.UInt16,System.Byte,System.Byte,System.Byte,System.Byte,System.Byte[])
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.TextForegroundColorIndex
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.TextBackgroundColorIndex
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.CharacterCellWidth
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.CharacterCellHeight
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.TextGridLeftPosition
- P:Aspose.PSD.FileFormats-Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.TextGridTopPosition
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.TextGridWidth
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.TextGridHeight
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.PlainTextData
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.Save(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.ExtensionLabel
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.BlockSize
- F:Aspose.PSD.FileFormats.Gif.Blocks.GifPlainTextRenderingBlock.SubBlockSize
- T:Aspose.PSD.FileFormats.Gif.Blocks.GifUnknownExtensionBlock
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifUnknownExtensionBlock.#ctor
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifUnknownExtensionBlock.#ctor(System.Byte,System.Byte[])
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifUnknownExtensionBlock.ExtensionLabel
- P:Aspose.PSD.FileFormats.Gif.Blocks.GifUnknownExtensionBlock.UnknownData
- M:Aspose.PSD.FileFormats.Gif.Blocks.GifUnknownExtensionBlock.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Gif.DisposalMethod
- F:Aspose.PSD.FileFormats.Gif.DisposalMethod.None
- F:Aspose.PSD.FileFormats.G