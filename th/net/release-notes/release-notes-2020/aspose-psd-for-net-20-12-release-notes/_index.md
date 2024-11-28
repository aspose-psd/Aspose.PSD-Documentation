---
title: บันทึกการเปลี่ยนแปลง Aspose.PSD for .NET 20.12
type: สารบัญ
weight: 10
url: /th/net/aspose-psd-for-net-20-12-release-notes/
---

{{% alert color="primary" %}} 

หน้านี้มีบันทึกการเปลี่ยนแปลงสำหรับ [Aspose.PSD for .NET 20.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-757|สนับสนุนการแปลงเลเยอร์เป็นชั้น Smart Object|คุณลักษณะ|
|PSDNET-764|เมธอด SmartObjectLayer.ReplaceContents เกิดข้อผิดพลาด NullReferenceException เมื่อพยายามเพิ่มไฟล์ PSB|ข้อบกพร่อง|
|PSDNET-773|การแสดงผลไม่ถูกต้องของภาพ CMYK 8 บิตและ CMYK 16 บิต หากชั้นใหญ่กว่า Canvas|ข้อบกพร่อง|
|PSDNET-782|ไฟล์ PSB ที่บันทึกสามารถเปิดด้วย API ของเรา, แต่ไม่สามารถเปิดด้วย Photoshop|ข้อบกพร่อง|
|PSDNET-783|หากเราพยายามเปลี่ยน Smart Layer ใน PSD ที่ระบุด้วยแหล่งข้อมูลที่ใช้ร่วมกัน เราได้รับข้อยกเว้น|ข้อบกพร่อง|
|PSDNET-172|การเปลี่ยนชื่อจาก FileFormatVersion เป็น PsdVersion เพื่อหลีกเลี่ยงความสับสน|การปรับปรุง|
|PSDNET-620|นำการกำหนดค่าของ Compact framework ออกจาก Aspose.PSD .NET|การปรับปรุง|
|PSDNET-765|PsdImageException: ส่วนหัวข้อมูลที่ไม่รู้จักเมื่อพยายามเปิดไฟล์ PSB ด้วย SmartObjectLayers|การปรับปรุง|
|PSDNET-798|ย้ายลำดับของคลาสการแมสก์เวกเตอร์ไปยังเนมสเปซหลักเพื่อให้มั่นใจว่า Aspose.PSD และ Aspose.Imaging ภาคผลิตสินค้าของเราเหมือนกัน|การปรับปรุง|

## **การเปลี่ยนแปลง API สาธารณะ**
# **API เพิ่มเติม:**
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

(ข้อคิดความเป็นไปในตอนนี้...)

