# Privacy Policy — Birdsoniq

**Ultimo aggiornamento:** 4 giugno 2026
**Versione documento:** 1.4

> Lo storico completo delle modifiche a questa Privacy Policy è pubblicamente consultabile sul repository git del documento: `https://github.com/giovannisecci/birdsoniq-legal`. Ogni versione precedente resta verificabile e scaricabile.

---

## 1. Premesse e identità del Titolare del trattamento

La presente Privacy Policy descrive le modalità con cui **Birdsoniq** (di seguito "l'app") raccoglie, utilizza, conserva e condivide i dati personali degli utenti. L'informativa è redatta in conformità al Regolamento UE 2016/679 ("GDPR"), al Decreto Legislativo 196/2003 (Codice Privacy italiano come modificato dal D.Lgs. 101/2018) e alle linee guida del Garante per la Protezione dei Dati Personali.

**Titolare del trattamento**

* **Nome:** Giovanni Secci
* **Indirizzo:** Via Baccarini, 08100 Nuoro (NU), Italia
* **Partita IVA:** [IT\_\_**\_\_**\_\_ — in corso di attivazione alla data di prima pubblicazione]
* **Email per questioni privacy:** privacy@birdsoniq.app
* **Email per supporto generale:** privacy@birdsoniq.app


**Accettazione**

Scaricando, installando o utilizzando Birdsoniq, l'utente prende atto della presente informativa. Qualora l'utente non concordi con le modalità descritte, può scegliere di non utilizzare l'app e disinstallarla dal proprio dispositivo.

---

## 2. Principi generali e approccio "privacy by design"

Birdsoniq è progettata secondo il principio della **minimizzazione dei dati**: raccoglie esclusivamente le informazioni strettamente necessarie a fornire le funzionalità richieste dall'utente e nella quantità minima indispensabile.

Caratteristiche chiave dell'approccio adottato:

* **Account facoltativo.** L'app non richiede registrazione: l'identificazione delle specie tramite foto e audio funziona interamente senza account. L'utente può facoltativamente creare un account (email e password, oppure accesso Google) per abilitare funzioni accessorie quali la sincronizzazione cloud della cronologia (Gold) e il profilo struttura. L'account è eliminabile in qualsiasi momento direttamente dall'app (v. §3.10).
* **Identificazione interamente on-device.** I modelli di intelligenza artificiale per l'identificazione di uccelli tramite foto e audio girano interamente sul dispositivo dell'utente. Le registrazioni audio non vengono mai trasmesse a server esterni; le fotografie non vengono trasmesse né per l'identificazione standard né per la condivisione community. Unica eccezione: la funzione facoltativa **AI Premium** (§3.11) che — dietro consenso esplicito dedicato e su azione manuale dell'utente — invia la singola fotografia selezionata al backend per un'analisi avanzata.
* **Community "metadata-only".** La funzione community consente di condividere i soli metadati di un'osservazione (nome della specie, data, coordinate GPS, livello di confidenza). Audio, fotografie e qualsiasi altro file multimediale non vengono mai caricati sul cloud. Cfr. §3.8.
* **Condivisione community opt-in.** La pubblicazione dei metadati nel feed community richiede il consenso esplicito dell'utente, richiesto tramite un dialog informativo al primo tentativo di condivisione.
* **Nessuna pubblicità, nessun tracker.** L'app non integra SDK pubblicitari, servizi di analisi comportamentale, strumenti di profilazione o tracker di terze parti.

---

## 3. Categorie di dati trattati

Di seguito l'elenco dettagliato delle categorie di dati che Birdsoniq tratta, con indicazione per ciascuna di finalità, base giuridica, destinatari e tempi di conservazione.

### 3.1 Identificativi anonimi (communityId e installId)

* **Cosa viene raccolto:** due identificativi distinti, con funzioni separate. (1) Il **communityId**: identificativo univoco generato casualmente (UUID v4) al primo utilizzo delle funzioni community e memorizzato nelle preferenze locali; è l'identità pseudonima che accompagna i contenuti pubblicati (osservazioni, commenti, segnalazioni, classifica). (2) L'**installId**: identificativo tecnico dell'installazione — coincidente con l'identificativo Android del dispositivo (SSAID) o, ove non disponibile, con un UUID v4 casuale — utilizzato esclusivamente per la prevenzione delle frodi.
* **Finalità:** communityId — identificazione pseudonima dei contenuti pubblicati ed esercizio dei diritti GDPR senza necessità di account; installId — prevenzione di frodi e abusi (periodi di prova gratuiti, quote di utilizzo).
* **Base giuridica:** legittimo interesse del Titolare (art. 6(1)(f) GDPR), rispettivamente alla funzionalità del servizio e alla prevenzione degli abusi.
* **Destinatari:** Google Firestore (infrastruttura Google Ireland Ltd. / Google LLC). Il communityId viene trasmesso solo quando l'utente, previo consenso, pubblica contenuti o partecipa alla classifica (v. §3.6 e §3.8); l'installId solo all'attivazione di periodi di prova, per il conteggio delle quote o nell'ambito della funzione AI Premium (v. §3.11).
* **Conservazione:** finché l'app resta installata sul dispositivo. L'utente può richiedere la cancellazione di tutti i contenuti associati al proprio communityId in qualsiasi momento (v. §9).

