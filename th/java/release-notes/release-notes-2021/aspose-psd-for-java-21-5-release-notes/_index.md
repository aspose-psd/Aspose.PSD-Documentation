---
title: Aspose.PSD for Java 21.5 - บันทึกการอัปเดต
type: docs
weight: 40
url: /java/aspose-psd-for-java-21-5-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
นี้เป็นเวอร์ชันระหว่างทางของ Aspose.PSD for Java
มีปัญหาบางอย่างที่รู้จัก ดังนั้นหากคุณต้องการเวอร์ชันที่เสถียร คุณควรใช้ [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) จนกว่า Aspose.PSD 21.6 จะถูกปล่อย
การอัปเดตนี้รวมทุกฟีเจอร์ของ Aspose.PSD .Net (รวมถึงออบเจกต์ฉลอง) ตั้งแต่เวอร์ชัน 20.9 และฟีเจอร์ที่ระบุด้านล่าง
{{% /alert %}} 

|**สำคัญ**|**สรุป**|**ประเภท**|
| :- | :- | :- |
|PSDJAVA-340|สนับสนุนการปรับขนาดชั้นรูปทรงที่มีพาธเวกเตอร์เมื่อเพียงเพียงผู้ปรับขนาดชั้นน้อยลงเท่านั้น|ฟีเจอร์|
|PSDJAVA-341|สนับสนุนการปรับขนาดชั้นรูปทรงที่มีพาธเวกเตอร์|ฟีเจอร์|
|PSDJAVA-342|ข้อความที่ถูกตัด|ข้อบกพร่อง|

# **การเปลี่ยนแปลง API สาธารณะ**
# **เพิ่ม API:**
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
- M:com.aspose.psd.asynctask.AsyncTaskAction.run(com.asposepose.psd.system.io.Stream)
- M:com.aspose.psd.asynctask.AsyncTaskAction.#ctor
- M:com.aspose.psd.asynctask.AsyncTaskAction.run
- T:com.aspose.psd.asynctask.AsyncTaskFunc
- M:com.aspose.psd.asynctask.AsyncTaskFunc.invoke
- M:com.aspose.psd.system.io.Stream.get_Position
- M:com.aspose.psd.system.io.Stream.set_Position(long)
- M:com.aspose.psd.system.io.Stream.get_Length
- M:com.aspose.psd.system.io.Stream.set_Length(long)
- M:com.aspose.psd.system.io.Stream.Read(byte[],int,int)
- M:com.aspose.psd.system.io.Stream.WriteByte(byte)
- M:com.aspose.psd.system.io.Stream.Write(byte[],int,int)
- M:com.aspose.psd.system.io.Stream.Close
- T:com.aspose.psd.system.io.StreamAsyncResult
- M:com.aspose.psd.system.io.StreamAsyncResult.#ctor(com.aspose.psd.asynctask.AsyncTaskAction,java.lang.Object)
- M:com.aspose.psd.system.io.StreamAsyncResult.get_Action
- M:com.aspose.psd.system.io.StreamAsyncResult.get_AsyncState
- M:com.aspose.psd.system.io.StreamAsyncResult.get_CompletedSynchronously
- M:com.aspose.psd.system.io.StreamAsyncResult.get_IsCompleted
- M:com.aspose.psd.system.io.StreamAsyncResult.get_UserState
- M:com.aspose.psd.system.io.StreamAsyncResult.get_Exception
- T:com.aspose.psd.system.io.StreamContainer
- F:com.aspose.psd.system.io.StreamContainer._stream
- M:com.aspose.psd.system.io.StreamContainer.get_ByteBuffer
- M:com.aspose.psd.system.io.StreamContainer.get_CanRead
- M:com.aspose.psd.system.io.StreamContainer.get_CanSeek
- M:com.aspose.psd.system.io.StreamContainer.get_CanWrite
- M:com.aspose.psd.system.io.StreamContainer.get_Length
- M:com.aspose.psd.system.io.StreamContainer.get_Position
- M:com.aspose.psd.system.io.StreamContainer.set_Position(long)
- M:com.aspose.psd.system.io.StreamContainer.read(byte[],int,int)
- M:com.aspose.psd.system.io.StreamContainer.WriteByte(byte)
- M:com.aspose.psd.system.io.StreamContainer.write(byte[],int,int)
- M:com.aspose.psd.system.io.StreamContainer.close
- M:com.aspose.psd.system.io.StreamContainer.seek(long,com.aspose.psd.system.io.SeekOrigin)
- F:com.aspose.psd.system.io.StreamContainer._stream
- F:com.aspose.psd.system.io.StreamContainer.buffer
- M:com.aspose.psd.system.io.StreamContainer.flush
- M:com.aspose.psd.system.io.StreamContainer.seek(long,com.aspose.psd.system.io.SeekOrigin)
- T:com.aspose.psd.system.io.Stream.MemoryStream
- F:com.aspose.psd.system.io.Stream.MemoryStream$$owner
- F:com.aspose.psd.system.io.Stream.MemoryStream.pos
- F:com.aspose.psd.system.io.Stream.MemoryStream.buffer
- F:com.aspose.psd.system.io.Stream.MemoryStream.get_Length
- F:com.aspose.psd.system.io.Stream.MemoryStream.get_Capacity
- M:com.aspose.psd.system.io.Stream.MemoryStream.set_Capacity(int)
- F:com.aspose.psd.system.io.Stream.MemoryStream.get_CanRead
- F:com.aspose.psd.system.io.Stream.MemoryStream.get_CanWrite
- M:com.aspose.psd.system.io.Stream.MemoryStream.get_Position
- M:com.aspose.psd.system.io.Stream.MemoryStream.set_Position(long)
- M:com.aspose.psd.system.io.Stream.MemoryStream.Seek(long,com.aspose.psd.system.io.SeekOrigin)
- M:com.aspose.psd.system.io.Stream.MemoryStream.Read(byte[],int,int)
- M:com.aspose.psd.system.io.Stream.MemoryStream.Write(byte[],int,int)
- M:com.aspose.psd.system.io.Stream.MemoryStream.Close