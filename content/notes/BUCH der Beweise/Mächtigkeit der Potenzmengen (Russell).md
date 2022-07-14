---
title: "Mächtigkeit der Potenzmengen (Russell)"
---

# Mächtigkeit der Potenzmengen (Russell)

Mithilfe der *Russellschen Antinomie* lässt sich beweisen, dass die Mächtigkeit der Potenzmenge einer Menge stets größer ist als die Mächtigkeit dieser ursprünglichen Menge selbst. Betrachten wir dazu eine beliebige Menge $X$ sowie deren Potenzmenge (also Menge aller Teilmengen) $\mathcal{P}(X)$.

Offenbar lässt sich $X$ injektiv auf $\mathcal{P}(X)$, sodass nach dem [Cantor-Bernstein-Satz](notes/BUCH%20der%20Beweise/Cantor-Bernstein-Satz.md) $|X| \leq |\mathcal{P}(X)|$ folgt. Würde nun $|X| = |\mathcal{P}(X)|$ gelten, dann müsste eine **Bijektion** $\phi: X \rightarrow \mathcal{P}(X)$ existieren. Es sei nun $R$ die Menge aller Elemente aus $X$, die in ihrem Abbild in $\mathcal{P}(X)$ *nicht* enthalten sind. Offenbar ist $R$ eine Teilmenge von $X$ und damit Element von $\mathcal{P}(X)$. Es stellt sich nun die Frage, welches Element $r \in X$ auf $R \in \mathcal{P}(X)$ abbildet.

Offensichtlich kann $r$ entweder Element von $R$ sein oder eben nicht. 
Gilt nun $r \notin R$, so ist $r$ damit in seinem Abbild in $\mathcal{P}(X)$ *nicht* enthalten und müsste damit Element von $R$ sein, was im **Widerspruch zur Annahme** steht.
Gilt alternativ $r \in R$, so ist $r$ damit in seinem Abbild in $\mathcal{P}(X)$ enthalten und dürfte somit kein Element von $R$ sein, was im **Widerspruch zur Annahme** steht.

Da also beide möglichen Fälle zum Widerspruch führen, muss die **Annahme falsch** sein, dass $|X| = |\mathcal{P}(X)|$ gelte. In Verbindung mit den obigen Erkenntnissen folgt damit $|X| < |\mathcal{P}(X)|$. Für jede beliebige Menge $X$ ist also die Potenzmenge $\mathcal{P}(X)$ echt mächtiger als die Menge $X$ selber.

## Verallgemeinerung
Hieraus folgt unter anderem, dass es **keine größte Kardinalzahl** geben kann, da sich über die Potenzmenge stets eine größere Mächtigkeit finden lässt.