### 3.2 Registrazioni audio dal microfono

* **Cosa viene raccolto:** registrazioni WAV (48 kHz, mono) della durata di pochi secondi, effettuate al momento dell'identificazione di un uccello tramite il canto.
* **Finalità:** identificazione della specie mediante il modello BirdNET 2.4 eseguito interamente sul dispositivo.
* **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR), espresso tramite concessione del permesso microfono al sistema operativo.
* **Destinatari:** **nessuno**. Le registrazioni restano sempre ed esclusivamente sul dispositivo dell'utente. Non vengono trasmesse a server esterni né per l'identificazione né per la condivisione community. L'audio non lascia mai il dispositivo dell'utente.
* **Conservazione:** le registrazioni sono salvate in una cartella temporanea del dispositivo. L'utente può cancellarle in qualsiasi momento tramite il file manager del sistema operativo o reinstallando l'app.

### 3.3 Fotografie da fotocamera o galleria

* **Cosa viene raccolto:** fotografie scattate dalla fotocamera del dispositivo o selezionate dalla galleria dell'utente al fine dell'identificazione.
* **Finalità:** identificazione della specie mediante il modello EfficientNet Birds (AIY V1) eseguito interamente sul dispositivo.
* **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR), espresso tramite concessione dei permessi di fotocamera e/o accesso ai media.
* **Destinatari:** **nessuno per l'identificazione standard**: le fotografie restano sul dispositivo e non vengono trasmesse né per l'identificazione on-device né per la condivisione community. Unica eccezione, su scelta esplicita e azione manuale dell'utente: la funzione facoltativa **AI Premium**, che invia la singola fotografia selezionata al backend per l'analisi, senza conservarla (v. §3.11).
* **Conservazione:** le fotografie restano nella cartella designata dall'utente (galleria o memoria dispositivo), secondo la sua scelta.

### 3.4 Dati di posizione geografica (GPS)

* **Cosa viene raccolto:** coordinate geografiche (latitudine e longitudine) del dispositivo dell'utente al momento di un'osservazione o durante la consultazione di funzionalità che richiedono il contesto geografico (mappe, filtri per regione, suggerimenti di specie locali).
* **Finalità:**
  + filtraggio delle specie visualizzate in base all'area geografica dell'utente;
  + associazione delle osservazioni alla relativa posizione (se l'utente sceglie di salvarle);
  + notifiche di specie rare nelle vicinanze (funzionalità disponibile solo con abbonamento Gold);
  + ricerca di hotspot eBird e osservazioni recenti (solo se l'utente ha configurato la propria chiave API eBird, v. §5.3).
* **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR), espresso tramite concessione del permesso di localizzazione al sistema operativo.
* **Destinatari:**
  + nessun destinatario se l'utente utilizza solo le funzionalità locali;
  + Firebase Firestore se l'utente pubblica un'osservazione nella community (coordinate pubblicate come metadato);
  + GBIF se l'utente consulta mappe di distribuzione (query con coordinate anonime);
  + eBird / Cornell Lab of Ornithology, solo se l'utente ha attivato l'integrazione eBird configurando la propria chiave API personale.
* **Conservazione:** sul dispositivo, a scelta dell'utente (viene conservata insieme al record dell'osservazione nella cronologia locale). Su Firebase Firestore, per le osservazioni pubblicate: finché l'utente non richiede la cancellazione dei propri dati.

### 3.5 Dati di osservazione

* **Cosa viene raccolto:** dettagli testuali delle osservazioni effettuate dall'utente: specie identificata (nome scientifico e comune), confidenza del riconoscimento, timestamp, eventuale posizione geografica. **I media (audio e fotografie) associati all'identificazione restano sempre sul dispositivo e non fanno parte dei dati di osservazione trasmessi al server.**
* **Finalità:** costruzione della cronologia personale dell'utente (disponibile agli abbonati Gold), calcolo di statistiche personali (specie viste, streak giornalieri, badge), condivisione opzionale con la community.
* **Base giuridica:** esecuzione del contratto (art. 6(1)(b) GDPR) per la cronologia personale degli utenti Gold; consenso esplicito (art. 6(1)(a) GDPR) per la condivisione community.
* **Destinatari:** restano sul dispositivo per default; caricati su Firebase Firestore (solo nei campi testuali/numerici, senza media) se l'utente sottoscrive l'abbonamento Gold (cronologia sincronizzata, richiede un account) o condivide con la community.
* **Conservazione:** sul dispositivo finché l'app resta installata; su Firebase Firestore finché l'utente non richiede cancellazione o disdice l'abbonamento Gold.

### 3.6 Dati di utilizzo dell'app

* **Cosa viene raccolto:** statistiche personali non identificative dell'utente: numero di specie osservate, streak di giorni consecutivi di attività, badge guadagnati, preferenze di utilizzo dell'app.
* **Finalità:** gamification e motivazione dell'utente (sistema di badge, livelli, achievement).
* **Base giuridica:** esecuzione del contratto (art. 6(1)(b) GDPR).
* **Destinatari:** memorizzati localmente sul dispositivo. La sincronizzazione su Firebase Firestore avviene solo in due casi: (1) per gli utenti Gold, ai fini dell'accesso multi-dispositivo e della validazione server-side dei badge; (2) per la classifica della community (punteggio e conteggi, associati al communityId), esclusivamente se l'utente ha attivato la condivisione community — consenso revocabile in qualsiasi momento, alla revoca cessano le trasmissioni.
* **Conservazione:** sul dispositivo finché l'app resta installata. Su Firestore: dati Gold finché l'abbonamento è attivo; dati classifica finché l'utente non ne richiede la cancellazione (v. §9).

