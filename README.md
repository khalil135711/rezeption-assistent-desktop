# Rezeption Assistent (Desktop)

Desktop-App für die Reha-Rezeption: Termine (Heilmittel, Rehasport, Nachsorge, Selbstzahler),
Kunden mit Aufnahme/Entlassung, Kasse, Kontrolllisten und ein lokaler Assistent
(regelbasiert, **ohne API, ohne Cloud**). Läuft offline unter Windows, macOS und Linux (Electron).

## Starten (Entwicklung)
    npm install
    npm start

## Installer bauen
    npm run dist          # für das aktuelle Betriebssystem
    npm run dist:win      # .exe (Installer + portable), am besten unter Windows
    npm run dist:mac      # .dmg, nur unter macOS
    npm run dist:linux    # .AppImage + .deb, unter Linux

Ergebnisse liegen in `dist/`. Alle drei Systeme gleichzeitig baut die GitHub Action
`.github/workflows/build.yml` (Actions → "Build Desktop App" → Run workflow).

## Hinweise
- Daten bleiben lokal im App-Speicher des Rechners. Vor echtem Patientendaten-Einsatz:
  Verschlüsselung, Backup und DSGVO-Konzept ergänzen.
- Optional: eigenes Icon als `build/icon.png` (512×512) ablegen.
- Unsignierte Installer lösen unter Windows (SmartScreen) und macOS (Gatekeeper) Warnungen aus.

## Befehle des Assistenten
Aufnahme Max Muster kasse TK · Entlassung Berger · Termin Berger morgen 10 Uhr Massage ·
Kasse 25 Lang Massage · Brief an Kostenträger für Berger · Termine heute · Suche Lang
