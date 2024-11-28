---
title: Aspose.PSD Performansı, Özelleştirilebilir Önbellek Kullanarak İyileştirme
type: docs
weight: 30
url: /tr/java/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Özelleştirilebilir Önbellek ile Performansı İyileştirme**
Aspose.PSD geçici veri depolama için önbellek kullanır. Mekanizma kullanımı basit, özelleştirilebilir ve şeffaftır. Görüntü işleme sırasında performans sorunlarının olmamasını sağlar. Bu makale, Aspose.PSD API'si ile önbelleği nasıl özelleştireceğinizi açıklar.
### **Önbelleği Özelleştirme**
Bir işlem geçici veri depolama gerektiğinde, bu depolama önbellekte ayrılır. Önbellek, kullanıcı tarafından ayarlanabilen bellek veya disk alanı olabilir. Geçici verilere artık ihtiyaç duyulmadığında, alan serbest bırakılır. Ayrılan alanın istatistikleri her zaman incelenebilir. Aspose.PSD'nin nasıl önbellek ayradığı ve kullandığı özelleştirilebilir. Bu bölüm farklı ayarları ve varsayılanları açıklar ve aşağıdaki kod parçaları bunların nasıl kullanılabileceğini gösterir.
### **Önbelleğin Ayrıldığı Yerin Ayarlanması**
Önbellek alanının nasıl ayrıldığını özelleştirmek için CacheType özelliğini ayarlayın. Varsayılan olarak, önbellek bellekte ayrılır ve bellekte daha fazla alan kalmadığında diske ayrılır. Bu davranış Otomatik mod ile gerçekleştirilir. Otomatik mod esnektir ve performansı maksimize eder. Ayrıca diğer modlar da vardır:

- Yalnızca Diskte Önbelleğe Al modu: sadece diske ayrılanalan.
- Yalnızca Bellekte Önbelleğe Al modu: sadece belleğe ayrılan alan.

Yalnızca Diskte Önbelleğe Al modunu seçmek performansta kötü sonuçlanabilir.
### **Önbelleğin Boyutunun Ayarlanması**
Önbellek tarafından ayrılabilecek maksimum alanı (bayt cinsinden) belirleyerek disk veya bellekte MaxDiskSpaceForCache ve MaxMemoryForCache özellikleri ayarlanır. Varsayılan olarak, her iki değer de 0 olarak ayarlanmıştır, yani üst sınır yoktur.
### **Önbellek Yeniden Ayrılmasının Kontrol Edilmesi**
Yeni bir önbellek ayrıldığında bellekte yeterli alan yoksa (MaxMemoryForCache özelliği tarafından belirtildiği gibi) önbellek diske ayrılır. Eğer diskte yeterli alan yoksa, bir istisna fırlatılır. Önbelleğin ayrılma süreci bellekten diske doğru ilerler ama aksi yönde değil. Önbellek yeniden ayrılmasını kontrol etmek için ExactReallocateOnly özelliği kullanılır. Yeniden ayrılma genellikle önceden ayrılmış önbellekler için gerçekleşebilir. Bu, ayrılmış alanın yetersiz olacağını sistem belirlediğinde olabilir. ExactReallocateOnly varsayılan değeri olan False olarak ayarlandığında, alan aynı ortama yeniden ayrılır. True olarak ayarlandığında, yeniden ayrılma belirtilen maksimum alana ulaşamaz. Bu durumda bellekteki mevcut ayrılmış önbellek (yeniden ayrılması gereken) serbest bırakılır ve genişletilmiş alan diske ayrılır.
### **Program Örnekleri**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-kaynak-main-java-com-aspose-psd-örnekleri-Düzenleme ve DönüştürmeGörüntüleri-PSD-ÖnbellekYenidenAyarlama-KontrolÖnbellekYenidenAyrılması.java" >}}