### 3.7 Dati relativi all'abbonamento Gold

* **Cosa viene raccolto:** stato di abbonamento (attivo / non attivo / periodo di prova), data di scadenza, identificativi di transazione Google Play Billing.
* **Finalità:** erogazione delle funzionalità riservate agli abbonati Gold, verifica server-side della validità dell'abbonamento per prevenire abusi.
* **Base giuridica:** esecuzione del contratto (art. 6(1)(b) GDPR).
* **Destinatari:** Google Play Billing (merchant of record dell'abbonamento) e Firebase Cloud Functions (verifica validità). Birdsoniq **non accede** a dati della carta di pagamento dell'utente: tali dati sono gestiti esclusivamente da Google secondo i propri termini.
* **Conservazione:** finché attivo l'abbonamento; dopo la disdetta, i dati relativi all'ultimo ciclo di fatturazione sono conservati per 10 anni ai fini fiscali e contabili (obbligo legale, art. 2220 c.c.).

### 3.8 Contenuti condivisi con la community (architettura metadata-only)

> **Principio fondamentale — nessun media nel cloud.** La funzione community di Birdsoniq è progettata come servizio "metadata-only": quando l'utente sceglie di condividere un'osservazione, **le fotografie e le registrazioni audio non vengono mai trasmesse al server**. Solo i metadati testuali e numerici dell'osservazione vengono caricati su Firebase Firestore.

* **Cosa viene raccolto:** quando l'utente sceglie esplicitamente di pubblicare un'osservazione nella community (operazione opt-in), i seguenti dati — e **solo** questi — vengono caricati su Firebase Firestore:
  + l'installId dell'utente (identificativo pseudonimo)
  + la specie identificata (nome scientifico e comune)
  + la data e l'ora dell'osservazione
  + le coordinate GPS dell'avvistamento
  + il livello di confidenza del riconoscimento
  + la sorgente dell'identificazione (foto, audio, o combinata)
  + gli eventuali commenti testuali pubblicati dall'utente sulle osservazioni del feed (testo del commento, identificativo pseudonimo dell'autore, data e ora)
* **Cosa NON viene raccolto né trasmesso:**
  + la fotografia eventualmente scattata per l'identificazione;
  + la registrazione audio eventualmente utilizzata per l'identificazione;
  + qualsiasi altro file multimediale presente sul dispositivo.
* **Finalità:** costruzione di un feed comunitario di osservazioni utile alla citizen science e al monitoraggio della biodiversità, senza compromettere la privacy audio/fotografica dell'utente.
* **Base giuridica:** consenso esplicito dell'utente (art. 6(1)(a) GDPR), espresso tramite un dialog informativo che richiede conferma al primo tentativo di condivisione e al quale l'utente può scegliere di dare consenso persistente o revocabile per singola occasione.
* **Destinatari:** altri utenti dell'app che visualizzano il feed community, cui vengono mostrati i metadati dell'osservazione con l'installId pseudonimizzato (non identificativo). Firebase Firestore come infrastruttura di memorizzazione. Firebase Storage **non viene utilizzato** per la community.
* **Conservazione:** fino a richiesta di cancellazione da parte dell'utente. Il consenso può essere revocato in qualsiasi momento dalle Impostazioni Privacy dell'app; la revoca disabilita future condivisioni ma non cancella automaticamente i metadati delle osservazioni già pubblicate (per queste l'utente deve inoltrare richiesta di cancellazione — v. §9).

**Segnalazioni e moderazione.** Se l'utente segnala un contenuto della community (avvistamento o commento), viene registrata su Firebase Firestore una segnalazione contenente: tipo e identificativo del contenuto segnalato, motivo della segnalazione (spam, contenuto inappropriato, molestie, altro), identificativo pseudonimo dell'autore del contenuto (se presente), un identificativo tecnico anonimo del segnalante (generato tramite autenticazione anonima Firebase, privo di dati identificativi) e data e ora. Finalità: moderazione dei contenuti e sicurezza della community. Base giuridica: legittimo interesse del Titolare alla sicurezza del servizio (art. 6(1)(f) GDPR). Le segnalazioni sono conservate per il tempo necessario alla gestione della moderazione.

### 3.9 Chiavi API di servizi esterni (eBird, IUCN)

* **Cosa viene raccolto:** le chiavi API personali che l'utente può facoltativamente inserire nelle impostazioni dell'app per abilitare integrazioni con eBird e IUCN Red List.
* **Finalità:** permettere all'utente di utilizzare la propria chiave API gratuita per accedere a funzionalità aggiuntive (hotspot eBird, stato di conservazione IUCN dettagliato).
* **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR).
* **Destinatari:** le chiavi sono memorizzate esclusivamente sul dispositivo dell'utente, mai trasmesse ai server di Birdsoniq. Quando utilizzate, vengono inviate direttamente al servizio corrispondente (Cornell Lab of Ornithology per eBird; IUCN per la Red List).
* **Conservazione:** sul dispositivo finché l'utente non le rimuove manualmente dalle impostazioni.

