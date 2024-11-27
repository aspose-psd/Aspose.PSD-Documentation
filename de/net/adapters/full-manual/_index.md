---
title: Aspose.PSD Adapter für .NET Vollhandbuch
type: docs
weight: 10
url: /de/net/adapters/voll-handbuch
keywords: Adapter Voll Handbuch PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP Schnellstartanleitung
description: Aspose.PSD Adapter Vollhandbuch.
---

## Überblick

Dies ist ein vollständiges Handbuch zur Arbeit mit Aspose.PSD-Adaptern zur Erweiterung der Aspose.PSD-Fähigkeiten. Adapter sind spezielle Nuget-Pakete, die eine nahtlose Integration von Aspose.PSD mit anderen Aspose-Produkten ermöglichen, sodass Sie Ihre Dateien mühelos in verschiedene nicht unterstützte Formate exportieren können, ohne zusätzlichen Integrationscode schreiben zu müssen.

## Anwendung von Lizenzen

Bitte überprüfen Sie den vollständigen [Artikel zur Anwendung von Lizenzen](/psd/de/net/adapters/lizenz) für Adapter.

{{% alert color="primary" %}}
Bitte beachten Sie, dass zur Verwendung von Adaptern sowohl eine Aspose.PSD- als auch eine Adaptee-Lizenz erforderlich sind.
{{% /alert %}}

Die Lizenz kann mithilfe dieses Beispiels angewendet werden:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapter-CSharp-Lizenz.cs" >}}

Es ist besser, die Lizenz einmal im Initialisierungsmodul Ihres Projekts anzuwenden.

## Verweis auf Aspose.PSD-Adapter

Zunächst müssen Sie Aspose.PSD.Adapters.Imaging von [Nuget](https://www.nuget.org/aspose.psd.adapters.imaging) referenzieren oder sie von [Aspose Release Page](https://releases.aspose.com/psd/net/) herunterladen (Adapter sind im Hauptrelease-Artefakt in diesem Moment als separate Binärdatei enthalten) in Ihr Projekt.

![Notwendige Verweise](references.png)

Möglicherweise müssen Sie auch auf weitere zusätzliche Pakete verweisen

## Aktivieren von Ladern und Exporteuren der Adaptees

### Aktivierung von Adaptern
Wenn Sie Adapter verwenden möchten, verwenden Sie einfach den folgenden Code:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapter-CSharp-Adapter-aktivieren.cs" >}}


### Deaktivierung von Adaptern
Im Entwicklungsprozess kann es vorkommen, dass Adapter deaktiviert werden müssen. Dies ist der Fall, wenn Sie in einem Codeabschnitt Aspose.PSD-Lader verwenden und in einem anderen Adaptees'-Lader verwenden möchten. Verwenden Sie in diesem Fall einfach den folgenden Code:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapter-CSharp-Adapter-deaktivieren.cs" >}}

## Laden von Bildern mithilfe von Adaptern

Mit Adaptern können Sie [beliebte von Aspose.PSD nicht unterstützte Formate laden]((/net/adapters/nicht-unterstützte-formate-laden)) wie SVG oder WebP.

### Einfache Verwendung
Verwenden Sie einfach den folgenden Code zum Laden:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapter-CSharp-Imaging-Adapter-hinzufügen-Laden-nicht-unterstützter-Formate.cs" >}}

### Zwischennutzung für die komplexe Bildverarbeitung
Wenn Sie zusätzliche Optionen angeben müssen, die vom Adaptee bereitgestellt werden, überprüfen Sie bitte das folgende Beispiel:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapter-CSharp-Vollhandbuch-Komplexes-Laden.cs" >}}

Sie können mit einem Methodenaufruf mit allen Imaging-Funktionen mit einem SVG-Bild arbeiten und es dann exportieren.

## Exportieren von Bildern mit Adaptern

Es gibt viele Situationen, in denen Sie [nicht unterstützte Formate öffnen müssen](/net/adapters/nicht-unterstützte-formate-laden), sondern [dorthin exportieren müssen](/net/adapters/exportieren-in-nicht-unterstützte-formate). In diesen Fällen sollten Sie Exporteure aktivieren und den folgenden Code verwenden:
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapter-CSharp-Imaging-Adapter-hinzufügen-Exportieren-in-nicht-unterstützte-Formate.cs" >}}

## Fazit

Die Verwendung von Aspose.PSD-Adaptern zum Laden und Exportieren von Dateien ist ein Game-Changer für Entwickler. Diese leistungsstarken Nuget-Pakete ermöglichen eine nahtlose Integration von Aspose.PSD mit anderen Aspose-Produkten, was es einfacher denn je macht, mit nicht unterstützten Dateiformaten zu öffnen und zu arbeiten, ohne zusätzlichen Integrationscode schreiben zu müssen. Mit Aspose.PSD-Adaptern sparen Sie Zeit und Mühe, indem Sie den Bedarf an zusätzlichem Code und manuellen Konvertierungsprozessen eliminieren. Egal, ob Sie Dateien laden oder exportieren, Aspose.PSD-Adapter bieten eine bequeme und effiziente Lösung, die neue Möglichkeiten für Ihre Projekte eröffnet. Erleben Sie die Kraft der Aspose.PSD-Adapter und bringen Sie Ihren Entwicklungsprozess auf die nächste Stufe.
