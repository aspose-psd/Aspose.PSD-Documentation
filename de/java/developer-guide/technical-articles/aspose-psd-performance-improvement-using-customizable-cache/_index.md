---
title: Verbesserung der Leistung von Aspose.PSD durch anpassbaren Cache
type: docs
weight: 30
url: /de/java/aspose-psd-leistungssteigerung-durch-anpassbaren-cache/
---

## **Verbessert die Leistung mit anpassbarem Cache**
Aspose.PSD verwendet Caching für die temporäre Datenspeicherung. Der Mechanismus ist einfach zu bedienen, anpassbar und transparent. Dadurch werden Leistungsprobleme bei der Bildverarbeitung vermieden. Dieser Artikel erläutert, wie der Cache mit der Aspose.PSD-API für Java angepasst werden kann.
### **Anpassen des Cache**
Wenn ein Prozess temporären Datenspeicher benötigt, wird dieser im Cache allokiert. Der Cache kann im Arbeitsspeicher oder auf der Festplatte gespeichert werden und wird vom Benutzer festgelegt. Wenn die temporären Daten nicht mehr benötigt werden, wird der Speicher freigegeben. Die Statistiken des allokierten Speicherplatzes können jederzeit überprüft werden. Wie Aspose.PSD Caches allokiert und verwendet, kann angepasst werden. Dieser Abschnitt beschreibt die verschiedenen Einstellungen und deren Standardwerte, und die unten stehenden Codeausschnitte zeigen, wie sie verwendet werden können.
### **Festlegen des Speicherorts des Caches**
Um festzulegen, wie der Cache-Speicherplatz allokiert wird, setzen Sie die Eigenschaft CacheType. Standardmäßig wird der Cache im Arbeitsspeicher allokiert und wenn im Arbeitsspeicher kein Platz mehr verfügbar ist, wird er auf der Festplatte allokiert. Dieses Verhalten wird durch den automatischen Modus erfasst. Der automatische Modus ist flexibel und maximiert die Leistung. Es gibt auch andere Modi:

- CacheOnDiskOnly-Modus: alleinige Allokation auf der Festplatte.
- CacheInMemoryOnly-Modus: alleinige Allokation im Arbeitsspeicher.

Die Auswahl des CacheOnDiskOnly-Modus kann zu einer schlechten Leistung führen.
### **Festlegen der Cache-Größe**
Legen Sie den maximalen Speicherplatz (in Byte) fest, der auf der Festplatte oder im Arbeitsspeicher allokiert werden kann, indem Sie die Eigenschaften MaxDiskSpaceForCache und MaxMemoryForCache entsprechend setzen. Standardmäßig sind beide Werte auf 0 gesetzt, was bedeutet, dass kein Höchstwert festgelegt ist.
### **Kontrolle der Cache-Neuallokation**
Wenn im Arbeitsspeicher nicht genügend Speicherplatz verfügbar ist (wie durch die Eigenschaft MaxMemoryForCache festgelegt), wenn ein neuer Cache allokiert wird, wird der Cache auf der Festplatte allokiert. Wenn auf der Festplatte nicht genügend Platz vorhanden ist, wird eine Ausnahme ausgelöst. Der Cache-Allokationsprozess bewegt sich vom Arbeitsspeicher zur Festplatte, aber nicht umgekehrt. Die Eigenschaft ExactReallocateOnly wird verwendet, um die Neuallokation des Speichers zu steuern. Die Neuallokation tritt höchstwahrscheinlich bei vorab allokierten Caches auf. Sie kann auftreten, wenn das System feststellt, dass der allokierte Speicherplatz nicht ausreicht. Wenn ExactReallocateOnly auf den Standardwert False gesetzt ist, wird der Speicherplatz auf demselben Medium neu allokiert. Wenn er auf True gesetzt ist, darf die Neuallokation den maximal angegebenen Platz nicht überschreiten. In diesem Fall wird der bereits im Arbeitsspeicher allokierte Cache (der eine Neuallokation erfordert) freigegeben und zusätzlicher Speicherplatz wird auf der Festplatte allokiert.
### **Beispielscodes**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiel-src-main-java-com-aspose-psd-Beispiele-BilderÄndernUndKonvertieren-PSD-SteuerungCacheNeuallokation-SteuerungCacheNeuallokation.java" >}}
