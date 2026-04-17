---
layout: default
title: Privacy Policy — Birdsoniq (IT)
description: Informativa privacy di Birdsoniq ai sensi del Regolamento UE 2016/679 (GDPR).
lang: it
---

# Privacy Policy — Birdsoniq

**Ultimo aggiornamento:** [DA COMPILARE ALLA PRIMA PUBBLICAZIONE]
**Versione documento:** 1.0

> Lo storico completo delle modifiche a questa Privacy Policy è pubblicamente consultabile sul repository git del documento: `https://github.com/giovannisecci/birdsoniq-legal`. Ogni versione precedente resta verificabile e scaricabile.

---

## 1. Premesse e identità del Titolare del trattamento

La presente Privacy Policy descrive le modalità con cui **Birdsoniq** (di seguito "l'app") raccoglie, utilizza, conserva e condivide i dati personali degli utenti. L'informativa è redatta in conformità al Regolamento UE 2016/679 ("GDPR"), al Decreto Legislativo 196/2003 (Codice Privacy italiano come modificato dal D.Lgs. 101/2018) e alle linee guida del Garante per la Protezione dei Dati Personali.

**Titolare del trattamento**

- **Nome:** Giovanni Secci
- **Indirizzo:** Via Baccarini, 08100 Nuoro (NU), Italia
- **Partita IVA:** [IT__________ — in corso di attivazione alla data di prima pubblicazione]
- **Email per questioni privacy:** giovannisecci72@gmail.com
- **Email per supporto generale:** giovannisecci72@gmail.com

> **Nota sugli indirizzi email:** gli indirizzi sopra indicati sono provvisori e saranno sostituiti con indirizzi sul dominio `birdsoniq.app` non appena il dominio sarà attivo. Gli aggiornamenti verranno pubblicati in una nuova versione di questo documento.

**Accettazione**

Scaricando, installando o utilizzando Birdsoniq, l'utente prende atto della presente informativa. Qualora l'utente non concordi con le modalità descritte, può scegliere di non utilizzare l'app e disinstallarla dal proprio dispositivo.

---

## 2. Principi generali e approccio "privacy by design"

Birdsoniq è progettata secondo il principio della **minimizzazione dei dati**: raccoglie esclusivamente le informazioni strettamente necessarie a fornire le funzionalità richieste dall'utente e nella quantità minima indispensabile.

Caratteristiche chiave dell'approccio adottato:

- **Nessun account utente.** L'app non richiede registrazione, login, email o password. Non viene raccolto alcun dato identificativo diretto dell'utente.
- **Identificazione on-device.** I modelli di intelligenza artificiale per l'identificazione di uccelli tramite foto e audio girano interamente sul dispositivo dell'utente. Le registrazioni audio e le fotografie non vengono mai trasmesse a server esterni per l'identificazione.
- **Condivisione community opt-in.** La pubblicazione di osservazioni nel feed community richiede il consenso esplicito dell'utente, richiesto tramite un dialog informativo al primo tentativo di condivisione.
- **Nessuna pubblicità, nessun tracker.** L'app non integra SDK pubblicitari, servizi di analisi comportamentale, strumenti di profilazione o tracker di terze parti.

---

## 3. Categorie di dati trattati

Di seguito l'elenco dettagliato delle categorie di dati che Birdsoniq tratta, con indicazione per ciascuna di finalità, base giuridica, destinatari e tempi di conservazione.

### 3.1 Identificativo anonimo di installazione

- **Cosa viene raccolto:** un identificativo univoco generato casualmente al primo avvio dell'app (UUID v4, denominato "installId"), memorizzato sul dispositivo dell'utente nelle preferenze locali.
- **Finalità:** consentire all'utente di esercitare i diritti GDPR (in particolare cancellazione) senza la necessità di un account; identificare pseudonimamente i contenuti pubblicati nella community.
- **Base giuridica:** legittimo interesse del Titolare a garantire la funzionalità dell'app e la possibilità di esercitare i diritti degli interessati (art. 6(1)(f) GDPR).
- **Destinatari:** Google Firestore (infrastruttura Google Ireland Ltd. / Google LLC) quando l'utente pubblica contenuti community o attiva l'abbonamento Gold.
- **Conservazione:** finché l'app resta installata sul dispositivo. L'utente può richiedere la cancellazione di tutti i contenuti associati al proprio installId in qualsiasi momento (v. §9).

### 3.2 Registrazioni audio dal microfono

