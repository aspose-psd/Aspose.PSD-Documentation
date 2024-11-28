---

title: การแก้ไขหน้ากากชั้นเราสเตอร์ในไฟล์ PSD ผ่าน API
type: เอกสาร
weight: 20
url: /th/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **ภาพรวม**
**เพื่อออโตเมติกการแก้ไขรูปแบบ PSD และเปลี่ยนไฟล์ PSD โดยไม่ต้องใช้ Adobe® Photoshop® คุณสามารถใช้ Aspose.PSD API ด้านล่างได้ มีโค้ดย่อ C# และ .NET ที่ช่วยให้คุณสามารถแก้ไขไฟล์ PSD**

การใช้ PSD Layer และ Vector Masks เราสามารถซ่อนและแสดงพิกเซลของชั้นโดยไม่ลบอย่างถาวร หน้ากากเราสเตอร์เรียกอีกชื่อหนึ่งว่าหน้ากากชั้นหรือหน้ากากผู้ใช้ การเข้าถึงหน้ากากแรสเตอร์และเวกเตอร์ใน Aspose.PSD มีทางเข้าผ่านคุณสมบัติเลเยอร์ [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata)ซึ่งสามารถเป็นตัวอย่างของคลาส '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' และ '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' ที่เป็นคลาสลูกของคลาส 'LayerMaskData' อย่างน้อยถ้าเลเยอร์มีทั้งหน้ากากแรสเตอร์และเวกเตอร์ จะมีอินสแตนซ์ของ [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull) ถูกนำมา หากเลเยอร์มีเพียงแค่หน้ากากแรสเตอร์หรือเวกเตอร์ จะมีอินสแตนซ์ของ [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort) ถูกนำมา พรอพเพอร์ตี LayerMaskData ถ้าค่าเป็น null แสดงว่าเลเยอร์ไม่มีหน้ากากหรือมีเพียงหน้ากากเวกเตอร์ที่ปิดการใช้งานอย่างเดียว

|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>หน้ากากแรสเตอร์และหน้ากากเวกเตอร์ที่ถูกปิดใช้งาน LayerMaskDataShort</p><p>หน้ากากราชเทอร์ที่ถูกปิดใข้งาน LayerMaskDataShort</p><p>หน้ากากแรสเตอร์และหน้ากากเวกเตอร์ LayerMaskDataFull</p><p>หน้ากากแรสเตอร์ LayerMaskDataShort</p><p>หน้ากากเวกเตอร์ LayerMaskDataShort</p><p>หน้ากากเว็คเตอร์ที่ถูกปิดการใช้งาน null (แต่มีทรัพยากรเวกเตอร์)</p>|
| :- | :- |
## **วิธีการดึงหน้ากากแรสเตอร์ของเลเยอร์ในไฟล์ PSD?**
ต้องมั่นใจก่อนว่าเลเยอร์มีทั้งหน้ากากเวกเตอร์และหน้ากากราชเทอร์:

โค้ดตัวอย่างด้านล่างแสดงวิธีการดึงหน้ากากแรสเตอร์ของเลเยอร์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

มิฉะนั้น ประเภทของสมบัติเลเยอร์ LayerMaskData คือ LayerMaskDataShort ในกรณีนี้ มาตรวจสอบว่าเลเยอร์มีหน้ากากแรสเตอร์อย่างเดียวหรือไม่โดยการตรวจสอบสมบัติ Flags ไม่ควรมี [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).UserMaskFromRenderingOtherData flag มิฉะนั้นหน้ากากก็คือแคชของหน้ากากเวกเตอร์

การดึงโค้ดหน้ากาก:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

หากคุณต้องการ **ดึงหน้ากากแรสเตอร์** เป็น LayerMaskDataShort (สำหรับการจัดการต่อไป) แม้ว่าทั้งสองหน้ากากจะมีอยู่ LayerMaskDataFull ควรสกัดและแปลงไปเป็น LayerMaskDataShort  โค้ดต่อไปนี้สามารถใช้ได้สำหรับทั้งสองกรณี:

การสกัดหน้ากากแรสเตอร์จาก PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **การตรวจสอบว่าเลเยอร์ในไฟล์ PSD มีหน้ากากแรสเตอร์หรือไม่?**
โค้ด C# ต่อไปนี้อาจช่วยให้คุณตรวจสอบว่าเลเยอร์มีหน้ากากแรสเตอร์หรือไม่:

