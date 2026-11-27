# Requisiti hardware — SailSense Live

## Piattaforma

| Requisito | Valore |
|-----------|--------|
| Sistema operativo | Android 8.0 (API 26) o superiore |
| RAM consigliata | ≥ 3 GB |
| Spazio libero | ≥ 50 MB |

---

## Sensori obbligatori

| Sensore | Uso | Se assente o guasto |
|---------|-----|---------------------|
| **GPS** | Posizione, SOG, COG, VMG | App non utilizzabile per navigazione dati |
| **Accelerometro** | Heel, trim, assetto target | Solo GPS/COG; nessun heel/trim |
| **Magnetometro (bussola)** | Prua (HDG) | Prua da COG GPS in movimento |
| **Giroscopio** | Fusione IMU (consigliato) | Rotation vector può essere meno stabile |

### Come verificare prima di uscire in mare

Installare un'app di test sensori (es. **Sensor Test**, **CPU-Z**, **AndroSensor**) e controllare che:

1. **Accelerometro** — valori cambiano inclinando il telefono
2. **Giroscopio** — valori cambiano ruotando il telefono
3. **Bussola** — valori cambiano orientando il telefono
4. **Auto-rotazione schermo** — se il telefono non ruota lo schermo, l'accelerometro è probabilmente guasto

---

## Telefoni testati

| Modello | Esito | Note |
|---------|-------|------|
| **Blackview BV8800** | ✅ Compatibile | IMU OK; fix MediaTek rotation vector (5 valori) applicato |
| **Blackview BV8900** | ⚠️ Parziale | Accelerometro/giroscopio non funzionanti a livello sistema; solo GPS/bussola |

> Lista da aggiornare con feedback beta tester.

---

## Montaggio consigliato

- Telefono fissato saldamente (supporto anti-vibrazione)
- **Verticale o orizzontale** — l'app adatta gli assi automaticamente
- Premere **Calibra** con barca in assetto di riferimento (es. planata)
- Evitare vicinanza a motori, altoparlanti e metallo massiccio (disturbi bussola)
- Per allineare la prua al COG: **pressione lunga su Calibra** navigando dritti > 1,5 kn

---

## Rete e alimentazione

- **Nessuna connessione** richiesta in mare (offline completo)
- Consigliato: batteria piena o power bank; GPS e sensori consumano energia
- Il servizio in primo piano mantiene l'acquisizione a schermo spento

---

## Export dati

File salvati in:

```
/storage/emulated/0/Download/AtlasLive/atlaslive_YYYYMMDD_HHMMSS.csv
```

Frequenza registrazione: **10 campioni/secondo** (10 Hz).

---

## Limitazioni note

- La direzione del vento è **stimata** dalle virate marcate (Port/Stbd), non da anemometro
- Precisione GPS tipica 2–10 m; in coperta o con alberi può peggiorare
- Target adattivi richiedono alcuni minuti di navigazione sopra ~1,5 kn dopo aver marcato il vento

---

## Supporto

Segnalare modelli problematici a: **[EMAIL]**

Includere: marca/modello, versione Android, screenshot app test sensori.
