---
title: Problemi Noti
type: docs
weight: 40
url: /it/net/problemi-noti/
---

## **Framework Compact .NET**
- E' stato osservato che su alcune versioni specifiche di Windows come Windows Mobile 5.0-6.0 le assemblee del framework compatto firmate con certificato (o certificati duali) non funzionano come previsto e non riescono a caricarsi correttamente (viene generata un'eccezione di tipo TypeLoadException). Per risolvere il problema, l'utente deve rimuovere qualsiasi certificato e quindi utilizzare l'assemblea aggiornata. Si noti che si farà ciò a proprio rischio e pericolo e non garantiamo un corretto funzionamento a causa di tale modifica dell'assemblea. Inoltre, non inviamo assemblee senza firma in quanto si tratta di una potenziale minaccia per la sicurezza. Invece, i clienti dovrebbero evitare di utilizzare tali vecchi sistemi operativi, se possibile, e/o aggiornare il sistema operativo a edizioni o pacchetti di servizi più recenti che risolvono il problema di firma del certificato.