วิธีตรวจสอบว่าหน้ากากแรสเตอร์ถูกนำไปใช้กับ [PSD Layer](/psd/th/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **วิธีการลบ / เพิ่ม / อัปเดตหน้ากากแรสเตอร์ของเลเยอร์ในไฟล์ PSD?**
การลบ / เพิ่ม / อัปเดตเพียงแค่ LayerMaskData ไม่เพียงพอสำหรับการบันทึกให้ถูกต้องเพราะช่องไม่ได้รับการอัพเดท แม้ว่าจะสามารถให้การแสดงผลได้อย่างถูกต้อง นี้ไม่ทำให้ช่องหน้ากากเปลี่ยนไป:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

ควรใช้วิธีการเพิ่มเลเยอร์ AddLayerMask สำหรับการลบ / เพิ่ม / อัปเดต

นี้จะเพิ่ม / อัปเดตทั้งหน้ากากและช่อง:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

นี้จะลบทั้งหน้ากากและช่อง:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **การลบหน้ากากแรสเตอร์ของเลเยอร์ในภาพ PSD**
ก่อนอื่นเราตรวจสอบว่าหน้ากากเป็นรูปแบบสั้นและหากมันไม่ใช่หนึ่งเวกเตอร์เราสามารถเรียก AddLayerMask method ด้วย null เพื่อลบหน้ากากแรสเตอร์ แต่หากมันเป็นรูปแบบเต็มเราต้องแปลงเป็นรูปแบบสั้นเพื่อทิ้งเฉพาะหน้ากากเวกเตอร์ไว้เพียงอย่างเดียว สำหรับการลบหน้ากากชั้น ข้อมูลนี้เป็นตัวอย่าง

โค้ดตัวอย่างวิธีการลบหน้ากากชั้นจากไฟล์ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **การอัปเดตหน้ากากแรสเตอร์ของเลเยอร์ในภาพ PSD**
นี่ คือง่ายต่อการกระทำ: หน้ากากเป็นชนิดสั้นเราต้องเปลี่ยน ImageData และ MaskRectangle ถ้าจำเป็น, มิฉะนั้น [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)และ [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle) ควรเปลี่ยน โค้ดตัวอย่างนี้สามารถใช้สำหรับการอัปเดตหน้ากากชั้น:

อัปเดต PSD Layer Mask ด้วย C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

นี่คือตัวอย่างของการกระทำที่เป็นไปได้ที่เปลี่ยนหน้ากากแรสเตอร์ อันนี้กลับด้านหน้าของหน้ากากของเลเยอร์:

อัปเดต PSD Layer Mask ด้วย C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **การอัปเดตหน้ากากเวกเตอร์ในไฟล์ PSD เมื่อหน้ากากแรสเตอร์ของเลเยอร์มีอยู่**
มันถูกคาดว่าผู้ใช้ได้เปลี่ยนโอปเจ็คเวกเตอร์ไปแล้ว จากนั้นนั้นสามารถอัปเดตหน้ากากเวกเตอร์ได้โดยกระทำการเรียก [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask) ต่อเลเยอร์:

อัปเดต [PSD Layer Vector Mask ](/psd/th/net/layer-vector-mask/)ด้วย C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **การเพิ่มหน้ากากแรสเตอร์ของเลเยอร์ในไฟล์ PSD**
ถ้าเลเยอร์ไม่มีหน้ากากเราสามารถเพิ่มหน้ากากแรสเตอร์ที่กำหนดโดยการเรียก AddLayerMask layer method

ถ้าหน้ากากไม่มี [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)flag หมายความว่ามันมีหน้ากากแรสเตอร์อยู่แล้ว และเราต้องอัปเดตมันตามที่ได้อธิบายไว้ข้างบน มิฉะนั้น หากรูปแบบหน้ากากนี้เป็นรูปแบบสั้นเราจะแปลงเป็นรูปแบบเต็ม หากไม่ เราใช้เหมือนเดิม จากนั้นอัปเดต UserMaskData UserMaskRectangle และคุณสมบัติอื่นๆ ด้วยคุณสมบัติหน้ากากที่กำหนด โค้ดตัวอย่างวิ
