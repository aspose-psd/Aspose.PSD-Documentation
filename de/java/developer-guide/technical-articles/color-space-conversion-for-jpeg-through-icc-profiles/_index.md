---
title: Farbraumkonvertierung für JPEG durch ICC-Profile
type: docs
weight: 50
url: /de/java/farbraumkonvertierung-für-jpeg-durch-icc-profile/
---

## **Farbmanagement für das JPEG-Format**


Dieser Artikel erörtert die Verwendung von ICC-Profilen zur Durchführung des Farbraummanagements beim Umgang mit dem JPEG-Format mit Aspose.PSD APIs. Der innere Farbraum von JPEG ist YCbCr, jedoch kann dieses Format auch Graustufen, RGB, CMYK und YCCK-Farbräume aufnehmen, um die Metadaten des Bildes zu speichern. Aspose.PSD APIs arbeiten hauptsächlich im RGB-Raum, daher muss die API Farbraumkonvertierungen von und zu durchführen, um JPEG-Dateien ordnungsgemäß zu verarbeiten. Graustufen- zu RGB- und YCbCr- zu RGB-Konvertierungen können mit mathematischen Transformationen durchgeführt werden, während CMYK- und YCCK-Räume nicht so einfach in den RGB-Raum konvertiert werden können.



Die Aspose.PSD APIs müssen eine direkte RGB-zu-CMYK-Farbumwandlung für JPEG-Bilder durchführen, die den CMYK-Farbraum besitzen. Andererseits erfordern Bilder, die den YCCK-Farbraum besitzen, eine RGB- zu CMYK- zu YCCK-Farbumwandlung, wobei die CMYK- zu YCCK-Wandlung die ITU-R BT.601-Konvertierung für die ersten drei Kanäle verwendet und den k-Kanal unberührt lässt. Kurz gesagt müssen Aspose.PSD APIs die Interkonvertierung von RGB- und CMYK-Farbräumen für beide CMYK- und YCCK-Bilder durchführen, und diese Transformationen werden mithilfe von ICC-Profilen durchgeführt, die im Grunde Look-up-Tabellen sind, die die Eigenschaften einer Farbe beschreiben und bei den Farbtransformationen helfen.


## **ICC-Profile**
Der ICC-Umwandlungsmechanismus verwendet „Profile“, die den Quellfarbraum auf geräteunabhängige CIELAB- oder CIEXYZ-Farbräume abbilden. Aspose.PSD kann Daten in den erforderlichen Farbraum konvertieren, während diese beiden Farbräume mit zusätzlichen Profilen verwendet werden. Daher muss der Benutzer für die ICC-Umwandlung zwei Profile bereitstellen - ein RGB-Profil, um zum inneren CIE-Farbraum zu gelangen, und ein CMYK-Profil, um die CMYK-Farbeigenschaften zu erhalten. Um die CMYK- zu RGB-Konvertierung zu erreichen, muss man die Profile vertauschen, d.h. das CMYK-Profil als Quellprofil und das RGB-Profil als Zielprofil verwenden.
## **Farbkonvertierung für JPEG durch ICC-Profile**
Aspose.PSD APIs verbergen die Details und bieten einen einfach zu verwendenden Mechanismus zur Angabe von ICC-Profilen über die JpegOptions-Klasse. Darüber hinaus verwendet Aspose.PSD die Beispieldateien der SWOP CMYK und sRGB, die in den Kern eingebettet sind, daher muss der Benutzer in den meisten gängigen Anwendungsfällen nicht nach spezifischen Profilen suchen. Es gibt einen Nachteil solcher Korrekturen, nämlich dass solche Farbraumkonvertierungen nicht rückgängig gemacht werden können, da man nicht erwarten kann, nach der RGB- zu CMYK- zu RGB-Konvertierung dieselbe Farbe zu erhalten, aufgrund inkompatibler Farbräume und unterschiedlicher Farbprofile. Der folgende Codeausschnitt zeigt die Verwendung von Aspose.PSD für die Java-API zur Angabe von RGB- und CMYK-Farbprofilen für das YCCK-JPEG-Bild. Im folgenden Beispiel werden RGB- und CMYK-Farbprofile geändert und das Bild im YCCK-Farbraum gespeichert. Bitte beachten Sie, dass diese RgbColorProfile- und CmykColorProfile-Eigenschaften zum Ändern von Pixeldaten für den YCCK-Farbraum funktionieren. Alle anderen Farbräume greifen nicht auf die Farbprofile zurück, um die Farbdaten zu aktualisieren.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}



Wenn keine Profile festgelegt sind, verwendet Aspose.PSD für die Java-API die Standardprofile. Im folgenden Beispiel werden die Eigenschaften der Zielprofile verwendet, um den Zielfarbraum für die meisten JpegImages zu ändern.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}
