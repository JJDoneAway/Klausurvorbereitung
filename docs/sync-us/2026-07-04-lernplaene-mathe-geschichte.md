# Lernpläne Mathematik (9.7.) & Geschichte (10.7.) — sync-us interview
Date: 2026-07-04 · Status: completed · Goal: Lernplan Geschichte für Ben nach dem bewährten Baum-Prinzip, mit den Verbesserungen aus der SoWi-Retro. (Mathe: bewusst keine Vorbereitung.)

## Summary / key decisions
- Ausgangslage: SoWi-Klausur am 3.7. lief gut. Baum-Ansatz bleibt gesetzt.
- Reale Lernkapazität: 3,5 h/Tag nominal, davon ~2 h effektiv → Pläne auf 2 h effektive Zeit dimensionieren.
- Verbesserungen (aus Retro, gesetzt):
  1. Original-Abituraufgaben NRW + Lerninhalte aus dem Internet dazuladen.
  2. Passende Quellentexte aus dem Internet dazuladen.
  3. Karteikarten-Zusammenfassung je Station = zentrales Inhalts-Dokument (nicht nur Plan).
  4. Aufgabenverständnis trainieren (Operatoren: Was verlangt „Analyse" genau?) — war Problem in der Klausur.
  5. Zeitmanagement in der Klausur trainieren — war Problem in der Klausur.
- Termine: Mathematik Mi 9.7.2026, Geschichte Do 10.7.2026 → nur 1 Tag Abstand, Pläne überlappen.
- Priorität: **Nur Geschichte.** Mathe-Klausur (Do 9.7.) wird ohne Vorbereitung mitgeschrieben — reine Klausurerfahrung (Lücken zu groß, Klausurnoten zählen an der Privatschule nicht in die Abi-Note).
- Kalender: Sa 4.7. (heute) Setup + YouTube-Einstieg · So 5.7.–Mi 8.7. = 4 Lerntage × 2 h effektiv · Do 9.7. Mathe-Klausur · Fr 10.7. Geschichte-Klausur.
- Klausurformat: immer eine alte NRW-Abiturklausur, gestellt auf **135 min**. Blaupause mit Erwartungshorizont liegt vor (Abi 2024 GK HT 3).
- Moodle: kein direkter Connector verfügbar. Optionen: (a) manueller Export der Kursinhalte in den Repo-Ordner, (b) Skript-Download über Moodle-Web-Service-API mit Bens Zugangsdaten (falls Schule die Mobile-App-Schnittstelle aktiviert hat).

## Entschieden (Kurzfassung)
- Thema: **Weimarer Republik** — Schwerpunkt Zerstörung der Republik / Ära Brüning 1930–33, Krisenjahre 1919–23 als Fundament.
- Klausur: originale NRW-Abi-GK-Klausur der letzten Jahre, 135 min, Aufgabenart A oder B unbekannt → beides trainieren.
- Ziel: gute Note (≥ 11 Punkte); Geschichte wird schriftliches Abifach 2027 → alles wiederverwendbar bauen.
- Kalender: So 5.7.–Mi 8.7. je 2 h effektiv, Mi = volle Generalprobe (~3 h, bewusste Ausnahme), Do 9.7. nur leichter Karten-Block nach der Mathe-Klausur, Fr 10.7. Klausur.
- Karteikarten: druckbares PDF (echte Karten zum Ausschneiden), Markdown als Quelle.
- Korrektur: Selbstkorrektur mit Checklisten je Aufgabentyp (kein Claude-Feedback-Loop).
- Baseline: Ben hat die Dezember-Klausur nicht mitgeschrieben und hat Lücken → 10.7. ist seine **erste Geschichte-Klausur im Abi-Format**. Selbsttest am Tag 1 kalibriert die Tiefe; Express-Pfad als Fallback; Format-Training ist Pflicht.

## Open branches
(keine — Interview abgeschlossen)

## Nachtrag 4.7. abends — Repo umstrukturiert
Repo umbenannt in `Klausurvorbereitung`. Neue Struktur: Root nur `Lernpfad.md` (SoWi) + `Lernpfad_Geschichte.md` (+ Konfiguration). `sowi/` (Aufgabenstellung, Erwartungshorizont, Studienbericht, `material/`), `geschichte/` (Karteikarten, Generalprobe, Druck-PDF, `material/weimar` + `material/klausuren`), `archiv/unsorted/`, `docs/sync-us/`. Pfad-Angaben in älteren Protokoll-Einträgen unten (`content/…`) sind historisch.

## Build-Tasks — ERLEDIGT am 4.7.
1. ✅ Material sortiert: 21 Weimar-Dateien + 2 Original-Abiturklausuren (2019 GK Karikatur-Interpretation, 2024 GK Darstellungsanalyse 1848, beide mit Erwartungshorizont) → `content/geschichte/`.
2. ✅ Netz-Recherche: offizielle NRW-Klausuren nur hinter Schul-Login → Fallback umgesetzt: eigene Generalprobe im exakten Abi-Format (`Generalprobe_Klausur_Geschichte.md`), Aufgabenart A, Karikatur „Dr. Brüning" (Beier-Red, Eulenspiegel Jan. 1931 — liegt als PNG im Material, Beschreibung via geschichte-abitur.de verifiziert), mit vollem Erwartungshorizont + Notenschlüssel.
3. ✅ `Lernpfad_Geschichte.md`: Baum (Stamm „Warum stirbt die erste deutsche Demokratie?", 4 Äste + Krone), Tagesplan Sa–Fr, Operatoren-Dekoder, Zeitstrategie 135 min, Selbstkorrektur-Checklisten, Selbsttest, Express-Pfad, YouTube-Liste für heute Abend.
4. ✅ `Karteikarten_Geschichte.md` (42 Karten, Codes H/B/C/D/E/F) + `karteikarten_geschichte_druck.pdf` (A4, 8 Karten/Blatt, Rückseiten für Duplex-Druck lange Kante gespiegelt, Schnittlinien).
2. Mathe: Welche Themen kommen dran? Wie groß sind die Lücken? (zurückgestellt bis Geschichte steht)
2a. Moodle-Zugang: manueller Export oder Skript-Download? Moodle-URL der Schule?
3. Stufe/Kursart bestätigen (vermutlich Q1 GK, Abi-Jahrgang 2027 — aus SoWi-Repo abgeleitet)
4. Zeitaufteilung: Wie werden die Tage 4.7.–10.7. zwischen Mathe und Geschichte aufgeteilt? (Wochenende = mehr Zeit?)
5. Karteikarten-Format: Markdown-Dokument, druckbare Karten, Anki?
6. Repo-/Ordnerstruktur: gleiches Repo mit Unterordnern mathe/ und geschichte/?
7. Baum-Format für Mathe: Wissens-Baum vs. Fertigkeiten-Baum (Rechnen üben ≠ Text verstehen)
8. Probeklausur unter Zeitdruck einplanen? Wann?
9. Was hat bei SoWi die 1,5 h Differenz (3,5 h → 2 h effektiv) gekostet? Lässt sich das verbessern?

## Q&A log

### Q14 — Nachtrag Ausgangslage (Korrektur zu Q4/Q11)
- Asked: — (vom Nutzer nachgeliefert)
- Decision: **Ben hat die Dezember-Klausur (Abi 2024, 1848) NICHT mitgeschrieben und hat Lücken.**
- Konsequenz: Die Klausur am 10.7. ist Bens **erste Geschichte-Klausur im Abi-Format**. Format-Training (tägliche Übung unter Zeit + volle Generalprobe am Mi) ist damit Pflichtteil, nicht Kür. Baseline eher „lückig" → Selbsttest Tag 1 entscheidet zwischen Normalplan und Express-Pfad. Erwartung kalibrieren: ≥ 11 Punkte bleibt das Ziel, aber ohne jede Klausurerfahrung im Fach wären auch 8–10 Punkte ein Erfolg.
- Flags: —

### Q13 — Aufgabenart der Klausur
- Asked: Aufgabenart A (Quelleninterpretation) oder B (Darstellungsanalyse)?
- Recommended: Bei Unklarheit beides trainieren (gemeinsames Gerüst + Unterschieds-Karte).
- Decision: „Weiß ich nicht, aber es wird **definitiv eine originale Abi-GK-Klausur aus den letzten Jahren** sein."
- Konsequenz: (a) Beide Aufgabenarten trainieren — Gerüst ist identisch (Analysieren → Einordnen → Beurteilen). (b) **Kandidatenpool eingrenzbar**: NRW-Abi-GK-Klausuren der letzten Jahre mit Weimar-Bezug sammeln (Netz + `GE19_xGK…pdf` prüfen) — die echte Klausur ist wahrscheinlich eine davon. Generalprobe aus diesem Pool wählen.
- Flags: —

### Q12 — Korrektur-Loop
- Asked: Soll ich Bens Übungsantworten gegen den Erwartungshorizont korrigieren?
- Recommended: Ja, täglich + Generalprobe.
- Decision: **Nein, Selbstkorrektur reicht.**
- Konsequenz: Der Plan bekommt pro Aufgabentyp eine **Selbstkorrektur-Checkliste** im Stil des Erwartungshorizonts (abhakbare Kriterien + Punkte-Logik), damit die Selbstkorrektur trotzdem greift.
- Flags: —

### Q11 — Ausgangslage Geschichte
- Asked: Note der letzten Geschichte-Klausur + Präsenz des Weimar-Stoffs?
- Recommended: — (Kalibrierungsfrage)
- Decision: **„Weiß ich nicht genau"** — Baseline unbekannt.
- Konsequenz: Plan kalibriert sich selbst: Tag 1 (So 5.7.) beginnt mit 15-min-Selbsttest (Kernfragen Weimar). Ergebnis steuert Tiefe: gut → Handwerks-Fokus; lückig → Inhalts-Fokus mit Express-Pfad (wie bei SoWi).
- Flags: Letzte Klausurnote unbekannt → Ben kann sie nachliefern, ändert ggf. Gewichtung Tag 2.

### Q10 — Probeklausur / Klausurtraining
- Asked: Wie trainieren wir die Klausursituation?
- Recommended: Volle Generalprobe am Mi 8.7.
- Decision: **Volle Generalprobe am Mi 8.7.** (135 min am Stück + Selbstkorrektur gegen Erwartungshorizont; Mi wird bewusst ~3-h-Tag). So–Di: jeden Tag EINE Teilaufgabe unter Teilzeit (So: Analysieren 35 min, Mo: Erläutern/Einordnen 45 min, Di: Stellung nehmen 35 min).
- Konsequenz: Ich brauche eine passende alte NRW-Abiturklausur mit Weimar-Thema + Erwartungshorizont als Generalprobe-Klausur (aus dem Netz laden, Retro-Punkt). `GE19_xGK…pdf` auf Thema prüfen.
- Flags: —

### Q9 — Karteikarten-Format
- Asked: In welchem Format soll die Karteikarten-Zusammenfassung je Station entstehen?
- Recommended: Zentrales Markdown-Dokument.
- Decision: **Druckbare echte Karteikarten (PDF)** — zum Ausdrucken und Ausschneiden, physisches Selbstabfragen.
- Konsequenz: Ich baue (a) die Inhalte als Markdown (Quelle, versionierbar) und (b) daraus ein druckfertiges PDF im Karteikarten-Layout (Vorderseite Frage / Rückseite Antwort, beidseitiger Druck oder Falt-Layout). Drucker muss vorhanden sein.
- Flags: Papierformat/Drucker-Setup (A4 beidseitig ok?) → Johannes/Ben, kläre ich beim Bauen mit Standardannahme A4 beidseitig, Schnittmarken.

### Q8 — Erfolgsmaßstab Geschichte
- Asked: Was ist der Erfolgsmaßstab für die Geschichte-Klausur?
- Recommended: Klausurhandwerk meistern (Operatoren + Zeit).
- Decision: **Gute Note (≥ 11 Punkte)** UND: **„Ich mache nächstes Jahr Geschichte GK schriftlich"** → Geschichte ist schriftliches Abiturfach 2027. Diese Klausur = direktes Abi-Training.
- Konsequenz: Beides zählt — Inhaltstiefe (Brüning/Präsidialkabinette detailliert) UND Klausurhandwerk (Operatoren, Zeitbudget, Erwartungshorizont-Logik). Alles, was wir jetzt bauen (Baum, Karteikarten, Operatoren-Dekoder), ist fürs Abi wiederverwendbar.
- Flags: —

### Q7 — Aufteilung Geschichte/Mathe + Kalender-Korrektur
- Asked: Aufteilung der Lerntage zwischen Geschichte und Mathe?
- Recommended: Geschichte zuerst, dann Mathe-Triage.
- Decision (Korrekturen des Nutzers):
  - **Heute ist Samstag, 4.7.** (nicht Freitag). Heute: nur Vorbereitung, kein Lernen — „maximal YouTube-Videos" (Sofa-Einstieg wie bei SoWi Tag 1).
  - **Mathe wird NICHT gelernt** — Ben schreibt die Mathe-Klausur nur mit, um Klausurerfahrung zu sammeln. Voller Fokus auf Geschichte.
  - Kontext: **Privatschule, Klausurnoten fließen nicht in die Abi-Note ein** → Druck niedriger, Klausuren = Übungsfeld fürs Abitur 2027.
- Konsequenz — korrigierter Kalender:
  - Sa 4.7. (heute): Setup durch uns + abends YouTube-Einstieg (kein Stift)
  - So 5.7. – Mi 8.7.: 4 Lerntage × 2 h effektiv = 8 h Geschichte
  - Do 9.7.: Mathe-Klausur (nur mitschreiben) → danach ggf. leichter Geschichte-Block (Karteikarten)
  - Fr 10.7.: Geschichte-Klausur
- Flags: Mathe-Branch geschlossen. Kein Mathe-Lernplan nötig.

### Q6 — Zeitbudget 4.7.–10.7.
- Asked: Wie viel Lernzeit pro Tag ist realistisch, gibt es blockierte Tage?
- Recommended: Wie bei SoWi (~3,5 h nominal → 2 h effektiv)
- Decision: „Jeden Tag die zwei effektiven Stunden." → Planungsgrundlage (nach Kalender-Korrektur in Q7): **2 h effektiv × 4 Lerntage (So 5.7. – Mi 8.7.) = 8 h**, plus leichter Karten-Block Do 9.7. abends. Heute (Sa 4.7.) kein Lernen. Keine blockierten Tage genannt.
- Konsequenz: Stationen auf 25–40-min-Häppchen dimensionieren (ADS-gerecht wie bei SoWi), pro Tag 3–4 Häppchen.
- Flags: Mi 9.7. ist vormittags Mathe-Klausur → an dem Tag nur leichter Geschichte-Block (Wiederholung Karteikarten, keine neuen Inhalte).

### Q5 — Geschichte: Klausurdauer
- Asked: Wie lange dauert die Geschichte-Klausur am 10.7.?
- Recommended: 135 min (Q1-GK-üblich)
- Decision: **135 min**
- Konsequenz: Zeit-Budget-Training auf 135 min: ~10 min Lesen/Markieren, ~35 min Aufgabe 1, ~45 min Aufgabe 2, ~35 min Aufgabe 3, ~10 min Puffer/Korrektur.
- Flags: —

### Q4 — Geschichte: Klausurformat (durch Material-Exploration gelöst)
- Asked: Wie ist das Format der Geschichte-Klausur?
- Decision: „Die Klausur ist immer eine alte Abiturklausur." Alle Unterlagen liegen in `content/unsorted/`.
- Befund aus Exploration:
  - `GE(11.)121225_…pdf` = **Original NRW-Abitur 2024, GE GK HT 3** (Thema 1848/Nationalbewegung) **inkl. Erwartungshorizont + Punkteraster** — die Klausur vom 12.12.25, die **Ben nicht mitgeschrieben hat** (Korrektur siehe Q14; dient nur als Format-Blaupause). Format: 3 Aufgaben (1. Analysieren 26 P, 2. Erläutern + charakterisieren 28 P, 3. Kritisch Stellung nehmen 26 P) + Darstellungsleistung 20 P = 100 P. Aufgabenart B (Analyse von Darstellungen) — es gibt auch Aufgabenart A (Quelleninterpretation).
  - `GE19_xGK_G_HT_GG_…pdf` = weitere Original-Abiturklausur (2019 GK), noch nicht gesichtet.
  - Materiallage Weimar-Schwerpunkt gut: bpb „Zerstörung der Demokratie 1930–33", WWK 1929, „3 große Fehler", Karikatur Scheitern WR, Spoerer/Streb WWK, Evans, Kershaw (Hitler), Young-Plan, Dawes-Plan-Propaganda, Hyperinflation, Ruhrbesetzung, Dolchstoßlegende.
  - Ordner enthält auch Bens eigene Antworttexte (Hitler-Prozess, Bismarck-Mythos, Bündnissysteme) → Niveau-Anhaltspunkt: solide Wiedergabe, eher knapp, wenig Quellenbelege/Zitate.
  - Ordner umfasst auch Nicht-Weimar-Stoff (1848, Bismarck, Kaiserreich, WWI) und Fremd-Stoff (Genetik, Skalarprodukt) → Sortierung nötig.
- Flags: Klausurdauer unklar → Ben. Ist die Klausur am 10.7. Aufgabenart A (Quelle) oder B (Darstellung) oder unbekannt? → Ben

### Q3 — Geschichte: Eingrenzung Weimarer Republik
- Asked: Welcher Abschnitt der Weimarer Republik ist klausurrelevant?
- Recommended: — (Mehrfachauswahl aus Phasen)
- Decision: **Krisenjahre 1919–1923 + Scheitern 1929–1933.** Zuletzt behandelt: „Zerstörung der Weimarer Republik, Ära Brüning 1930–33" → das ist der wahrscheinliche Klausur-Schwerpunkt (zuletzt Behandeltes = meist Kern der Klausur). Krisenjahre 1919–23 als Fundament/Vergleichsfolie.
- Flags: —

### Q2 — Geschichte: Thema
- Asked: Welche Themen kommen in der Geschichte-Klausur am 10.7. dran?
- Recommended: — (offene Themenfrage, Optionen aus typischem NRW-Q1-Stoff)
- Decision: **Weimarer Republik**
- Flags: Eingrenzung nötig → welcher Abschnitt? (Revolution 1918/19, Krisenjahr 1923, Goldene Zwanziger, Scheitern 1930–33) → Ben

### Q1 — Priorisierung Mathe vs. Geschichte
- Asked: (implizit, bei Klärung vor Themenfrage)
- Recommended: Beide parallel planen wegen 1 Tag Abstand.
- Decision: „Lass uns erst auf Geschichte fokussieren, da Ben in Mathe zu große Lücken hat. Wenn Geschichte vom Umfang her überschaubar ist, können wir nachher noch Mathe machen."
- Flags: Mathe-Lücken sind groß → wenn Mathe drankommt, realistische Ziele setzen (Schadensbegrenzung statt Vollabdeckung?) → Johannes

### Q0 — Retro-Input (aus Manöverkritik, vorab geliefert)
- Asked: — (vom Nutzer proaktiv mitgeteilt)
- Decision:
  - Baum war „richtig gute Idee", half Verständnis + Übersicht, verhinderte Rabbit Holes → beibehalten.
  - Klausur gut gelaufen bis auf: Zeitproblem + Verständnisproblem bei Aufgabenstellungen (z. B. „Was muss man bei einer Textanalyse genau machen?").
  - Fehlte: Karteikarten-Zusammenfassung je Station als zentrales Inhalts-Dokument.
  - Neu dazuladen: Original-Abituraufgaben NRW, Lerninhalte + passende Quellentexte aus dem Internet.
  - 3,5 h gelernt/Tag, ~2 h effektiv.
- Flags: —

## Open flags (pending input)
- Mathe-Themenliste → Ben / Lehrer
- Geschichte-Themenliste → Ben / Lehrer
