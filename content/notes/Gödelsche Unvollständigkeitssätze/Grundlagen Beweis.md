# Grundlagen Beweis
## Formale Systeme

Formales System (ähnlich zu Automatentheorie):
1. **Alphabet** $A$, beliebige Zeichen, aus denen sich Zeichenketten bilden lassen
2. **Sprache** $F$, Zeichenketten, die der Grammatik des Systems entsprechen (Sinn ergeben) / wohlgeformte Formeln
3. **Axiome** $A$, eine beliebige Menge wohlgeformter Formeln (Teilmenge der Sprache), die als Grundlage der Ableitungsrelation dienen
4. **Ableitungsrelationen** $R$, Menge an Ableitungsrelationen (mit Regeln), nach denen sich aus einer beliebigen Zahlen an wohlgeformten Formeln eine neue ableiten lässt
*Zusätzlich*: Sowohl die Axiome als auch die Ableitungsregeln eines Formalen Systems sind *entscheidbar* (es existiert ein abrechender Entscheidungsalgortihmus)

*Achtung:* In formalen Systemen wird rein *syntaktisch* abgeleitet, eine reininterpretierbare *semantische* Bedeutung liegt außerhalb des Systems, wenn sie auch häufig interessant sein kann.

## Theorien, Aussagen, Theoreme und andere Begriffe

**Theorie (Theory):**

**Aussage (Statement):**

**Theorem:**

**Formel (Formula)**

## Wohlgeformte Formeln


## Eigenschaften Formaler Systeme

Begriff der *Vollständigkeit*: Jede wohlgeformte Formel kann entweder selbst abgeleitet werden oder ihre Negation kann abgeleitet werden (oder beides).

Begriff der *Konsistenz*: Es gibt keine wohlgeformte Formel in dem Formalen System, die selbst abgeleitet werden kann und ihre Negation auch. *Inkonsitente* Formale Systeme sind *vollständig* (ex contradictione sequitur quodlibet), weshalb im Folgenden nur *konsistente* Formale Systeme betrachtet werden.

Begriff der *$\omega$-Konsistenz*: Ein Formales System $F$ ist *$\omega$-konsistent*, wenn keine Formel $\phi(x)$ existiert, sodass $F \vdash \lnot \phi(\underline{n}) \land F \vdash \exists x \phi(x)$ gilt. 

Begriff der *1-Konsitenz*: Ein Formales System ist *1-konsistent*, wenn die obige Aussage für alle Formeln $\phi(x)$ der Klasse $\Sigma^0_1$ gilt.

## Ex contradictione sequitur quodlibet

In einem *inkonsistenten* Formalen System, in dem also zwei widersprüchliche Formeln ableitbar sind, lässt sich jede beliebige Formel (und ihr jeweiliges Gegenteil) ableiten, sodass jedes *inkonsistente* Formale System ein *vollständiges* ist. Eine Beweisskizze sieht wie folgt aus:

In dem Formalen System $F$ seien sowohl die $A$ als auch $\lnot A$ ableitbar. Es sein $B$ eine beliebige andere Formel. Egal wie $B$ gewählt ist, lässt es sich auf die folgende Weise ableiten:

$$F \vdash A$$
$$\rightarrow F \vdash (F \lor B) \ \ (1)$$
Zudem gilt:
$$F \vdash \lnot A$$
Setzt man dies in (1) ein, so erhält man:
$$F \vdash B$$

## Die arithmetische Formel-Hierarchie

Die *arithmetische Formel-Hierarchie* wird induktiv definiert:

Formeln, die keine Quantoren enthalten oder äquivaltent zu solchen sind, die keine Quantoren enthalten, erhalten die Klassifikation $\Sigma^0_0$ beziehungsweise $\Pi^0_0$.

**Beispiele:**
$$3 \times 3 = 9$$
$$5 + 7 = 13$$
$$\exists x < 1 \exists y < 2  (x \times y = 14) \leftrightarrow (0 \times 0 = 14) \lor (0 \times 1 = 14)$$

Es sei $\phi$ eine Formel der Klasse $\Pi^0_n$, dann ist $\exists x_1 \exists x_2 \dots \exists x_k \phi$ eine Formel der Klasse $\Sigma^0_{n+1}$ und umgekehrt ($\phi$ hat Klasse $\Sigma^0_n$, dann hat $\forall x_1 \forall x_2 \dots \forall x_k \phi$ die Klasse $\Pi^0_{n+1}$). Formeln der für uns relevanten Klasse $\Sigma^0_1$ können damit wie folgt aussehen:

$$\exists x \exists y (x \times y = 14)$$
$$\exists x (4 + x = 3)$$

## Arithmetik und Interpretierbarkeit

Die Arithmetik befasst sich vorrangig mit natürlichen Zahlen und mit dem Rechnen mit diesen (Grundrechenarten). Nicht alle Formalen Systeme sind für diese Anwendung konzipiert, doch häufig lassen sich diese Operationen dennoch darstellen und durchführen (im einfachsten Fall: die [Robinson-Arithmetik](Robinson-Arithmetik.md) ist in diesem System *interpretierbar*).

Ein Formales System $F_1$ ist in einem anderen Formalen System $F_2$ interpretierbar, wenn jede ableitbare Formel aus $F_1$ (Theorem) in eine Formel in $F_2$ übersetzt werden kann, die wiederum in $F_2$ ableitbar ist.

## Übertragbarkeit der Unvollständigkeit

Warum lässt sich die Unvollständigkeit übertragen ([Robinson-Arithmetik](Robinson-Arithmetik.md) auf Formale Systeme, in denen diese interpretierbar ist)?

## Repräsentierbarkeit