- **Cosa viene raccolto:** registrazioni WAV (48 kHz, mono) della durata di pochi secondi, effettuate al momento dell'identificazione di un uccello tramite il canto.
- **Finalità:** identificazione della specie mediante il modello BirdNET 2.4 eseguito interamente sul dispositivo.
- **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR), espresso tramite concessione del permesso microfono al sistema operativo.
- **Destinatari:** **nessuno**. Le registrazioni restano esclusivamente sul dispositivo dell'utente. Non vengono trasmesse a server esterni per l'identificazione.
- **Conservazione:** le registrazioni sono salvate in una cartella temporanea del dispositivo. L'utente può cancellarle in qualsiasi momento. Solo se l'utente decide esplicitamente di condividere l'osservazione con la community, l'audio viene caricato su Firebase Storage (v. §3.8).

### 3.3 Fotografie da fotocamera o galleria

- **Cosa viene raccolto:** fotografie scattate dalla fotocamera del dispositivo o selezionate dalla galleria dell'utente al fine dell'identificazione.
- **Finalità:** identificazione della specie mediante il modello EfficientNet Birds eseguito interamente sul dispositivo.
- **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR), espresso tramite concessione dei permessi di fotocamera e/o accesso ai media.
- **Destinatari:** **nessuno**. Le fotografie restano esclusivamente sul dispositivo. Non vengono trasmesse a server esterni per l'identificazione.
- **Conservazione:** le fotografie restano nella cartella designata dall'utente (galleria o memoria dispositivo). Solo se l'utente decide esplicitamente di condividere l'osservazione con la community, la foto viene caricata su Firebase Storage (v. §3.8).

### 3.4 Dati di posizione geografica (GPS)

- **Cosa viene raccolto:** coordinate geografiche (latitudine e longitudine) del dispositivo dell'utente al momento di un'osservazione o durante la consultazione di funzionalità che richiedono il contesto geografico (mappe, filtri per regione, suggerimenti di specie locali).
- **Finalità:**
    - filtraggio delle specie visualizzate in base all'area geografica dell'utente;
    - associazione delle osservazioni alla relativa posizione (se l'utente sceglie di salvarle);
    - notifiche di specie rare nelle vicinanze (funzionalità disponibile solo con abbonamento Gold);
    - ricerca di hotspot eBird e osservazioni recenti (solo se l'utente ha configurato la propria chiave API eBird, v. §5.3).
- **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR), espresso tramite concessione del permesso di localizzazione al sistema operativo.
- **Destinatari:**
    - nessun destinatario se l'utente utilizza solo le funzionalità locali;
    - Firebase Firestore se l'utente pubblica un'osservazione nella community;
    - GBIF se l'utente consulta mappe di distribuzione (query con coordinate anonime);
    - eBird / Cornell Lab of Ornithology, solo se l'utente ha attivato l'integrazione eBird configurando la propria chiave API personale.
- **Conservazione:** sul dispositivo, a scelta dell'utente (viene conservata insieme al record dell'osservazione nella cronologia locale). Su Firebase Firestore, per le osservazioni pubblicate: finché l'utente non richiede la cancellazione dei propri dati.

### 3.5 Dati di osservazione

- **Cosa viene raccolto:** dettagli delle osservazioni effettuate dall'utente: specie identificata, confidenza del riconoscimento, timestamp, eventuale posizione geografica, eventuale foto o audio associati.
- **Finalità:** costruzione della cronologia personale dell'utente (disponibile agli abbonati Gold), calcolo di statistiche personali (specie viste, streak giornalieri, badge), condivisione opzionale con la community.
- **Base giuridica:** esecuzione del contratto (art. 6(1)(b) GDPR) per la cronologia personale degli utenti Gold; consenso esplicito (art. 6(1)(a) GDPR) per la condivisione community.
- **Destinatari:** restano sul dispositivo per default; caricati su Firebase Firestore solo se l'utente sottoscrive l'abbonamento Gold (cronologia sincronizzata) o condivide con la community.
- **Conservazione:** sul dispositivo finché l'app resta installata; su Firebase Firestore finché l'utente non richiede cancellazione o disdice l'abbonamento Gold.

### 3.6 Dati di utilizzo dell'app

- **Cosa viene raccolto:** statistiche personali non identificative dell'utente: numero di specie osservate, streak di giorni consecutivi di attività, badge guadagnati, preferenze di utilizzo dell'app.
- **Finalità:** gamification e motivazione dell'utente (sistema di badge, livelli, achievement).
- **Base giuridica:** esecuzione del contratto (art. 6(1)(b) GDPR).
- **Destinatari:** memorizzati localmente sul dispositivo; per utenti Gold, sincronizzati su Firebase Firestore per permettere l'accesso da più dispositivi e la validazione server-side dei badge.
- **Conservazione:** sul dispositivo finché l'app resta installata. Su Firestore finché attivo l'abbonamento Gold.

