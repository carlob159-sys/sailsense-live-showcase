# Piano di commercializzazione — SailSense Live v1.0

Documento di strategia per il lancio a prezzo contenuto.  
Data: 29 giugno 2026

---

## 1. Prodotto e valore

**Problema:** strumenti dedicati (GPS+IMU da barca) costano 400–600 € + abbonamenti.  
**Soluzione:** SailSense Live usa il telefono già in tasca (GPS, accelerometro, bussola) come strumento coach in tempo reale.

**Funzioni differenzianti v1.0:**
- GPS ad alta frequenza (10 Hz) con dead reckoning
- Heel, trim, TWA, VMG, COG/SOG
- Target adattivo (heel/trim/velocità per angolo al vento)
- Feedback visivo alto contrasto (sfondo rosso/verde)
- Confronto VMG mure port/stbd
- Registrazione a schermo spento + export CSV
- Funzionamento offline

---

## 2. Canali di distribuzione

### Canale principale: Google Play Store
- Costo account sviluppatore: ~25 € (una tantum)
- Pagamenti: Google Play Billing (acquisto o abbonamento)
- Vantaggi: aggiornamenti, recensioni, fiducia, nessuna installazione manuale APK

### Canale complementare: vendita diretta
- Sito con pagina prodotto + link Play Store
- Utile per beta e passaparola in club/scuole vela
- Pagamento: Stripe / PayPal / Gumlow

### Canale community
- Forum vela, gruppi Facebook/WhatsApp, scuole vela
- Demo video 2–3 min in barca (colori target, VMG mure)
- Partnership "fleet" per scuole (licenza multipla scontata)

---

## 3. Prezzo consigliato

| Modello | Prezzo | Note |
|---------|--------|------|
| **Early adopter (beta)** | 5–9,99 € una tantum | Primi 50–100 utenti, feedback in cambio |
| **Lancio Play Store** | **14,99 €** una tantum | Posizionamento "contenuto ma serio" |
| **Alternativa** | **6,99 €/anno** | Se si vogliono aggiornamenti continui |
| **Freemium (futuro)** | Gratis + Pro 9,99 €/anno | GPS+log base gratis; target+match in Pro |

**Perché non sotto i 5 €:** percepito come giocattolo; difficile coprire supporto, account Play, tempo sviluppo.

**Confronto:** hardware Vakaros ~500 € → SailSense a 15 € è un messaggio di vendita forte.

---

## 4. Strategia in 3 fasi

### Fase 1 — Beta a pagamento (ora → 2 mesi)
- 10–15 velisti fidati (club, amici regatanti)
- Prezzo simbolico 5–10 € o gratuito contro feedback strutturato
- Obiettivo: validare IMU su modelli telefono, CSV in Sailing Analyzer, UX in barca
- Deliverable: lista bug, 3 testimonianze, 1 video demo

### Fase 2 — Play Store Early Access (mese 2–4)
- Pubblicazione con descrizione onesta ("evoluzione continua")
- Prezzo lancio **9,99 €** per primi 3 mesi, poi 14,99 €
- Privacy policy online, disclaimer in app e su store
- Obiettivo: 50–200 download, rating > 4.0

### Fase 3 — Consolidamento (mese 4+)
- Export GPX se richiesto da Sailing Analyzer
- Soglie target regolabili in Impostazioni
- Eventuale tier Pro (cloud backup opzionale, polar avanzati)
- Marketing: regate locali, articoli su blog vela

---

## 5. Requisiti legali e tecnici pre-lancio

- [ ] Nome **SailSense** verificato (marchio EU, Play Store)
- [ ] Privacy policy su URL pubblico
- [ ] Disclaimer in app (schermata Info o primo avvio)
- [ ] Keystore release Android (non debug)
- [ ] AAB firmato per Play Console
- [ ] Screenshot e video store (portrait + landscape)
- [ ] Policy contenuti: nessun dato venduto a terzi

---

## 6. Costi stimati

| Voce | Costo |
|------|-------|
| Account Google Play | 25 € |
| Dominio + hosting privacy (opz.) | 10–30 €/anno |
| Keystore / firma | 0 € |
| Marketing iniziale | 0 € (passaparola) |
| **Totale minimo** | **~25–55 €** |

---

## 7. Metriche di successo (primo anno)

| Metrica | Obiettivo conservativo |
|---------|------------------------|
| Download | 200–500 |
| Conversione beta → pagamento | > 60% dei tester |
| Rating Play Store | ≥ 4.0 |
| Churn abbonamento (se usato) | < 30%/anno |
| Sessioni registrate exportate | > 50% utenti attivi |

---

## 8. Rischi e mitigazioni

| Rischio | Mitigazione |
|---------|-------------|
| IMU non funzionante su alcuni telefoni | Documento REQUISITI-HARDWARE; test pre-acquisto con app sensori |
| Import CSV non automatico in SA | Aggiungere export GPX in v1.1 |
| Responsabilità navigazione | Disclaimer chiaro: strumento coach, non cartografia certificata |
| Concorrenza hardware | Prezzo e offline come leva; non competere su certificazioni |

---

## 9. Prossimi passi operativi

1. Compilare email e sito in tutti i documenti `release/`
2. Pubblicare PRIVACY-POLICY su `[SITO]/privacy`
3. Aggiungere schermata "Info / Disclaimer" in app (v1.1)
4. Creare keystore release e build AAB
5. Aprire listing Play Store in bozza
6. Invitare 10 beta tester con APK o link test chiuso
