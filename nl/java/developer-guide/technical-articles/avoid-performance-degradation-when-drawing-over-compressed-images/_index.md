---
title: Vermijd Prestatieverslechtering bij Tekenen over Gecomprimeerde Afbeeldingen
type: docs
weight: 40
url: /nl/java/vermijd-prestatieverslechtering-bij-tekenen-over-gecomprimeerde-afbeeldingen/
---

## **Vermijd Prestatieverslechtering bij Tekenen over Gecomprimeerde Afbeeldingen**
Er zijn momenten waarop u zeer uitgebreide grafische bewerkingen wilt uitvoeren op een gecomprimeerde afbeelding. Wanneer Aspose.PSD afbeeldingen on-the-fly moet comprimeren en decomprimeren, kan er prestatieverlies optreden. Het tekenen over gecomprimeerde afbeeldingen kan ook een prestatieboete met zich meebrengen.
### **Oplossing**
Om prestatieverlies te voorkomen, raden we aan de afbeelding naar een ongecomprimeerd, of ruw, formaat te converteren voordat grafische bewerkingen worden uitgevoerd.
### **Gebruik van Bestandspad**
In het volgende voorbeeld wordt een PSD-afbeelding geconverteerd naar een ongecomprimeerd formaat (geen compressie) en opgeslagen op schijf. De ongecomprimeerde afbeelding wordt vervolgens geladen voordat er grafische bewerkingen op worden uitgevoerd. Dezelfde techniek is van toepassing op BMP- en GIF-bestanden.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetWijzigenEnConverterenVanAfbeeldingen-PSD-OngecomprimeerdeAfbeeldingGebruikVanBestand-OngecomprimeerdeAfbeeldingGebruikVanBestand.java" >}}
### **Gebruik van een Streamobject**
De volgende codefragment toont hoe een PSD-afbeelding wordt geconverteerd naar een ongecomprimeerd formaat (geen compressie) en wordt opgeslagen op schijf met behulp van een Streamobject.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetWijzigenEnConverterenVanAfbeeldingen-PSD-OngecomprimeerdeAfbeeldingStreamObject-OngecomprimeerdeAfbeeldingStreamObject.java" >}}
