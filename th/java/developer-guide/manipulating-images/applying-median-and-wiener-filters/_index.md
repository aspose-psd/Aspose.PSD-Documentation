---
title: การใช้งานตัวกรองมีเดียนและไวเนอร์
type: คู่มือ
weight: 10
url: /th/java/applying-median-and-wiener-filters/
---

## **การใช้งานตัวกรองมีเดียนและไวเนอร์**
ตัวกรองมีเดียนเป็นเทคนิคการกรองดิจิทัลที่ไม่เชิงเส้น และมักถูกใช้เพื่อลดสัญญาณรบกวน เป็นขั้นตอนการประมวลผลก่อนที่จะส่งผลลัพธ์ให้กับการประมวลผลขั้นถัดไป ตัวกรองไวเนอร์เป็นตัวกรองเชิงเส้นแบบแปรผัน MSE (mean squared error) ที่ช่วยลดความเสียหายของภาพที่ถูกทำให้เสียสมด้วยสัญญานก๊ากเพิ่มขึ้นและภาพที่เบลอ เจลใช้ Aspose.PSD สำหรับนักพัฒนา API ของ Java สามารถใช้ตัวกรองมีเดียนเพื่อลดสัญญาณรบกวนในภาพ และสามารถใช้ตัวกรองไวเนอร์กาวที่อยู่บนภาพ บทความนี้สาธิตว่าตัวกรองมีเดียนและตัวกรองไวเนอร์กาวสามารถใช้บนภาพได้อย่างไร
### **การใช้งานตัวกรองมีเดียน**
Aspose.PSD มีคลาส MedianFilterOptions เพื่อใช้ตัวกรองบน RasterImage โค้ดย่อที่ให้ด้านล่างสาธิตวิธีการใช้ตัวกรองมีเดียนกับภาพราสเตอร์


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **การใช้งานตัวกรองไวเนอร์กาว**
Aspose.PSD มีคลาส GaussWienerFilterOptions เพื่อใช้ตัวกรองบน RasterImage โค้ดย่อที่ให้ด้านล่างสาธิตวิธีการใช้ตัวกรองไวเนอร์กาวกับภาพราสเตอร์


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **การใช้งานตัวกรองไวเนอร์กาวสำหรับภาพสี**
Aspose.PSD มี GaussWienerFilterOptions สำหรับภาพสีด้วย โค้ดย่อที่ให้ด้านล่างสาธิตวิธีการใช้ตัวกรองไวเนอร์กาวกับภาพสี


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **การใช้งานตัวกรองไวเนอร์เคลื่อนไหว**
Aspose.PSD มีคลาส MotionWienerFilterOptions เพื่อใช้ตัวกรองบน RasterImage โค้ดย่อที่ให้ด้านล่างสาธิตวิธีการใช้ตัวกรองไวเนอร์เคลื่อนไหวกับภาพราสเตอร์


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **การใช้ตัวกรองการแก้ข้อผิดพลาดบนภาพ**
บทความนี้สาธิตวิธีการใช้ Aspose.PSD สำหรับ Java เพื่อทำตัวกรองการแก้ไขบนภาพ API ของ Aspose.PSD ได้เปิดเผยวิธีการใช้งานที่มีประสิทธิภาพและง่ายต่อการใช้งานเพื่อบรรลุวัตถุประสงค์นี้ Aspose.PSD สำหรับ Java ได้เปิดเผยคลาส BilateralSmoothingFilterOptions และ SharpenFilterOptions สำหรับการกรอง คลาส BilateralSmoothingFilterOptions จำเป็นต้องใช้เป็นจำนวนเต็ม เพื่อการกรองขั้นตอนการปรับขนาดจะง่ายดังด้านล่าง


1. โหลดภาพโดยใช้เมทอดโรงงาน Load ที่เปิดเผยโดยคลาสภาพ.
1. แปลงภาพเป็น RasterImage
1. สร้างอินสแตนส์ของคลาส BilateralSmoothingFilterOptions และ SharpenFilterOptions
1. เรียกเมทอดการกรองราสเตอร์ในขณะระบุสี่เหลี่ยมเป็นขอบภาพและอินสแตนส์คลาส BilateralSmoothingFilterOptions
1. เรียกเมทอดการกรองราสเตอร์ในขณะระบุสี่เหลี่ยมเป็นขอบภาพและอินสแตนส์คลาส SharpenFilterOptions
1. ปรับความคมชัน
1. กำหนดความสว่าง
1. บันทึกผลลัพธ์

โค้ดย่อด้านล่างแสดงวิธีการใช้ตัวกรองการแก้ข้อผิดพลาด


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **ใช้ขั้นพอร์ต Bradley threshold algorithm**
การกำหนดโปรแกรมระดับภาพถูกใช้ในแอพพลิเคชันกราฟิก วัตถุของการกำหนดขอบภาพคือการจำแนกพิกเซลเป็น "เข้ม" หรือ "สว่าง" Aspose.PSD API ช่วยให้คุณสามารถใช้ขั้นพอร์ต Bradley thresholding ขณะทำการแปลงภาพ โค้ดย่อต่อไปนี้จะแสดงให้เห็นวิธีการกำหนดค่าขีดจำกัดแล้วเรียกใช้อัลกอริทึมของ Bradley


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
