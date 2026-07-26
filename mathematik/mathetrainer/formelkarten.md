# 🃏 Formel-Karteikarten — Vektorrechnung GK-Abi 2027

**TL;DR:** Alle Formeln, die du für den Mathetrainer brauchst — und nur die. Nichts außerhalb des GK-Abi-2027-Horizonts. Zum schnellen Wiederholen vor einer Session.

---

## M1 — Vektor-Grundlagen & Betrag

- **Vektor zwischen zwei Punkten:** $\vec{AB} = B - A$ (Spitze minus Fuß, koordinatenweise).
- **Ortsvektor:** $\vec{OP} = \begin{pmatrix} p_1 \\ p_2 \\ p_3 \end{pmatrix}$ für den Punkt $P(p_1\,|\,p_2\,|\,p_3)$.
- **Vielfaches / kollinear:** $\vec{a}$ und $\vec{b}$ sind kollinear, wenn $\vec{b} = r\cdot\vec{a}$ für ein $r$.
- **Betrag (Länge):** $|\vec{v}| = \sqrt{v_1^2 + v_2^2 + v_3^2}$.

## M2 — Skalarprodukt & Winkel

- **Skalarprodukt:** $\vec{a}\circ\vec{b} = a_1 b_1 + a_2 b_2 + a_3 b_3$.
- **Orthogonal (senkrecht):** $\vec{a}\circ\vec{b} = 0$.
- **Winkel zwischen Vektoren:** $\cos\varphi = \dfrac{\vec{a}\circ\vec{b}}{|\vec{a}|\cdot|\vec{b}|}$.

## M3 — Geraden aufstellen

- **Parametergleichung:** $g:\ \vec{x} = \vec{p} + t\cdot\vec{u}$ ($\vec{p}$ Stützvektor, $\vec{u}$ Richtungsvektor).
- **Aus zwei Punkten $A$, $B$:** $\vec{p} = \vec{OA}$, $\vec{u} = \vec{AB}$.
- **Punktprobe:** Punkt einsetzen, prüfen, ob ein einziges $t$ alle drei Zeilen erfüllt.

## M4 — Lagebeziehung von Geraden

- **Richtungsvektoren vergleichen:** Vielfache voneinander → parallel oder identisch; sonst → schneidend oder windschief.
- **identisch:** parallel **und** ein Punkt der einen liegt auf der anderen.
- **echt parallel:** parallel, aber Punkt liegt nicht drauf.
- **schneidend:** nicht parallel, LGS $\vec{p_1}+t\vec{u} = \vec{p_2}+s\vec{w}$ hat eine Lösung.
- **windschief:** nicht parallel und LGS hat keine Lösung.

## M5 — Ebenen

- **Parameterform:** $E:\ \vec{x} = \vec{p} + s\cdot\vec{u} + t\cdot\vec{w}$.
- **Koordinatenform:** $a x_1 + b x_2 + c x_3 = d$.
- **Normalenvektor** aus Koordinatenform: $\vec{n} = \begin{pmatrix} a \\ b \\ c \end{pmatrix}$.
- **Punktprobe:** Punkt in die Koordinatenform einsetzen; Gleichung erfüllt → Punkt liegt in $E$.
- *(Nur überstreichen)* **Normalenform:** $\vec{n}\circ(\vec{x}-\vec{p}) = 0$ — ausmultipliziert ergibt sie die Koordinatenform.

## M6 — Lagebeziehung Gerade–Ebene (Durchstoßpunkt)

1. Zeilen der Geraden ($x_1, x_2, x_3$) in die Koordinatenform von $E$ einsetzen.
2. Nach $t$ auflösen (per Hand oder CAS: `solve(..., t)`).
3. $t$ zurück in die Gerade → Durchstoßpunkt.
- **Sonderfälle:** $t$ fällt weg und Aussage falsch → parallel; Aussage wahr → Gerade liegt in $E$.

## M7 — Schnittwinkel

- **Gerade–Gerade:** $\cos\varphi = \dfrac{|\vec{u}\circ\vec{w}|}{|\vec{u}|\cdot|\vec{w}|}$ (Richtungsvektoren).
- **Ebene–Ebene:** $\cos\varphi = \dfrac{|\vec{n_1}\circ\vec{n_2}|}{|\vec{n_1}|\cdot|\vec{n_2}|}$ (Normalenvektoren).
- **Gerade–Ebene:** $\sin\varphi = \dfrac{|\vec{u}\circ\vec{n}|}{|\vec{u}|\cdot|\vec{n}|}$ (Richtungs- gegen Normalenvektor).

*(Der Betrag im Zähler sorgt für den spitzen Winkel.)*
