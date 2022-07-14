---
title: "Gödelsche Unvollständigkeitssätze"
---

# Gödelscher Unvollständigkeitssatz

## Sätze
### 1. Gödelscher Unvollständigkeitssatz
> Sei $T$ ein *rekursiv aufzählbares* und *widerspruchsfreies* [Formales System](Formale%20System%20und%20Kalküle.md), in dem die [Robinson-Arithmetik](Robinson-Arithmetik.md) interpretierbar ist. Dann ist $T$ unvollständig (Es gibt also arithmetische Formeln, die in $T$ weder beweisbar noch widerlegbar sind).

### 2. Gödelscher Unvollständigkeitssatz
> Jedes hinreichend mächtige konsistente System kann die eigene Konsistenz nicht beweisen.

Aus: https://people.math.ethz.ch/~halorenz/4students/Literatur/HandoutGoedelsIncomp.pdf, https://www.biancahoegel.de/logik/beweis_goedel_unvoll_saetze.html

## Beweise
### 1. Satz
#### Voraussetzungen
Eine natürliche Zahl $n$ soll in der Standard-Sprache der Aritmetik als $\underline{n} = 0^{'...'}$ angegeben werden.

Ein formales System $F$ ist genau dann *$\omega$-konsistent*, wenn nicht sowohl $F \vdash \forall \underline{n}: \lnot A(\underline{n})$ als auch $F \vdash \exists x : A(x)$ für irgendeine Formel $A$ gilt.

Nach analoger Definition ist eine Theorie *1-konsistent*, wenn die obige Aussage (zunächst) nur für sogenannte *$\sum^0_1$-Formeln* gilt, welche die Form $\exists x_1 \exists x_2 ... \exists x_n B$ haben, wobei $B$ keine begrenzungsfreien Quantoren haben darf (etwa $\exists x < 2$)

#### Darstellbarkeit
Eine Menge $S$ natürlicher Zahlen ist *schwach darstellbar (weakly representable)* in $F$, wenn eine Formel $A(x)$ existiert, sodass für alle natürlichen Zahlen $n$ ($\forall n$) gilt:
$$n \in S \Rightarrow F \vdash A(\underline{n})$$
Eine Menge $S$ natürlicher Zahlen ist *stark darstellbar (strongly representable)* in $F$, wenn eine Formel $A(x)$ existiert, für die neben dem obigen zusätzlich gilt:
$$n \notin S \Rightarrow F \vdash \lnot A(\underline{n})$$

Ferner gilt nun das **Darstellbarkeitstheorem**:
> 1. Eine Menge (oder eine Relation) ist genau dann *stark darstellbar*, wenn diese *rekursiv* ist (es existiert eine abbrechende Entscheidungsmethode, ob eine Zahl Element ist oder nicht).
> 2. Eine Menge (oder eine Relation) ist genau dann *schwach darstellbar*, wenn diese *rekursiv aufzählbar* ist (die Elemente können generiert werden, aber ein Entscheidungsalgorithmus muss nicht halten)

*Hinweis:* Parallelen zur [Automatentheorie](Automatentheorie.md) und zum [Halte-Problem](Halte-Problem.md)

#### Gödel-Nummerierung
Zunächst werden den einzelnen Symbolen der Sprache des formalen Systems natürliche Zahlen zugeordnet und diese dann gesickt verknüpft, um jeder Formel und jedem Beweis (Ableitungen aus dem System) eine *eindeutige Nummer* (Gödel-Nummer) zuzuordnen, von der aus sich auch die *ursprüngliche Zeichenfolge* herleiten lässt.

Beispielhafte Codierung:
| Nummer | Symbol    | Bedeutung        |
| ------ | --------- | ---------------- |
| 11     | 0         | Null             |
| 12     | '         | Nachfolger       |
| 13     | =         | Gleichheit       |
| 14     | +         | Addition         |
| 15     | $\times$  | Multiplikation   |
| 16     | (         | Linke Klammer    |
| 17     | )         | Rechte Klammer   |
| 18     | $x$       | Variable         |
| 19     | $^.$      | weitere Variable |
| 21     | $\exists$ | Existenzquantor  |
| 22     | $\forall$ | Allquantor       |
| 23     | $\land$   | logisches Und    |
| 24     | $\lor$    | logisches Oder   |
| 25     | $\lnot$   | Negation         | 

Die Formel $K = \forall x \forall x^. (x + x^. = x^. + x)$ des Kommutativgesetzes der Addition wird damit wie folgt codiert:

$┌K┐=$ 22 18 22 18 19 16 18 14 18 19 13 18 19 14 18 17 (Lücken nur zur Lesbarkeit)

Aus: https://www.biancahoegel.de/logik/beweis_goedel_unvoll_saetze.html


Hierauf aufbauend lassen sich nun zahlreiche arithmetische Funktionen definieren, durch die jegliche Eigenschaften und Operationen des gerade betrachteten [Formalen Systems](Formale%20System%20und%20Kalküle.md) auf der Ebene der Zahlen und damit in der [Robinson-Arithmetik](Robinson-Arithmetik.md) ausdrücken lassen.

