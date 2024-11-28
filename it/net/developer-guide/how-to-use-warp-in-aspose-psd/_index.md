---
title: Come Utilizzare il Warp in Aspose.PSD
type: docs
weight: 40
url: /it/net/come-utilizzare-il-warp-in-aspose-psd/
---

## **Parte 1 – Rendering di un File PSD con l'Effetto Warp**

Photoshop salva l'immagine renderizzata dopo aver applicato l'effetto Warp. La nostra libreria può riprodurre o ri-renderizzare l'immagine con l'effetto Warp. Per abilitare questa funzionalità, basta impostare il flag AllowWarpRepaint nelle impostazioni quando si apre il file PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-Aspose-PSD-Warp-Rendering-1.cs" >}}

Risultato:
![Risultato di Aspose.PSD per .NET con Warp 1](warp1.png)

Oltre a renderizzare l'effetto Warp per SmartLayers, la nostra libreria supporta anche il Warp per TextLayers. Il codice di implementazione rimane identico, con l'unica differenza nel nome del file.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-Aspose-PSD-Warp-Rendering-2.cs" >}}

Risultato:
![Risultato di Aspose.PSD per .NET con Warp 2](warp2.png)

**! Nota:** Attualmente, la nostra libreria supporta il rendering sia per Custom Warp* (dove gli utenti manipolano i punti della mesh) che per tutti i tipi standard di Warp.
* - Attualmente, la nostra libreria supporta Custom Warp con la mesh standard, e stiamo lavorando attivamente per espandere il nostro supporto per includere tutti i tipi di mesh in futuro.


## **Parte 2 – Modifica dell'Effetto Warp**

La nostra libreria ti consente non solo di renderizzare ma anche di modificare (aggiungere) l'effetto Warp. 
Queste modifiche sono facilitate attraverso le funzionalità della classe **WarpParams**.

| **Funzionalità** | **Descrizione**                                                         | 
|:-----------------|:-------------------------------------------------------------------------|
| Bounds           | Restituisce i limiti dell'immagine distorta.                             |
| MeshPoints       | Un array di punti, con ciascun punto che rappresenta un vertice della mesh di distorsione. |
| Valore           | Il valore dell'effetto Warp per gli effetti di distorsione non personalizzati. |
| WarpRotates      | Un'enumerazione che definisce la direzione degli effetti Warp non personalizzati. |
| WarpStyles       | Un'enumerazione che definisce il tipo di effetto Warp.                   |

L'esempio di codice di seguito mostra come determinare il tipo di effetto Warp per uno SmartLayer e regolare il tipo e l'intensità della distorsione per l'effetto.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-Aspose-PSD-Warp-Rendering-3.cs" >}}

Risultato:
![Risultato di Aspose.PSD per .NET con Warp 3](warp3.png)

## **Parte 3 – Aggiunta dell'Effetto Warp**

L'esempio di codice di seguito mostra come aggiungere un effetto Warp standard a uno SmartLayer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7 c0ce974175c" "Documentazione-Aspose-PSD-Warp-Rendering-4.cs" >}}

Risultato:
![Risultato di Aspose.PSD per .NET con Warp 4](warp4.png)

L'esempio di codice di seguito mostra come aggiungere un effetto Warp personalizzato a uno SmartLayer.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-Aspose-PSD-Warp-Rendering-5.cs" >}}

Risultato:
![Risultato di Aspose.PSD per .NET con Warp 5](warp5.png)

L'esempio di codice di seguito mostra come aggiungere un effetto Warp a uno Strato di Testo.
**! Nota:** Secondo gli standard di Photoshop, l'effetto Warp per i TextLayers è tipicamente limitato al tipo standard. Tuttavia, la nostra libreria supporta l'uso di due tipi di effetti Warp. Si noti che tali file potrebbero non essere pienamente compatibili con Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-Aspose-PSD-Warp-Rendering-6.cs" >}}

Risultato:
![Risultato di Aspose.PSD per .NET con Warp 6](warp6.png)

Continuiamo a perfezionare ed espandere le capacità del nostro effetto Warp, concentrandoci su migliorarne la velocità, la qualità e le funzionalità supportate. Restate aggiornati con i nostri rilasci mensili per le ultime novità.
Il Tuo Team Aspose.PSD
