# QA-Bericht – Sichtwort Landingpage-Prototyp

Geprüft: `04-prototype/index.html` (388 Zeilen)
Abgleich mit: `02-strategy.md`, `03-copywriting.md`
Datum: 24.11.2026
Methode: Code-Durchsicht und automatisierter Test im Headless-Chrome (Desktop 1280 px, Mobil 390 px, Dark Mode). Getestet: horizontales Überlaufen, Sprachwechsel im Sichtfeld inklusive Arabisch (RTL), Mobil-Menü, Formularvalidierung, JavaScript-Fehler.

---

## 1. HTML/CSS und Technik

- 🟢 Gültige Grundstruktur: `<!DOCTYPE html>`, `lang="de"`, Viewport, `<meta name="description">` (Z. 6) – der fehlende Description-Tag aus dem GridMind-QA ist behoben.
- 🟢 Keine JavaScript-Fehler in der Konsole, weder auf Desktop noch auf Mobil.
- 🟢 Kein horizontales Überlaufen: `scrollWidth` entspricht bei 1280 px und bei 390 px genau der Fensterbreite.
- 🟢 Sprachwechsel im Sichtfeld funktioniert für alle 6 Sprachen. Arabisch setzt korrekt `dir="rtl"` und `lang="ar"`.
- 🟢 Dark Mode lesbar (über `light-dark()` und `data-theme`), Kontraste in beiden Modi ausreichend.
- 🟢 Ein Fehler wurde beim Bauen gefunden und behoben: Das Formular las den Namen über `form.name`. Das liefert den Namen des Formulars statt des Eingabefelds. Jetzt wird über `getElementById` gelesen.
- 🟢 Ein Layoutfehler wurde beim Testen gefunden und behoben: Auf Mobil verdeckte die Sichtfeld-Einblendung die Sprachknöpfe. Szene und Knöpfe sind jetzt getrennt.

## 2. Inhaltliche Übereinstimmung mit 03-copywriting.md

- 🟢 Hero (Eyebrow, H1, Subline, beide CTAs) wortgleich mit der Copy (Z. 157–167).
- 🟢 Die vier Nutzenversprechen und die fünf Funktionen sind wortgleich übernommen.
- 🟢 Beide Zielgruppentexte (Produktion; Betriebsrat & Datenschutz) wortgleich übernommen.
- 🟢 Slogan „Verstehen. Nicht filmen.“ steht im `<title>` und im Footer.
- 🟡 Die CTA-Überschrift „Ihre Fragen direkt klären“ (Rückruf) aus der Copy fehlt auf der Seite. Der Button ist da, die Überschrift nicht. Kein Fehler, aber nicht vollständig.

## 3. Übereinstimmung mit der Strategie (02-strategy.md)

- 🟢 Kamerafreiheit als Kernversprechen ist überall sichtbar (Hero, Badge „Keine Kamera verbaut“ Z. 199, Nutzenkarte 3).
- 🟢 Beide Entscheider aus der Strategie werden angesprochen: eigener CTA und eigene Karte für Betriebsrat und Datenschutz.
- 🟢 Pilotphase und Region (3–5 Betriebe, BW und Bayern) stehen offen auf der Seite (Z. 209). Funktionen sind als „geplanter Pilotumfang“ gekennzeichnet.
- 🟢 Keine erfundenen Zahlen, Kundenstimmen oder Zertifikate. „Betriebsrat-ready“ wird nicht als Zulassung verkauft („Die Entscheidung bleibt bei Ihnen“).
- 🟢 Logistik, Pflege und Privatkunden tauchen nicht auf – passt zu den zurückgestellten Zielgruppen.
- 🟡 **„In jeder Sprache“ (H1, Z. 160) ist zu groß versprochen.** Laut Strategie startet der Pilot mit Deutsch plus 5–6 Sprachen. Vorschlag: „In der Sprache Ihres Teams.“
- 🟡 **„Ihre Daten bleiben in der EU“ und „wird … nicht gespeichert“** sind als feste Zusagen formuliert. Das ist eine Designentscheidung in unserer Hand, hängt aber von den Anbietern für Spracherkennung und Übersetzung ab (Strategie Abschnitt 5, Punkt 2). Erst nach Vertrag mit diesen Anbietern so absolut formulieren.

