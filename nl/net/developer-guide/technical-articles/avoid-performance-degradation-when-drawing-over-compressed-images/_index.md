---
title: Vermijd prestatievermindering bij tekenen over gecomprimeerde afbeeldingen
type: docs
weight: 10
url: /nl/net/vermijd-prestatievermindering-bij-tekenen-over-gecomprimeerde-afbeeldingen/
---

## **Vermijd prestatievermindering bij tekenen over gecomprimeerde afbeeldingen**
Er zijn momenten waarop u zeer uitgebreide grafische bewerkingen wilt uitvoeren op een gecomprimeerde afbeelding. Wanneer Aspose.PSD afbeeldingen op de vlieg moet comprimeren en decomprimeren, kan er prestatievermindering optreden. Het tekenen over gecomprimeerde afbeeldingen kan ook een prestatiestraf met zich meebrengen.
### **Oplossing**
Om prestatievermindering te voorkomen, raden we aan de afbeelding naar een ongecomprimeerd of rauw formaat te converteren voordat u grafische bewerkingen uitvoert.
### **Met behulp van bestandspad**
In het volgende voorbeeld wordt een PSD-afbeelding geconverteerd naar raw formaat (geen compressie) en opgeslagen op schijf. Vervolgens wordt de ongecomprimeerde afbeelding geladen voordat er grafische bewerkingen op worden uitgevoerd. Dezelfde techniek geldt voor BMP- en GIF-bestanden.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **Met behulp van een Stream-object**
De volgende codefragment toont hoe een PSD-afbeelding wordt geconverteerd naar raw formaat (geen compressie) en opgeslagen op schijf met behulp van MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