### 3.10 Dati dell'account utente (facoltativo)

* **Cosa viene raccolto:** se l'utente sceglie di creare un account — operazione **facoltativa**, non necessaria per l'identificazione delle specie — vengono trattati: l'indirizzo email; le credenziali di autenticazione (gestite da Firebase Authentication: la password non è mai accessibile al Titolare in chiaro); in caso di accesso con Google, l'identificativo dell'account Google e il nome visualizzato forniti dal provider. L'app non raccoglie né utilizza la fotografia del profilo.
* **Finalità:** autenticazione dell'utente; sincronizzazione multi-dispositivo della cronologia e delle statistiche (riservata agli abbonati Gold); funzionalità per strutture (profilo Venue, quote e codici ospite); gestione della lista di utenti bloccati nella community; esercizio semplificato dei diritti GDPR.
* **Base giuridica:** esecuzione del contratto (art. 6(1)(b) GDPR), per le funzionalità richieste dall'utente con la creazione dell'account.
* **Destinatari:** Google Firebase Authentication e Cloud Firestore (Google Ireland Ltd. / Google LLC) come infrastruttura.
* **Conservazione:** finché l'account esiste. L'utente può eliminare l'account **in qualsiasi momento, con effetto immediato e irreversibile**, dall'app (Profilo → Elimina account) oppure inviando una richiesta email dall'indirizzo associato all'account. L'eliminazione cancella l'account di accesso, la cronologia sincronizzata e la Life list cloud, il profilo struttura con quote e codici ospite, e la lista degli utenti bloccati. Restano: i metadati pubblicati nella community (associati all'installId e non all'account — rimovibili su richiesta, v. §9) e i record antiabuso relativi all'eventuale periodo di prova gratuito (associati all'installazione e conservati per legittimo interesse del Titolare alla prevenzione degli abusi, art. 6(1)(f) GDPR). Procedura dettagliata: `https://legal.birdsoniq.app/account_deletion.html`.

### 3.11 Funzione facoltativa "AI Premium" (analisi fotografica cloud)

* **Cosa viene trattato:** se l'utente — titolare di un piano a pagamento e di un account — attiva volontariamente l'analisi AI Premium su una fotografia, vengono trasmessi al backend di Birdsoniq (Cloud Function su Google Cloud, regione europe-west1): la singola fotografia selezionata, le coordinate GPS dell'osservazione (se presenti, per disambiguare specie morfologicamente simili), la lingua dell'app e l'identificativo anti-frode dell'installazione (installId, v. §3.1).
* **Come funziona:** il backend inoltra l'immagine al fornitore del modello di analisi **Anthropic** (v. §5.5), che la elabora e restituisce le specie candidate; l'app mostra il risultato all'utente.
* **Base giuridica e consenso:** consenso esplicito e dedicato dell'utente (art. 6(1)(a) GDPR), richiesto al primo utilizzo e revocabile in qualsiasi momento dalle impostazioni privacy; ogni singolo invio è inoltre avviato manualmente dall'utente.
* **Conservazione:** Birdsoniq **non conserva l'immagine**: viene trattata in memoria per la sola durata dell'analisi e non viene scritta su alcun database o storage del Titolare. Vengono conservati esclusivamente contatori di utilizzo (giornaliero, mensile, annuale) associati all'account, per finalità di erogazione equa del servizio e prevenzione degli abusi. Il fornitore del modello tratta l'immagine secondo i propri termini commerciali, che non ne prevedono l'utilizzo per l'addestramento dei modelli (v. §5.5 e §6).

---

## 4. Base giuridica del trattamento

Come indicato per ciascuna categoria nel paragrafo precedente, le basi giuridiche su cui si fonda il trattamento dei dati sono quelle previste dall'art. 6(1) del GDPR, nello specifico:

* **Consenso (art. 6(1)(a)):** per il trattamento di dati sensibili quali audio e immagini (entrambi restano on-device), posizione, e per la condivisione dei metadati community.
* **Esecuzione del contratto (art. 6(1)(b)):** per le funzionalità essenziali dell'app e per l'erogazione dell'abbonamento Gold.
* **Legittimo interesse (art. 6(1)(f)):** per la generazione dell'installId pseudonimo (necessario a garantire la funzionalità dell'app mantenendo privacy-by-design).
* **Obbligo legale (art. 6(1)(c)):** per la conservazione dei dati contabili relativi alle transazioni.

---

## 5. Destinatari dei dati e servizi di terze parti

Birdsoniq si avvale di alcuni servizi di terze parti per erogare le proprie funzionalità. Di seguito l'elenco completo dei destinatari dei dati trattati.

### 5.1 Servizi Google

**Google Firebase** (Google Ireland Ltd. e Google LLC): infrastruttura di backend dell'app.

* *Cloud Firestore:* archiviazione dei metadati delle osservazioni community, cronologia Gold (metadati testuali), statistiche sincronizzate, record di validazione.
* *Cloud Functions:* verifica server-side della validità dell'abbonamento Gold.
* *Firebase Core:* inizializzazione dei servizi.
* *Firebase Authentication:* gestione degli account utente facoltativi (email/password e accesso con Google), v. §3.10; autenticazione tecnica anonima (senza dati identificativi) per l'invio delle segnalazioni di contenuti, v. §3.8.

