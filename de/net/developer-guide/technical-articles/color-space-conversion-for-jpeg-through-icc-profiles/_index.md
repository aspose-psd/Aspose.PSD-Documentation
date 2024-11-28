---
title: Farbraumkonvertierung für JPEG über ICC-Profile
type: docs
weight: 60
url: /de/net/farbraumkonvertierung-fuer-jpeg-ueber-icc-profile/
---

## **Farbmanagement für das JPEG-Format**

Dieser Artikel diskutiert die Verwendung von ICC-Profilen zur Durchführung des Farbraummanagements beim Umgang mit dem JPEG-Format mithilfe der Aspose.PSD APIs. Der innere Farbraum von JPEG ist YCbCr, jedoch kann dieses [Format](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) auch Graustufen, RGB, CMYK und YCCK-Farbräume aufnehmen, um die Metadaten des Bildes zu speichern. Die Aspose.PSD APIs arbeiten hauptsächlich im RGB-Farbraum, daher muss die API zur ordnungsgemäßen Verarbeitung von JPEG-Dateien eine Farbraumkonvertierung von und zu durchführen. Graustufen-zu-RGB- und YCbCr-zu-RGB-Konvertierungen können mit mathematischen Transformationen durchgeführt werden, jedoch können CMYK- und YCCK-Farbräume nicht einfach in den RGB-Farbraum konvertiert werden.

Die Aspose.PSD APIs müssen eine direkte RGB-zu-CMYK-Farbtransformation für JPEG-Bilder mit CMYK-Farbraum durchführen. Andererseits erfordern Bilder mit YCCK-Farbraum eine RGB-zu-CMYK-zu-YCCK-Farbtransformation, wobei die CMYK-zu-YCCK-Transformation die [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601)-Konvertierung für die ersten drei Kanäle verwendet und den k-Kanal unverändert lässt. Kurz gesagt, die Aspose.PSD APIs müssen eine Interkonvertierung von RGB- und CMYK-Farbräumen für sowohl CMYK- als auch YCCK-Bilder durchführen, und solche Transformationen werden mithilfe von ICC-Profilen durchgeführt, die im Grunde Look-up-Tabellen sind, die die Eigenschaften einer Farbe beschreiben und bei den Farbtransformationen helfen.

## **ICC-Profile**
Das ICC-Konvertierungsmechanismus verwendet "Profile", die den Quellfarbraum auf geräteunabhängige CIELAB- oder CIEXYZ-Farbräume abbilden. Aspose.PSD kann Daten in den erforderlichen Farbraum konvertieren, indem diese beiden Farbräume mit zusätzlichen Profilen verwendet werden. Daher muss der Benutzer für die ICC-Konvertierung zwei Profile bereitstellen - ein RGB-Profil, um zum inneren CIE-Farbraum zu gelangen, und ein CMYK-Profil, um die CMYK-Farbeigenschaften zu erhalten. Um die CMYK-zu-RGB-Konvertierung zu erreichen, müssen Profile getauscht werden, das heißt, das CMYK-Profil als Quellprofil und das RGB-Profil als Zielprofil verwenden.

## **Farbkonvertierung für JPEG über ICC-Profile**
Aspose.PSD APIs verbergen die Details und bieten einen einfachen Mechanismus zur Angabe von ICC-Profilen über die Klassen [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Darüber hinaus verwendet Aspose.PSD die Musterprofile von SWOP, CMYK und sRGB, die in seinen Kern eingebettet sind. Daher muss der Benutzer in den meisten üblichen Anwendungsfällen nicht nach spezifischen Profilen suchen. Es gibt einen Nachteil solcher Korrekturen, nämlich dass solche Farbraumkonvertierungen irreversibel sind, da wir nach der RGB-zu-CMYK-zu-RGB-Konvertierung nicht erwarten können, dieselbe Farbe zu erhalten, aufgrund inkompatibler Farbräume und unterschiedlicher Farbprofile. Der folgende Code-Schnipsel zeigt die Verwendung von Aspose.PSD für die .NET API zum Angeben von RGB- und CMYK-Farprofilen für YCCK-JPEG-Bild. Im folgenden Beispiel werden RGB- und CMYK-Farprofile geändert und das Bild im YCCK-Farbraum gespeichert. Bitte beachten Sie, dass diese [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile)- und [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile)-Eigenschaften funktionieren zur Änderung der Pixeldaten für den YCCK-Farbraum. Alle anderen Farbräume holen die Farbprofile nicht ab, um die Farbdaten zu aktualisieren.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

Wenn keine Profile festgelegt sind, verwendet Aspose.PSD für die .NET API standardmäßig die Standardprofile. Das folgende Beispiel verwendet die Profileigenschaften des Zielprofils, die den Zielfarbraum für die meisten JPEG-Bilder ändern.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
