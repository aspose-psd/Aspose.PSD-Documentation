---
title: Prestatieverbetering van Aspose.PSD met aanpasbare Cache
type: docs
weight: 20
url: /nl/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Verbeter de prestaties met aanpasbare Cache**
[Aspose.PSD](https://products.aspose.com/psd/family) maakt gebruik van caching voor tijdelijke gegevensopslag. Het mechanisme is eenvoudig te gebruiken, aanpasbaar en transparant. Hiermee worden prestatieproblemen tijdens de verwerking van afbeeldingen voorkomen. Dit artikel legt uit hoe de cache aangepast kan worden met behulp van de Aspose.PSD API voor .NET.
### **Aanpassen van de Cache**
Wanneer een proces tijdelijke gegevensopslag nodig heeft, wordt deze opslag toegewezen in de cache. De cache kan zich in het geheugen of op de schijf bevinden en kan door de gebruiker worden ingesteld. Wanneer de tijdelijke gegevens niet langer nodig zijn, wordt de ruimte vrijgegeven. Op elk moment kan de statistiek van de toegewezen ruimte worden geïnspecteerd. Hoe Aspose.PSD caches toewijst en gebruikt kan worden aangepast. Dit gedeelte beschrijft de verschillende instellingen en hun standaardwaarden, en de onderstaande codefragmenten tonen hoe ze kunnen worden gebruikt.
### **Instellen waar de Cache wordt toegewezen**
Om aan te passen hoe de cache-ruimte wordt toegewezen, stelt u de eigenschap [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype) in. Standaard wordt de cache toegewezen in het geheugen en wanneer er geen ruimte meer beschikbaar is in het geheugen, wordt deze toegewezen op de schijf. Dit gedrag wordt vastgelegd door de modus Auto. De Auto modus is flexibel en maximaliseert de prestaties. Er zijn ook andere modi:

- Modus CacheOnDiskOnly: toewijzing alleen op schijf.
- Modus CacheInMemoryOnly: toewijzing alleen in het geheugen.

Het selecteren van de modus CacheOnDiskOnly kan leiden tot slechte prestaties.
### **Instellen van de grootte van de Cache**
Stel de maximale ruimte (in bytes) in die kan worden toegewezen op de schijf of in het geheugen door respectievelijk de eigenschappen [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) en [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) in te stellen. Standaard zijn beide waarden ingesteld op 0, wat betekent dat er geen bovengrens is.
### **Beheersen van Cache Herallocatie**
Als er niet voldoende ruimte beschikbaar is in het geheugen (zoals gespecificeerd door de eigenschap MaxMemoryForCache) wanneer er een nieuwe cache wordt toegewezen, wordt de cache toegewezen op de schijf. Als er niet genoeg ruimte is op de schijf, wordt er een uitzondering gegenereerd. Het cache-toewijzingsproces verplaatst zich van het geheugen naar de schijf, maar niet andersom. De eigenschap [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) wordt gebruikt om de herallocatie van het geheugen te regelen. Herallocatie is het meest waarschijnlijk voor vooraf toegewezen caches. Het kan gebeuren wanneer het systeem constateert dat de toegewezen ruimte niet voldoende zal zijn. Als ExactReallocateOnly is ingesteld op de standaardwaarde, False, wordt de ruimte opnieuw toegewezen aan hetzelfde medium. Wanneer ingesteld op True, kan de herallocatie het maximumaantal gespecificeerde ruimte niet overschrijden. In dit geval wordt de bestaande in het geheugen toegewezen cache (die herallocatie vereist) vrijgegeven en wordt er extra ruimte toegewezen op de schijf.
### **Programmavoorbeelden**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-HetWijzigenEnConverterenVanAfbeeldingen-PSD-BeheersenCacheHerallocatie-BeheersenCacheHerallocatie.cs" >}}
