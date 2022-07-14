---
title: "Sätze aus dem BUCH der Beweise"
---

# Sätze aus dem BUCH der Beweise

## Satz 1

> Die Menge $\mathbb{Q}$ der rationalen Zahlen ist abzählbar.

**Beweis:**
Zunächst einmal genügt ein Beweis dieser Aussage für $\mathbb{Q}^+$, sind die positiven rationalen nämlich abzählbar, gilt dies auch für $\mathbb{Q}$. Um das zu sehen, genügt es, die Elemente von $\mathbb{Q}^+$ geordnet aufzuschreiben, eine 0 an den Beginn der Liste zu setzen und das Negative eines jeden Bruches jeweils hinter diesem anzufügen. Es entsteht eine Liste aller rationalen Zahlen.

Für einen Beweis der Abzählbarkeit von $\mathbb{Q}^+$ siehe [Cantor'sches Diagonalverfahren](notes/BUCH%20der%20Beweise/Cantor'sches%20Diagonalverfahren.md) oder [Calkin-Wilf-Aufzählung](notes/BUCH%20der%20Beweise/Calkin-Wilf-Aufzählung.md).

## Satz 2

> Die Menge $\mathbb{R}$ der reellen Zahlen ist nicht abzählbar.

**Beweis:** 
Siehe [Cantors Diagonalisierungsmethode](notes/BUCH%20der%20Beweise/Cantors%20Diagonalisierungsmethode.md).

## Satz 3

> Die Menge $\mathbb{R}^2$ aller geordneten Paaren von reellen Zahlen (die reelle Ebene) hat dieselbe Mächtigkeit wie $\mathbb{R}$.

**Beweis:**
Wir zeigen zunächst, dass die Menge aller Paare reeller Zahlen $(x, y)$ mit $0 < x, y \leq 1$ bijektiv auf das Intervall $(0, 1]$ abgebildet werden kann. Dazu werden $x$ und $y$ in ihrer eindeutigen unendlichen Dezimaldarstellung (keine $\overline{0}$) aufgeschrieben und die Nachkommastellen in *Gruppen* aufgeteilt, die stets an der ersten folgenden Stelle ungleich $0$ enden. Diese *Gruppen* werden nun wie im folgenden Beispiel abwechselnd gewählt und zu einer neuen reellen Zahl $z \in (0, 1]$ zusammengesetzt:

$$x = 0, \ 3 \ 01 \ 2 \ 007 \ 08 \dots$$
$$y = 0, \ 009 \ 2 \ 05 \ 1 \ 0008$$
$$z = 0, \ 3 \ 009 \ 01 \ 2 \ 2 \ 05 \ 007 \ 1 \ 08 \ 0008 \ \dots$$

Die Bedingung, dass solche *Gruppen* nicht auf eine $0$ enden dürfen ist notwendig, um eine direkte Bijektion von den Paaren reeller Zahlen auf das Intervall zu ermöglichen. Wählt man $z$ nämlich so, dass es sich abwechselnd aus einzelnen Nachkommastellen von $x$ und $y$ ergibt, so hätte $z = 0,\overline{01}$  kein Urbild $(x, y)$, denn es müsste $x = 0,\overline{0}$ gelten. Damit wäre weder $0 < x$ noch die Bedingung erfüllt, dass $x$ in der eindeutigen unendlichen Dezimaldarstellung zu schreiben ist.

Aus dem [Cantor'schen Diagonalverfahren](notes/BUCH%20der%20Beweise/Cantor'sches%20Diagonalverfahren.md) folgt, dass aus der Abzählbarkeit einer Menge auch die Abzählbarkeit der Menge aller paarweise verschiedenen Paare aus Elementen dieser Menge folgt. Damit exisiert eine bijektive Abbildung $g: \mathbb{G^2} \rightarrow \mathbb{G}$. Die Menge aller reellen Paare $(x, y) \in \mathbb{R}^2$ lässt sich mithilfe dieser Erkenntnis wie im folgenden Beispiel auf die reellen Zahlen $\mathbb{R}$ abbilden:

$$x = a, \ 3 \ 01 \ 2 \ 007 \ 08 \dots$$
$$y = b, \ 009 \ 2 \ 05 \ 1 \ 0008$$
$$z = g(a, b), \ 3 \ 009 \ 01 \ 2 \ 2 \ 05 \ 007 \ 1 \ 08 \ 0008 \ \dots$$

Induktiv folgt auch $|\mathbb{R}^n| = |\mathbb{R}|$. [^1]

[^1]: Oliver Deiser "Reelle Zahlen" Seite 84

## Satz 4

> Wenn jede von von zwei Mengen M und N injektiv in die jeweils andere abgebildet werden kann, dann existiert eine Bijektion von M auf N, das heißt, es gilt dann |M| = |N|.

**Beweis:**
Siehe [Cantor-Bernstein-Satz](notes/BUCH%20der%20Beweise/Cantor-Bernstein-Satz.md).

## Satz 5

> Es bezeichne $(P_0)$ die Eigenschaft einer Familie $\{f_{\alpha}\}$ von paarweise verschiedenen analytischen Funktionen auf den komplexen Zahlen, dass für jedes $z \in \mathbb{C}$ gilt: Die Menge der Werte $\{f_{\alpha}(z)\}$ ist höchstens abzählbar.
> 
> Wenn $c > \aleph_1$ ist, so ist jede Familie $\{f_{\alpha}\}$, welche $(P_0)$ erfüllt, höchstens abzählbar. Wenn andererseits $c = \aleph_1$ ist, so exisiert eine Familie $\{f_{\alpha}\}$ mit der Eigenschaft $(P_0)$, welche die Mächtigkeit $c$ hat.

**Beweis:**
Siehe [Abhängigkeit von der Kontinuumshypothese](notes/BUCH%20der%20Beweise/Abhängigkeit%20von%20der%20Kontinuumshypothese.md).