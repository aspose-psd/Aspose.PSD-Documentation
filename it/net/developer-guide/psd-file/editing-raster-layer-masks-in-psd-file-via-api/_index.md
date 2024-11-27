---
title: Modifica delle maschere del layer raster nel file PSD tramite API
type: docs
weight: 20
url: /it/modifica-delle-maschere-del-layer-raster-nel-file-psd-tramite-api/
---

## **Panoramica**
**Per automatizzare la modifica del formato PSD e cambiare i file PSD senza Adobe® Photoshop® è possibile utilizzare l'API Aspose.PSD fornita di seguito. Ci sono frammenti di codice C# e .NET che possono aiutarti a modificare i file PSD.**

Utilizzando le maschere di livello e di vettore PSD siamo in grado di nascondere e mostrare i pixel del livello senza eliminarli definitivamente. Le maschere raster sono anche chiamate maschera di livello o maschera utente. L'accesso sia alle maschere raster che a quelle vettoriali in Aspose.PSD è fornito tramite la proprietà di livello [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) che può essere un'istanza delle classi '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' e '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' che sono classi figlie della classe astratta 'LayerMaskData'. Se un livello ha sia maschere raster che vettoriali, allora viene fornita un'istanza di [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull). Se un livello ha solo una maschera raster o una vettoriale, allora viene fornita un'istanza di [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort). Se la proprietà LayerMaskData è nulla, allora il livello non ha maschere o ha solo una maschera vettoriale disabilitata.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Una maschera raster e una maschera vettoriale disabilitata LayerMaskDataShort</p><p>Una maschera raster disabilitata LayerMaskDataShort</p><p>Una maschera raster e una maschera vettoriale LayerMaskDataFull</p><p>Una maschera raster LayerMaskDataShort</p><p>Una maschera vettoriale LayerMaskDataShort</p><p>Una maschera vettoriale disabilitata nullo (Ma è presente una risorsa vettoriale)</p>|
| :- | :- |

## **Come ottenere una maschera raster di un layer nel file PSD?**
Innanzitutto, dovremmo capire se un layer ha sia maschere vettoriali che raster:

Il codice di esempio fornito di seguito dimostra come ottenere una maschera raster di un layer

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Altrimenti, il tipo della proprietà di livello LayerMaskData è LayerMaskDataShort. In questo caso, verifichiamo se il livello ha solo una maschera raster controllando la proprietà Flags. Non dovrebbe contenere il flag [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData**, altrimenti la maschera è una cache vettoriale.

Ottenere frammento di codice della maschera:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Se hai bisogno di **estrarre una maschera raster** come LayerMaskDataShort (per ulteriori manipolazioni), anche quando sono presenti entrambe le maschere, è necessario estrarre LayerMaskDataFull e convertirlo in LayerMaskDataShort. Il seguente codice può essere utilizzato per entrambi i casi:

Estrarre una maschera raster dal PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}

## **Come verificare se un layer nel file PSD ha una maschera raster?**
Il seguente codice C# potrebbe aiutarti a verificare se un layer ha una maschera raster:

Come sapere se la maschera raster è applicata al [Layer PSD](/psd/it/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}

## **Come rimuovere / aggiungere / aggiornare una maschera raster di un layer nel file PSD?**
Semplicemente rimuovere / aggiungere / aggiornare LayerMaskData non è sufficiente per il salvataggio corretto perché i canali non vengono aggiornati; anche se potrebbero fornire un rendering corretto. Questo non cambia i canali della maschera:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Dovremmo utilizzare il metodo AddLayerMask del livello per rimuovere / aggiungere / aggiornare.

Questo aggiunge/aggiorna sia la maschera che i canali:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Questo rimuove sia la maschera che i canali:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}

## **Rimozione di una maschera raster di un layer nell'immagine PSD**
Innanzitutto, verifichiamo se la maschera è nel formato corto e se non è una maschera vettoriale possiamo semplicemente chiamare il metodo AddLayerMask con null per eliminare la maschera raster. Ma se è nel formato completo dobbiamo convertirla in un formato corto lasciando solo la maschera vettoriale. Per rimuovere una maschera di layer questo frammento di codice C# .NET può essere utilizzato:

Frammento di codice su come rimuovere la maschera di un layer dal file PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

## **Aggiornamento di una maschera raster di un layer nell'immagine PSD**
Questo è semplice: se la maschera è nel formato corto dobbiamo cambiare ImageData e MaskRectangle se necessario, altrimenti [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)e [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)dovrebbero essere cambiati. Il seguente frammento di codice C# .NET può essere utilizzato per aggiornare una maschera di layer:

Aggiorna maschera di layer PSD con C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Ecco un esempio di possibili azioni che cambiano una maschera raster. Questo inverte una maschera utente di un layer:

Aggiorna maschera di layer PSD con C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}

## **Aggiornamento di una maschera vettoriale nel file PSD quando è presente una maschera raster di un layer**
Si presume che un utente abbia già modificato una risorsa vettoriale del percorso. Quindi può aggiornare la maschera vettoriale semplicemente chiamando il metodo di layer [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask):

Aggiorna [Maschera Vettoriale del Layer PSD ](/psd/it/net/layer-vector-mask/)con C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}

## **Aggiunta di una maschera raster di un layer nel file PSD**
Se un layer non ha maschere possiamo aggiungere la maschera raster data semplicemente chiamando il metodo di layer AddLayerMask.

Se la maschera non ha il flag [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)allora ha già una maschera raster e dobbiamo aggiornarla come descritto sopra. Altrimenti, se questa maschera è in un formato corto la convertiamo in formato completo. Se non lo è la usiamo così com'è. Quindi aggiorniamo UserMaskData, UserMaskRectangle e altre proprietà con le proprietà della maschera data. Il seguente frammento di codice C# .NET può essere utilizzato per aggiungere (aggiornare) una maschera di layer:

Aggiungi nuova Maschera di Layer a PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Come verificare se una maschera di un layer è abilitata?**
Per scoprire lo stato abilitato della maschera raster del layer possiamo controllare lo stato del flag LayerMaskFlags.Disabled nella proprietà Flags per LayerMaskDataShort o in RealFlags per LayerMaskDataFull. Il seguente frammento di codice C# .NET può essere utilizzato per ottenere lo stato abilitato di una maschera di layer:

Verifica se una maschera è abilitata:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}

## **Come abilitare o disabilitare una maschera raster di un layer?**
Per abilitare o disabilitare una maschera raster di un layer possiamo cambiare lo stato del flag LayerMaskFlags.Disabled nella proprietà Flags per LayerMaskDataShort o in RealFlags per LayerMaskDataFull. Il seguente frammento di codice C# .NET può essere utilizzato per cambiare lo stato abilitato di una maschera di layer:

Abilita o disabilita la Maschera di Layer Raster:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentazione-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}
