# stau-prognose

App-Prototyp für den Projektkurs (Jugend forscht 2026/27): Stau nicht nur anzeigen, sondern im Voraus planen. Für jede Route gibt die App die Ankunftszeit als Wahrscheinlichkeit an und empfiehlt die späteste sichere Abfahrt.

## Funktionen
- Drei Routen im Vergleich (Verspätung, Wahrscheinlichkeit pünktlich zu sein)
- Abfahrtsempfehlung für 80, 90 oder 95 % Sicherheit
- Zeit- und Spritrechnung pro Fahrt und Jahr
- Messfahrten: mittlerer Fehler der Prognose gegen das normale Navi

## Modell
Fahrzeit ~ logarithmische Normalverteilung. Mittelwert und Streuung wachsen mit der Auslastung.
`P(pünktlich) = P(Fahrzeit <= verfügbare Zeit)`

## Datenquellen (geplant)
Mobilithek, Autobahn GmbH, open.nrw (z. B. Bonn), Deutscher Wetterdienst, eigene Messfahrten.

## Status
Basisfahrzeiten, Auslastungskurve, Regen-/Baustellenzuschlag, Verbrauch und Streckenlängen sind Demo-Annahmen. Keine Live-Daten.

## Roadmap
- [x] Prototyp mit Wahrscheinlichkeitsmodell
- [ ] Google Maps und Waze bei der Vorausplanung prüfen
- [ ] Echte Daten aus Mobilithek anbinden
- [ ] Messfahrten auswerten (Experiment 1)
- [ ] Maschinelles Lernen gegen das Modell testen
- [ ] Umfrage unter Mitschülern und Eltern (Experiment 2)

## Veröffentlichen
`index.html` (die App) und diese `README.md` ins Repo hochladen, dann Settings, Pages, Branch `main`.

## Lizenz
MIT
