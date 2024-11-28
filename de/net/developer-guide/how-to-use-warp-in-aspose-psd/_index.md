---
title: So verwenden Sie Warp in Aspose.PSD
type: docs
weight: 40
url: /de/net/so-verwenden-sie-warp-in-aspose-psd/
---

## **Teil 1 – Rendern einer PSD-Datei mit dem Warp-Effekt**

Photoshop speichert das gerenderte Bild nach Anwendung des Warp-Effekts. Unsere Bibliothek kann das Bild mit dem Warp-Effekt reproduzieren oder neu rendern. Um diese Funktion zu aktivieren, setzen Sie einfach das AllowWarpRepaint-Flag in den Einstellungen, wenn Sie die PSD-Datei öffnen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-Aspose-PSD-Warp-Rendern-1.cs" >}}

Ergebnis:
![Aspose.PSD für .NET Warp Ergebnis 1](warp1.png)

Zusätzlich zur Darstellung des Warp-Effekts für SmartLayers unterstützt unsere Bibliothek auch Warp für TextLayers. Der Implementierungscode bleibt identisch, der einzige Unterschied besteht im Dateinamen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-Aspose-PSD-Warp-Rendern-2.cs" >}}

Ergebnis:
![Aspose.PSD für .NET Warp Ergebnis 2](warp2.png)

**! Hinweis: ** Aktuell unterstützt unsere Bibliothek das Rendern sowohl benutzerdefinierter Warps (bei denen Benutzer die Gitterpunkte manipulieren) als auch alle Standard-Warptypen. 
* - Aktuell unterstützt unsere Bibliothek benutzerdefinierte Warps mit dem Standardgitter, und wir arbeiten aktiv daran, unsere Unterstützung in naher Zukunft auf alle Gittertypen auszudehnen.


## **Teil 2 – Modifizieren des Warp-Effekts**

Unsere Bibliothek ermöglicht es Ihnen nicht nur, den Warp-Effekt zu rendern, sondern auch zu modifizieren (hinzuzufügen).
Diese Modifikationen werden durch die Funktionen der **WarpParams**-Klasse erleichtert.

| **Funktion** | **Beschreibung**                                                                 |
|:-------------|:-------------------------------------------------------------------------------|
| Bounds       | Gibt die Grenzen des verzerrten Bildes zurück.                                |
| MeshPoints   | Ein Array von Punkten, wobei jeder Punkt einen Vertex des Warp-Gitters darstellt. |
| Wert         | Der Wert des Warp-Effekts für nicht benutzerdefinierte Warp-Effekte.               |
| WarpRotates  | Eine Enumeration, die die Richtung der nicht-benutzerdefinierten Warp-Effekte definiert. |
| WarpStyles   | Eine Enumeration, die den Typ des Warp-Effekts definiert.                       |

Das untenstehende Codebeispiel zeigt, wie der Typ des Warp-Effekts für eine Smart Layer bestimmt und der Typ sowie die Intensität der Verzerrung für den Effekt angepasst werden.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-Aspose-PSD-Warp-Rendern-3.cs" >}}

Ergebnis:
![Aspose.PSD für .NET Warp Ergebnis 3](warp3.png)

## **Teil 3 – Hinzufügen des Warp-Effekts**

Das untenstehende Codebeispiel zeigt, wie ein Standard Warp-Effekt zu einer Smart Layer hinzugefügt wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-Aspose-PSD-Warp-Rendern-4.cs" >}}

Ergebnis:
![Aspose.PSD für .NET Warp Ergebnis 4](warp4.png)

Das untenstehende Codebeispiel zeigt, wie ein benutzerdefinierter Warp-Effekt zu einer Smart Layer hinzugefügt wird.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-Aspose-PSD-Warp-Rendern-5.cs" >}}

Ergebnis:
![Aspose.PSD für .NET Warp Ergebnis 5](warp5.png)

Das untenstehende Codebeispiel zeigt, wie ein Warp-Effekt zu einer Text Layer hinzugefügt wird. 
**! Hinweis:** Gemäß den Standards von Photoshop ist der Warp-Effekt für Text Layers in der Regel auf den Standardtyp begrenzt. Unsere Bibliothek unterstützt jedoch die Verwendung von zwei Arten von Warp-Effekten. Bitte beachten Sie, dass solche Dateien möglicherweise nicht vollständig kompatibel mit Photoshop sind.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-Aspose-PSD-Warp-Rendern-5.cs" >}}

Ergebnis:
![Aspose.PSD für .NET Warp Ergebnis 6](warp6.png)

Wir verfeinern und erweitern kontinuierlich die Möglichkeiten unseres Warp-Effekts, um seine Geschwindigkeit, Qualität und unterstützte Funktionalität zu verbessern. Bleiben Sie mit unseren monatlichen Veröffentlichungen über die neuesten Entwicklungen auf dem Laufenden.
Ihr Aspose.PSD-Team
