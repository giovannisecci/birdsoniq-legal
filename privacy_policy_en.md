---
layout: default
title: Privacy Policy — Birdsoniq (EN)
description: Birdsoniq privacy policy pursuant to EU Regulation 2016/679 (GDPR).
lang: en
---

# Privacy Policy — Birdsoniq

**Last updated:** 17 April 2026
**Document version:** 1.0

> The complete history of modifications to this Privacy Policy is publicly available on the document's git repository: `https://github.com/giovannisecci/birdsoniq-legal`. Each previous version remains verifiable and downloadable.

> **Note on language:** the Italian version of this Privacy Policy (`privacy_policy_it.md`) is the authoritative version for legal purposes. This English version is provided for the convenience of international users. In case of discrepancies between the two versions, the Italian version prevails.

---

## 1. Introduction and identity of the Data Controller

This Privacy Policy describes how **Birdsoniq** (hereinafter "the app") collects, uses, stores and shares users' personal data. The policy is drafted in compliance with Regulation (EU) 2016/679 ("GDPR"), the Italian Legislative Decree 196/2003 (Italian Privacy Code as amended by Legislative Decree 101/2018) and the guidelines of the Italian Data Protection Authority (Garante per la Protezione dei Dati Personali).

**Data Controller**

- **Name:** Giovanni Secci
- **Address:** Via Baccarini, 08100 Nuoro (NU), Italy
- **VAT number:** [IT__________ — pending activation at the date of first publication]
- **Email for privacy matters:** giovannisecci72@gmail.com
- **Email for general support:** giovannisecci72@gmail.com

> **Note on email addresses:** the email addresses indicated above are provisional and will be replaced with addresses on the `birdsoniq.app` domain as soon as the domain becomes active. Updates will be published in a new version of this document.

**Acceptance**

By downloading, installing or using Birdsoniq, the user acknowledges this policy. If the user does not agree with the terms described, they may choose not to use the app and uninstall it from their device.

---

## 2. General principles and "privacy by design" approach

Birdsoniq is designed according to the principle of **data minimization**: it collects exclusively the information strictly necessary to provide the functionalities requested by the user, in the minimum indispensable quantity.

Key features of the adopted approach:

- **No user account.** The app does not require registration, login, email or password. No direct identifying data of the user is collected.
- **On-device identification.** The artificial intelligence models for bird identification via photo and audio run entirely on the user's device. Audio recordings and photographs are never transmitted to external servers for identification purposes.
- **Opt-in community sharing.** Publishing observations in the community feed requires the user's explicit consent, requested via an informative dialog at the first sharing attempt.
- **No advertising, no tracker.** The app does not integrate advertising SDKs, behavioral analytics services, profiling tools or third-party trackers.

---

## 3. Categories of data processed

Below is the detailed list of the categories of data that Birdsoniq processes, with indication for each of purpose, legal basis, recipients and retention periods.

### 3.1 Anonymous installation identifier

- **What is collected:** a randomly generated unique identifier (UUID v4, called "installId") created at the first launch of the app and stored on the user's device in local preferences.
- **Purpose:** to allow the user to exercise GDPR rights (in particular deletion) without the need for an account; to identify content published in the community in a pseudonymous manner.
- **Legal basis:** legitimate interest of the Data Controller in ensuring the functionality of the app and the possibility of exercising the rights of data subjects (art. 6(1)(f) GDPR).
- **Recipients:** Google Firestore (Google Ireland Ltd. / Google LLC infrastructure) when the user publishes community content or activates the Gold subscription.
- **Retention:** as long as the app remains installed on the device. The user may request the deletion of all content associated with their installId at any time (see §9).

### 3.2 Audio recordings from the microphone

