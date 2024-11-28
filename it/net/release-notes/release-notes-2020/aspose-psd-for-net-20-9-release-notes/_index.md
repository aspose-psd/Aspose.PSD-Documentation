---
title: Note sulla versione di Aspose.PSD per .NET 20.9
type: docs
weight: 40
url: /it/net/aspose-psd-per-net-20-9-note-sulla-versione/
---

{{% alert color="primary" %}} 

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-408|Supporto di SoLEResource (risorsa esterna del livello oggetto intelligente)|Funzionalità|
|PSDNET-614|Supporto di oggetti intelligenti collegati|Funzionalità|
|PSDNET-615|Supporto di oggetti intelligenti incorporati|Funzionalità|
|PSDNET-690|L'aggiornamento del testo in un dato file PSD e il salvataggio cambia alcuni parametri del livello e del testo|Errore|
|PSDNET-696|FillLayer non viene aggiornato dopo la creazione e non può essere reso correttamente|Errore|
|PSDNET-712|Regression: Aspose.PSD 20.8.0 non può aprire il file|Errore|
|PSDNET-714|In un file PSD specifico, il ridimensionamento del TextLayer rompe il valore della posizione|Errore|

## **Modifiche API pubbliche**
# **API aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LanguageIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Fractions
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manuale
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metrico
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optico
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.PlacedId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Personalizzato
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.NumeroPagina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PagineTotali
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PolicyAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TipoLivelloPostato
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Sx
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Su
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Dx
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Giù
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Bound
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.MatriceTrasformazione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PuntiReteOrizzontale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PuntiReteVerticale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UnitàPuntoReteOrizzontale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UnitàPuntoReteVerticale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Firma
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Valore
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Prospettiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.AltriProspettiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.OrdineU
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.OrdineV
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Elementi
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.CompIdOriginale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.NumeroPagina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PagineTotali
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PolicyAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TipoLivelloPostato
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.MatriceTrasformazione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.MatriceNonAffineTransform
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Firma
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Lunghezza
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.VersionePsd
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Elementi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Ritaglia
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.NumeroFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Risoluzione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.UnitàRisoluzione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Larghezza
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Altezza
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PassipFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.DenominatoreFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.NumeratoreDurata
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.DenominatoreDurata
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Salva(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.Chiave
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.ChiaveStrumentoTipo
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CreatoreRisorsaIntelligente
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CreatoreRisorsaIntelligente.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CreatoreRisorsaIntelligente.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CreatoreRisorsaIntelligente.#ctor(System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CreatoreRisorsaIntelligente.GeneraRisorsaPostata
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CreatoreRisorsaIntelligente.GeneraRisorsaIntegrataIntelligente
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CreatoreRisorsaIntelligente.GeneraRisorsaEsternaIntelligente
- T:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente
- P:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.BoundContenuti
- P:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.FontiContenuti
- P:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.Contenuti
- P:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.TipoContenuto
- P:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.FornitoreOggettoIntelligente
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.EsportaContenuti(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.CaricaContenuti(Aspose.PSD.LoadOptions)
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.SostituisciContenuti(Aspose.PSD.Immagine)
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.SostituisciContenuti(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.IncorporaCollegato
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.ConvertiInCollegato(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.RicollegaAFile(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.StratoOggettoIntelligente.AggiornaContenutoModificato
- T:Aspose.PSD.FileFormats.Psd.FornitoreOggettoIntelligente
- M:Aspose.PSD.FileFormats.Psd.FornitoreOggettoIntelligente.IncorporaTuttiCollegati
- M:Aspose.PSD.FileFormats.Psd.FornitoreOggettoIntelligente.AggiornaTuttoIlContenutoModificato
- T:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.TipoOggettoIntelligente
- F:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.TipoOggettoIntelligente.Incorporato
- F:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.TipoOggettoIntelligente.CollegatoDisponibile
- F:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.TipoOggettoIntelligente.CollegatoNonDisponibile
- F:Aspose.PSD.FileFormats.Psd.Layers.OggettiIntelligenti.TipoOggettoIntelligente.LinkLibreria
- P:Aspose.PSD.FileFormats.Psd.PsdImage.FornitoreOggettoIntelligente

# **API rimosse:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Personalizzato
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.NumeroPagina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PagineTotali
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PolicyAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TipoLivelloPostato
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Sx
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Su
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Dx
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Giù
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bound
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.MatriceTrasformazione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PuntiReteOrizzontale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PuntiReteVerticale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UnitàPuntoReteOrizzontale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UnitàPuntoReteVerticale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Valore
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Elementi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.CompIdOriginale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Personalizzato
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.NumeroPagina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PagineTotali
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PolicyAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TipoLivelloPostato
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Sx
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Su
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Dx
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Giù
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Bound
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.MatriceTrasformazione
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.MatriceNonAffineTransform
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PuntiReteOrizzontale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PuntiReteVerticale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UnitàPuntoReteOrizzontale
- P:Aspose.PSD.FileFormats.PuntePuntoReteVerticale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Firma
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Lunghezza
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VersionePsd
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Valore
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Prospettiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.SpecificaProspettiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UOrdine
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VOrdine
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Elementi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Taglio
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.ConteggioFrame
- P:Aspose.P