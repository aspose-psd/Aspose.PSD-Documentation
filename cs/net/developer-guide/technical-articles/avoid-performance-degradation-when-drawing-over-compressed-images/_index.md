---
title: Vyhněte se degradaci výkonu při kreslení nad komprimovanými obrázky
type: docs
weight: 10
url: /cs/net/vyhnete-se-degradaci-vykonu-pri-kresleni-nad-komprimovanymi-obrazky/
---

## **Vyhněte se degradaci výkonu při kreslení nad komprimovanými obrázky**
Existují časy, kdy chcete provádět extrémně rozsáhlé grafické operace na komprimovaném obrázku. Když musí Aspose.PSD komprimovat a dekomprimovat obrázky na počkání, může dojít k degradaci výkonu. Kreslení nad komprimovanými obrázky může také nést trestní výkon.
### **Řešení**
Pro předejití degradaci výkonu doporučujeme, abyste před provedením grafických operací převedli obrázek do nekomprimovaného nebo surového formátu.
### **Použití cesty k souboru**
V následujícím příkladu je obrázek PSD převeden do surového formátu (bez komprese) a uložen na disk. Nekomprimovaný obrázek je poté znovu načten před provedením grafických operací na něm. Stejná technika platí pro soubory BMP a GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **Použití objektu proudění**
Následující výňatek kódu vám ukazuje, jak je obrázek PSD převeden do surového formátu (bez komprese) a uložen na disk pomocí MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