- **What is collected:** WAV recordings (48 kHz, mono) of a few seconds duration, made at the time of identifying a bird through its song.
- **Purpose:** species identification via the BirdNET 2.4 model executed entirely on the device.
- **Legal basis:** user consent (art. 6(1)(a) GDPR), expressed through granting microphone permission to the operating system.
- **Recipients:** **none**. Recordings remain exclusively on the user's device. They are not transmitted to external servers for identification purposes.
- **Retention:** recordings are saved in a temporary folder on the device. The user may delete them at any time. Only if the user explicitly decides to share the observation with the community, the audio is uploaded to Firebase Storage (see §3.8).

### 3.3 Photographs from camera or gallery

- **What is collected:** photographs taken with the device's camera or selected from the user's gallery for identification purposes.
- **Purpose:** species identification via the EfficientNet Birds model executed entirely on the device.
- **Legal basis:** user consent (art. 6(1)(a) GDPR), expressed through granting camera and/or media access permissions.
- **Recipients:** **none**. Photographs remain exclusively on the device. They are not transmitted to external servers for identification purposes.
- **Retention:** photographs remain in the folder designated by the user (gallery or device storage). Only if the user explicitly decides to share the observation with the community, the photo is uploaded to Firebase Storage (see §3.8).

### 3.4 Geographic location data (GPS)

- **What is collected:** geographic coordinates (latitude and longitude) of the user's device at the time of an observation or when using functionalities that require geographical context (maps, region filters, local species suggestions).
- **Purpose:**
    - filtering of species displayed based on the user's geographic area;
    - association of observations with their location (if the user chooses to save them);
    - notifications of rare species nearby (functionality available only with the Gold subscription);
    - search for eBird hotspots and recent observations (only if the user has configured their eBird API key, see §5.3).
- **Legal basis:** user consent (art. 6(1)(a) GDPR), expressed through granting location permission to the operating system.
- **Recipients:**
    - no recipient if the user uses only local features;
    - Firebase Firestore if the user publishes an observation in the community;
    - GBIF if the user consults distribution maps (query with anonymous coordinates);
    - eBird / Cornell Lab of Ornithology, only if the user has activated the eBird integration by configuring their personal API key.
- **Retention:** on the device, at the user's discretion (stored together with the observation record in the local history). On Firebase Firestore, for published observations: until the user requests deletion.

### 3.5 Observation data

- **What is collected:** details of the observations made by the user: identified species, recognition confidence, timestamp, any geographic location, any associated photo or audio.
- **Purpose:** construction of the user's personal history (available to Gold subscribers), calculation of personal statistics (species seen, daily streaks, badges), optional community sharing.
- **Legal basis:** performance of a contract (art. 6(1)(b) GDPR) for the personal history of Gold users; explicit consent (art. 6(1)(a) GDPR) for community sharing.
- **Recipients:** remain on the device by default; uploaded to Firebase Firestore only if the user subscribes to Gold (synced history) or shares with the community.
- **Retention:** on the device as long as the app remains installed; on Firebase Firestore until the user requests deletion or cancels the Gold subscription.

### 3.6 App usage data

- **What is collected:** non-identifying personal statistics of the user: number of species observed, streak of consecutive days of activity, badges earned, app usage preferences.
- **Purpose:** gamification and user motivation (badge, level, achievement system).
- **Legal basis:** performance of a contract (art. 6(1)(b) GDPR).
- **Recipients:** stored locally on the device; for Gold users, synchronized on Firebase Firestore to allow access from multiple devices and server-side validation of badges.
- **Retention:** on the device as long as the app remains installed. On Firestore as long as the Gold subscription is active.

### 3.7 Subscription-related data (Gold)

- **What is collected:** subscription status (active / inactive / trial period), expiry date, Google Play Billing transaction identifiers.
- **Purpose:** provision of features reserved for Gold subscribers, server-side verification of subscription validity to prevent abuse.
- **Legal basis:** performance of a contract (art. 6(1)(b) GDPR).
- **Recipients:** Google Play Billing (merchant of record of the subscription) and Firebase Cloud Functions (validity verification). Birdsoniq **does not access** the user's payment card data: such data is managed exclusively by Google under its own terms.
- **Retention:** as long as the subscription is active; after cancellation, data relating to the last billing cycle are retained for 10 years for tax and accounting purposes (legal obligation, art. 2220 of the Italian Civil Code).