Birdsoniq **non utilizza** Firebase Storage (conseguentemente nessun audio né fotografia viene mai caricato su server Firebase), Firebase Analytics, Firebase Crashlytics, Firebase Cloud Messaging, Firebase Remote Config né altri servizi di analisi o profilazione di Google.

Privacy policy di riferimento: `https://policies.google.com/privacy`.

**Google Play Billing** (Google Ireland Ltd.): gestione dell'abbonamento Gold. Google agisce come *merchant of record* nell'Unione Europea, il che significa che è Google stessa a gestire integralmente i dati di pagamento degli utenti, la fatturazione e l'IVA. Birdsoniq non accede mai ai dati della carta di credito.

Privacy policy di riferimento: `https://payments.google.com/payments/apis-secure/get_legal_document`.

**Google Translate** (Google LLC): utilizzato per tradurre automaticamente dall'inglese alla lingua dell'utente le descrizioni enciclopediche delle specie provenienti da Wikipedia. Le richieste di traduzione contengono esclusivamente i testi enciclopedici delle specie e non dati personali dell'utente.

Privacy policy di riferimento: `https://policies.google.com/privacy`.

### 5.2 Fonti scientifiche aperte

**GBIF** (Global Biodiversity Information Facility, con sede a Copenaghen, Danimarca): fonte dei dati di distribuzione geografica e frequenza mensile delle specie, accessibile via API pubblica. Quando l'utente consulta mappe di distribuzione, le coordinate vengono trasmesse a GBIF senza identificativi personali.

Privacy policy: `https://www.gbif.org/terms/privacy-policy`.

**iNaturalist** (California Academy of Sciences / National Geographic Society, USA): fonte di fotografie di specie e informazioni tassonomiche, accessibile via API pubblica. Birdsoniq interroga iNaturalist trasmettendo il nome scientifico della specie di interesse, senza dati personali dell'utente e senza inviare fotografie dell'utente. L'app non utilizza servizi di computer vision di iNaturalist: l'identificazione fotografica è interamente on-device.

Privacy policy: `https://www.inaturalist.org/pages/privacy`.

**Wikipedia / Wikimedia Commons** (Wikimedia Foundation, San Francisco, USA): fonte di descrizioni enciclopediche e fotografie di specie in modalità fallback. Birdsoniq accede alle API pubbliche tramite il nome scientifico della specie, senza dati personali dell'utente.

Privacy policy: `https://foundation.wikimedia.org/wiki/Privacy_policy`.

**IUCN Red List** (International Union for Conservation of Nature, con sede in Svizzera; server nel Regno Unito): utilizzato solo se l'utente configura la propria chiave API IUCN gratuita, per ottenere lo stato di conservazione aggiornato delle specie. Trasmette il nome scientifico.

Privacy policy: `https://www.iucnredlist.org/privacy`.

**Xeno-canto** (Stichting Xeno-canto voor Geluiden van Vogels, con sede in Paesi Bassi): fonte di registrazioni audio di canti e richiami di uccelli, accessibile via API pubblica. Birdsoniq trasmette il nome scientifico della specie. Le registrazioni vengono riprodotte in streaming diretto dai server di Xeno-canto senza essere scaricate, modificate o archiviate.

Termini d'uso: `https://xeno-canto.org/about/terms`.

### 5.3 Integrazione eBird (opt-in)

**eBird** (Cornell Lab of Ornithology, Cornell University, Ithaca, NY, USA): integrazione **opzionale** che l'utente può attivare inserendo nelle impostazioni dell'app la propria chiave API personale eBird (ottenibile gratuitamente previa registrazione su `https://ebird.org/api/keygen`).

Quando l'utente attiva l'integrazione, le seguenti informazioni vengono trasmesse ai server eBird:

* coordinate GPS del dispositivo (per la ricerca di hotspot e osservazioni notevoli nelle vicinanze);
* la chiave API personale dell'utente;
* il nome scientifico delle specie di interesse.

In assenza di chiave API configurata, **nessun dato viene trasmesso** a eBird. La chiave API configurata si può rimuovere in qualsiasi momento dalle impostazioni, disattivando l'integrazione.

Privacy policy: `https://www.birds.cornell.edu/home/privacy/`.

### 5.4 Esportazione verso eBird (funzione locale)

Birdsoniq offre una funzionalità di esportazione delle osservazioni nel formato "eBird Record Format". Tale esportazione produce esclusivamente un file CSV salvato nella memoria del dispositivo dell'utente. Il file può essere successivamente caricato dall'utente in modo autonomo su `ebird.org/import` o condiviso tramite qualsiasi canale scelga. **Birdsoniq non effettua alcun caricamento automatico verso eBird** nell'ambito di questa funzionalità.

---

### 5.5 Anthropic (funzione AI Premium)

Per la sola funzione facoltativa AI Premium (§3.11), il backend di Birdsoniq inoltra la fotografia e gli eventuali dati di contesto (coordinate, lingua) ad **Anthropic PBC** (Stati Uniti), fornitore del modello di analisi, che agisce quale fornitore di servizi per conto del Titolare. Secondo i termini commerciali del fornitore, i dati inviati tramite API non vengono utilizzati per l'addestramento dei modelli. Per le garanzie sul trasferimento extra-UE v. §6.

