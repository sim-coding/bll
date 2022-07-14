---
title: "Peano-Arithmetik"
---

# Peano-Arithmetik

Die Peano-Arithmetik ($PA$) ist eine Theorie der [Arithmetik](notes/Grundlagen%20der%20Mathematik/Arithmetik.md) formuliert in der [Prädikatenlogik erster Ordnung](notes/Grundlagen%20der%20Mathematik/Prädikatenlogik%20erster%20Ordnung.md), deren Axiome als Erweiterung der [Robinson-Arithmetik](notes/Gödelsche%20Unvollständigkeitssätze/Robinson-Arithmetik.md) gesehen werden können. Diese Arithmetik charakterisiert die natürlichen Zahlen sowie ihre Eigenschaften.

## Axiome
Vereinfacht aus der [Robinson-Arithmetik](notes/Gödelsche%20Unvollständigkeitssätze/Robinson-Arithmetik.md) übernommen:
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

Zusätzlich:
- $ϕ(0)∧∀x[ϕ(x)→ϕ(x′)]→∀xϕ(x)$
	- Induktionsschema

Anzahl der Axiome: Vereinfacht 7 aus der [Robinson-Arithmetik](notes/Gödelsche%20Unvollständigkeitssätze/Robinson-Arithmetik.md), unendlich viele Axiome aus dem Induktionsschema (unendlich viele Formeln $ϕ$ einsetzbar)