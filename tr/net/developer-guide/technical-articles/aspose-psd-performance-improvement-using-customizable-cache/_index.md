---
title: Aspose.PSD Performansını Özelleştirilebilir Önbellek Kullanarak İyileştirme
type: docs
weight: 20
url: /tr/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Özelleştirilebilir Önbellek Kullanarak Performansı İyileştirir**
[Aspose.PSD](https://products.aspose.com/psd/family), geçici veri depolama için önbellek kullanır. Mekanizma kullanımı kolay, özelleştirilebilir ve şeffaftır. Bu, görüntü işleme sırasında performans sorunu olmadığından emin olur. Bu makale, .NET için Aspose.PSD API ile önbelleği nasıl özelleştireceğinizi açıklar.

### **Önbelleği Özelleştirme**
Bir işlem geçici veri depolamaya ihtiyaç duyduğunda, bu depolama önbellekte ayrılır. Önbellek, kullanıcı tarafından ayarlanabilen bellekte veya diskte yer olabilir. Geçici veri artık gerekli olmadığında, alan serbest bırakılır. Tahsis edilen alanın istatistikleri her zaman incelenebilir. Aspose.PSD'nin nasıl önbellek ayırdığını ve kullandığını özelleştirmek mümkündür. Bu bölüm, çeşitli ayarları ve varsayılanlarını açıklar ve aşağıdaki kod parçaları bunların nasıl kullanılabileceğini gösterir.

### **Önbelleğin Ayrıldığı Yeri Ayarlama**
Önbellek alanının nasıl ayrılacağını özelleştirmek için [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype) özelliğini ​​ayarlayın. Varsayılan olarak, önbellek bellekte ayrılır ve bellekte daha fazla alan mevcut olmadığında diskte ayrılır. Bu davranış, Otomatik mod tarafından yakalanır. Otomatik mod esnektir ve performansı maksimize eder. Ayrıca diğer modlar da vardır:

- Yalnızca Diskte Önbellek Modu: Yalnızca diske ayrılma.
- Yalnızca Bellekte Önbellek Modu: Yalnızca belleğe ayrılma.

Yalnızca Diskte Önbellek Modu seçmek, zayıf performansa neden olabilir.

### **Önbellek Boyutunun Ayarlanması**
Diskte veya bellekte ayrılabilecek maksimum alanı (byte cinsinden) [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) ve [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) özelliklerini sırasıyla ayarlayarak belirleyin. Varsayılan olarak, her iki değer de 0 olarak ayarlanmıştır, bu da bir üst sınır olmadığı anlamına gelir.

### **Önbellek Yeniden Dağıtımını Kontrol Etme**
Yeni bir önbelleğe yer ayrılacağında bellekte yeterli yer yoksa (MaxMemoryForCache özelliği belirtildiği gibi) önbellek diske ayrılır. Diskte yeterli alan yoksa, bir istisna oluşturulur. Önbellek tahsis süreci, bellekten diske ancak tam tersi şekilde taşınır. [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) özelliği hafızayı yeniden tahsis etmeyi kontrol etmek için kullanılır. Yeniden tahsis, önceden tahsis edilmiş önbellekler için muhtemelen gerçekleşir. Tahsis edilen alanın yetersiz olacağını sistem fark ederse gerçekleşebilir. ExactReallocateOnly varsayılan değeri False olarak ayarlandığında, alan aynı ortama yeniden tahsis edilir. True olarak ayarlandığında, yeniden tahsis, belirtilen maksimum alanı aşamaz. Bu durumda, mevcut bellekte tahsis edilen önbellek (yeniden tahsis gerektiren) serbest bırakılır ve genişletilmiş alan diskte ayrılır.

### **Program Örnekleri**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}