---

## 6. Trasferimenti di dati extra-UE

Alcuni dei destinatari elencati al §5 si trovano al di fuori dello Spazio Economico Europeo. Di seguito la tabella dei trasferimenti extra-UE e le garanzie adottate per ciascuno:

| Destinatario | Paese | Garanzia ex art. 46 GDPR |
| --- | --- | --- |
| Google Ireland Ltd. | Irlanda (UE) | — |
| Google LLC | Stati Uniti | Standard Contractual Clauses (SCC) + Data Privacy Framework |
| iNaturalist | Stati Uniti | Standard Contractual Clauses equivalenti (policy pubblica) |
| Wikimedia Foundation | Stati Uniti | Adesione pubblica al Data Privacy Framework |
| IUCN / server UK | Svizzera / Regno Unito | Decisioni di adeguatezza della Commissione UE |
| Xeno-canto | Paesi Bassi (UE) | — |
| Cornell Lab of Ornithology | Stati Uniti | Trasferimento su iniziativa dell'utente (art. 49(1)(a) GDPR) |
| GBIF | Danimarca (UE) | — |
| Anthropic PBC | Stati Uniti | Standard Contractual Clauses (SCC); solo funzione facoltativa AI Premium, su azione volontaria dell'utente (§3.11) |

Per quanto riguarda i trasferimenti negli Stati Uniti, le garanzie si basano sulla Decisione di adeguatezza 2023/1795 della Commissione Europea relativa al *EU-US Data Privacy Framework*, eventualmente integrata dalle Standard Contractual Clauses (SCC) ove applicabili.

---

## 7. Durata di conservazione

| Categoria di dati | Durata di conservazione |
| --- | --- |
| communityId | Finché l'app resta installata; contenuti associati cancellabili su richiesta (v. §9) |
| installId (SSAID, anti-frode) | Finché l'app resta installata |
| Registrazioni audio | Sul dispositivo (cartella temporanea), finché l'utente non le elimina. **Non vengono mai trasmesse a server esterni.** |
| Fotografie | Sul dispositivo, a discrezione dell'utente. **Non trasmesse a server esterni**, salvo invio volontario della singola foto alla funzione AI Premium, che non la conserva (v. §3.11). |
| Coordinate GPS (non pubblicate) | Sul dispositivo finché non cancellate dall'utente |
| Metadati osservazioni e commenti community pubblicati | Finché l'utente non ne richiede la cancellazione |
| Segnalazioni di contenuti | Per il tempo necessario alla gestione della moderazione |
| Cronologia osservazioni (metadati) | Finché l'abbonamento Gold è attivo |
| Dati abbonamento attivi | Per la durata dell'abbonamento |
| Dati contabili abbonamento | 10 anni dalla disdetta (obbligo legale) |
| Chiavi API esterne | Finché l'utente non le rimuove |
| Dati account (email, identificativi di accesso) | Finché l'account esiste; eliminazione immediata dall'app o su richiesta email (v. §3.10) |
| Record antiabuso del periodo di prova | Associati all'installazione; conservati anche dopo l'eliminazione dell'account (legittimo interesse) |
| Contatori di utilizzo AI Premium | Associati all'account, per erogazione equa del servizio e prevenzione abusi |

---

## 8. Diritti dell'interessato

L'utente ha il diritto, in qualunque momento, di esercitare i diritti riconosciuti dagli articoli da 15 a 22 del GDPR, tra cui:

* **Diritto di accesso (art. 15):** ottenere conferma del trattamento dei propri dati e, in tal caso, accesso a tali dati e alle informazioni sul trattamento.
* **Diritto di rettifica (art. 16):** ottenere la rettifica di dati inesatti o incompleti.
* **Diritto alla cancellazione (art. 17):** ottenere la cancellazione dei propri dati personali.
* **Diritto alla limitazione del trattamento (art. 18):** ottenere la limitazione del trattamento dei propri dati in determinate circostanze.
* **Diritto alla portabilità dei dati (art. 20):** ricevere i propri dati in formato strutturato, di uso comune e leggibile da dispositivo automatico.
* **Diritto di opposizione (art. 21):** opporsi al trattamento dei propri dati.
* **Diritto di revoca del consenso (art. 7.3):** revocare in qualsiasi momento il consenso precedentemente prestato, senza che ciò pregiudichi la liceità del trattamento effettuato prima della revoca.

---

## 9. Come esercitare i diritti

Per esercitare uno qualsiasi dei diritti elencati al §8, l'utente può inviare una richiesta all'indirizzo email:

**privacy@birdsoniq.app**

indicando nell'oggetto della mail "Richiesta GDPR — [tipo di diritto]" (ad esempio: "Richiesta GDPR — cancellazione").

