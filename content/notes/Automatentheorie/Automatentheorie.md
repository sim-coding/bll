---
title: "Automatentheorie"
---

# Automatentheorie

## Kontextfreie Grammatik / Sprache

Besteht aus:
- Variablen (**V**); Symbole, die weiter abgeleitet werden können (nichtterminal)
- Alphabet (**T**); Symbole, die nicht weiter abgeleitet werden können (terminal)
- Produktionen / Regeln (**P**); Regeln nach denen abgeleitet wird:
	- Kopf: Variable / nichtterminales Symbol
	- Produktionssymbol: $\rightarrow$
	- Rumpf: Zeichenreihe aus terminalen und nichtterminalen Symbolen (auch leere Zeichenkette $\epsilon$ möglich)
- Startsymbol (**S**); beginnt die Ableitung, kann wiederholt auftretend (nichtterminal)

## Chomsky-Normalform

- Besondere Form einer kontextfreien Grammatik
- Feste Umformungsregeln führen stets zu folgenden Eigenschaften:
	- Ausschließlich das Startsymbol *S* lässt sich auf die leere Zeichenkette $\epsilon$ ableiten.
	- Terminalsymbole treten nur noch alleinstehend als Ableitung (ggf. eine von mehreren) einer nichtterminalen Variable auf.
	- Jede andere Ableitung führt von einer Variable auf exakt zwei nichtterminale Variablen.

## Pumping-Lemma für kontextfreie Sprachen

Aussage:
*L* sei kontextfreie Sprache (Sprache, die aus einer kontextfreien Grammatik hervorgeht).
Dann existiert für diese Sprache eine Konstante *n*, sodass sich alle Wörter *w* mit Mindestlänge *n* in fünf Abschnitte *uvxyz* zerlegen lassen, für die gilt:

1) |*vxy*| $\leq$ *n*, die mittleren Abschnitte ohne *u* und *z* sind also maxmial *n* Zeichen lang.
2) *vy* $\neq \epsilon$, mindestens einer der beiden "aufpumpbaren" Abschnitte *v* und *y* ist also nicht leer.
3) Alle Wörter *uv$^k$xy$^k$z* mit k$\geq$ 0 sind auch Wörter in *L*, die Abschnitte *v* und *y* lassen sich also aufpumpen.

## Nicht-kontextfreie Sprachen

Beweis über Widerspruch zum Pumping Lemma. 

Hierzu genügt ein einziges Gegenbeispiel, weshalb häufig strategisch gewählte Wörter der Sprache untersucht werden, in denen die Variable *n* prominent auftritt.