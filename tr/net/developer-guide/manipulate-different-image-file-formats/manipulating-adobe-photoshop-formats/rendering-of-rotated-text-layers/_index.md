---
title: Döndürülmüş Metin Katmanlarının Oluşturulması
type: docs
weight: 40
url: /tr/net/rendering-of-rotated-text-layers/
---

## **Döndürülmüş Metin Katmanlarının Oluşturulması**
Aspose.PSD, döndürülmüş Metin katmanlarının oluşturulması özelliğini sağlar. Aşağıdaki örnekte, mevcut bir PSD dosyası, Dosya yolunu Image sınıfının static Yükle yöntemine ileterek yüklenir. Şimdi [PsdImage] (https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage) örneğinin [Kaydet] (https://reference.aspose.com/psd/net/aspose.psd/image/methods/save) yöntemini çağırın.

Aşağıdaki kod parçacığı size nasıl döndürülmüş [Metin katmanını](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer) oluşturacağınızı gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-GoruntuDuzenlemeVeCevirme-PSD-DondurulmusMetinKatmaniOlusturma-DondurulmusMetinKatmani.cs" >}}
## **Vektör Maske ve Metin Katmanlarının Döndürülmesi**
Aspose.PSD, Vektör Maske ve Metin katmanlarının döndürülmesi özelliğini sağlar. Aspose.PSD, Vektör Maske ve Metin katmanlarını döndürmek için RotateFlip yöntemini açığa çıkarmıştır. Katmanları döndürme adımları aşağıdaki gibi basittir:

- Image sınıfı tarafından sağlanan Yükle fabrika yöntemi kullanarak bir PSD dosyasını bir resim olarak yükleyin.
- Gerekli [RotateFlipType](https://reference.aspose.com/psd/net/aspose.psd/rotatefliptype)'ı ayarlayın.
- [RotateFlip](https://reference.aspose.com/psd/net/aspose.psd/image/methods/rotateflip) yöntemini çağırın.
- Sonuçları kaydedin.

Aşağıdaki kod parçacığı size Vektör Maske ve Metin katmanlarını nasıl döndüreceğinizi gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-GoruntuDuzenlemeVeCevirme-PSD-DestekVektoreKatmaninDondurulmesi-DestekVektoreKatmaninDondurulmesi.cs" >}}
