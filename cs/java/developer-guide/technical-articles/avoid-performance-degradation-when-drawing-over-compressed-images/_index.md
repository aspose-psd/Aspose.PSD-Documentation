---
title: Vyhněte se degradaci výkonu při kreslení nad komprimovanými obrázky
type: docs
weight: 40
url: /cs/java/vyhnete-se-degradaci-vykonu-pri-kresleni-nad-komprimovanymi-obrazky/
---

## **Vyhněte se degradaci výkonu při kreslení nad komprimovanými obrázky**
Jsou okamžiky, kdy chcete provádět extrémně rozsáhlé grafické operace na komprimovaném obrázku. Když musí Aspose.PSD komprimovat a dekomprimovat obrázky na letu, může dojít k degradaci výkonu. Kreslení nad komprimovanými obrázky může také nést pokutu za výkon.

### **Řešení**
Abychom zabránili degradaci výkonu, doporučujeme převést obrázek do nepožitého nebo surového formátu před provedením grafických operací.

### **Použití cesty k souboru**
V následujícím příkladu je obrázek PSD převeden do nepožitého formátu (bez komprese) a uložen na disk. Nepožitý obrázek je pak načten zpět před provedením grafických operací na něm. Stejná technika platí pro soubory BMP a GIF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}

### **Použití objektu Stream**
Následující ukázka kódu vám ukazuje, jak je obrázek PSD převeden do nepožitého formátu (bez komprese) a uložen na disk pomocí objektu Stream.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
