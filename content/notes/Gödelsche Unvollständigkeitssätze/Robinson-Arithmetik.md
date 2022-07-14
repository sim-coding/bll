---
title: "Robinson-Arithmetik"
---

# Robinson-Arithmetik

Die Robinson-Aritmetik ($Q$) ist eine Theorie der [Arithmetik](notes/Grundlagen%20der%20Mathematik/Arithmetik.md) formuliert in der [Prädikatenlogik erster Ordnung](notes/Grundlagen%20der%20Mathematik/Prädikatenlogik%20erster%20Ordnung.md), deren Axiome die Grundlage der [Peano-Arithmetik](notes/Gödelsche%20Unvollständigkeitssätze/Peano-Arithmetik.md) bilden.

## Axiome
- $¬(0=x′)$
	- Null hat keinen Vorgänger.
-  $x′=y′→x=y$
	- Variabeln mit gleichen Nachfolgern sind untereinander gleich.
-  $¬(x=0)→∃y(x=y′)$
	- Jede von Null verschiedene Variable hat einen Vorgänger.
-  $x+0=x$
	- Variabeln bleiben bei Addition gleich.
-  $x+y′=(x+y)′$
	- Rekurisve Definition der Addition.
-  $x×0=0$
	- Multiplikation mit Null ergibt stets Null.
-  $x×y′=(x×y)+x$
	- Rekursive Definition der Multiplikation

Anzahl der Axiome: 7

$(x \times ) y = 4$