So lässt sich etwa definieren: $neg(┌A┐) = (┌\lnot A┐)$ oder $impl(┌A┐, ┌B┐) = ┌A \rightarrow B┐$ 
Auch existiert etwa eine Formel $Fmla(x)$, die genau dann wahr ist, wenn $x$ eine wohlgeformte Formel des Systems ist. Ebenso lässt sich in $Q$ und damit im Rahmen des [Formalen Systems](Formale%20System%20und%20Kalküle.md) $F$, in dem $Q$ [interpretierbar](Interpretierbarkeit.md) ist, eine Formel $Prf_F(x,y)$ finden, die genau dann wahr ist, wenn $x$ die Gödelnummer des Beweises einer Formel mit der Gödelnummer $y$ ist. Diese Relation wird durch die Formel *stark dargestellt.*

Es lässt sich nun die Formel $Prov_F(x) = \exists y Prf_F(y,x)$ aufstellen, die also genau dann wahr ist, wenn in dem [Formalen System](Formale%20System%20und%20Kalküle.md) ein Beweis für $x$ existiert. Diese Relation wird hierbei nur *schwach* und nicht *stark dargestellt*:

$$F \vdash A \Rightarrow F \vdash Prov_F(┌A┐)$$

Allerdings kann $Prov_F(x)$ stets als *$\sum^0_1$-Formel* gewählt werden.

*Hinweis:* Unbewiesene Aussagen

#### Diagonalisierung
Das **Diagonalisierungs-Lemma**:
> Es sei $A(x)$ eine beliebige Formel der Sprache des [Formalen Systems](Formale%20System%20und%20Kalküle.md) $F$, in dem $Q$ [interpretierbar](Interpretierbarkeit.md) ist, mit nur einer freien Variable $x$. Dann kann stets ein Satz $D$ konstruiert werden, sodass:
> $$F \vdash D \leftrightarrow A(┌D┐)$$


#### Abschluss des Beweises
Wendet man nun das Diagonalisierungs-Lemma auf die negierte Formel $Prov_F(x)$ an, so muss es einen Satz $G_F$ geben, sodass:
$$F \vdash G_F \leftrightarrow \lnot Prov_F(┌G_F┐) \ \ \ \ (1)$$
Nehmen wir nun an, dass $G_F$ in $F$ beweisbar wäre. Da die durch $Prov_F(x)$ definierte Beweisbarkeits-Relation, wie oben bereits erwähnt, *schwach darstellbar* ist, folgt $F \vdash Prov_F(┌G_F┐)$. In (1) eingesetzt beweist $F$ damit aber auch $G_F$, sodass $F$ inkonsistent wäre. $F$ kann also nur konsistent sein, wenn $G_F$ in $F$ nicht beweisbar ist.

Von hier an ist es nun notwendig anzunehmen, dass $F$ *1-konsistent* ist und $Prov_F(┌G_F┐)$ als *$\sum^0_1$-Formel* gewählt wurde.

Nehmen wir an, dass $F \vdash \lnot G_F$ und wie oben bereits angesprochen $\lnot(F \vdash G_F$). Aus letzterem folgt, dass es keine natürliche Zahl $n$ geben kann, die die Gödelnummer eines Beweises von $G_F$ ist. Aus der *starken Darstellbarkeit* der Beweis-Relation $Prf_F(x, y)$ folgt dann $\forall n : F \vdash \lnot Prf_F(\underline{n}, ┌G_F┐)$.

Aufgrund der *1-Konsistenz* gilt ferner: $\lnot (F \vdash \exists x Prf_F(x, ┌G_F┐)) \Leftrightarrow \lnot (F \vdash Prov_F(┌G_F┐))$. Aus (1) folgt damit, dass auch $\lnot G_F$ nicht in $F$ beweisbar ist.

Somit gilt **Gödels erster Unvollständigkeitssatz** in der folgenden Form:
> Es sei $F$ ein [Formales System](Formale%20System%20und%20Kalküle.md), in dem die [Robinson-Arithmetik](Robinson-Arithmetik.md) $Q$ interpretierbar ist. Dann lässt sich ein Satz $G_F$ in der Sprache von $F$ konstruieren, sodass:
> 1. Wenn $F$ *konsistent* ist, dann gilt $F \not \vdash G_F$
> 2. Wenn $F$ *1-konsistent* ist, dann gilt $F \not \vdash \lnot G_F$ 

### 2. Satz

#### Voraussetzungen


#### Ableitbarkeitsbedingungen


#### Fefermans alternativer Ansatz


## In der Praxis

Über die Unentscheidbarkeit: [Halte-Problem](notes/Automatentheorie/Halte-Problem.md), [Kontinuumshypotese](notes/BUCH%20der%20Beweise/Kontinuumshypotese.md)

Ist die [Collatz-Vermutung](notes/Weitere%20Gebiete/Collatz-Vermutung.md) vielleicht gar nicht entscheidbar?