---
title: Aspose.PSD Prestatieverbetering met Aanpasbare Cache
type: docs
weight: 30
url: /nl/java/aspose-psd-prestatieverbetering-met-aanpasbare-cache/
---

## **Verbetering van de Prestaties met Aanpasbare Cache**
Aspose.PSD maakt gebruik van caching voor tijdelijke gegevensopslag. Het mechanisme is eenvoudig te gebruiken, aanpasbaar en transparant. Het zorgt ervoor dat er geen prestatieproblemen zijn tijdens de verwerking van afbeeldingen. Dit artikel legt uit hoe de cache aangepast kan worden met behulp van Aspose.PSD API voor Java.
### **Het Aanpassen van de Cache**
Wanneer een proces tijdelijke gegevensopslag nodig heeft, worden deze gegevens toegewezen in de cache. De cache kan geheugenruimte zijn of op schijf staan en wordt ingesteld door de gebruiker. Wanneer de tijdelijke gegevens niet langer nodig zijn, wordt de ruimte vrijgegeven. Op elk moment kan de statistiek van de toegewezen ruimte worden onderzocht. Hoe Aspose.PSD caches toewijst en gebruikt kan worden aangepast. Dit gedeelte beschrijft de verschillende instellingen en hun standaardwaarden, en de onderstaande codefragmenten tonen hoe ze kunnen worden gebruikt.
### **Instellen waar de Cache toegewezen wordt**
Om aan te passen hoe de cache ruimte toegewezen wordt, stel de eigenschap CacheType in. Standaard wordt de cache toegewezen in het geheugen en wanneer er geen ruimte meer beschikbaar is in het geheugen, wordt deze toegewezen aan de schijf. Dit gedrag wordt vastgelegd door de automodus. De automodus is flexibel en maximaliseert de prestaties. Er zijn ook andere modi:

- AlleenCacheOpSchijf modus: toewijzing alleen aan schijf.
- AlleenCacheInGeheugen modus: toewijzing alleen in het geheugen.

Het selecteren van de AlleenCacheOpSchijf modus kan resulteren in slechte prestaties.
### **Instellen van de Grootte van de Cache**
Stel de maximale ruimte (in bytes) in die toegewezen kan worden op schijf of in het geheugen door respectievelijk de eigenschappen MaxDiskSpaceForCache en MaxMemoryForCache in te stellen. Standaard zijn beide waarden ingesteld op 0, wat betekent dat er geen bovengrens is.
### **Controle over Cache Herallocatie**
Als er niet genoeg ruimte beschikbaar is in het geheugen (zoals gespecificeerd door de MaxMemoryForCache eigenschap) wanneer er een nieuwe cache toegewezen wordt, wordt de cache toegewezen aan de schijf. Als er niet genoeg ruimte op de schijf is, wordt een uitzondering gegenereerd. Het cache-toewijzingsproces verplaatst zich van geheugen naar schijf maar niet andersom. De ExactReallocateOnly eigenschap wordt gebruikt om de herallocatie van geheugen te controleren. Herallocatie is het meest waarschijnlijk voor vooraf toegewezen caches. Het kan gebeuren wanneer het systeem erachter komt dat de toegewezen ruimte niet voldoende zal zijn. Als ExactReallocateOnly is ingesteld op de standaardwaarde, False, wordt de ruimte opnieuw toegewezen aan hetzelfde medium. Wanneer het is ingesteld op True, kan de herallocatie de maximale gespecificeerde ruimte niet overschrijden. In dit geval wordt de bestaande toegewezen in-memory-cache (die herallocatie vereist) vrijgegeven en wordt er extra ruimte toegewezen op schijf.
### **Voorbeelden van Programma's**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}