### 3.8 Content shared with the community

- **What is collected:** when the user explicitly chooses to publish an observation in the community (opt-in operation), the following data are uploaded to Firebase Firestore and Firebase Storage:
    - the user's installId (pseudonymous identifier)
    - the identified species (scientific and common name)
    - the date and time of the observation
    - the GPS coordinates of the sighting
    - any photograph taken
    - any audio recording made
- **Purpose:** construction of a community feed of scientific observations useful for citizen science and biodiversity monitoring.
- **Legal basis:** explicit user consent (art. 6(1)(a) GDPR), expressed through an informative dialog that requires confirmation at the first sharing attempt and to which the user may choose to give persistent consent or consent revocable on a single occasion.
- **Recipients:** other users of the app who view the community feed, to whom observations are shown with the pseudonymized installId (non-identifying). Firebase Firestore and Firebase Storage as storage infrastructure.
- **Retention:** until the user requests deletion. Consent may be revoked at any time from the app's Privacy Settings; revocation disables future sharing but does not automatically delete previously published observations (for these the user must submit a deletion request — see §9).

### 3.9 External service API keys (eBird, IUCN)

- **What is collected:** personal API keys that the user may optionally enter in the app's settings to enable integrations with eBird and the IUCN Red List.
- **Purpose:** to allow the user to use their free API key to access additional features (eBird hotspots, detailed IUCN conservation status).
- **Legal basis:** user consent (art. 6(1)(a) GDPR).
- **Recipients:** keys are stored exclusively on the user's device, never transmitted to Birdsoniq servers. When used, they are sent directly to the corresponding service (Cornell Lab of Ornithology for eBird; IUCN for the Red List).
- **Retention:** on the device until the user manually removes them from the settings.

---

## 4. Legal basis for processing

As indicated for each category in the previous paragraph, the legal bases on which data processing is based are those provided for in art. 6(1) of the GDPR, specifically:

- **Consent (art. 6(1)(a)):** for the processing of sensitive data such as audio, images, location and for community sharing.
- **Performance of a contract (art. 6(1)(b)):** for the essential functions of the app and for the provision of the Gold subscription.
- **Legitimate interest (art. 6(1)(f)):** for the generation of the pseudonymous installId (necessary to ensure the functionality of the app while maintaining privacy-by-design).
- **Legal obligation (art. 6(1)(c)):** for the retention of accounting data related to transactions.

---

## 5. Data recipients and third-party services

Birdsoniq relies on some third-party services to provide its functionalities. Below is the complete list of the recipients of the data processed.

### 5.1 Google services

**Google Firebase** (Google Ireland Ltd. and Google LLC): backend infrastructure of the app.

- *Cloud Firestore:* storage of community observations, Gold history, synchronized statistics, validation records.
- *Firebase Storage:* storage of photos and audio shared with the community.
- *Cloud Functions:* server-side verification of Gold subscription validity.
- *Firebase Core:* service initialization.

Birdsoniq **does not use** Firebase Authentication, Firebase Analytics, Firebase Crashlytics, Firebase Cloud Messaging, Firebase Remote Config or any other Google analysis or profiling services.

Reference privacy policy: `https://policies.google.com/privacy`.

**Google Play Billing** (Google Ireland Ltd.): Gold subscription management. Google acts as *merchant of record* in the European Union, which means that Google itself fully manages users' payment data, billing and VAT. Birdsoniq never accesses credit card data.

Reference privacy policy: `https://payments.google.com/payments/apis-secure/get_legal_document`.

**Google Translate** (Google LLC): used to automatically translate from English to the user's language the encyclopedic descriptions of species coming from Wikipedia. Translation requests contain exclusively encyclopedic texts of species and not personal data of the user.

Reference privacy policy: `https://policies.google.com/privacy`.

