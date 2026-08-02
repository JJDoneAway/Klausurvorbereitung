# 🧭 Spec — Mathetrainer Vektorrechnung (GK-Abi-2027 NRW)

**TL;DR:** Ben braucht einen interaktiven Mathetrainer für Vektorrechnung, der ihn **genau auf den GK-Abitur-2027-Erwartungshorizont in NRW** vorbereitet — keinen Schritt weiter. Der Trainer ist eine Claude-Code-Skill `/mathetrainer` in diesem Git-Repo plus eine Fortschrittsdatei. Er führt Ben in **8 Modulen × 3 Stufen** (7 Themenmodule M1–M7 + Werkzeugmodul M4b Kreuzprodukt, einfach → Abiturniveau) Sprosse für Sprosse hoch, ohne Abkürzung. Pro Aufgabe zeigt Claude die Aufgabe in schöner Notation **ohne die Antwortoptionen** (Anti-Anker); Ben rechnet **auf Papier**, blendet mit `L` die Optionen A/B/C ein und tippt dann `A/B/C` (Multiple Choice) oder `E` für eine Erklärung. Der Umfang ist auf die **Themenliste der Lehrerin ∩ GK-Abi-2027** begrenzt; Abstände, Hesse-Normalenform, Vektorraum/Basis und reine Beweise fallen raus. Portabilität auf einen anderen Claude-Account läuft über `git pull` (der Trainer committet+pusht die Fortschrittsdatei selbst).

---

## Problem Statement

Ben ist in der Q1 (Privatschule NRW, Abitur 2027). Mathe-Grundkurs. Er will Vektorrechnung so üben, dass er **exakt die Anforderungen der GK-Abiturprüfung** trifft — nicht mehr und nicht weniger. Bisher fehlt ihm:

- ein Weg, der ihn **Level für Level ohne Abkürzung** von einfach bis Abiturniveau bringt,
- eine **wiederaufnehmbare** Übungsform, die sich seinen Lernstand merkt,
- die Sicherheit, dass er **nichts Überflüssiges** lernt (kein Stoff über den GK-Horizont hinaus),
- eine Lösung, die er auch **auf einem anderen Claude-Account** weiterführen kann.

Offene Frage des Nutzers war zusätzlich: „Kann man eine Claude-Session auf einen anderen Account portieren?" — Antwort: Eine laufende Session **nicht**, aber die Trainer-Anleitung und der Lernstand als Dateien schon (über git).

## Solution

Ein Trainer als **Claude-Code-Skill `/mathetrainer`** in diesem Repo. Claude ist der live-adaptive Tutor. Der Lernstand liegt in einer **Fortschrittsdatei**. „Portieren" heißt: auf dem anderen Account das Repo `git pull`en und `/mathetrainer` starten — der Trainer macht am exakten Punkt weiter.

Ablauf einer Sitzung:

1. Ben startet `/mathetrainer`.
2. Claude liest die Fortschrittsdatei und zeigt ein kurzes Dashboard (erledigte Sprossen, aktuelle Position, Top-Fehler).
3. Claude stellt die nächste Aufgabe in schöner mathematischer Notation (KaTeX im Browser/IDE) — **noch ohne Antwortoptionen**, damit Ben nicht geankert wird. Darunter: `L` = Optionen A/B/C einblenden, `E` = Erklärung, `Stopp` = Stand sichern & pausieren.
4. Ben rechnet **auf Papier**, blendet mit `L` die drei Optionen ein und tippt dann `A`, `B` oder `C` — oder `E` für eine Erklärung, oder `Stopp` zum Pausieren. `L` ist der Normalfall und beeinflusst die Serie nicht.
5. Claude wertet aus, zeigt die vollständige Musterlösung und fragt: „War dein Weg sauber?".
6. Claude aktualisiert Serien-Zähler und Fortschrittsdatei und stellt die nächste Aufgabe.

