# 📐 Lernpfad Mathe-Minimalprogramm — Ebenen in 4 × 20 Minuten

**TL;DR:** Mathe-Klausur Do 9.7. (Kapitel IX „Ebenen", Lambacher Schweizer). Kein Vollprogramm — 4 Tage à **10 min Video + 10 min Übung direkt danach**. Ziel: die Standard-Rechenrezepte erkennen und Teilpunkte holen statt leeres Blatt. Die Übungen stehen hier im Dokument, mit kompletten Lösungen zum Selbstkontrollieren. CAS ist erlaubt — `solve` ist dein bester Freund.

**Die Logik:** Du kannst in 80 Minuten nicht Kapitel IX lernen. Du kannst aber 3 Rezepte lernen, die in fast jeder Ebenen-Klausur Punkte bringen: **Punktprobe → Skalarprodukt → Durchstoßpunkt.** Alles sind Einsetz-und-Ausrechnen-Rezepte — kein tiefes Verständnis nötig.

---

## 📅 DER PLAN (jeden Tag ~20 min, am besten vormittags — getrennt vom Geschichte-Block)

### ▢ TAG 1 — So 5.7. — Vektoren von null + Skalarprodukt
**▶️ Video (10 min):** [Grundlagen Vektoren (Analytische Geometrie) | simpleclub](https://www.youtube.com/watch?v=UKfKOPjOGio)

**✏️ Übung (10 min):**
**Rezept 1 — Vektor zwischen zwei Punkten:** „Spitze minus Fuß": $\vec{AB} = B - A$ (koordinatenweise).
**Rezept 2 — Skalarprodukt:** Zeile mal Zeile, dann addieren. **Ergebnis 0 = senkrecht!**

1. Gegeben A(1|2|3) und B(4|6|3). Berechne $\vec{AB}$ und seinen Betrag $|\vec{AB}| = \sqrt{x_1^2+x_2^2+x_3^2}$.
2. Berechne das Skalarprodukt von $\vec{a} = \begin{pmatrix}2\\-1\\3\end{pmatrix}$ und $\vec{b} = \begin{pmatrix}4\\2\\-2\end{pmatrix}$. Stehen sie senkrecht aufeinander?
3. Skalarprodukt von $\vec{c} = \begin{pmatrix}1\\2\\2\end{pmatrix}$ und $\vec{d} = \begin{pmatrix}3\\0\\4\end{pmatrix}$ — senkrecht oder nicht?

<details><summary>✅ Lösungen Tag 1 (erst nach dem Rechnen aufklappen!)</summary>

1. $\vec{AB} = \begin{pmatrix}4-1\\6-2\\3-3\end{pmatrix} = \begin{pmatrix}3\\4\\0\end{pmatrix}$, Betrag: $\sqrt{9+16+0} = \sqrt{25} = 5$
2. $2\cdot4 + (-1)\cdot2 + 3\cdot(-2) = 8 - 2 - 6 = 0$ → **ja, senkrecht!**
3. $1\cdot3 + 2\cdot0 + 2\cdot4 = 3 + 0 + 8 = 11 \neq 0$ → **nicht senkrecht**
</details>

### ▢ TAG 2 — Mo 6.7. — Ebenengleichung lesen + Punktprobe (leichteste Klausurpunkte!)
**▶️ Video (10 min):** [Punktprobe bei Ebenen in Koordinatenform, Parameterform | Mathe by Daniel Jung](https://www.youtube.com/watch?v=6WTiYADAka8)

**✏️ Übung (10 min):**
**Rezept 3 — Punktprobe (Koordinatenform):** Punkt in die Gleichung einsetzen. Stimmt die Gleichung → Punkt liegt in der Ebene.
**Rezept 4 — Normalenvektor ablesen:** Bei $ax_1 + bx_2 + cx_3 = d$ ist $\vec{n} = \begin{pmatrix}a\\b\\c\end{pmatrix}$ der Normalenvektor (steht senkrecht auf der Ebene).

Gegeben ist die Ebene $E:\; 2x_1 + 3x_2 - x_3 = 7$.
1. Liegt P(2|1|0) in E? Liegt Q(1|1|1) in E?
2. Gib den Normalenvektor $\vec{n}$ von E an.
3. Steht $\vec{v} = \begin{pmatrix}1\\0\\2\end{pmatrix}$ senkrecht auf $\vec{n}$? (Skalarprodukt von gestern!)

<details><summary>✅ Lösungen Tag 2</summary>

1. P: $2\cdot2 + 3\cdot1 - 0 = 7$ ✓ → **P liegt in E.** Q: $2\cdot1 + 3\cdot1 - 1 = 4 \neq 7$ → **Q liegt nicht in E.**
2. $\vec{n} = \begin{pmatrix}2\\3\\-1\end{pmatrix}$ (einfach die Zahlen vor $x_1, x_2, x_3$)
3. $\vec{n}\cdot\vec{v} = 2\cdot1 + 3\cdot0 + (-1)\cdot2 = 0$ → **ja, senkrecht** (v verläuft also parallel zur Ebene / „liegt in Richtung der Ebene")
</details>

### ▢ TAG 3 — Di 7.7. — DAS Kernrezept: Durchstoßpunkt Gerade–Ebene
**▶️ Video (10 min):** [Lage Gerade & Ebene | Version Schnittpunkt | Mathe by Daniel Jung](https://www.youtube.com/watch?v=yji7ab3y5f8)

**✏️ Übung (10 min):**
**Rezept 5 — Durchstoßpunkt in 3 Schritten:**
1. Die drei Zeilen der Geraden ($x_1 = …$, $x_2 = …$, $x_3 = …$) in die Ebenengleichung einsetzen
2. Nach t auflösen (per Hand oder **CAS: `solve(…, t)`**)
3. t zurück in die Gerade einsetzen → fertig ist der Durchstoßpunkt

Gegeben: $g:\; \vec{x} = \begin{pmatrix}1\\2\\0\end{pmatrix} + t\cdot\begin{pmatrix}2\\1\\1\end{pmatrix}$ und $E:\; x_1 + x_2 + 2x_3 = 8$.
1. Bestimme den Durchstoßpunkt D von g und E.
2. Nun $h:\; \vec{x} = \begin{pmatrix}0\\0\\1\end{pmatrix} + t\cdot\begin{pmatrix}1\\-1\\0\end{pmatrix}$ und dieselbe Ebene E. Was passiert beim Einsetzen — und was heißt das?
3. **CAS-Drill:** Löse Aufgabe 1 nochmal, aber lass das ClassPad die t-Gleichung lösen (`solve(3+5t=8,t)`) — Tastenfolge im [ClassPad-solve-Video](https://www.youtube.com/watch?v=cIDgdYbtRHY). Präge sie dir ein!

<details><summary>✅ Lösungen Tag 3</summary>

1. Zeilen von g: $x_1 = 1+2t$, $x_2 = 2+t$, $x_3 = t$. Einsetzen: $(1+2t) + (2+t) + 2t = 8 \Rightarrow 3 + 5t = 8 \Rightarrow t = 1$. Zurück in g: $D(3|3|1)$. Probe: $3+3+2\cdot1 = 8$ ✓
2. $(t) + (-t) + 2\cdot1 = 2 \neq 8$ — das t fällt weg, es bleibt „2 = 8" (falsch) → **keine Lösung → g ist parallel zu E** (kein gemeinsamer Punkt). *(Wäre „2 = 2" herausgekommen: unendlich viele Lösungen → h läge IN E.)*
3. CAS liefert t = 1 — gleiche Antwort, null Rechenaufwand. In der Klausur: Gleichung aufstellen gibt Punkte, solve rechnet.
</details>

### ▢ TAG 4 — Mi 8.7. — Lage zweier Ebenen + Wiederholungs-Mix
**▶️ Video (10 min):** [Lage von 2 Ebenen in Koordinatenform, Beispiel Schnittgerade | Mathe by Daniel Jung](https://www.youtube.com/watch?v=YhQphAm9ci4)

**✏️ Übung (10 min):**
**Rezept 6 — Lage zweier Ebenen (Koordinatenform), nur Normalenvektoren vergleichen:**
- $\vec{n_1}$ ist Vielfaches von $\vec{n_2}$ UND rechte Seite passt mit → **identisch**
- $\vec{n_1}$ ist Vielfaches von $\vec{n_2}$, rechte Seite passt NICHT → **echt parallel**
- kein Vielfaches → **sie schneiden sich** (in einer Schnittgeraden)

Gegeben: $E_1:\; x_1 + 2x_2 + 2x_3 = 4$
1. Lage von $E_1$ und $E_2:\; 2x_1 + 4x_2 + 4x_3 = 8$?
2. Lage von $E_1$ und $E_3:\; 2x_1 + 4x_2 + 4x_3 = 10$?
3. Lage von $E_1$ und $E_4:\; x_1 - x_2 + x_3 = 1$?
4. **Mix (Wiederholung Tag 3):** $g:\; \vec{x} = \begin{pmatrix}2\\0\\1\end{pmatrix} + t\cdot\begin{pmatrix}1\\2\\0\end{pmatrix}$, $E:\; 2x_1 + x_2 + x_3 = 9$ — Durchstoßpunkt?

<details><summary>✅ Lösungen Tag 4</summary>

1. $E_2 = 2\cdot E_1$ komplett (auch die 8 = 2·4) → **identisch**
2. Linke Seite ist das Doppelte, aber $10 \neq 2\cdot4$ → **echt parallel**
3. $\begin{pmatrix}1\\2\\2\end{pmatrix}$ und $\begin{pmatrix}1\\-1\\1\end{pmatrix}$ — kein Vielfaches → **schneiden sich** (Schnittgerade; ihre Berechnung überlässt du in der Klausur dem CAS oder lässt sie weg)
4. $2(2+t) + (2t) + 1 = 9 \Rightarrow 5 + 4t = 9 \Rightarrow t = 1 \Rightarrow D(3|2|1)$. Probe: $6+2+1 = 9$ ✓
</details>

---

## 🎯 KLAUSUR-STRATEGIE für Do 9.7. (5 min am Mi-Abend lesen)

1. **Blatt zuerst scannen:** Wo kommen die Wörter „liegt in", „Durchstoßpunkt/Schnittpunkt", „parallel", „orthogonal/senkrecht" vor? Das sind deine Rezept-Aufgaben — die zuerst!
2. **Punktprobe-Aufgaben sind Geschenke** — einsetzen, ausrechnen, fertig (Rezept 3).
3. **„Senkrecht?" heißt immer Skalarprodukt = 0** (Rezept 2).
4. **Durchstoßpunkt = 3-Schritte-Rezept** (Rezept 5) — die Gleichung ans CAS geben.
5. **Auch wenn du nicht fertig rechnest:** Ansatz hinschreiben („Einsetzen von g in E:…") gibt Teilpunkte. Leeres Blatt gibt null.
6. Nicht verzetteln: Wenn eine Aufgabe nach 5 min nicht läuft → nächste. Du sammelst Punkte, du gewinnst keinen Preis für Reihenfolge.

## 🖩 Dein CAS: Casio ClassPad II (FX-CP400)
- **Pflicht (einmal anschauen, ~5 min, am besten schon am So):** [CASIO ClassPad II (fx-CP400) — Gleichungen lösen](https://www.youtube.com/watch?v=cIDgdYbtRHY) — genau der `solve`-Befehl aus Rezept 5.
- **Bonus (falls Schnittgerade drankommt):** [Gleichungen und Gleichungssysteme lösen mit dem ClassPad 2](https://www.youtube.com/watch?v=GVTklscjUH0)
- **Nachschlagewerk:** [Playlist: ClassPad II — die Grundlagen](https://www.youtube.com/playlist?list=PLldPWW4gZZV66GEOcBkCAviSEndSJKxS4)
- Rechner **am Mi-Abend laden** und in die Tasche packen!