### 5.2 Open scientific sources

**GBIF** (Global Biodiversity Information Facility, based in Copenhagen, Denmark): source of data on geographical distribution and monthly frequency of species, accessible via public API. When the user consults distribution maps, the coordinates are transmitted to GBIF without personal identifiers.

Privacy policy: `https://www.gbif.org/terms/privacy-policy`.

**iNaturalist** (California Academy of Sciences / National Geographic Society, USA): source of species photographs and taxonomic information, accessible via public API. Birdsoniq queries iNaturalist by transmitting the scientific name of the species of interest, without user personal data.

Privacy policy: `https://www.inaturalist.org/pages/privacy`.

**Wikipedia / Wikimedia Commons** (Wikimedia Foundation, San Francisco, USA): source of encyclopedic descriptions and species photographs in fallback mode. Birdsoniq accesses the public APIs via the species scientific name, without user personal data.

Privacy policy: `https://foundation.wikimedia.org/wiki/Privacy_policy`.

**IUCN Red List** (International Union for Conservation of Nature, based in Switzerland; servers in the United Kingdom): used only if the user configures their free IUCN API key, to obtain the updated conservation status of species. Transmits the scientific name.

Privacy policy: `https://www.iucnredlist.org/privacy`.

**Xeno-canto** (Stichting Xeno-canto voor Geluiden van Vogels, based in the Netherlands): source of audio recordings of bird songs and calls, accessible via public API. Birdsoniq transmits the scientific name of the species. Recordings are played via direct streaming from Xeno-canto servers without being downloaded, modified or stored.

Terms of use: `https://xeno-canto.org/about/terms`.

### 5.3 eBird integration (opt-in)

**eBird** (Cornell Lab of Ornithology, Cornell University, Ithaca, NY, USA): **optional** integration that the user can activate by entering their personal eBird API key in the app's settings (obtainable free of charge after registration at `https://ebird.org/api/keygen`).

When the user activates the integration, the following information is transmitted to eBird servers:

- device GPS coordinates (for searching hotspots and notable observations nearby);
- the user's personal API key;
- the scientific name of the species of interest.

In the absence of a configured API key, **no data is transmitted** to eBird. The configured API key can be removed at any time from the settings, deactivating the integration.

Privacy policy: `https://www.birds.cornell.edu/home/privacy/`.

### 5.4 Export to eBird (local function)

Birdsoniq offers a functionality to export observations in the "eBird Record Format" format. This export produces exclusively a CSV file saved in the user's device memory. The file can subsequently be uploaded by the user autonomously to `ebird.org/import` or shared via any channel they choose. **Birdsoniq does not perform any automatic uploading to eBird** as part of this functionality.

---

## 6. Extra-EU data transfers

Some of the recipients listed in §5 are located outside the European Economic Area. Below is the table of extra-EU transfers and the safeguards adopted for each:

| Recipient | Country | Safeguard pursuant to art. 46 GDPR |
|---|---|---|
| Google Ireland Ltd. | Ireland (EU) | — |
| Google LLC | United States | Standard Contractual Clauses (SCC) + Data Privacy Framework |
| iNaturalist | United States | Equivalent Standard Contractual Clauses (public policy) |
| Wikimedia Foundation | United States | Public adherence to Data Privacy Framework |
| IUCN / UK servers | Switzerland / United Kingdom | EU Commission adequacy decisions |
| Xeno-canto | Netherlands (EU) | — |
| Cornell Lab of Ornithology | United States | Transfer at the user's initiative (art. 49(1)(a) GDPR) |
| GBIF | Denmark (EU) | — |

Regarding transfers to the United States, the safeguards are based on EU Commission Adequacy Decision 2023/1795 concerning the *EU-US Data Privacy Framework*, possibly supplemented by Standard Contractual Clauses (SCC) where applicable.

---

## 7. Retention periods

