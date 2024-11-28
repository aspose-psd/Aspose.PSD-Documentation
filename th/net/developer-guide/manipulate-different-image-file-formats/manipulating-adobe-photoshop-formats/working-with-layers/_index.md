---
title: การทำงานกับเลเยอร์
type: docs
weight: 150
url: /th/net/working-with-layers/
---

## **สร้างกลุ่มเลเยอร์**
กลุ่มเลเยอร์ประกอบด้วยหนึ่งหรือมากกว่าหนึ่งเลเยอร์และช่วยในการจัดระเบียบเลเยอร์ที่คล้ายหรือเกี่ยวข้องกัน โดยใช้ Aspose.PSD สำหรับ .NET คุณสามารถสร้างกลุ่มเลเยอร์ ในวัตถุดิบบใหม่ [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) **ได้** โดยเพิ่มเมธอดใหม่ในคลาส **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** เพื่อเพิ่มกลุ่มเลเยอร์

ขั้นตอนในการสร้างกลุ่มเลเยอร์มีความง่ายดังต่อไปนี้:

- สร้างอินสแตนซ์ของภาพโดยใช้คลาส PsdImage ด้วยความกว้างที่ระบุ, ความสูง และตัวเลือกของภาพ
- สร้าง **[LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/layers/layergroup)** ด้วยชื่อกลุ่มและดัชนีที่ระบุ
- สร้างอินสแตนซ์ของคลาสเลเยอร์ และกำหนดภาพ PSD ให้กับมัน
- เพิ่มเลเยอร์ที่สร้างขึ้นไปยังกลุ่มเลเยอร์โดยใช้เมธอด AddLayer ที่เปิดเผยโดยคลาส LayerGroup
- บันทึกผลลัพธ์

ส่วนโค้ดต่อไปนี้จะแสดงวิธีการสร้างกลุ่มเลเยอร์

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **เปลี่ยนชื่อเลเยอร์**
คุณสามารถใช้ชื่อใดก็ตามที่คุณต้องการ แต่วิธีปฏิบัติที่ทั่วไปคือการใช้คำอธิบายทั่วไปของวัตถุหรือองค์ประกอบที่อยู่บนเลเยอร์นั้น บทความนี้สาธิตถึงวิธีการเปลี่ยนชื่อเลเยอร์โดยใช้ Aspose.PSD สำหรับ .NET ในเชิงนี้ มีเพิ่มคุณสมบัติใหม่ [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) ในคลาสเลเยอร์เพื่อแสดงชื่อเลเยอร์อย่างถูกต้อง ได้มีการสังเกตว่าเมื่อ Photoshop บันทึกชื่อเลเยอร์โดยใช้คุณสมบัติ [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/name) แล้ว ตัวอักขระเกาหลีถูกเก็บเป็น byte 63'?' ในรหัส ASCII ดังนั้นหากคุณต้องการแสดงชื่อเลเยอร์อย่างถูกต้องให้ใช้คุณสมบัติ **DisplayName** เพราะคุณสมบัติ **Name** ไม่รองรับตัวอักษรเกาหลี

โค้ดตัวอย่างต่อไปนี้แสดงวิธีการเปลี่ยนชื่อเลเยอร์


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **สนับสนุนเลเยอร์ที่เชื่อมโยงกัน**
การเชื่อมโยงเลเยอร์เหมือนกับการจัดกลุ่มเลเยอร์ หากคุณเชื่อมโยงเลเยอร์สองหรือมากกว่า จะช่วยให้คุณทำการเปลี่ยนแปลงบางอย่างให้กับเลเยอร์ที่เชื่อมโยงทั้งหมด ตัวอย่างเช่น หากคุณใช้การแปรผันกับเลเยอร์หนึ่ง จะถูกใช้กับเลเยอร์ที่เชื่อมโยงอื่นๆ บทความนี้สาธิตถึงวิธีการดึงข้อมูลและยกเลิกการเชื่อมโยงของเลเยอร์โดยใช้ [Aspose.PSD](https://products.aspose.com/psd)
  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
