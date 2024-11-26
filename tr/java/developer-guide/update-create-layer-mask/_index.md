---
title: Java ile Aspose.PSD'de maskelerle çalışma
weight: 100
type: docs
description: PSD Dosyası içinde Kırpma, Raster ve Vektör Maskeleriyle çalışmanın örnekleri
keywords: [maskeler, katman maskesi, vektör maske, kırpma maskesi, psd, psd api, java, kod örneği]
url: tr/java/update-create-layer-mask/
---

## **Genel Bakış**

**Genel Bakış**
	
	PSD dosyalarında 3 tür maske bulunmaktadır:
	1. Kırpma Maskeleri
	2. Raster Maskeleri
	3. Vektör Maskeleri
	
	Bu makale tüm 3 türü kapsamaktadır.


** Kırpma Maskeleri **

Kırpma maskeleri, grafik tasarım ve görüntü düzenleme yazılımlarında güçlü bir özelliktir, özellikle Java'da. Diğer bir katmanın şekline ve içeriğine dayanarak bir katmanın görünürlüğü üzerinde hassas kontrol sağlar. Temelde, bir kırpma maskesi, bir katmanın görünürlüğünü, altında bulunan başka bir katmanın şekline göre sınırlar.

Java'da bir kırpma maskesini uygulamak için öncelikle iki katmana ihtiyacınız olacaktır: taban katmanı ve kırpmayı niyet ettiğiniz katman. Taban katmanı, görünür kalan şekli veya alanı tanımlar, kırpmak için niyet ettiğiniz katman ise taban katmanın şekline uyan içeriği içerir.

Java'da bir kırpma maskesi uygulandığında, kırılan katmanın içeriği yalnızca taban katmanın sınırları içinde görünür olur. Bu sınırların dışındaki içerikler gizlenecek veya kırpılacaktır.

Kırpma maskeleri, özellikle bir resmin veya sanat eserinin belirli alanlarına dokular veya desenler gibi etkiler uygulanırken son derece değerlidir. Bir kırpma maskesi kullanarak, etkiyi resmin geri kalanını etkilemeden istenilen alanla sınırlayabilirsiniz.

Açıklamalar için lütfen sayfanın sonundaki örneğe bakınız.

** Raster Maskeleri **

Java dosyalarındaki raster maskeler, bir katmanda belirli alanların görünürlüğünü yönetmek için kullanılır. Vektör maskelerinin aksine, maskelenmiş alanları tanımlamak için matematiksel şekilleri kullanan vektör maskelerinin aksine, raster maskeler piksel tabanlı bilgileri kullanarak görünür veya gizli bölgeleri belirler.

Bir raster maskesi, bir katmana uygulanan bir tonlama görüntüsünden oluşmaktadır. Maskenin beyaz alanları görünürlüğü ifade ederken, siyah alanlar gizli kısımları temsil eder. Gri tonlar arasında, kısmi şeffaflık veya yarı görünür bölgeler oluşturulabilir.

Daha iyi anlayış için lütfen sayfanın sonundaki örneğe bakınız.

** Vektör Maskeleri **

Java dosyalarındaki vektör maskeleri, matematiksel şekillere dayanarak bir katmanda belirli alanların görünürlüğünü çizmek için kullanılan çok yönlü araçlardır. Vektörel maskeler, piksel tabanlı verilere dayalı raster maskelerin aksine, yolları ve eğrileri kullanarak pürüzsüz ve ölçeklenebilir maskelenmiş alanlar oluşturmak için kullanır.

Bir vektör maskesi esasen bir katmana uygulanan bir yolun bir parçasıdır. Bu yolun şekli, katmanın hangi bölümlerinin görünür, hangilerinin gizli olduğunu belirler. Yolun kontrol noktalarını ve eğrilerini manipüle ederek, hassas ve karmaşık maskelenmiş alanlar oluşturabilirsiniz.

Vektör maskeler ekleyerek bilgi için lütfen [Vektör Maskeleri sayfasına](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) bakınız.

## **Örnek**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Belgeleme-Java-Aspose-psd-update-create-layer-mask.java" >}}
