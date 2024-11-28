---
title: Anwendung von Median- und Wiener-Filtern
type: docs
weight: 10
url: /de/anwendung-von-median-und-wiener-filter/
---

## **Anwendung von Median- und Wiener-Filtern**
Der Medianfilter ist eine nichtlineare digitale Filterungstechnik, die häufig zur Rauschunterdrückung verwendet wird. Eine solche Rauschreduzierung ist ein typischer Vorverarbeitungsschritt, um die Ergebnisse späterer Verarbeitungsschritte zu verbessern. Der Wiener-Filter ist der MSE (Mean Squared Error) optimale stationäre lineare Filter für Bilder, die durch additives Rauschen und Verschwommung beeinträchtigt sind. Mit der Aspose.PSD für .NET-API können Entwickler einen Medianfilter auf das Bild anwenden und den Gauss-Wiener-Filter auf Bilder anwenden. Dieser Artikel zeigt, wie der Medianfilter und der Gauss-Wiener-Filter auf Bilder angewendet werden können.
### **Anwendung des Medianfilters**
Aspose.PSD bietet die Klasse [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) zur Anwendung eines Filters auf ein [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) an. Der unten bereitgestellte Codeausschnitt zeigt, wie der Medianfilter auf ein Rasterbild angewendet wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Anwendung des Gauss-Wiener-Filters**
Aspose. PSD bietet die Klasse [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) zur Anwendung eines Filters auf ein [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) an. Der unten bereitgestellte Codeausschnitt zeigt, wie der Gauss-Wiener-Filter auf ein Rasterbild angewendet wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Anwendung des Gauss-Wiener-Filters für ein Farbbild**
Aspose. PSD bietet auch die [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) für Farbbilder an. Der unten bereitgestellte Codeausschnitt zeigt, wie der Gauss-Wiener-Filter auf ein Farbbild angewendet wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Anwendung des Motion-Wiener-Filters**
Aspose. PSD bietet die Klasse [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) zur Anwendung eines Filters auf ein [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) an. Der unten bereitgestellte Codeausschnitt zeigt, wie der Motion-Wiener-Filter auf ein Rasterbild angewendet wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Anwendung des Korrekturfilters auf ein Bild**
Dieser Artikel zeigt die Verwendung von Aspose.PSD für .NET zur Durchführung von Korrekturfiltern auf einem Bild. Die APIs von Aspose.PSD haben effiziente und benutzerfreundliche Methoden bereitgestellt, um dieses Ziel zu erreichen. Aspose.PSD für .NET hat die Klassen [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) und [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) für die Filtration freigelegt. Die Klasse BilateralSmoothingFilterOptions benötigt eine Ganzzahl als Größe. Die Schritte zur Durchführung der Skalierung sind so einfach wie unten beschrieben:

1. Laden Sie ein Bild mit der vom Image-Klasse freigegebenen Factory-Methode Load.
1. Konvertieren Sie das Bild in ein RasterImage.
1. Erstellen Sie eine Instanz der Klassen BilateralSmoothingFilterOptions und SharpenFilterOptions.
1. Rufen Sie die Methode [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) auf und geben Sie dabei als Bildbereich ein Rechteck und eine Instanz der Klasse BilateralSmoothingFilterOptions an.
1. Rufen Sie die Methode [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) auf und geben Sie dabei als Bildbereich ein Rechteck und eine Instanz der Klasse SharpenFilterOptions an.
1. Passen Sie den Kontrast an.
1. Einstellen der Helligkeit
1. Speichern Sie die Ergebnisse.

## **Verwendung des Bradley-Schwellenwertalgorithmus**
Die Bildschwellenwertbestimmung wird in Grafikanwendungen verwendet. Das Ziel der Schwellenwertbestimmung eines Bildes besteht darin, Pixel als "dunkel" oder "hell" zu klassifizieren. Aspose.PSD-API ermöglicht es Ihnen, den Bradley-Schwellenwert zu verwenden, während Bilder konvertiert werden. Der folgende Codeausschnitt zeigt, wie Sie den Schwellenwert festlegen und dann den Bradley-Schwellenwertalgorithmus aufrufen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