**Utenti con account.** L'utente che ha creato un account può eliminarlo direttamente dall'app (Profilo → Elimina account), con effetto immediato e irreversibile, oppure inviare la richiesta dall'indirizzo email associato all'account (necessario per verificare l'identità del richiedente). Procedura dettagliata: `https://legal.birdsoniq.app/account_deletion.html` e §3.10.

**Procedura per utenti senza account.** Per i dati non associati a un account (contenuti community e dati legati all'installazione), Birdsoniq non dispone di alcun dato identificativo diretto dell'utente: per identificare i dati associati a una specifica installazione è necessario che l'utente fornisca il proprio **communityId**. Per visualizzarlo, l'utente può aprire l'app e accedere al menu *Impostazioni → Informazioni Legali → Il mio identificativo anonimo*. Questo identificativo è l'unico elemento che collega l'utente ai contenuti pubblicati nella community e alla relativa classifica.

**Tempi di risposta.** Il Titolare risponde alle richieste entro **30 giorni** dalla ricezione della richiesta completa, nel rispetto dell'art. 12(3) GDPR. In casi di particolare complessità, tale termine può essere prorogato di altri 60 giorni, con comunicazione motivata all'utente.

**Verifica dell'identità.** Il Titolare potrà richiedere informazioni aggiuntive per verificare l'identità del richiedente, quando ciò sia necessario a prevenire accessi non autorizzati ai dati di altri utenti.

---

## 10. Reclamo all'autorità di controllo

L'utente ha in ogni caso il diritto di proporre reclamo all'autorità di controllo competente, in Italia individuata nel:

**Garante per la Protezione dei Dati Personali**
Piazza Venezia 11, 00187 Roma
Email: `protocollo@gpdp.it`
Sito web: `https://www.garanteprivacy.it`

---

## 11. Sicurezza dei dati

I dati trattati da Birdsoniq sono protetti tramite:

* **Cifratura in transito:** tutte le comunicazioni tra l'app e i server (Firebase, servizi terzi) avvengono tramite protocollo HTTPS / TLS 1.2 o superiore.
* **Pseudonimizzazione:** l'identificativo utente è un UUID casuale, non un dato identificativo diretto.
* **Minimizzazione:** vengono raccolti esclusivamente i dati strettamente necessari alle funzionalità dichiarate. In particolare, audio e fotografie non lasciano mai il dispositivo: il principale vettore di rischio per la privacy è stato così eliminato alla radice.
* **Security rules Firebase:** l'accesso ai dati su Firestore è regolato da regole di sicurezza che limitano la lettura e scrittura ai soli casi legittimi e vincolano il formato dei dati caricabili.
* **Nessuna vendita a terzi:** i dati degli utenti non sono mai venduti, ceduti o trasferiti a terzi per finalità commerciali o pubblicitarie.

Nonostante le misure adottate, nessun sistema informatico è sicuro al 100%. In caso di violazione dei dati personali che possa comportare un rischio elevato per i diritti e le libertà dell'utente, il Titolare provvederà a notificare l'evento all'utente e al Garante Privacy nei termini previsti dagli articoli 33 e 34 del GDPR (entro 72 ore dalla conoscenza della violazione).

---

## 12. Utenti minori di età

L'app Birdsoniq è destinata a utenti di età pari o superiore a **16 anni**. L'installazione e l'utilizzo dell'app sono vietati ai minori di 16 anni.

L'app include una modalità denominata "Kids" che fornisce un'interfaccia semplificata con elementi visivi adatti a un contesto familiare o educativo. Tuttavia, tale modalità è pensata per essere utilizzata da persone di qualsiasi età **purché tutte di età pari o superiore a 16 anni**. La modalità Kids **non raccoglie né trasmette alcun dato aggiuntivo** rispetto alla modalità standard.

Il Titolare non raccoglie consapevolmente dati personali di minori di 16 anni. Qualora venisse a conoscenza che dati relativi a un minore di 16 anni sono stati trattati senza consenso genitoriale valido, provvederà tempestivamente a cancellarli. I genitori o tutori che ritenessero che il figlio minore abbia utilizzato l'app possono contattare il Titolare all'indirizzo email indicato nel §9 per richiedere la cancellazione dei dati.

---

## 13. Cookie e tecnologie simili

L'**app Birdsoniq non utilizza cookie** né tecnologie analoghe a scopo di tracciamento. Le preferenze dell'utente sono memorizzate localmente sul dispositivo tramite il meccanismo nativo di SharedPreferences di Android, che non costituisce un cookie ai sensi della normativa ePrivacy.

Il sito web `birdsoniq.app` (dove è pubblicata la presente Privacy Policy) può utilizzare esclusivamente cookie tecnici essenziali al funzionamento del sito, per i quali non è richiesto consenso ai sensi dell'art. 122 del Codice Privacy italiano.

---

## 14. Modifiche alla Privacy Policy

Il Titolare si riserva il diritto di modificare la presente Privacy Policy in qualsiasi momento, per riflettere cambiamenti nelle funzionalità dell'app, nei servizi di terze parti integrati, o nella normativa applicabile.

Le modifiche entrano in vigore al momento della pubblicazione della nuova versione del documento. La data dell'ultimo aggiornamento è indicata in cima al documento.

**Modifiche sostanziali** (ad esempio: nuove categorie di dati raccolti, nuovi destinatari, modifica delle finalità di trattamento) saranno comunicate all'utente tramite un avviso in-app al successivo avvio dell'app, dando all'utente la possibilità di revisionare la nuova versione.

**Storico delle versioni.** Tutte le versioni precedenti della Privacy Policy sono pubblicamente consultabili sul repository git del documento: `https://github.com/giovannisecci/birdsoniq-legal`. Ciascuna versione è identificata dal proprio commit git con hash crittografico e data verificabile.

**Principali modifiche nella versione 1.4 (4 giugno 2026):** separati gli identificativi pseudonimi (communityId per i contenuti community, installId/SSAID confinato alla prevenzione frodi — §3.1, §3.6, §7, §9); la sincronizzazione della classifica community è ora subordinata al consenso esplicito dell'utente (§3.6); documentata la funzione facoltativa AI Premium di analisi fotografica cloud: nuove §3.11 e §5.5 (Anthropic), aggiornati §2, §3.3, §6 e §7.

**Principali modifiche nella versione 1.3 (4 giugno 2026):** recepita l'introduzione degli account utente facoltativi (Firebase Authentication: email/password e accesso Google) e della funzione di eliminazione account in-app. Aggiunta la sezione §3.10 (dati dell'account utente); aggiornati §2 (da "nessun account utente" ad "account facoltativo"), §3.5, §3.8 (commenti e segnalazioni di contenuti), §5.1, §7 e §9; pubblicata la pagina dedicata `https://legal.birdsoniq.app/account_deletion.html`.

**Principali modifiche nella versione 1.2 (2 giugno 2026):** aggiornati gli indirizzi email di contatto del Titolare all'indirizzo definitivo sul dominio (privacy@birdsoniq.app) e i link ai documenti al dominio `legal.birdsoniq.app`, a seguito dell'attivazione del dominio `birdsoniq.app`. Rimossa la nota sugli indirizzi email provvisori (§1).

**Principali modifiche nella versione 1.1 (19 aprile 2026):** aggiornamento per riflettere il passaggio a un'architettura community "metadata-only". Audio e fotografie dell'utente non vengono più trasmessi a Firebase Storage: restano sempre ed esclusivamente sul dispositivo. Sezioni aggiornate: §2, §3.2, §3.3, §3.5, §3.8, §5.1, §7, §11.

---

## 15. Fonti dei dati mostrati nell'app e relative attribuzioni

Birdsoniq integra dati, testi, immagini e registrazioni audio forniti da progetti scientifici e di citizen science di terze parti, ciascuno sotto la propria licenza. In questa sezione sono indicate le fonti utilizzate e le modalità d'uso, in conformità con le rispettive licenze.

**Registrazioni audio — Xeno-canto.** L'app riproduce registrazioni di canti e richiami di uccelli ospitate sulla piattaforma Xeno-canto, fornite dai suoi contributori sotto licenze Creative Commons (CC BY o CC BY-SA; sono escluse le registrazioni con clausola Non-Commercial). Le registrazioni vengono riprodotte in streaming diretto dai server di Xeno-canto senza essere scaricate, modificate o archiviate localmente. Per ciascuna registrazione Birdsoniq mostra l'attribuzione richiesta (autore, identificativo Xeno-canto, licenza specifica) con link alla pagina originale.

**Dati di osservazione — GBIF.** I dati di distribuzione geografica e frequenza mensile delle specie sono ottenuti tramite le API di GBIF sotto licenza Creative Commons Attribution 4.0 (CC BY 4.0) o Public Domain (CC0). I pacchetti offline includono esclusivamente dati CC BY 4.0 e CC0.

**Foto e tassonomia — iNaturalist.** Le fotografie delle specie e parte delle informazioni tassonomiche sono ottenute dalle API di iNaturalist. Ciascuna foto mantiene l'attribuzione fornita dalla piattaforma (autore, licenza, link alla foto originale).

**Foto di fallback e descrizioni — Wikipedia / Wikimedia Commons.** Quando non disponibili tramite iNaturalist, le foto di copertina e le descrizioni enciclopediche sono ottenute dalle API di Wikipedia. I contenuti sono distribuiti sotto licenza Creative Commons Attribution-ShareAlike (CC BY-SA); l'attribuzione nell'app rimanda alla pagina Wikipedia di origine.

**Stato di conservazione — IUCN Red List.** Lo stato di conservazione delle specie è ottenuto tramite l'API IUCN Red List v4 (con chiave API configurata dall'utente).

