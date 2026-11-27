# Checklist release — SailSense Live v1.0

Usare questa lista prima di ogni pubblicazione su Google Play.

---

## A. Brand e documenti legali

- [ ] Nome **SailSense Live** verificato (ricerca marchio EUIPO / Google Play)
- [ ] Sostituiti `[EMAIL]`, `[SITO]`, `[NOME]` in tutti i file `release/`
- [ ] Privacy policy pubblicata su URL pubblico (es. `[SITO]/privacy`)
- [ ] Termini d'uso e disclaimer linkati da sito o schermata Info in app
- [ ] README release aggiornato con versione e data

---

## B. App Android

- [ ] `versionCode` incrementato in `app/build.gradle`
- [ ] `versionName` aggiornato (es. `1.0`)
- [ ] Nome visualizzato: **SailSense Live** in `strings.xml`
- [ ] Icona launcher definitiva (non placeholder)
- [ ] Schermata Info con link a Privacy + Disclaimer (consigliato v1.1)
- [ ] Nessun log diagnostico verboso in produzione
- [ ] Test su almeno 1 telefono con IMU funzionante (es. BV8800)
- [ ] Test registrazione schermo spento
- [ ] Test export CSV e apertura in Sailing Analyzer

---

## C. Build e firma

- [ ] Keystore release creato e **backup sicuro** (password salvate)
- [ ] `assembleRelease` o `bundleRelease` senza errori
- [ ] APK/AAB firmato con keystore release (non debug)
- [ ] ProGuard/R8: `minifyEnabled` valutato (v1.0 può restare false)

```bash
# Esempio creazione keystore (una tantum)
keytool -genkey -v -keystore sailsense-release.jks -keyalg RSA -keysize 2048 -validity 10000 -alias sailsense
```

---

## D. Google Play Console

- [ ] Account sviluppatore attivo (25 €)
- [ ] App creata con package `com.atlaslive` o `com.sailsense.live`
- [ ] AAB caricato in track **Internal testing** o **Closed testing**
- [ ] Breve + lunga descrizione (da PLAY-STORE-LISTING.md)
- [ ] Screenshot (min 2 telefono)
- [ ] Icona 512×512 e feature graphic 1024×500
- [ ] Classificazione contenuti completata
- [ ] Dichiarazione sicurezza dati (posizione: elaborata su dispositivo)
- [ ] URL privacy policy inserito
- [ ] Prezzo impostato (9,99 € early / 14,99 € standard)
- [ ] Paesi di distribuzione selezionati

---

## E. Beta tester (prima del pubblico)

- [ ] 5–10 tester invitati con link opt-in
- [ ] Questionario feedback (IMU, colori, CSV, UX in barca)
- [ ] Almeno 1 sessione reale in acqua documentata
- [ ] Bug critici risolti o documentati in note di rilascio

---

## F. Post-lancio

- [ ] Monitoraggio recensioni Play Store (prima settimana)
- [ ] Email supporto attiva: [EMAIL]
- [ ] Piano v1.1: GPX export, schermata Info, soglie regolabili
- [ ] Aggiornare REQUISITI-HARDWARE.md con nuovi telefoni testati

---

## File release generati

```
release/
├── README.md
├── BRAND.md
├── PIANO-COMMERCIALIZZAZIONE.md
├── DISCLAIMER.md
├── PRIVACY-POLICY.md
├── TERMINI-USO.md
├── PLAY-STORE-LISTING.md
├── REQUISITI-HARDWARE.md
├── RELEASE-CHECKLIST.md
└── IN-APP-DISCLAIMER.txt
```

---

**Data checklist:** 29 giugno 2026  
**Versione target:** SailSense Live 1.0
