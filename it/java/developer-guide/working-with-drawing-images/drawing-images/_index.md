---
title: Disegno Immagini
type: docs
weight: 10
url: /it/java/disegno-immagini/
---

## **Disegno Linee**
Questo esempio utilizza la classe Graphics per disegnare le forme di linea sulla superficie dell'immagine. Per dimostrare l'operazione, l'esempio crea una nuova immagine e disegna linee sulla superficie dell'immagine utilizzando il metodo DrawLine esposto dalla classe Graphics. Per prima cosa, creeremo un'immagine PsdImage specificando la sua altezza e larghezza.

Una volta creata l'immagine, utilizzeremo il metodo Clear esposto dalla classe Graphics per impostare il colore di sfondo. Il metodo DrawLine della classe Graphics viene utilizzato per disegnare una linea su un'immagine che collega due strutture di punti. Questo metodo ha diversi sovraccarichi che accettano l'istanza della classe Pen e le coppie di coordinate dei punti o strutture Point/PointF come argomenti. La classe Pen definisce un oggetto utilizzato per disegnare linee, curve e figure. La classe Pen ha diversi costruttori sovraccaricati per disegnare linee con colore, larghezza e pennello specificati. La classe SolidBrush viene utilizzata per disegnare in modo continuo con un colore specifico. Infine, l'immagine viene esportata nel formato file BMP. Il seguente frammento di codice mostra come disegnare le forme delle linee sulla superficie dell'immagine.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}
## **Disegno Ellisse**
L'esempio di disegno di ellissi è il secondo articolo della serie sul disegno di forme. Utilizzeremo la classe Graphics per disegnare la forma dell'ellisse sulla superficie dell'immagine. Per dimostrare l'operazione, l'esempio crea una nuova immagine e disegna la forma dell'ellisse sulla superficie dell'immagine utilizzando il metodo DrawEllipse esposto dalla classe Graphics. Per prima cosa, creeremo un'immagine PsdImage specificando la sua altezza e larghezza.

Dopo aver creato l'immagine, creeremo e inizializzeremo un oggetto della classe Graphics e imposteremo il colore di sfondo dell'immagine utilizzando il metodo Clear della classe Graphics. Il metodo DrawEllipse della classe Graphics viene utilizzato per disegnare la forma dell'ellisse su una superficie di immagine specificata dalla struttura del rettangolo delimitante. Questo metodo ha diversi sovraccarichi che accettano le istanze delle classi Pen e Rectangle/RectangleF o una coppia di coordinate, altezza e larghezza come argomenti. La classe Pen definisce un oggetto utilizzato per disegnare linee, curve e figure. La classe Pen ha diversi costruttori sovraccaricati per disegnare linee con colore, larghezza e pennello specificati. La classe Rectangle memorizza un insieme di quattro interi che rappresentano la posizione e le dimensioni di un rettangolo. La classe Rectangle ha diversi costruttori sovraccaricati per disegnare la struttura del rettangolo con dimensioni e posizione specificate. La classe SolidBrush viene utilizzata per disegnare in modo continuo con un colore specifico. Infine, l'immagine viene esportata nel formato file BMP. Il seguente frammento di codice mostra come disegnare la forma dell'ellisse sulla superficie dell'immagine.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
## **Disegno Rettangolo**
In questo esempio disegneremo la forma del rettangolo sulla superficie dell'immagine. Per dimostrare l'operazione, l'esempio crea una nuova immagine e disegna la forma del rettangolo sulla superficie dell'immagine utilizzando il metodo DrawRectangle esposto dalla classe Graphics. Per prima cosa, creeremo un'immagine PsdImage specificando la sua altezza e larghezza. Successivamente, imposteremo il colore di sfondo dell'immagine utilizzando il metodo Clear della classe Graphics.