**Servizio di traduzione.** Le descrizioni in lingue diverse dall'inglese sono ottenute tramite Google Translate. Birdsoniq non è responsabile dell'accuratezza delle traduzioni automatiche.

**Niente ridistribuzione.** Birdsoniq non redistribuisce i contenuti di terze parti a soggetti diversi dall'utente finale che utilizza l'app. L'app non espone endpoint pubblici, non pubblica archivi, non condivide i dati con inserzionisti.

**Segnalazioni.** Se sei l'autore di una registrazione, fotografia o altro contenuto mostrato nell'app e ritieni che l'uso non sia conforme alla licenza applicabile, puoi contattare Birdsoniq all'indirizzo email indicato nel §16 e valuteremo tempestivamente la segnalazione, inclusa la rimozione del contenuto se opportuno.

---

## 16. Contatti

**Titolare del trattamento:** Giovanni Secci
**Indirizzo:** Via Baccarini, 08100 Nuoro (NU), Italia
**Email (privacy, copyright, supporto):** privacy@birdsoniq.app
**Partita IVA:** [IT\_\_**\_\_**\_\_ — in corso di attivazione]

Per qualsiasi questione relativa alla presente Privacy Policy o al trattamento dei propri dati, l'utente può scrivere all'indirizzo email sopra indicato. Il Titolare si impegna a rispondere nei tempi previsti dalla normativa applicabile.

---

*Fine del documento.*