## 4. Nutzbarkeit

- 🟢 Mobil-Menü vorhanden (Z. 142): Auf 390 px ist die Navigation zunächst eingeklappt und öffnet sich per Knopf, der Top-CTA bleibt erreichbar. Der wichtigste Mobilfehler aus dem GridMind-QA ist behoben.
- 🟢 Keine `href="#"`-Platzhalter. Alle CTAs springen zum Anfrageformular und wählen dabei das passende Anliegen vor. Das Formular prüft Name und E-Mail und zeigt ehrlich an, dass im Prototyp nichts übermittelt wird.
- 🟢 Interaktive Elemente mindestens 44 px groß, sichtbarer Fokusrahmen, Formularfelder mit Labels, Sprachknöpfe mit `aria-pressed`.
- 🟡 Die Seite verwendet die Gender-Schreibweise „Kolleg:innen“ / „Besucher:innen“. Im produzierenden Mittelstand in BW/Bayern kann das bei Teilen der Zielgruppe ablenken (Bayern hat Gender-Sonderzeichen 2024 in Verwaltung und Schulen untersagt). Kein Fehler, aber vor Livegang bewusst entscheiden – neutrale Formulierungen („neue Teammitglieder“) wären eine Alternative.

---

## 🔴 Muss vor einem echten Livegang behoben werden

*(Für den Prototyp unkritisch, weil die Seite nicht öffentlich beworben wird. Für eine Datenschutz-Marke aber ein Glaubwürdigkeitsproblem.)*

1. **Google Fonts werden vom Google-Server geladen** (Z. 8–10). Das LG München hat 2022 entschieden, dass das dynamische Einbinden von Google Fonts ohne Einwilligung die IP-Adresse unzulässig an Google überträgt. Für ein Produkt, das mit „Datenschutz von Anfang an“ wirbt und sich an Datenschutzbeauftragte richtet, ist das ein Eigentor. → Schriften selbst hosten.
2. **Impressum, Datenschutzerklärung und Datenschutzhinweis am Formular fehlen.** Für eine deutsche Geschäftsseite sind diese Pflichtangaben erforderlich (Impressumspflicht nach § 5 DDG; Informationspflichten nach Art. 13 DSGVO). → Vor Livegang ergänzen und rechtlich prüfen lassen.

## 🟡 Sollte verbessert werden

1. H1 „In jeder Sprache“ → „In der Sprache Ihres Teams“ (Z. 160).
2. EU-Datenhaltung und „nicht gespeichert“ erst nach Anbieterverträgen so absolut formulieren.
3. Fehlende CTA-Überschrift „Ihre Fragen direkt klären“ ergänzen oder aus der Copy streichen.
4. Gender-Schreibweise bewusst für die Zielgruppe entscheiden.

## 🟢 Bestanden

- Technisch fehlerfrei auf Desktop, Mobil und im Dark Mode; kein Überlaufen.
- Copy und Strategie sauber umgesetzt, inklusive offener Kennzeichnung der Pilotphase.
- Alle drei Hauptkritikpunkte des GridMind-QA (Mobil-Navigation, Platzhalter-Links, interner Fachbegriff im Hero) sind hier von Anfang an vermieden.

## Fazit

**Als Prototyp abnahmefähig.** Kein Fehler, der Besucher:innen in die Irre führt oder die Seite unbenutzbar macht. Die zwei 🔴-Punkte betreffen nur einen echten Livegang. Dort sind sie aber Pflicht, weil sie genau das Versprechen untergraben, mit dem Sichtwort sich abheben will: Datenschutz.
