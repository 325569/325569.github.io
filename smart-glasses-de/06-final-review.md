# Abschlussbericht: Smart Glasses für den deutschen Markt (Arbeitsname „Sichtwort“)

> Datum: 24.11.2026
> Geprüft: 01-research.md, 02-strategy.md, 03-copywriting.md, 04-prototype/index.html, 05-qa-report.md

---

## Zusammenfassung

Im deutschen Smart-Glasses-Markt ist 2026 nicht die Brille das Problem, sondern die Kamera. Meta beherrscht weltweit rund 69 % des Marktes (IDC). In Deutschland laufen gleichzeitig eine Strafanzeige gegen Hersteller und Händler, eine Verbotsdebatte und erste kommunale Verbote. 76 % der Deutschen wollen nicht mit Smart Glasses gefilmt werden (Bitkom). Das Team leitet daraus eine klare Position ab: **keine eigene Hardware, sondern ein kamerafreier KI-Arbeitsassistent auf fremden Brillen** – für mehrsprachige Produktionsteams im Mittelstand, mit Unterlagen für Betriebsrat und Datenschutz im Paket. Der erste Markt sind Lebensmittel- und Verpackungsbetriebe mit 50–500 Beschäftigten in Baden-Württemberg und Bayern. In der Lebensmittelherstellung haben fast 44 % der Beschäftigten keinen deutschen Pass.

Die Kette von Recherche über Strategie und Copy bis zum Prototyp ist schlüssig. Im Vergleich zum GridMind-Projekt sind offene Annahmen diesmal von Anfang an markiert, und die Website behauptet nichts, was es noch nicht gibt. **Trotzdem steht alles auf ungeprüften Annahmen.** Niemand hat mit einem Werksleiter, einem Betriebsrat oder einer Person an der Linie gesprochen. Ob die Hardware im Werk überhaupt eingesetzt werden darf (Schutzbrillenpflicht) und ob Spracherkennung in einer lauten Halle gut genug funktioniert, ist offen. **Fazit: ein guter Ausgangspunkt für eine Validierung, noch kein Geschäftsplan.**

---

## Überblick

| Phase | Ergebnis | Status |
|---|---|---|
| 01 Recherche | Markt, Datenschutzdebatte in DE, 6 Wettbewerber, 4 Zielgruppen, Recht (DSGVO, KUG, BetrVG, AI Act), ~20 Quellen | Fertig. Schätzungen und widersprüchliche Marktgrößen offen markiert |
| 02 Strategie | Positionierung, Zielgruppen-Priorität, Abgrenzung, 3-Phasen-Plan, 7 offene Annahmen | Fertig. Jede Aussage auf Recherche-Abschnitte zurückgeführt |
| 03 Copy | Slogan, Hero, Nutzen, Funktionen, Texte für zwei Entscheider, CTAs, 5-Folien-Pitch | Fertig. Eigene Regeln gegen Übertreibung, die Lehren aus GridMind umsetzen |
| 04 Prototyp | Responsive Landingpage mit interaktivem Sichtfeld (6 Sprachen inkl. RTL), Mobil-Menü, Demo-Formular | Fertig, veröffentlicht als privater Link |
| 05 QA | Technik-Test im Browser, Abgleich mit Copy und Strategie | 2 🔴 (nur für Livegang), 4 🟡, ansonsten bestanden |

---

## Stärken

1. **Die Positionierung nutzt die deutsche Besonderheit, statt gegen sie zu kämpfen.** Kamerafreiheit ist kein Verzicht, sondern das Verkaufsargument genau dort, wo andere Ärger haben: beim Betriebsrat und beim Datenschutz.
2. **Ehrlicher Umgang mit Unsicherheit.** Die Strategie hat einen eigenen Abschnitt „Annahmen, keine Fakten“. Die Copy hat Regeln gegen Überversprechen. Die Website sagt offen „Pilotphase“. Genau das fehlte bei GridMind (AEMO-Lizenz, Compliance im Präsens).
3. **Die zwei Entscheider sind erkannt.** In deutschen Betrieben entscheidet bei so einer Technik nicht nur die Werksleitung, sondern zwingend auch der Betriebsrat (§ 87 Abs. 1 Nr. 6 BetrVG). Copy und Website sprechen beide direkt an.
4. **Realistischer Wettbewerbsblick.** Kein Angriff auf Meta im Privatkundenmarkt, Logistik bewusst erst später wegen TeamViewer, Pflege bewusst zurückgestellt wegen Gesundheitsdaten.
5. **Der Prototyp ist technisch sauber und zeigt die Idee in Sekunden:** Ein Arbeitsschritt im Sichtfeld, umschaltbar von Deutsch bis Arabisch. Die drei QA-Kritikpunkte von GridMind sind von Anfang an vermieden.

---

## Schwachstellen

