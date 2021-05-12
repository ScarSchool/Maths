# Permutationen
###### tags: `Maths` `Probability`
Dieses Dokument behandelt nur die ultimativen basics des Permutations-Themas
Es umfasst dennoch alle im Unterricht besprochenen Themen.

Weitere Informationen zu finden unter:
https://www.grund-wissen.de/mathematik/stochastik/kombinatorik.html


## Grundsätzliches
Permutationen bezeichnen mögliche Anordnungen von verschiedenen Objekten.
Eine Permutation beschreibt hierbei eine Anordnung.

$$
 n: Beschreibt\ wie\ viele\ verschiedene\ Elemente\ vorhanden\ sind\\
 k: Beschreibt\ wie\ viele\ Gruppen\ in\ einer\ Menge\ bestehen
$$

### Fakultät
> Es wird bis zur fakultierten Zahl kumuliert multipliziert

$$
    6! = 6\cdot 5\cdot 4\cdot 3\cdot 2\cdot 1
$$

> Nützlich:

$$
    \require{cancel}
    \frac{6!}{4!} = 
    \frac{6\cdot 5\cdot 4\cdot 3\cdot 2\cdot 1}{{4\cdot 3\cdot 2\cdot 1}} =
    6\cdot 5
$$


### Normale Permutation
Besteht, wenn n und k gleichgesetzt sind

>  Gegeben:

$$
    \fbox{A},\fbox{B},\fbox{C},\fbox{D},\fbox{E}\\
    n = 5; k = 5;
$$

### Variation
Besteht wenn n und k unterschiedliche Werte haben.

> Gegeben:

$$
    \fbox A, \fbox B, \fbox C,  \fbox {D, E}\\
    n = 5; k = 4;
$$

### Wahrscheinlichkeitsfunktionen

> Nicht zurücklegen; Reihenfolge wird beachtet:

$$
     nCr \rightarrow V_{n,k} = \frac{n!}{(n-k)!\cdot k!}
$$

> Nicht zurücklegen; Reihenfolge wird nicht beachtet

$$
    nPr \rightarrow V_{n,k} = \frac{n!}{(n-k)!} 
$$

> Wiederholung

$$
    V_{n,k} = n^k
$$