Der Umfang folgt der **Themenliste der Lehrerin, abgeglichen mit den GK-Abi-2027-Vorgaben**. Aufgaben kommen aus drei Quellen: Buchaufgaben (Hinführung) → generierte Drills im Original-Stil (festigen) → echte + generierte Abi-Aufgaben (Schlussstein).

## User Stories

1. Als Schüler will ich immer eine Aufgabe mit 3 Antwortmöglichkeiten bekommen, damit ich mein Papier-Ergebnis mit einem Tastendruck melden kann.
1a. Als Schüler will ich, dass die Antwortoptionen A/B/C erst auf `L` erscheinen (nicht sofort), damit mich die vorgegebenen Zahlen beim Rechnen auf Papier nicht ankern.
2. Als Schüler will ich statt zu antworten auch eine Erklärung anfordern können, damit ich ein Thema erst verstehe, bevor ich es übe.
3. Als Schüler will ich auf Papier rechnen und trotzdem schöne, saubere Notation auf dem Bildschirm sehen, damit das Üben der echten Klausur entspricht.
4. Als Schüler will ich Level für Level ohne Abkürzung aufsteigen, damit ich Lücken nicht überspringe.
5. Als Schüler will ich, dass eine Stufe erst als bestanden gilt, wenn ich 2 Aufgaben in Folge im ersten Versuch richtig löse, damit „bestanden" wirklich Beherrschung heißt.
6. Als Schüler will ich, dass ein Fehler nur den Zähler der aktuellen Sprosse zurücksetzt und nicht den ganzen Fortschritt, damit ein Ausrutscher mich nicht weit zurückwirft.
7. Als Schüler will ich die Sitzung jederzeit pausieren und später fortsetzen, damit ich in mehreren kurzen Einheiten lernen kann.
8. Als Schüler will ich, dass der Trainer nur den GK-Abi-2027-Stoff übt, damit ich keine Zeit mit Überflüssigem verliere.
9. Als Schüler will ich, dass jede Aufgabe als „hilfsmittelfrei" oder „mit CAS" gekennzeichnet ist, damit ich beide Prüfungsteile richtig trainiere.
10. Als Schüler will ich, dass die falschen Antwortoptionen aus typischen Fehlern gebaut sind, damit ich aus einer falschen Wahl sofort meinen Fehler erkenne.
11. Als Schüler will ich zu jeder Aufgabe wissen, was der Operator verlangt (z.B. „berechnen" = Ansatz zeigen), damit ich in der Klausur die volle Punktzahl schreibe.
12. Als Schüler will ich, dass sich der Trainer meine typischen Fehler merkt und gezielt wiederholt, damit ich an meinen Schwächen arbeite.
13. Als Schüler will ich als Schlussstein eine echte Original-Abi-Aufgabe unter Klausurbedingungen (Zeit, Formelsammlung) lösen, damit ich weiß, ob ich prüfungsfit bin.
14. Als Schüler will ich ein Karteikarten-Set mit allen relevanten Formeln, damit ich schnell wiederholen kann.
15. Als Nutzer will ich den Trainer auf einem anderen Claude-Account fortsetzen können, damit ich nicht an ein Konto gebunden bin.
16. Als Nutzer will ich, dass der Trainer die Fortschrittsdatei selbst committet und pusht, damit der Sync ohne Handgriff passiert.

## Implementation Decisions

**Deep Modules (klar abgegrenzte, testbare Bausteine):**

- **Aufgabenbank** — liefert eine Aufgabe für (Modul, Stufe, Hilfsmittel). Enthält: einmalig aus den HEIC-Buchfotos extrahierte In-Scope-Aufgaben, Vorlagen für generierte Drills im Original-Stil, echte Abi-Aufgaben aus den PDFs. Jede Aufgabe getaggt mit Modul, Stufe (Grund/Standard/Abi), Hilfsmittel (hilfsmittelfrei/CAS), Operator und typischen Fehlern (für die MC-Distraktoren).
- **Fortschritts-Store** — liest/schreibt den Lernstand als JSON. Inhalt: erledigte Sprossen, aktuelles Modul + Stufe, Serien-Zähler, Fehlerprotokoll pro Thema. Schnittstelle: Stand lesen, Ergebnis verbuchen, Sprosse freischalten.
- **Sitzungslogik (Trainer-Schleife)** — Aufgabe wählen → in KaTeX **ohne Optionen** zeigen (Menü `L/E/Stopp`) → auf `L` die Optionen A/B/C einblenden → `A/B/C/E/Stopp` entgegennehmen → auswerten → Serie/Gate aktualisieren → Musterlösung → Selbsteinschätzung → nächste Aufgabe.
- **Operatoren-Dekoder** — Nachschlage-Baustein: Operator → was er verlangt. Quelle: `m_operatoren_ab_2023_angepasst_2026.pdf`.
- **Formel-Karteikarten** — generiertes Nachschlage-Set der In-Scope-Formeln.
- **Generalprobe** — echte Original-Abi-Aufgabe unter Klausurbedingungen + Korrektur.
- **Sync** — committet + pusht ausschließlich die Fortschrittsdatei.

**Architektur-Entscheidungen:**

- Laufzeit: Browser (claude.ai/code) oder IDE mit Mathe-Rendering → Aufgaben und Lösungen als KaTeX direkt im Chat.
- Hilfsmittel: CAS/MMS (Casio ClassPad II). Der Trainer übt auch die passenden CAS-Handgriffe (z.B. `solve`).
- Aufstiegsregel: **2 richtige in Folge im ersten Versuch** (ohne vorher `E`/Erklärung geöffnet) → Sprosse bestanden. Falsch oder vorher Erklärung → zählt nicht; ein Fehler setzt nur den Sprossen-Zähler auf 0, nie den Gesamtfortschritt.
- Tempo: offen, beherrschungsgetrieben, kein Termin. Richtwert ~20–30 min pro Sitzung.
- Antwort-Eingabe: nur `A/B/C` (keine Mathe-Eingabe), Optionen erst nach `L` sichtbar. Weg-Kontrolle über Musterlösung + ehrliche Selbsteinschätzung (`j` / kleiner Fehler / Ansatz gefehlt).
- Auto-Sync: Der Trainer darf die Fortschrittsdatei selbst committen+pushen — **bewusste Ausnahme von der globalen Regel „nie automatisch pushen", begrenzt auf genau diese Datei.**

**Schema Fortschrittsdatei (JSON):** Module M1–M7, je Stufe Status (offen/aktiv/bestanden), aktuelle Position, Serien-Zähler, `mc_rotation` (Rotations-Zähler für die Position der richtigen MC-Option), Fehlerprotokoll (Thema → Fehlertyp → Anzahl).

**Umfang (Themenliste Lehrerin ∩ GK-Abi-2027 + Werkzeugmodul Kreuzprodukt), 8 Module × 3 Stufen, streng der Reihe nach:**

| Modul | Inhalt | Tiefe |
|---|---|---|
| M1 | Vektor-Grundlagen & Betrag (Länge) | voll |
| M2 | Skalarprodukt & Winkel zwischen Vektoren | voll |
| M3 | Geraden aufstellen | voll |
| M4 | Lagebeziehung von Geraden (+ LGS) | voll |
| M4b | Kreuzprodukt (Vektorprodukt) — Werkzeug für Normalenvektoren | Werkzeug; **nur** orthogonale/Normalen-Vektoren, **nicht** Fläche/Volumen/Spat |
| M5 | Ebenen: Parameterform, Koordinatenform, Normalenvektor (per Kreuzprodukt oder LGS) | voll; **Normalenform nur überstreichen** |
| M6 | Lagebeziehung Gerade–Ebene / Durchstoßpunkt | voll |
| M7 | Schnittwinkel (Gerade–Gerade, Gerade–Ebene, Ebene–Ebene) | voll |

## Testing Decisions

Verifiziert wird der Trainer durch einen Trockenlauf, nicht durch Code-Tests:

- **Scope-Filter:** Über eine Sitzung darf **keine** Aufgabe zu Abständen, Hesse-Normalenform, Vektorraum/Basis oder reinen Beweisen erscheinen.
- **Aufstiegsregel:** 2 richtige in Folge schalten frei; eine falsche Antwort setzt nur den Sprossen-Zähler zurück, der Gesamtfortschritt bleibt.
- **MC-Distraktoren:** Zu einer Beispielaufgabe wird geprüft, dass jede falsche Option einem typischen Fehler entspricht.
- **MC-Position:** Über mehrere Aufgaben ist die richtige Option nicht immer A; sie folgt `mc_rotation mod 3` (A/B/C) und ist damit gleichmäßig verteilt.
- **Anti-Anker:** Direkt nach dem Stellen einer Aufgabe erscheinen keine Antwortoptionen; A/B/C werden erst nach Eingabe von `L` sichtbar.
- **Persistenz & Resume:** Nach `Stopp`, einem simulierten `git pull` und neuem `/mathetrainer` macht der Trainer an der exakten Sprosse weiter.
- **Rendering:** Aufgaben und Musterlösungen erscheinen als saubere KaTeX-Notation (Spaltenvektoren, Brüche, Wurzeln).
- **Hilfsmittel-Kennzeichnung:** Jede Aufgabe zeigt „hilfsmittelfrei" oder „mit CAS".

## Out of Scope

- **Themen außerhalb GK-Abi-2027-GK:** Abstände (Punkt–Gerade, Punkt–Ebene, windschiefe Geraden), Hesse-Normalenform, Spiegelungen, Volumen/Pyramiden, Vektorraum/Basis/Dimension, reine Geometrie-Beweise. Buchkapitel „X Abstände und Winkel" und „XII Beweisen in der Geometrie" werden entsprechend gefiltert.
- **Normalenform:** wird nur kurz überstrichen, keine eigene Übungs-Sprosse.
- **Andere Sachgebiete:** Analysis und Stochastik sind nicht Teil dieses Trainers.
- **Foto-Korrektur / Freitext-Eingabe:** bewusst nicht — Eingabe bleibt `A/B/C`.
- **Termin-Taktung:** kein Countdown auf ein Klausurdatum.
- **Bestehende Datei `Lernpfad_Mathe.md`:** bleibt unangetastet (altes Ebenen-Minimalprogramm).

## Open Questions

1. **`.gitignore` blockiert `.claude/`:** Eine Skill unter `.claude/skills/mathetrainer/` würde nicht mit gepusht — das bricht die Portabilität. **Empfehlung:** eine gezielte `.gitignore`-Ausnahme für `.claude/skills/mathetrainer/**` ergänzen, und/oder die schweren Inhalte (Aufgabenbank, Fortschrittsdatei, Karteikarten) unter dem bereits getrackten Ordner `mathematik/mathetrainer/` ablegen. Änderung an `.gitignore` braucht dein OK.
2. **Buchmaterial-Dichte:** ✅ Erledigt. Alle 15 Fotos katalogisiert in `mathematik/mathetrainer/aufgabenbank.md`. In-Scope-Aufgaben liegen in Kap. VIII (Geraden, S.302–303 → M1/M3/M4), Kap. IX (Ebenen, S.334–335 → M5/M6) und wenige in Kap. X (Schnittwinkel, S.368 → M7) und XII (Skalarprodukt, S.416 → M2). Für M1-Betrag und M2-Winkel gibt es kaum reine Buch-Aufgaben → Trainer ergänzt generiert. Kap. XI (Kreise & Kugeln) ist komplett außerhalb.
3. **Umfang Schnittwinkel Gerade–Ebene / Ebene–Ebene:** in GK-Abi-2027 enthalten, von der Lehrerin unter „Winkel zwischen Vektoren" subsumiert. Aktuell als volles Modul M7 geplant — bei Bedarf kürzbar.