1. **Null Primärforschung.** Die Schmerzpunkte (Einarbeitung, Sprachbarrieren, keine Hand frei) sind aus Statistiken abgeleitet. Es ist nicht belegt, dass Werksleitungen dafür zahlen würden oder dass Mitarbeitende eine Brille acht Stunden lang tragen *wollen*. Laut Bitkom kommt für 52 % das Tragen von Smart Glasses nicht infrage.
2. **Die Hardware passt womöglich nicht ins Werk.** Even G2 ist nach unserer Recherche keine zertifizierte Schutzbrille. In Bereichen mit Schutzbrillenpflicht fällt sie aus. Offen sind außerdem Tragekomfort über eine Schicht, Akkulaufzeit im Dauerbetrieb und Kosten für Korrekturgläser bei Brillenträgern.
3. **Das technische Kernversprechen ist unbewiesen.** Das Even-SDK liefert nur Roh-Audio. Spracherkennung und Übersetzung in einer lauten Halle, EU-gehostet und ohne Speicherung, müssen wir selbst lösen. Das ist der eigentliche Produktkern und bisher nur Behauptung.
4. **Mikrofon ist auch ohne Kamera ein Datenschutzthema.** Die Übersetzung verarbeitet die Sprache von Kolleg:innen. Ob Push-to-Talk und „keine Speicherung“ rechtlich ausreichen, ist nicht geprüft.
5. **Abhängigkeit von einem kleinen Hardware-Hersteller.** Das Enterprise SDK von Even Realities ist zwei Wochen alt (10.11.2026). Preise, Schnittstellen und Lieferfähigkeit liegen nicht in unserer Hand.
6. **Keine Zahlen zur Wirtschaftlichkeit.** Preis pro Brille und Monat, Kosten für Spracherkennung und Übersetzung und der Gegenwert für den Betrieb (kürzere Einarbeitung, weniger Fehler) sind nicht beziffert. Eine deutsche Marktgröße gibt es nicht. Allein die Hardware kostet rund 699 € pro Arbeitsplatz.
7. **Wettbewerbsreaktion unterschätzt?** TeamViewer (deutscher MDAX-Konzern, im Mittelstand bekannt) könnte einen kamerafreien Modus mit Übersetzung nachrüsten. Meta hat mit Ray-Ban Meta Audio gerade selbst eine kamerafreie Brille gebracht.
8. **Website noch nicht livefähig** (QA 🔴): Google Fonts werden extern geladen, und Impressum sowie Datenschutzhinweise fehlen. Für eine Datenschutz-Marke wäre ein Livegang so ein Glaubwürdigkeitsproblem.

---

## Nächste Schritte (nach Priorität)

1. **10–15 Gespräche vor Ort** in Lebensmittel- und Verpackungsbetrieben in BW/Bayern, jeweils mit Werksleitung, Fachkraft für Arbeitssicherheit, Betriebsrat und 2–3 Mitarbeitenden an der Linie. Ziel: Ist der Schmerz echt? Wer zahlt wie viel? Würden die Leute die Brille tragen?
2. **Arbeitsplatz-Check zur Schutzbrillenpflicht** in genau diesen Betrieben. Wie viele Arbeitsplätze kommen überhaupt infrage? Wenn es zu wenige sind, ändert sich die Zielbranche.
3. **Technischer Machbarkeitstest (2–4 Wochen):** Even G2 plus EU-gehostete Spracherkennung und Übersetzung, getestet bei echtem Hallenlärm. Messen: Erkennungsrate, Verzögerung, Akkulaufzeit über eine Schicht.
4. **Rechtliche Ersteinschätzung** durch eine auf Datenschutz und Arbeitsrecht spezialisierte Kanzlei: Mikrofon und Umstehende, Inhalt der Muster-Betriebsvereinbarung, Gerüst für die Datenschutz-Folgenabschätzung.
5. **Kontakt zu Even Realities** über das Enterprise-Partnerprogramm: Konditionen, Mengenpreise, Lieferzeiten, Support in Deutschland. Parallel prüfen, welche zweite Plattform realistisch ist.
6. **Einfaches Preis- und Kostenmodell:** Kosten pro Brille und Monat (Spracherkennung, Hosting, Support) gegen den Wert für den Betrieb. Erst danach eine Preisspanne in Gespräche mitnehmen.
7. **Website-Fixes vor jedem Livegang:** Schriften selbst hosten, Impressum und Datenschutzerklärung ergänzen, die 🟡-Punkte aus der QA umsetzen (vor allem „In jeder Sprache“).
8. **Marke prüfen:** Ist „Sichtwort“ als Marke (DPMA/EUIPO) und als Domain frei?

---

**In einem Satz:** Die Idee trifft einen echten deutschen Nerv und ist ehrlich aufgeschrieben. Ob sie trägt, entscheiden aber drei Dinge, die noch niemand geprüft hat: Wollen Betriebe und Mitarbeitende das, darf die Brille ins Werk, und funktioniert die Übersetzung in der Halle?
