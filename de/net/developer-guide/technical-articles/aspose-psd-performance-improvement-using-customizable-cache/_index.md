---
title: Verbesserung der Leistung von Aspose.PSD mit anpassbarem Cache
type: docs
weight: 20
url: /de/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Verbessert die Leistung mit anpassbarem Cache**
[Aspose.PSD](https://products.aspose.com/psd/family) verwendet Caching für die temporäre Datenspeicherung. Der Mechanismus ist einfach zu verwenden, anpassbar und transparent. Er stellt sicher, dass es während der Bildverarbeitung keine Leistungsprobleme gibt. Dieser Artikel erläutert, wie man den Cache mit der Aspose.PSD-API für .NET anpassen kann.
### **Anpassen des Caches**
Wenn ein Prozess temporären Datenspeicher benötigt, wird dieser im Cache zugewiesen. Der Cache kann im Speicher oder auf der Festplatte sein und wird vom Benutzer festgelegt. Wenn die temporären Daten nicht mehr benötigt werden, wird der Speicher freigegeben. Die Statistiken des zugewiesenen Speichers können jederzeit inspiziert werden. Wie Aspose.PSD Caches zuteilt und verwendet, kann angepasst werden. Dieser Abschnitt beschreibt die verschiedenen Einstellungen und deren Standards, und die unten stehenden Code-Schnipsel zeigen, wie sie verwendet werden können.
### **Festlegen des Speicherorts für den Cache**
Um festzulegen, wie Cache-Speicher zugeordnet wird, setzen Sie die Eigenschaft [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Standardmäßig wird der Cache im Speicher zugewiesen und wenn im Speicher kein Platz mehr verfügbar ist, wird er auf die Festplatte ausgelagert. Dieses Verhalten wird vom Auto-Modus erfasst. Der Auto-Modus ist flexibel und maximiert die Leistung. Es gibt auch andere Modi:

- Nur-CacheAufFestplatte-Modus: Zuteilung ausschließlich auf die Festplatte.
- Nur-CacheImSpeicher-Modus: Zuteilung ausschließlich im Speicher.

Die Auswahl des CacheAufFestplatte-Modus kann zu schlechter Leistung führen.
### **Festlegen der Größe des Caches**
Legen Sie den maximalen Speicherplatz (in Bytes) fest, der auf der Festplatte oder im Speicher zugeordnet werden kann, indem Sie die Eigenschaften [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) und [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) entsprechend setzen. Standardmäßig sind beide Werte auf 0 gesetzt, was bedeutet, dass es keine obere Grenze gibt.
### **Steuerung der Cache-Neuzuordnung**
Wenn im Speicher nicht genügend Platz verfügbar ist (wie durch die Eigenschaft MaxMemoryForCache angegeben), wenn ein neuer Cache zugewiesen wird, wird der Cache auf die Festplatte ausgelagert. Wenn auf der Festplatte nicht genügend Platz vorhanden ist, wird eine Ausnahme ausgelöst. Der Cache-Zuordnungsprozess wird vom Speicher auf die Festplatte verschoben, aber nicht umgekehrt. Die Eigenschaft [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) wird verwendet, um die Speicherneuzuordnung zu steuern. Eine Neuzuordnung tritt höchstwahrscheinlich für vorab zugewiesene Caches auf. Sie kann stattfinden, wenn das System feststellt, dass der zugewiesene Speicherplatz nicht ausreicht. Wenn ExactReallocateOnly auf den Standardwert False gesetzt ist, wird der Speicherplatz auf dasselbe Medium umgeschrieben. Wenn er auf True gesetzt ist, darf die Neuzuordnung den maximal angegebenen Speicherplatz nicht überschreiten. In diesem Fall wird der vorhandene im-Speicher zugewiesene Cache (der eine Neuzuordnung erfordert) freigegeben und zusätzlicher Speicherplatz wird auf der Festplatte zugewiesen.
### **Programmbeispiele**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenVonBildern-PSD-SteuerungCacheNeuzuordnung-SteuerungCacheNeuzuordnung.cs" >}}
