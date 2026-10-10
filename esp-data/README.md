# ESP data export

Dieser Ordner ist fuer kleine, ESP-freundliche Datendateien gedacht.

Erzeugung am Mac:

```bash
cd /Users/marvin/Documents/Codex/2026-10-05/referenced-chatgpt-conversation-this-is-an/outputs/CrowPanel_ESP32S3_EPaper_FlightRadar
python3 tools/build_esp_data.py "/Pfad/zum/standing-data-main" esp-data
```

Danach diese Dateien in dein GitHub-Datenrepo kopieren:

- `version.json`
- `airlines.json`
- `nearby-frequencies.json`
- `routes/` komplett

Der ESP soll spaeter nur diese kleinen Dateien laden, nicht die grossen Original-CSV-Dateien durchsuchen.
Die Routen sind absichtlich in Buchstaben-Dateien aufgeteilt, damit die Webseite bei einem ausgewaehlten Flug nur z.B. `routes/P.json` fuer `PGT5965` nachladen muss.
