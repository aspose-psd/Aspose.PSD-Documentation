---
title: Intestazione dei file PSD e PSB
type: docs
weight: 40
url: /it/net/psd-and-psb-file-header/
---

## **Descrizione**
L'intestazione del file di Adobe Photoshop contiene informazioni sulla versione del file (1 per i file PSD e 2 per i file PSB), il numero di canali, la modalità colore e la profondità di bit.

Puoi apprendere le combinazioni supportate da Aspose.PSD di Modalità Colore e Profondità di Bit dall'articolo correlato.


L'intestazione del file contiene le proprietà di base dell'immagine.

|**Lunghezza**|**Descrizione**|
| :- | :- |
|4|Firma: sempre uguale a *"8BPS"*|
|2|[Versione PSD](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): sempre uguale a 1 per i file PSD e 2 per i file PSB. Aspose.PSD può rilevare una versione del Formato File e leggerla correttamente.|
|6|Riservati: devono essere zero.|
|2|Il numero di canali nell'immagine, inclusi eventuali canali alfa. L'intervallo supportato è da 1 a 56.|
|4|L'altezza dell'immagine in pixel. L'intervallo supportato è da 1 a 30.000. Il File PSB supporta un'altezza fino a 300.000 pixel. Anche i file PSB sono supportati da Aspose.PSD.|
|4|La larghezza dell'immagine in pixel. L'intervallo supportato è da 1 a 30.000. Il File PSB supporta una larghezza fino a 300.000 pixel. Il processo batch di grandi file PSD/PSB è supportato anche da Aspose.PSD.|
|2|Profondità: il numero di bit per canale. I valori supportati sono 1, 8, 16 e 32, ma non ogni Modalità Colore funziona con ogni profondità.|
|2|La [modalità colore PSD](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) del file. I valori supportati sono: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multicanale = 7; Duotono = 8; Lab = 9.|
Puoi controllare il nostro [Riferimento API PSD](https://reference.aspose.com/psd) per questo.