| Data category | Retention period |
|---|---|
| installId | As long as the app remains installed |
| Audio recordings | Temporary, until the user deletes them |
| Photographs | At the user's discretion (device memory) |
| GPS coordinates (not published) | On the device until deleted by the user |
| Observation history | As long as the Gold subscription is active |
| Published community observations | Until the user requests deletion |
| Active subscription data | For the duration of the subscription |
| Subscription accounting data | 10 years from cancellation (legal obligation) |
| External API keys | Until the user removes them |

---

## 8. User rights

The user has the right, at any time, to exercise the rights recognized by articles 15 to 22 of the GDPR, including:

- **Right of access (art. 15):** to obtain confirmation of the processing of their data and, if so, access to such data and information on the processing.
- **Right of rectification (art. 16):** to obtain the rectification of inaccurate or incomplete data.
- **Right to erasure (art. 17):** to obtain the deletion of their personal data.
- **Right to restriction of processing (art. 18):** to obtain the restriction of the processing of their data under certain circumstances.
- **Right to data portability (art. 20):** to receive their data in a structured, commonly used and machine-readable format.
- **Right to object (art. 21):** to object to the processing of their data.
- **Right to withdraw consent (art. 7.3):** to revoke at any time the consent previously given, without prejudice to the lawfulness of the processing carried out before the withdrawal.

---

## 9. How to exercise the rights

To exercise any of the rights listed in §8, the user may send a request to the email address:

**giovannisecci72@gmail.com**

indicating in the subject of the email "GDPR Request — [type of right]" (for example: "GDPR Request — deletion").

**Special procedure for users without an account.** Since Birdsoniq does not require registration or login, it does not have any direct identifying data of the user: to identify the data associated with a specific installation, the user must provide their **installId**. To view their installId, the user can open the app and access the menu *Settings → Legal Information → My anonymous identifier*. This identifier is the only element that links the user to data published in the community or to the synchronized Gold history.

**Response times.** The Data Controller responds to requests within **30 days** of receipt of the complete request, in compliance with art. 12(3) GDPR. In cases of particular complexity, this term may be extended by another 60 days, with reasoned communication to the user.

**Identity verification.** The Data Controller may request additional information to verify the identity of the requester, when this is necessary to prevent unauthorized access to other users' data.

---

## 10. Complaint to the supervisory authority

The user has in any case the right to lodge a complaint with the competent supervisory authority, identified in Italy as:

**Garante per la Protezione dei Dati Personali**
Piazza Venezia 11, 00187 Rome, Italy
Email: `protocollo@gpdp.it`
Website: `https://www.garanteprivacy.it`

---

## 11. Data security

The data processed by Birdsoniq are protected through:

- **Encryption in transit:** all communications between the app and the servers (Firebase, third-party services) take place via HTTPS / TLS 1.2 or higher protocol.
- **Pseudonymization:** the user identifier is a random UUID, not a direct identifying datum.
- **Minimization:** only the data strictly necessary for the declared functionalities are collected.
- **Firebase security rules:** access to data on Firestore is regulated by security rules that limit reading and writing to only legitimate cases.
- **No sale to third parties:** user data is never sold, transferred or assigned to third parties for commercial or advertising purposes.

Despite the measures adopted, no IT system is 100% secure. In the event of a personal data breach that may entail a high risk for the rights and freedoms of the user, the Data Controller will notify the event to the user and the Italian Data Protection Authority within the terms provided by articles 33 and 34 of the GDPR (within 72 hours of becoming aware of the breach).

---

## 12. Users under the age of 16

The Birdsoniq app is intended for users aged **16 years or older**. Installation and use of the app are prohibited for minors under the age of 16.

The app includes a mode called "Kids" which provides a simplified interface with visual elements suitable for a family or educational context. However, this mode is intended to be used by people of any age **provided that all are aged 16 years or older**. The Kids mode **does not collect or transmit any additional data** compared to the standard mode.

