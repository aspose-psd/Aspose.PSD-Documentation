---
title: Anwendung von Median- und Wiener-Filtern
type: docs
weight: 10
url: /de/java/anwendung-von-median-und-wiener-filtern/
---

## **Anwendung von Median- und Wiener-Filtern**
Der Medianfilter ist eine nichtlineare digitale Filtertechnik, die häufig zur Rauschunterdrückung verwendet wird. Diese Rauschreduktion ist ein typischer Preprocessing-Schritt, um die Ergebnisse der späteren Verarbeitung zu verbessern. Der Wienerfilter ist der MSE (Mean Squared Error) optimale stationäre lineare Filter für Bilder, die durch additive Rauschen und Unschärfe verschlechtert wurden. Mithilfe der Aspose.PSD für Java API können Entwickler den Medianfilter zur Rauschunterdrückung auf das Bild anwenden und den Gaußschen Wienerfilter auf Bilder anwenden. Dieser Artikel zeigt, wie der Medianfilter und der Gaußsche Wienerfilter auf Bilder angewendet werden können.

### **Anwendung des Medianfilters**
Aspose.PSD bietet die Klasse MedianFilterOptions, um den Filter auf ein Rasterbild anzuwenden. Der folgende Code-Ausschnitt zeigt, wie der Medianfilter auf ein Rasterbild angewendet wird.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **Anwendung des Gaußschen Wienerfilters**
Aspose.PSD bietet die Klasse GaussWienerFilterOptions, um den Filter auf ein Rasterbild anzuwenden. Der folgende Code-Ausschnitt zeigt, wie der Gaußsche Wienerfilter auf ein Rasterbild angewendet wird.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **Anwendung des Gaußschen Wienerfilters auf Farbbilder**
Aspose.PSD bietet auch GaussWienerFilterOptions für Farbbilder. Der folgende Code-Ausschnitt zeigt, wie der Gaußsche Wienerfilter auf ein Farbbild angewendet wird.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **Anwendung des Motion Wienerfilters**
Aspose.PSD bietet die Klasse MotionWienerFilterOptions, um den Filter auf ein Rasterbild anzuwenden. Der folgende Code-Ausschnitt zeigt, wie der Bewegungs-Wienerfilter auf ein Rasterbild angewendet wird.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **Anwendung von Korrekturfiltern auf ein Bild**
Dieser Artikel zeigt die Verwendung von Aspose.PSD für Java zur Durchführung von Korrekturfiltern auf ein Bild. Die Aspose.PSD APIs haben effiziente und einfach zu verwendende Methoden zur Erreichung dieses Ziels bereitgestellt. Aspose.PSD für Java hat die Klassen BilateralSmoothingFilterOptions und SharpenFilterOptions für die Filtration freigelegt. Die Klasse BilateralSmoothingFilterOptions benötigt eine Ganzzahl als Größe. Die Schritte zum Durchführen der Größenänderung sind so einfach wie unten beschrieben:

1. Laden Sie ein Bild mit der von der Klasse Image bereitgestellten Methode Load.
1. Konvertieren Sie das Bild in ein Rasterbild.
1. Erstellen Sie Instanzen der Klassen BilateralSmoothingFilterOptions und SharpenFilterOptions.
1. Rufen Sie die RasterImage.Filter-Methode auf, wobei Sie das Rechteck als Bildgrenzen und die Instanz der Klasse BilateralSmoothingFilterOptions angeben.
1. Rufen Sie die RasterImage.Filter-Methode auf, wobei Sie das Rechteck als Bildgrenzen und die Instanz der Klasse SharpenFilterOptions angeben.
1. Kontrast anpassen
1. Helligkeit einstellen
1. Speichern Sie die Ergebnisse.

Der folgende Code-Ausschnitt zeigt Ihnen, wie der Korrekturfilter angewendet wird.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **Verwendung des Bradley-Schwellenalgorithmus**
Die Bildschwellwertbestimmung wird in Grafikanwendungen verwendet. Das Ziel der Schwellwertbestimmung eines Bildes besteht darin, Pixel entweder als "dunkel" oder "hell" zu klassifizieren. Die Aspose.PSD API ermöglicht es Ihnen, den Bradley-Schwellenwert zu verwenden, während Sie Bilder konvertieren. Der folgende Code-Ausschnitt zeigt Ihnen, wie Sie den Schwellenwertwert definieren und dann den Bradley-Schwellenalgorithmus aufrufen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
