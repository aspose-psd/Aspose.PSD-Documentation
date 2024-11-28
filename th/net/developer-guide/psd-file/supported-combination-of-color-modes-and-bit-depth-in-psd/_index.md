---
title: การรองรับการผสมสีและความลึกข้อมูลใน PSD
type: docs
weight: 80
url: /th/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **คำอธิบาย**
Aspose.PSD รองรับการเปิดไฟล์ PSD ด้วยการผสมสีและความลึกข้อมูลใน Adobe Photoshop PSD Files ทุกประเภท คุณสามารถเปิดไฟล์เหล่านี้และใช้ Low-Level API เพื่อปรับปรุงเนื้อหาของไฟล์ แต่สำหรับบางการผสมของการได้รับความนิยมน้อยมีปัญหาเฉพาะบางประการ บางอย่างเกี่ยวข้องกับข้อจำกัดของโหมดสี

## **การสนับสนุนการส่งออกการผสมสีและความลึกข้อมูลใน PSD ในโหมดอ่านอย่างเดียว**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Multichannel|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|ความลึก 1|ใช่[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|ความลึก 8|-|ใช่|ใช่|ใช่|ใช่|ไม่ ค3-ค4|ไม่ ค3-ค4|ใช่[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|ความลึก 16|-|ใช่|-|ใช่|ใช่|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|ไม่ (ค3-ค4)|
|ความลึก 32|-|ใช่*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|ใช่*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* ปัญหาเล็กน้อยในบางกรณี

## **การสนับสนุนการส่งออกการผสมสีและความลึกข้อมูลใน PSD ในโหมดแก้ไขได้**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Multichannel|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|ความลึก 1|ใช่|-|-|-|-|-|-|-|
|ความลึก 8|-|ใช่|ไม่|ใช่|ใช่|ไม่ ค3-ค4|ไม่ ค3-ค4|ใช่*|
|ความลึก 16|-|ใช่|-|ใช่|ใช่*|-|-|ไม่ (ค3-ค4)|
|ความลึก 32|-|ไม่ (ค3-ค4)|-|ไม่ (ค3-ค4)|-|-|-|-|
\* ปัญหาเล็กน้อยในบางกรณี

หากคุณต้องการรับการสนับสนุนของการผสมสี / ความลึกข้อมูลใด ๆ คุณสามารถโพสต์ใน [Aspose Forums](https://forum.aspose.com/c/psd)
