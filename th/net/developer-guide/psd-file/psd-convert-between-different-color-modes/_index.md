---
title: การเปลี่ยนรูปแบบสีของ PSD ระหว่างโหมดสีต่าง ๆ
type: ด็อค
weight: 50
url: /th/net/psd-convert-between-different-color-modes/
---

คุณสามารถเรียนรู้โหมดสีที่รองรับของ Aspose.PSD จากบทความนี้

Aspose.PSD รองรับการแปลงจาก 8 เป็น 16 บิตต่อพิกเซลและกลับด้านกันด้วย การแปลง CMYK ICC-Profile และการแปลงอื่น ๆ จากรูปแบบลักษณะบิตเดพอื่น ๆ ที่นี่คุณสามารถดูตัวอย่างว่าจะแปลงเป็น Grayscale ในไฟล์ PSD
## **แปลงจาก CMYK, RGB, Grayscale เป็นโหมดสี Grayscale**
โค้ดตัวอย่างที่ให้ด้านล่างสาเหตุถึงวิธีทำการแปลง CMYK, RGB, หรือ Grayscale โดยไม่ใช้ Photoshop

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **16-bit รูปภาพโฟโต้ช็อปเป็นโหมด Grayscale 8 บิต**
แต่ถ้าคุณต้องการที่จะแปลงรูปภาพโฟโต้ช็อป Grayscale 16 บิตเป็นโหมด Grayscale 8 บิต คุณต้องใช้โค้ดย่อยต่อไปนี้ 8 บิตเป็นความลึกของบิตที่พบได้ในไฟล์ PSD ได้

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **แปลง Grayscale เป็น RGB**
กรณีที่ซับซ้อนอื่น ๆ คือเมื่อคุณต้องการที่จะแปลง Grayscale รูปภาพ PSD เป็นรูปภาพ RGB

รูปภาพ Grayscale มีแค่ช่องใหญ่ แต่รูปภาพ RGB มี 3 ช่อง: R - สีแดง, G - สีเขียว, B - สีน้ำเงิน Aspose.PSD สามารถทำการแปลง Grayscale เป็น RGB

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