### 3.7 Dati relativi all'abbonamento Gold

- **Cosa viene raccolto:** stato di abbonamento (attivo / non attivo / periodo di prova), data di scadenza, identificativi di transazione Google Play Billing.
- **Finalità:** erogazione delle funzionalità riservate agli abbonati Gold, verifica server-side della validità dell'abbonamento per prevenire abusi.
- **Base giuridica:** esecuzione del contratto (art. 6(1)(b) GDPR).
- **Destinatari:** Google Play Billing (merchant of record dell'abbonamento) e Firebase Cloud Functions (verifica validità). Birdsoniq **non accede** a dati della carta di pagamento dell'utente: tali dati sono gestiti esclusivamente da Google secondo i propri termini.
- **Conservazione:** finché attivo l'abbonamento; dopo la disdetta, i dati relativi all'ultimo ciclo di fatturazione sono conservati per 10 anni ai fini fiscali e contabili (obbligo legale, art. 2220 c.c.).

### 3.8 Contenuti condivisi con la community

- **Cosa viene raccolto:** quando l'utente sceglie esplicitamente di pubblicare un'osservazione nella community (operazione opt-in), i seguenti dati vengono caricati su Firebase Firestore e Firebase Storage:
    - l'installId dell'utente (identificativo pseudonimo)
    - la specie identificata (nome scientifico e comune)
    - la data e l'ora dell'osservazione
    - le coordinate GPS dell'avvistamento
    - eventuale fotografia scattata
    - eventuale registrazione audio effettuata
- **Finalità:** costruzione di un feed comunitario di osservazioni scientifiche utili alla citizen science e al monitoraggio della biodiversità.
- **Base giuridica:** consenso esplicito dell'utente (art. 6(1)(a) GDPR), espresso tramite un dialog informativo che richiede conferma al primo tentativo di condivisione e al quale l'utente può scegliere di dare consenso persistente o revocabile per singola occasione.
- **Destinatari:** altri utenti dell'app che visualizzano il feed community, cui vengono mostrate le osservazioni con l'installId pseudonimizzato (non identificativo). Firebase Firestore e Firebase Storage come infrastruttura di memorizzazione.
- **Conservazione:** fino a richiesta di cancellazione da parte dell'utente. Il consenso può essere revocato in qualsiasi momento dalle Impostazioni Privacy dell'app; la revoca disabilita future condivisioni ma non cancella automaticamente le osservazioni già pubblicate (per queste l'utente deve inoltrare richiesta di cancellazione — v. §9).

### 3.9 Chiavi API di servizi esterni (eBird, IUCN)

- **Cosa viene raccolto:** le chiavi API personali che l'utente può facoltativamente inserire nelle impostazioni dell'app per abilitare integrazioni con eBird e IUCN Red List.
- **Finalità:** permettere all'utente di utilizzare la propria chiave API gratuita per accedere a funzionalità aggiuntive (hotspot eBird, stato di conservazione IUCN dettagliato).
- **Base giuridica:** consenso dell'utente (art. 6(1)(a) GDPR).
- **Destinatari:** le chiavi sono memorizzate esclusivamente sul dispositivo dell'utente, mai trasmesse ai server di Birdsoniq. Quando utilizzate, vengono inviate direttamente al servizio corrispondente (Cornell Lab of Ornithology per eBird; IUCN per la Red List).
- **Conservazione:** sul dispositivo finché l'utente non le rimuove manualmente dalle impostazioni.

---

## 4. Base giuridica del trattamento

Come indicato per ciascuna categoria nel paragrafo precedente, le basi giuridiche su cui si fonda il trattamento dei dati sono quelle previste dall'art. 6(1) del GDPR, nello specifico:

- **Consenso (art. 6(1)(a)):** per il trattamento di dati sensibili quali audio, immagini, posizione e per la condivisione community.
- **Esecuzione del contratto (art. 6(1)(b)):** per le funzionalità essenziali dell'app e per l'erogazione dell'abbonamento Gold.
- **Legittimo interesse (art. 6(1)(f)):** per la generazione dell'installId pseudonimo (necessario a garantire la funzionalità dell'app mantenendo privacy-by-design).
- **Obbligo legale (art. 6(1)(c)):** per la conservazione dei dati contabili relativi alle transazioni.

---

## 5. Destinatari dei dati e servizi di terze parti

Birdsoniq si avvale di alcuni servizi di terze parti per erogare le proprie funzionalità. Di seguito l'elenco completo dei destinatari dei dati trattati.

### 5.1 Servizi Google

**Google Firebase** (Google Ireland Ltd. e Google LLC): infrastruttura di backend dell'app.

- *Cloud Firestore:* archiviazione di osservazioni community, cronologia Gold, statistiche sincronizzate, record di validazione.
- *Firebase Storage:* archiviazione di foto e audio condivisi con la community.
- *Cloud Functions:* verifica server-side della validità dell'abbonamento Gold.
- *Firebase Core:* inizializzazione dei servizi.

Birdsoniq **non utilizza** Firebase Authentication, Firebase Analytics, Firebase Crashlytics, Firebase Cloud Messaging, Firebase Remote Config né altri servizi di analisi o profilazione di Google.

Privacy policy di riferimento: `https://policies.google.com/privacy`.

**Google Play Billing** (Google Ireland Ltd.): gestione dell'abbonamento Gold. Google agisce come *merchant of record* nell'Unione Europea, il che significa che è Google stessa a gestire integralmente i dati di pagamento degli utenti, la fatturazione e l'IVA. Birdsoniq non accede mai ai dati della carta di credito.

Privacy policy di riferimento: `https://payments.google.com/payments/apis-secure/get_legal_document`.

**Google Translate** (Google LLC): utilizzato per tradurre automaticamente dall'inglese alla lingua dell'utente le descrizioni enciclopediche delle specie provenienti da Wikipedia. Le richieste di traduzione contengono esclusivamente i testi enciclopedici delle specie e non dati personali dell'utente.

Privacy policy di riferimento: `https://policies.google.com/privacy`.

### 5.2 Fonti scientifiche aperte

**GBIF** (Global Biodiversity Information Facility, con sede a Copenaghen, Danimarca): fonte dei dati di distribuzione geografica e frequenza mensile delle specie, accessibile via API pubblica. Quando l'utente consulta mappe di distribuzione, le coordinate vengono trasmesse a GBIF senza identificativi personali.

Privacy policy: `https://www.gbif.org/terms/privacy-policy`.

**iNaturalist** (California Academy of Sciences / National Geographic Society, USA): fonte di fotografie di specie e informazioni tassonomiche, accessibile via API pubblica. Birdsoniq interroga iNaturalist trasmettendo il nome scientifico della specie di interesse, senza dati personali dell'utente.

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

- coordinate GPS del dispositivo (per la ricerca di hotspot e osservazioni notevoli nelle vicinanze);
- la chiave API personale dell'utente;
- il nome scientifico delle specie di interesse.

In assenza di chiave API configurata, **nessun dato viene trasmesso** a eBird. La chiave API configurata si può rimuovere in qualsiasi momento dalle impostazioni, disattivando l'integrazione.

Privacy policy: `https://www.birds.cornell.edu/home/privacy/`.

### 5.4 Esportazione verso eBird (funzione locale)

Birdsoniq offre una funzionalità di esportazione delle osservazioni nel formato "eBird Record Format". Tale esportazione produce esclusivamente un file CSV salvato nella memoria del dispositivo dell'utente. Il file può essere successivamente caricato dall'utente in modo autonomo su `ebird.org/import` o condiviso tramite qualsiasi canale scelga. **Birdsoniq non effettua alcun caricamento automatico verso eBird** nell'ambito di questa funzionalità.

---

## 6. Trasferimenti di dati extra-UE

Alcuni dei destinatari elencati al §5 si trovano al di fuori dello Spazio Economico Europeo. Di seguito la tabella dei trasferimenti extra-UE e le garanzie adottate per ciascuno:

| Destinatario | Paese | Garanzia ex art. 46 GDPR |
|---|---|---|
| Google Ireland Ltd. | Irlanda (UE) | — |
| Google LLC | Stati Uniti | Standard Contractual Clauses (SCC) + Data Privacy Framework |
| iNaturalist | Stati Uniti | Standard Contractual Clauses equivalenti (policy pubblica) |
| Wikimedia Foundation | Stati Uniti | Adesione pubblica al Data Privacy Framework |
| IUCN / server UK | Svizzera / Regno Unito | Decisioni di adeguatezza della Commissione UE |
| Xeno-canto | Paesi Bassi (UE) | — |
| Cornell Lab of Ornithology | Stati Uniti | Trasferimento su iniziativa dell'utente (art. 49(1)(a) GDPR) |
| GBIF | Danimarca (UE) | — |

Per quanto riguarda i trasferimenti negli Stati Uniti, le garanzie si basano sulla Decisione di adeguatezza 2023/1795 della Commissione Europea relativa al *EU-US Data Privacy Framework*, eventualmente integrata dalle Standard Contractual Clauses (SCC) ove applicabili.

---

## 7. Durata di conservazione

| Categoria di dati | Durata di conservazione |
|---|---|
| installId | Finché l'app resta installata |
| Registrazioni audio | Temporanea, finché l'utente non le elimina |
| Fotografie | A discrezione dell'utente (memoria del dispositivo) |
| Coordinate GPS (non pubblicate) | Sul dispositivo finché non cancellate dall'utente |
| Cronologia osservazioni | Finché l'abbonamento Gold è attivo |
| Osservazioni community pubblicate | Finché l'utente non ne richiede la cancellazione |
| Dati abbonamento attivi | Per la durata dell'abbonamento |
| Dati contabili abbonamento | 10 anni dalla disdetta (obbligo legale) |
| Chiavi API esterne | Finché l'utente non le rimuove |

---

## 8. Diritti dell'interessato

L'utente ha il diritto, in qualunque momento, di esercitare i diritti riconosciuti dagli articoli da 15 a 22 del GDPR, tra cui:

- **Diritto di accesso (art. 15):** ottenere conferma del trattamento dei propri dati e, in tal caso, accesso a tali dati e alle informazioni sul trattamento.
- **Diritto di rettifica (art. 16):** ottenere la rettifica di dati inesatti o incompleti.
- **Diritto alla cancellazione (art. 17):** ottenere la cancellazione dei propri dati personali.
- **Diritto alla limitazione del trattamento (art. 18):** ottenere la limitazione del trattamento dei propri dati in determinate circostanze.
- **Diritto alla portabilità dei dati (art. 20):** ricevere i propri dati in formato strutturato, di uso comune e leggibile da dispositivo automatico.
- **Diritto di opposizione (art. 21):** opporsi al trattamento dei propri dati.
- **Diritto di revoca del consenso (art. 7.3):** revocare in qualsiasi momento il consenso precedentemente prestato, senza che ciò pregiudichi la liceità del trattamento effettuato prima della revoca.

---

## 9. Come esercitare i diritti

Per esercitare uno qualsiasi dei diritti elencati al §8, l'utente può inviare una richiesta all'indirizzo email:

**giovannisecci72@gmail.com**

indicando nell'oggetto della mail "Richiesta GDPR — [tipo di diritto]" (ad esempio: "Richiesta GDPR — cancellazione").

**Procedura speciale per utenti senza account.** Poiché Birdsoniq non richiede registrazione né login, non dispone di alcun dato identificativo diretto dell'utente: per identificare i dati associati a una specifica installazione è necessario che l'utente fornisca il proprio **installId**. Per visualizzare il proprio installId, l'utente può aprire l'app, accedere al menu *Impostazioni → Informazioni Legali → Il mio identificativo anonimo*. Questo identificativo è l'unico elemento che collega l'utente ai dati pubblicati nella community o alla cronologia Gold sincronizzata.

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

- **Cifratura in transito:** tutte le comunicazioni tra l'app e i server (Firebase, servizi terzi) avvengono tramite protocollo HTTPS / TLS 1.2 o superiore.
- **Pseudonimizzazione:** l'identificativo utente è un UUID casuale, non un dato identificativo diretto.
- **Minimizzazione:** vengono raccolti esclusivamente i dati strettamente necessari alle funzionalità dichiarate.
- **Security rules Firebase:** l'accesso ai dati su Firestore è regolato da regole di sicurezza che limitano la lettura e scrittura ai soli casi legittimi.
- **Nessuna vendita a terzi:** i dati degli utenti non sono mai venduti, ceduti o trasferiti a terzi per finalità commerciali o pubblicitarie.

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
**Email (privacy, copyright, supporto):** giovannisecci72@gmail.com
**Partita IVA:** [IT__________ — in corso di attivazione]

Per qualsiasi questione relativa alla presente Privacy Policy o al trattamento dei propri dati, l'utente può scrivere all'indirizzo email sopra indicato. Il Titolare si impegna a rispondere nei tempi previsti dalla normativa applicabile.

---

*Fine del documento.*
