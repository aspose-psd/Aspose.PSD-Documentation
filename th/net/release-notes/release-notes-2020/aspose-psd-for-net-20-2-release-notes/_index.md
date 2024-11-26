---
title: บันทึกการเปลี่ยนแปลง Aspose.PSD for .NET 20.2
type: สารบัญ
weight: 110
url: /th/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการเปลี่ยนแปลงสำหรับ [Aspose.PSD for .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-206|การปรับปรุงความสามารถในการแสดงข้อความสีต่าง ๆ ในชั้นข้อความ|คุณลักษณะ|
|PSDNET-369|สนับสนุนทรัพยากร clbl (ทรัพยากรชั้นข้อมูลเกี่ยวกับองค์ประกอบการตัดทำนอง)|คุณลักษณะ|
|PSDNET-274|สนับสนุนทรัพยากร blwh (ทรัพยากรมีข้อมูลเกี่ยวกับชั้นปรับปรุงขาว-ดำ)|คุณลักษณะ|
|PSDNET-230|ความสามารถในการส่งออกกลุ่มชั้นเป็น Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|คุณลักษณะ|
|PSDNET-372|สนับสนุนทรัพยากร lspf (มีการตั้งค่าเกี่ยวกับการตั้งค่าการป้องกันชั้น)|คุณลักษณะ|
|PSDNET-370|สนับสนุนทรัพยากร infx (มีข้อมูลเกี่ยวกับการผสมขององค์ประกอบภายใน)|คุณลักษณะ|
|PSDNET-251|การเรียกใช้รหัส PsdImage และ Layer เพื่อเปลี่ยนพฤติกรรมการแปลง (ปรับขนาด/หมุน/ตัดถ้าเราแปลงชั้นหนึ่งๆ โดยแยกกัน)|การปรับปรุง|
|PSDNET-276|ในบางการตั้งค่าวัฒนธรรมเล็กๆ รูปแบบ AI Image ไม่สามารถเปิด|ข้อบกพร่อง|
|PSDNET-194|หลังจากดำเนินการสับกลับรูปหรือหมุนในชั้น PSD รูปภาพเป็นไฟล์ที่ไม่สามารถอ่านได้|ข้อบกพร่อง|
|PSDNET-177. |System.ArgumentException ในระหว่างการโหลดไฟล์ PSD|ข้อบกพร่อง|
|PSDNET-249|หลังใช้วิธีการแปลงสำหรับชั้นเท่านั้น ชั้นที่บันทึกจะมีขอบไม่ถูกต้องหรือมาสก์|ข้อบกพร่อง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue

[ข้อความที่ระบุตกคล
حغمأم]- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykColor.Equals(System.Object)
- T:Aspose.PSD.CompositeException
- T:Aspose.PSD.CoreExceptions.IndexOutOFRangeException
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String)
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String,System.Exception)
- F:Aspose.PSD.FileFormat.Otg
- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000CustomException
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.IsDataStoredDiscretely
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetChannelData(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey
- T:Aspose.PSD.ImageOptions.TiffOptionsUtils
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])
- P:Aspose.PSD.ImageOptionsBase.ProgressEventHandler
- P:Aspose.PSD.LoadOptions.ProgressEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Metered.Equals(System.Object)
- T:Aspose.PSD.ProgressEventHandler
- T:Aspose.PSD.ProgressManagement.EventType
- F:Aspose.PSD.ProgressManagement.EventType.RelativeProgress
- F:Aspose.PSD.ProgressManagement.EventType.StageChange
- F:Aspose.PSD.ProgressManagement.EventType.Initialization
- F:Aspose.PSD.ProgressManagement.EventType.PreProcessing
- F:Aspose.PSD.ProgressManagement.EventType.Processing
- F:Aspose.PSD.ProgressManagement.EventType.Finalization
- T:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Description
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.EventType
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.MaxValue
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Value
- M:Aspose.PSD.RasterImage.GetSkewAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Color)