---
title: Liste der unterstützten globalen Bildressourcen in PSD-Dateien
type: docs
weight: 30
url: /de/net/liste-der-unterstützten-psd-globalen-bildressourcen/
---

## **Aspose.PSD unterstützt die Low-Level-Bearbeitung von Bildressourcen.**
Die Liste der vollständig unterstützten Bildressourcen finden Sie in Aspose.PSD .Net [API-Referenz](https://reference.aspose.com/psd/net).

Gemäß der Adobe® Photoshop®-Format-Spezifikation verwenden Bildressourcen mehrere standardisierte ID-Nummern, wie in den Bilderressourcen IDs gezeigt. Nicht alle Dateiformate verwenden alle IDs. Einige Informationen können in anderen Abschnitten der Datei gespeichert sein.

Für jene Ressourcen-IDs, die seit Photoshop 3.0 hinzugefügt wurden, gibt der Eintrag die Version an, in der sie eingeführt wurden, z.B. (*Photoshop 6.0*).

Bildressourcen-ID.

| **ID** | **Beschreibung** |
| :- | :- |
| **Dezimal** || 
|1000|*(Veraltet - Nur Photoshop 2.0)* Anzahl der Kanäle, Reihen, Spalten, Tiefe und Modus|
|1001|Macintosh-Druckmanager-Druckinformationsdatensatz|
|1002|Macintosh-Seitenformatinformationen. Wird von Photoshop nicht mehr gelesen. *(Veraltet)*|
|1003|*(Veraltet - Nur Photoshop 2.0)* Indizierte Farbtabelle|
|1005|[ResolutionInfo-Struktur](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource)|
|1006|Namen der Alpha-Kanäle in Form von Pascal-Strings|
|1007|*(Veraltet) Siehe ID 1077 DisplayInfo-Struktur*|
|1008|Die Bildunterschrift als Pascal-String|
|1009|[Randinformationen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource). Enthält eine feste Anzahl (2 Bytes echt, 2 Bytes Bruch) für die Randbreite und 2 Bytes für die Randeinheiten (1 = Zoll, 2 = cm, 3 = Punkte, 4 = Picas, 5 = Spalten)|
|1010|[Hintergrundfarbe](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Drucktflags. Eine Serie von ein-Byte-Booleschen Werten: Etiketten, Beschnittmarken, Farbbalken, Anmeldemarken, Negativ, Flip, interpolieren, Unterschrift, Druckfahnen|
|1012|Graustufen- und Mehrkanal-Halbtoninformationen|
|1013|[Farbhalbtöne-Informationen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Duoton-Halbtoninformationen|
|1015|Graustufen- und Mehrkanal-Transferfunktions|
|1016|[Farbübertragungsfunktionen](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|Duoton-Übertragungsfunktionen|
|1018|Duoton-Bildinformationen|
|1019|Zwei Bytes für die effektiven Schwarz- und Weißwerte für den Punktbereich|
|1020|*(Veraltet)*|
|1021|EPS-Optionen|
|1022|[Quick-Masken-Informationen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). Schnellmaskenkanal-ID; 1-Byte-Booleschen, der anzeigt, ob die Maske anfangs leer war|
|1023|*(Veraltet)*|
|1024|[Ebenenstatusinformationen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource)|
|1025|Arbeitsweg (nicht gespeichert). Pfaderessourcenformat|
|1026|[Ebenen-Gruppeninformationen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 Bytes pro Ebene, die eine Gruppen-ID für die ziehenden Gruppen enthalten. Ebenen in einer Gruppe haben dieselbe Gruppen-ID|
|1027|*(Veraltet)*|
|1028|IPTC-NAA-Datensatz. Enthält die *Dateiinformationen...* Informationen|
|1029|Bildmodus für Raw-Formatdateien|
|1030|JPEG-Qualität. Privat|
|1032|*(Photoshop 4.0) [Gitter- und Führungslinieninformationen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0) [](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[Daumenbildressource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[für Photoshop 4.0](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* nur|
|1034|*(Photoshop 4.0)* Copyright-Flagge. Boolean, das anzeigt, ob das Bild urheberrechtlich geschützt ist|
|1035|*(Photoshop 4.0)* URL. Handle eines Textstrings mit einheitlichem Ressourcenlokator*.*|
|1036|*(Photoshop 5.0)[Daumenbildressource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (ersetzt Ressource 1033)|
|1037|*(Photoshop 5.0) [Global Angle](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 Bytes, die eine ganze Zahl zwischen 0 und 359 enthalten, die den globalen Beleuchtungswinkel für Effektlayer darstellen. Wenn nicht vorhanden, wird angenommen, dass er 30 beträgt|
|1038|*(Veraltet) Siehe ID 1073 unten. (Photoshop 5.0)* Farbmessertressource|
|1039|*(Photoshop 5.0) [ICC-Profil](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. Die Rohbytes eines ICC (International Color Consortium) Formatprofils * |
|1040|*(Photoshop 5.0) [Wasserzeichen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*|
|1041|*(Photoshop 5.0) [ICC-ungekennzeichnetes Profil](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 Byte, das jegliche angenommene Profilverarbeitung beim Öffnen der Datei deaktiviert. 1 = absichtlich unmarkiert|
|1042|*(Photoshop 5.0)* Effekte sichtbar. 1-Byte-Globalflagge zum Ein-/Ausblenden aller Effektschichten. Nur vorhanden, wenn sie ausgeblendet sind|
|1043|*(Photoshop 5.0)* Spot-Halbton. 4 Bytes für Version, 4 Bytes für Länge und die variable Längendaten|
|1044|*(Photoshop 5.0)[Dokumentspezifische IDs](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* Seed-Nummer. 4 Bytes: Basenwert, ab dem Ebenen-IDs generiert werden (oder ein höherer Wert, wenn vorhandene IDs diesen bereits überschreiten). Zweck ist es, zu vermeiden, dass wir Ebenen hinzufügen, flattieren, speichern, öffnen und dann weitere Ebenen hinzufügen, die dieselben IDs wie der erste Satz haben|
|1045|*(Photoshop 5.0) [Unicode-Alphanamen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*|
|1046|*(Photoshop 6.0)* Indiziert Farbtabelle zählen. 2 Bytes für die Anzahl der tatsächlich definierten Farben in der Tabelle|
|1047|*(Photoshop 6.0)* [Transparenzindex](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource)|
|1049|*(Photoshop 6.0)* [Global Altitude](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Slices|
|1051|*(Photoshop 6.0)* Workflow-URL|
|1052|*(Photoshop 6.0)* Jump To XPEP. 2 Bytes Hauptversion, 2 Bytes Nebenversion, 4 Bytes Zähler. Folgendes wird für jedes Zählen wiederholt: 4 Bytes Blockgröße, 4 Bytes Schlüssel, wenn der Schlüssel = *'jtDd'* ist, dann folgt ein Boolescher Wert für das Dirty-Flag; andernfalls ist es ein 4-Byte-Eintrag für das Modifikationsdatum|
|1053|*(Photoshop 6.0)* Alpha-Identifikatoren|
|1054|*(Photoshop 6.0)[URL-Liste](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*|
|1057|*(Photoshop 6.0)* [Versionsinfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource)|
|1058|*(Photoshop 7.0)* EXIF-Daten 1|
|1059|*(Photoshop 7.0)* EXIF-Daten 3|
|1060|*(Photoshop 7.0)* [XMP-Metadaten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). Dateiinfo als XML-Textbeschreibung|
|1061|*(Photoshop 7.0)[Bildunterschrifts-Digest](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 Bytes: RSA-Data-Security, MD5-Nachrichten-Digest-Algorithmus|
|1062|*(Photoshop 7.0)[Druckskala](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = zentriert, 1 = an Größe anpassen, 2 = benutzerdefiniert). 4 Bytes x-Position (Fließkommawert). 4 Bytes y-Position (Fließkommawert). 4 Bytes Skalierung (Fließkommawert)|
|1064|*(Photoshop CS)* Pixel-Seitenverhältnis|
|1065|*(Photoshop CS)* Ebenen-Zusammenstellungen|
|1066|*(Photoshop CS)* Alternative Duotonfarben. Diese Ressource wird von Photoshop nicht gelesen oder verwendet|
|1067|*(Photoshop CS)* Alternative Spot-Farben. Diese Ressource wird von Photoshop nicht gelesen oder verwendet|
|1069|*(Photoshop CS2)* [Layer-Auswahl-ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerselectionidsresource)(s). 2 Bytes Zähler, gefolgt von jedem Zählen: 4 Bytes Ebenen-ID|
|1070|*(Photoshop CS2)* HDR-Toninformationen|
|1071|*(Photoshop CS2)* Druckinformationen|
|1072|*(Photoshop CS2)* [Aktivierte Layergruppen-ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 Byte für jede Ebene im Dokument, wiederholt durch die Länge der Ressource. HINWEIS: Layergruppen haben Start- und Endmarkierungen|
|1073|*(Photoshop CS3)* Farbmesserressource. Siehe auch ID 1038 für altes Format|
|1074|*(Photoshop CS3)* Messskala|
|1075|*(Photoshop CS3)* Zeitachseninformationen|
|1076|*(Photoshop CS3)* Blatt-Offenlegung|
|1077|*(Photoshop CS3)* DisplayInfo-Struktur zur Unterstützung von Fließgliederfarben. Siehe auch ID 1007|
|1078|*(Photoshop CS3)* Zwiewelhäute|
|1080|*(Photoshop CS4)* Zählinformationen|
|1082|*(Photoshop CS5)* Druckinformationen|
|1083|*(Photoshop CS5)* Druckstil. Die druckenden Markierungen, Etiketten, Ornamente, etc.|
|1084|*(Photoshop CS5)* Macintosh-NSPrintInfo. Variable OS-spezifische Informationen für Macintosh|
|1085|*(Photoshop CS5)* Windows-DEVMODE. Variable OS-spezifische Informationen für Windows|
|1086|*(Photoshop CS6)* Automatischer Speicherdateipfad|
|1087|*(Photoshop CS6)* Automatisches Speichernformat|
|1088|*(Photoshop CC)* Pfadauswahlstatus|
|2000-2997|Pfadinformationen (gespeicherte Pfade)|
|2999|Name des Ausschneidepfads|
|3000|*(Photoshop CC)* Ursprungspfad-Info|
|4000-4999|Plug-In-Ressource(n). Ressourcen, die von einem Plug-in hinzugefügt wurden|
|7000|Image Ready-Variablen. XML-Repräsentation der Variablendefinition|
|7001|Image Ready-Datensätze|
|7002|Bild Ready, standardmäßiger ausgewählter Status|
|7003|Image Ready 7-Rollover-erweiterter Zustand|
|7004|Image Ready-Rollover-erweiterter Zustand|
|7005|Image Ready speichert Ebeneneinstellungen|
|7006|Image Ready Version|
|8000|*(Photoshop CS3)* Lightroom-Workflow, falls vorhanden, befindet sich das Dokument mitten in einem Lightroom-Workflow|
|10000|[Druckfahneninformationen](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printflagsresource).|

Aspose.PSD unterstützt einige dieser Ressourcen. Wenn eine Ressource keine eigene Klasse hat, können Sie die [UnknownResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unknownresource) aus der Aspose.PSD-API-Referenz verwenden.

PSD-Globale Bildressourcen können für eine Vielzahl von Fällen verwendet werden. Sie können spezifische Low-Level-Daten erhalten, die Sie nicht in Adobe Photoshop erhalten können.

Fühlen Sie sich außerdem frei, über Bildressourcen zu berichten, die Sie benötigen. Das [Aspose Forum für PSD](https://forum.aspose.com/c/psd) kann helfen.