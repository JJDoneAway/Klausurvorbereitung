# 📱 Anleitung — Mathetrainer auf dem iPad starten

**TL;DR:** Ben startet den Trainer auf dem iPad am einfachsten über die **Claude-App** (Tab „Code"), wählt das GitHub-Repo `Klausurvorbereitung` und tippt **`/mathetrainer`**. Der Trainer läuft in der Cloud, merkt sich den Fortschritt und speichert ihn automatisch zurück ins Repo — auf jedem Gerät geht es am gleichen Punkt weiter. Einmalige Einrichtung macht Papa (Claude-Plan + GitHub verbinden). Kein Terminal, keine Installation von Programmen.

---

## Teil 1 — Einmalige Einrichtung (macht Papa, ~10 min)

1. **Claude-Plan:** Es braucht einen bezahlten Claude-Plan (Pro oder Max). Claude Code im Browser/in der App ist Teil davon (aktuell als „Research Preview").
2. **GitHub verbinden:** Am Rechner oder im Browser `claude.ai/code` öffnen → dem Hinweis folgen und die **Claude-GitHub-App** installieren → Zugriff auf das Repo `JJDoneAway/Klausurvorbereitung` erlauben.
3. **Fertig.** Das Repo ist schon auf GitHub (mit Skill, Aufgabenbank, Fortschrittsdatei). Mehr ist nicht nötig.

> Ben kann zu Beginn einfach **Papas Claude-Account** auf dem iPad benutzen — dann entfällt jede weitere Einrichtung. Ein eigener Account für Ben ist möglich (siehe Teil 4), aber nicht nötig.

## Teil 2 — Auf dem iPad starten (Weg A: Claude-App, empfohlen)

1. **Claude-App** aus dem App Store aufs iPad laden und mit dem Account anmelden.
2. Unten den Tab **„Code"** öffnen.
3. Auf **„Neue Session"** (oder „+") tippen und als Repository **`Klausurvorbereitung`** wählen, Branch **`main`**.
4. Warten, bis die Cloud-Session bereit ist (das Repo wird automatisch geladen).
5. Ins Textfeld **`/mathetrainer`** tippen und abschicken.
6. Der Trainer begrüßt Ben, zeigt den Stand und stellt die erste Aufgabe. Los geht's.

## Teil 2b — Alternative (Weg B: Browser)

1. Im iPad-Safari/Chrome **`claude.ai/code`** öffnen und anmelden.
2. Unter dem Eingabefeld das Repo **`Klausurvorbereitung`** und Branch `main` wählen.
3. **`/mathetrainer`** eintippen und abschicken.

*(Der Browser funktioniert, ist aber auf dem iPad etwas hakeliger als die App. Deshalb: App bevorzugen.)*

## Teil 3 — Täglicher Ablauf

1. Claude-App → **Code** → die `Klausurvorbereitung`-Session öffnen (oder neu starten) → **`/mathetrainer`**.
2. Aufgabe lesen → **auf Papier rechnen** → nur **`A`, `B` oder `C`** tippen.
   - `E` = Erklärung statt Antworten.
   - `Stopp` = Sitzung beenden.
3. Nach `Stopp` speichert der Trainer den Fortschritt automatisch zurück ins Repo.
4. **Nächstes Mal** — egal ob iPad, anderer Rechner oder anderer Account — geht es am exakt gleichen Punkt weiter. Das ist das „Portieren": Der Fortschritt reist über GitHub mit.

## Teil 4 — Eigener Claude-Account für Ben (optional)

Wenn Ben einen **eigenen** Claude-Account nutzen soll (statt Papas):

1. **GitHub:** Papa fügt Bens GitHub-Namen als **Collaborator** mit **Write**-Rechten hinzu (Repo → Settings → Collaborators → Add).
2. **Claude:** Ben legt einen eigenen Claude-Account (Pro/Max) an und verbindet in `claude.ai/code` seinen **eigenen** GitHub-Account.
3. Danach sieht Ben das Repo `Klausurvorbereitung` in seiner Code-Ansicht und kann lesen **und** speichern (Fortschritt pushen).

## Wenn die Mathe-Formeln als „Code-Text" erscheinen

Es kann sein, dass Formeln nicht schön gesetzt, sondern als Rohtext erscheinen (z.B. `\begin{pmatrix}2\\1\\-3\end{pmatrix}`) — das ist ein bekannter Darstellungs-Bug. **Sag dem Trainer dann einfach:** „Bitte Formeln als Klartext, nicht als LaTeX." Der Trainer schaltet dann auf eine gut lesbare Schreibweise um (z.B. Vektor als `(2 | 1 | -3)`). Die Aufgaben bleiben dieselben.

## Kurz-Spickzettel

| Ich will … | Ich tippe … |
|---|---|
| Starten / weitermachen | `/mathetrainer` |
| Antworten | `A` / `B` / `C` |
| Erklärung sehen | `E` |
| Formeln als Klartext | „Formeln bitte als Klartext" |
| Aufhören | `Stopp` |
