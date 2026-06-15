# ◎ Die Robotik-Revolution beobachten

Ein interaktives Ein-Seiten-Observatorium, das die **gesamte LiDAR- und Sensor-Lieferkette** als Frühwarnsystem darstellt — damit man an den Quartalszahlen erkennt, wann die Robotik- und Drohnen-Welle in die **Massenproduktion** kippt.

> **Keine Anlageberatung.** Strukturelle Markt- und Lieferketten-Analyse zu Beobachtungszwecken. Datenstand: Q1 2026 (gemeldet April–Mai 2026).

![Status](https://img.shields.io/badge/Stand-Q1%202026-35D6E8) ![Typ](https://img.shields.io/badge/100%25-statisches%20HTML-3FD17A) ![Lizenz](https://img.shields.io/badge/Hinweis-keine%20Anlageberatung-F4B23E)

**🔗 Live:** https://mendeltem.github.io/Die-Robotik-Revolution-beobachten/

---

## Was die Seite zeigt

| Abschnitt | Inhalt |
|---|---|
| **Hero** | Kernthese + 4 Leitkennzahlen, mit animierter LiDAR-Punktwolke als Signatur |
| **Wo wir stehen** | S-Kurve der Adoption bis ~2060. Klick auf eine Phase öffnet die Erklärung **inline darunter** (aus der Projekt-Doku), der „WIR SIND HIER"-Punkt **wandert** dabei auf der Kurve mit |
| **Signalkette** | Interaktive Supply-Chain: Laser → Detektor → LiDAR-System → Edge-Gehirn → Aktoren → Roboter. Klick auf eine Stufe zeigt die Firmen **inline**; die Liste bleibt sichtbar, während ein Firmendetail darunter erscheint |
| **Firmen-Explorer** | 22 Firmen, filterbar nach Schicht; Klick öffnet Finanzen, Sektor, Aktien-Ticker, Status und Frühsignal — alles **inline, ohne Popups** |
| **Use Cases** | 35 Physical-AI-Anwendungsfälle (Mobilität, Medizin, Landwirtschaft, Industrie, Notfall, Stadt, Service, Frontier, Enabler) aus der Projekt-Doku, filterbar nach Bereich; Klick zeigt Reife, Kennzahl, führende Anbieter (mit anklickbaren offiziellen Links aus der Doku) und Sensor-Bezug |
| **Frühindikatoren** | Die 5 Zahlen, die man pro Quartal prüft (Stückzahl-Wachstum, Robotik-vs-Auto-Mix, Umsatz-Anteil, Backlogs, Preis pro Einheit) |
| **Geopolitik** | China-Restriktionen (DoD-1260H, SAFE LiDAR Act) als Signalfaktor |

## Das Frühwarnsystem in Kürze

Die Firmen sind in drei Ampelstufen sortiert:

- 🟢 **reagiert zuerst** — LiDAR-System-Hersteller (RoboSense, Hesai, Ouster). Ihre Stückzahlen schlagen am frühesten aus.
- 🟡 **bestätigend** — Detektor-, Laser- und Compute-Lieferanten (Sony, STMicro, ams OSRAM, NVIDIA, Ambarella). Träger, aber unabhängig.
- 🔴 **Risiko** — insolvente oder fragile Player (Luminar) bzw. nicht handelbare China-Firmen mit Beschaffungsverboten.

**Das wichtigste Signal:** der Robotik-**Umsatz**-Anteil. Die Stückzahl-Wende ist im Q1 2026 passiert (RoboSense: Robotik überholt Auto, 56 %), die Geld-Wende steht noch aus. Echte Sättigung erst ~2050–60.

## Bedienung & Aktualisierung

- **Tab-Navigation statt Scrollen:** sechs Bereiche (Wo wir stehen, Signalkette, Firmen, Use Cases, Frühindikatoren, Geopolitik) als sticky Tabs — immer nur eine Ansicht sichtbar, jeder Tab in eigener Farbe (cyan/blau/amber/grün/violett/rot).

- **Sprache DE/EN** umschaltbar oben rechts (Button) — übersetzt die komplette Oberfläche *und* alle Daten (Firmen, Use Cases, Phasen); Auswahl wird gemerkt.
- **Suche** über jedem Raster (Firmen, Use Cases) — Name oder Ticker eintippen.
- **Klick** auf Firma / Stufe / Phase / Use Case öffnet Details **inline** (keine Popups); die Liste bleibt sichtbar.
- **Bewertung** (Marktkap./KGV-Einordnung), **letztes Quartal**, **Sektor** und **Frühsignal** stehen im Firmendetail.
- **Earnings-Countdown** zeigt die nächsten (voraussichtlichen) Berichtstermine als Pflicht-Checks.
- **Frühindikatoren** mit Trend-Pfeilen; **Deep-Links** (z.B. `…/#firm=sony`) zum direkten Teilen; **Filter-/Suchzustand** wird im Browser gemerkt.
- **Daten aktualisieren:** im `index.html` den Block hinter `// ===== DATEN — HIER AKTUALISIEREN =====` bearbeiten (Quartalszahlen, Bewertungen, Termine). Sonst nichts anfassen nötig.

## Lokal starten

Reines statisches HTML, keine Build-Tools nötig:

```bash
git clone https://github.com/<user>/robotik-observatorium.git
cd robotik-observatorium
python3 -m http.server 8000   # dann http://localhost:8000 öffnen
```

> Über einen lokalen Server öffnen (nicht per Doppelklick als `file://`), damit alle Teile sauber laden.

## Auf GitHub Pages veröffentlichen

1. Repo nach GitHub pushen (Dateien im Hauptverzeichnis, `index.html` muss im **root** liegen).
2. **Settings → Pages → Source: „Deploy from a branch" → Branch: `main`, Ordner: `/ (root)` → Save.**
3. Die Seite ist nach dem ersten Build (ein paar Minuten) live unter:

   **https://mendeltem.github.io/Die-Robotik-Revolution-beobachten/**

   Allgemeine Formel: `https://<benutzername>.github.io/<repo-name>/`

**Den genauen Link finden:** Nach dem Speichern erscheint oben auf der Pages-Seite ein grüner Kasten „Your site is live at …" mit **Visit site**-Button (ggf. Seite neu laden). Alternativ im Repo rechts unter **Deployments → github-pages** oder im Reiter **Actions** den grünen Haken des Pages-Builds prüfen.

> **Stolperfallen:** Groß-/Kleinschreibung im Pfad zählt (Repo-Name exakt übernehmen). Bei 404 kurz warten (Build läuft noch) oder prüfen, ob `index.html` wirklich im root liegt. Repo-Name lässt sich unter Settings → General umbenennen — dann ändert sich der Link entsprechend.

## Flowchart neu generieren (optionaler statischer Export)

Die Signalkette ist auf der Seite interaktiv (HTML/SVG). Zusätzlich liegt ein statisches Diagramm bei, das mit Python erzeugt wird:

```bash
pip install graphviz        # benötigt zusätzlich das System-Paket 'graphviz' (dot)
python3 make_flowchart.py   # schreibt supply_chain.svg
```

Farben und Schichten lassen sich oben in `make_flowchart.py` anpassen.

## Dateien

```
index.html          # die komplette interaktive Seite (CSS + JS inline)
supply_chain.svg    # optionales, mit Python generiertes Flowchart
make_flowchart.py   # Generator-Skript für das Flowchart
README.md
```

## Daten & Quellen

Zuletzt gemeldete Quartalszahlen (Q1 2026) aus öffentlichen Earnings-Releases sowie Branchendaten (Yole Group, Counterpoint Research, BofA, Goldman Sachs, Morgan Stanley, Unternehmensmeldungen, SEC/EDGAR).

**Hinweise zur Datenqualität:** Chinesische Zahlen sind nicht-GAAP/IFRS-gemischt. Sony, STMicroelectronics und onsemi schlüsseln keinen LiDAR-Detektor-Umsatz separat aus — ihre Signalkraft liegt in Produktlaunches und Design-Wins. Stückzahl- und Umsatz-Mix laufen wegen Preisunterschieden (Robotik viel günstiger als Auto) stark auseinander. Marktprognosen sind Szenarien, keine Fakten. Kurse und Bewertungen ändern sich täglich.

## Technik

Statisches HTML/CSS/JS ohne Laufzeit-Abhängigkeiten. Alle Interaktionen öffnen sich inline (keine Popups). Schriften via Google Fonts (Space Grotesk, Inter, IBM Plex Mono). Ambient-Animation respektiert `prefers-reduced-motion`. Responsiv bis Mobile.

---

*Erstellt als Beobachtungswerkzeug — keine Anlageberatung.*