The Data Controller does not knowingly collect personal data from minors under the age of 16. If the Data Controller becomes aware that data relating to a minor under the age of 16 has been processed without valid parental consent, they will promptly delete it. Parents or guardians who believe that their minor child has used the app may contact the Data Controller at the email address indicated in §9 to request deletion of the data.

---

## 13. Cookies and similar technologies

The **Birdsoniq app does not use cookies** or similar tracking technologies. User preferences are stored locally on the device via the native SharedPreferences mechanism of Android, which does not constitute a cookie within the meaning of the ePrivacy legislation.

The website `birdsoniq.app` (where this Privacy Policy is published) may use only technical cookies essential to the operation of the site, for which consent is not required pursuant to art. 122 of the Italian Privacy Code.

---

## 14. Changes to the Privacy Policy

The Data Controller reserves the right to modify this Privacy Policy at any time, to reflect changes in the app's functionality, integrated third-party services, or applicable legislation.

Changes take effect upon publication of the new version of the document. The date of the last update is indicated at the top of the document.

**Substantial changes** (for example: new categories of data collected, new recipients, modification of processing purposes) will be communicated to the user through an in-app notice upon the next launch of the app, giving the user the opportunity to review the new version.

**Version history.** All previous versions of the Privacy Policy are publicly available on the document's git repository: `https://github.com/giovannisecci/birdsoniq-legal`. Each version is identified by its git commit with cryptographic hash and verifiable date.

---

## 15. Sources of data shown in the app and related attributions

Birdsoniq integrates data, text, images and audio recordings provided by third-party scientific and citizen-science projects, each under its respective license. This section indicates the sources used and the manner of use, in compliance with the respective licenses.

**Audio recordings — Xeno-canto.** The app plays recordings of bird songs and calls hosted on the Xeno-canto platform, contributed by its members under Creative Commons licenses (CC BY or CC BY-SA; recordings carrying a Non-Commercial clause are excluded). Recordings are played via direct streaming from Xeno-canto servers without being downloaded, modified or stored locally. For each recording Birdsoniq displays the required attribution (author, Xeno-canto identifier, specific license) with a link to the original page.

**Observation data — GBIF.** Species distribution and monthly frequency data are obtained through the GBIF APIs under Creative Commons Attribution 4.0 (CC BY 4.0) or Public Domain (CC0) license. Offline packs include only CC BY 4.0 and CC0 data.

**Photos and taxonomy — iNaturalist.** Species photographs and some taxonomic information are obtained through the iNaturalist APIs. Each photo retains the attribution provided by the platform (author, license, link to the original photo).

**Fallback photos and descriptions — Wikipedia / Wikimedia Commons.** When not available via iNaturalist, cover photos and encyclopedic descriptions are obtained through the Wikipedia APIs. Content is distributed under Creative Commons Attribution-ShareAlike (CC BY-SA) license; attribution in the app refers to the source Wikipedia page.

**Conservation status — IUCN Red List.** Species conservation status is obtained through the IUCN Red List v4 API (with an API key configured by the user).

**Translation service.** Descriptions in languages other than English are obtained through Google Translate. Birdsoniq is not responsible for the accuracy of automatic translations.

**No redistribution.** Birdsoniq does not redistribute third-party content to entities other than the end user who uses the app. The app does not expose public endpoints, does not publish archives, does not share data with advertisers.

**Reports.** If you are the author of a recording, photograph or other content shown in the app and you believe the use does not comply with the applicable license, you can contact Birdsoniq at the email address indicated in §16 and we will promptly evaluate the report, including removal of the content if appropriate.

---

## 16. Contacts

**Data Controller:** Giovanni Secci
**Address:** Via Baccarini, 08100 Nuoro (NU), Italy
**Email (privacy, copyright, support):** giovannisecci72@gmail.com
**VAT number:** [IT__________ — pending activation]

For any matters relating to this Privacy Policy or the processing of their data, the user may write to the email address indicated above. The Data Controller undertakes to respond within the time limits provided by applicable legislation.

---

*End of document.*
