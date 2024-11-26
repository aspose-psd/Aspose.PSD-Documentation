---
title: Aspose.PSD'de Warp Nasıl Kullanılır
type: docs
weight: 40
url: /tr/net/aspose-psd-de-warp-nasil-kullanilir/
---

## **Bölüm 1 – Warp Efektiyle PSD Dosyası Oluşturma**

Photoshop, Warp efektini uyguladıktan sonra oluşturulan görüntüyü kaydeder. Kütüphanemiz, Warp efektiyle oluşturulan görüntüyü yeniden oluşturabilir veya tekrar oluşturabilir. Bu özelliği etkinleştirmek için PSD dosyasını açarken sadece AllowWarpRepaint bayrağını ayarlayın.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Belge-Aspose-PSD-Warp-Oluşturma-1.cs" >}}

Sonuç:
![Aspose.PSD için .NET Warp Sonucu 1](warp1.png)

Akıllı Katmanlar için Warp efektini oluşturmanın yanı sıra, kütüphanemiz ayrıca Metin Katmanları için de Warp'ı destekler. Uygulama kodu aynı kalırken, tek fark dosya adında bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Belge-Aspose-PSD-Warp-Oluşturma-2.cs" >}}

Sonuç:
![Aspose.PSD için .NET Warp Sonucu 2](warp2.png)

**! Not:** Şu anda kütüphanemiz, hem Özel Warp (kullanıcıların ağ point'leri manipüle ettiği) hem de tüm standart Warp türlerini oluşturmayı desteklemektedir.

_- Şu anda kütüphanemiz, standart ağ ile Özel Warp'ı desteklemektedir ve gelecekte tüm ağ türlerini içerecek şekilde desteğimizi genişletmek için aktif olarak çalışıyoruz._


## **Bölüm 2 – Warp Efektini Değiştirme**

Kütüphanemiz, sadece Warp efektini oluşturmanıza değil, aynı zamanda değiştirmenize (eklemenize) olanak tanır.
Bu değişiklikler, **WarpParams** sınıfının özellikleri aracılığıyla kolaylaştırılır.

| **Özellik**   | **Açıklama**                                                        | 
|:------------- |:-------------------------------------------------------------------|
| Sınırlar      | Warp edilmiş görüntünün sınırlarını döndürür.                       |
| Ağ Noktaları  | Her biri warp ağının bir köşesini temsil eden noktalar dizisi.      |
| Değer         | Özel olmayan warp efektinin warp efekti değeri.                     |
| Warp Döndürmeleri | Özel olmayan warp efektlerinin yönünü tanımlayan bir numaralandırma. |
| Warp Stilleri | Warp efektinin türünü tanımlayan bir numaralandırma.              |

Aşağıdaki kod örneği, Akıllı Katman için Warp efektinin türünü belirleme ve efekt için türü ve bozulmanın şiddetini ayarlama şeklini göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Belge-Aspose-PSD-Warp-Oluşturma-3.cs" >}}

Sonuç:
![Aspose.PSD için .NET Warp Sonucu 3](warp3.png)

## **Bölüm 3 – Warp Efekti Ekleme**

Aşağıdaki kod örneği, bir Akıllı Katmana standart bir Warp efekti eklemenin nasıl yapıldığını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Belge-Aspose-PSD-Warp-Oluşturma-4.cs" >}}

Sonuç:
![Aspose.PSD için .NET Warp Sonucu 4](warp4.png)

Aşağıdaki kod örneği, bir Akıllı Katmana Özel Warp efekti eklemenin nasıl yapıldığını göstermektedir.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Belge-Aspose-PSD-Warp-Oluşturma-5.cs" >}}

Sonuç:
![Aspose.PSD için .NET Warp Sonucu 5](warp5.png)

Aşağıdaki kod örneği, Metin Katmanına bir Warp efekti eklemenin nasıl yapıldığını göstermektedir. 
**! Not:** Photoshop standartlarına göre, Metin Katmanları için Warp efekti genellikle standart türle sınırlıdır. Bununla birlikte, kütüphanemiz iki tür Warp efektinin kullanımını destekler. Lütfen bu tür dosyaların Photoshop ile tam uyumlu olmayabileceğini unutmayın.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Belge-Aspose-PSD-Warp-Oluşturma-6.cs" >}}

Sonuç:
![Aspose.PSD için .NET Warp Sonucu 6](warp6.png)

Warp efektimizin kapasitelerini, hızını, kalitesini ve desteklenen işlevselliğini sürekli olarak geliştiriyor ve genişletiyoruz. En son gelişmeler için aylık sürümlerimizi takip edin.
Aspose.PSD Ekibiniz