Il metodo DrawRectangle della classe Graphics viene utilizzato per disegnare la forma del rettangolo su una superficie di immagine specificata dalla struttura del rettangolo. Questo metodo ha diversi sovraccarichi che accettano le istanze delle classi Pen e Rectangle/RectangleF o coppie di coordinate, larghezza e altezza come argomenti. La classe Rectangle memorizza un insieme di quattro interi che rappresentano la posizione e le dimensioni di un rettangolo. La classe Rectangle ha diversi costruttori sovraccaricati per disegnare la struttura del rettangolo con dimensioni e posizione specificate. Infine, l'immagine viene esportata nel formato file BMP. Il seguente frammento di codice mostra come disegnare la forma del rettangolo sulla superficie dell'immagine.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}
## **Disegno Arco**
In questa sessione della serie sul disegno di forme, disegneremo la forma dell'arco sulla superficie dell'immagine. Utilizzeremo il metodo DrawArc di Graphics per dimostrare l'operazione su un'immagine BMP. Per prima cosa, creeremo un'immagine PsdImage specificando la sua altezza e larghezza. Una volta creata l'immagine, utilizzeremo il metodo Clear esposto dalla classe Graphics per impostare il suo colore di sfondo.

Il metodo DrawArc della classe Graphics viene utilizzato per disegnare la forma dell'arco su una superficie di immagine. DrawArc rappresenta una parte di un'ellisse specificata dalla struttura del rettangolo o dalla coppia di coordinate. Questo metodo ha diversi sovraccarichi che accettano le istanze delle classi Pen e delle strutture Rectangle/RectangleF o una coppia di coordinate, larghezza e altezza come argomenti. Infine, l'immagine viene esportata nel formato file BMP. Il seguente frammento di codice mostra come disegnare la forma dell'arco sulla superficie dell'immagine.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
## **Disegno Bezier**
Questo esempio utilizza la classe Graphics per disegnare la forma di Bezier sulla superficie dell'immagine. Per dimostrare l'operazione, l'esempio crea una nuova immagine e disegna la forma di Bezier sulla superficie dell'immagine utilizzando il metodo DrawBezier esposto dalla classe Graphics. Per prima cosa, creeremo un'immagine PsdImage specificando la sua altezza e larghezza. Una volta creata l'immagine, utilizzeremo il metodo Clear esposto dalla classe Graphics per impostare il suo colore di sfondo.

Il metodo DrawBezier della classe Graphics viene utilizzato per disegnare la forma di Bezier spline su una superficie di immagine definita da quattro strutture Point. Questo metodo ha diversi sovraccarichi che accettano le istanze della classe Pen e quattro coppie ordinate di coordinate o quattro strutture Point/PointF o array di strutture Point/PointF. La classe Pen definisce un oggetto utilizzato per disegnare linee, curve e figure. La classe Pen ha diversi costruttori sovraccaricati per disegnare linee con colore, larghezza e pennello specificati. Infine, l'immagine viene esportata nel formato file BMP. Il seguente frammento di codice mostra come disegnare la forma di Bezier sulla superficie dell'immagine.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
## **Disegno Immagini utilizzando la Funzionalità Principale**
Aspose.PSD è una libreria che offre molte funzionalità preziose, tra cui la creazione di immagini da zero. Disegnare utilizzando la funzionalità principale come manipolare le informazioni bitmap di un'immagine, oppure utilizzare le funzionalità avanzate come Graphics e GraphicsPath per disegnare forme sulla superficie dell'immagine con l'aiuto di diversi pennelli e penne. Utilizzando la classe RasterImage di Aspose.PSD, è possibile recuperare le informazioni sui pixel di un'area dell'immagine e manipolarle. La classe RasterImage contiene l'intera funzionalità principale di disegno, come ottenere e impostare i pixel e altri metodi per la manipolazione delle immagini. Creare una nuova immagine utilizzando uno dei metodi descritti in Creazione File e assegnarla a un'istanza della classe RasterImage. Utilizzare il metodo LoadPixels della classe RasterImage per recuperare le informazioni dei pixel di una parte di un'immagine. Una volta ottenuto un array di pixel, è possibile manipolarlo, ad esempio cambiando il colore di ciascun pixel. Dopo aver manipolato le informazioni sui pixel, riportarle nell'area desiderata dell'immagine utilizzando il metodo SavePixels della classe RasterImage. Il seguente frammento di codice mostra come disegnare immagini utilizzando la funzionalità principale.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}
