# Differentialrechnung
#### tags: `Maths` `differential calculation`
## Grundsätzliches
Das Ziel der Differentialrechnung ist es, lokale Veränderungen in Funktionen darstellen und bemessen zu können.
> Als Beispiel ist die erste Ableitung einer Funktion die "Steigung" an einem gewissen Punkt, ist diese Steigung 0, gibt es an diesem Punkt keine Veränderung, weshalb die untersuchte Stelle als 'Extremum' gilt (Mehr dazu später)
## Ableitungsregeln
> WIP (I hob meine olten Mitschriften noch nit dabei lmao)
## Ableitung expliziter bzw impliziter Funktionen
Um eine Ableitung durchzuführen, muss man zuerst feststellen ob eine Funktion explizit oder implizit darstellbar ist, um die effizinteste Ableitungsmethode wählen zu können. 
### Ableitung expliziter Funktionen
Eine Funktion gilt als explizit ableitbar, wenn auf einer Seite eine Variable isoliert steht:

$$
    y = f(x)
$$

Konkretes Beispiel:

$$
    y = \frac{sin(x)\cdot e^{2x}}{5x + 3}
$$

Hier kann man ganz simpel die erste Ableitung $y' = f(x)$ aufstellen.
> Ganz simpel heißt nicht dass die wirkliche Ableitung einfach ist. Einfach in Geogebra eine klopfen donn hot mans

### Ableitung implizierter Funktionen
Eine Funktion gilt als implizit ableitbar, wenn die zu ableitenden Variablen nicht isoliert sind.
#### Methodik
Man möchte folgende Funktion nach $\frac{dy}{dx}$ ableiten, sodass man $y'(x)$ erhält.
$$
    \color{green}{2y} + \color{blue}{3x^2} + \color{black}{y^3} = \color{purple}{x+y}
$$
##### Schritt 1 
Ableitungsregeln anwenden, als wären die Variablen bereits isoliert.
$$
    \color{green}{2\cdot} \color{gold}{1} \color{green}{\cdot y'} + \color{blue}{3 \cdot 2 \cdot x} + \color{gold}{3\cdot y^2} \color{black}{\cdot y'} = \color{purple}{1+} \color{gold}{1} \color{purple}{\cdot y'}
$$

> Die gold-farbigen Werte sind jene, die bei der Ableitung einer y Variable zu stande gekommen sind.
> Zu bemerken ist, dass hierbei $y$ nach dem Ableiten immer mit $y'$ zu multiplizieren ist, da eine Art Kettenregel angewandt wird.

##### Schritt 2
Formel so umformen, sodass auf einer Seite alle $y'$ stehen.

$$
    y' = \frac{1-6x}{2+3y^2-1}
$$

### Ableiten expliziter Funktionen mit der impliziten Methode
Man kann nicht nur implizite Funktionen implizit Ableiten, sondern funktioniert dies auch mit herkömmlichen expliziten Funktionen.

Beide Lösungsansätze führen zum selben Ergebnis, auch wenn eines komplizierter Wirkt, sind beide Anwendungsfälle nützlich und gebräuchlich.

#### Beispiel:
Gegeben ist folgende Funktion:
$$
    2y + 3x^2 = x+y
$$
##### Implizite Methode
> Der Schüler bemerkt nicht, dass diese Funktion explizit darstellbar ist, und verwendet die implizite Methode

$$
    2 \cdot 1 \cdot y' + 6 \cdot x = 1 + 1 \cdot y'
$$

> Umformen auf y'

$$
    y' = 1-6x
$$

##### Explizite Methode
> Der Schüler bemerkt, dass es sich um eine explizite Methode handelt und formt die Funktion dementsprechend um

$$
    y = x- 3x^2
$$

> Umformen auf y'

$$
    y' = 1-6x
$$

## Logarithmische Differentiation
> Für Übungsbeispiele oder einfach eine andere Erklärung: http://www.math-grain.de/download/m1/diff-r/ableitung/log-ableitung-1.pdf

Vom logarithmischen Differentieren spricht man wenn die Funktionsgleichung zuerst logarithmiert wird und danach differenziert wird.
### Methodik
Gegeben ist folgende Funktion
$$
    y = 2^x
$$

Um diesen Fall zu lösen benötigt man eine logarithmusfunktion. Die Funktion wird zuerst auf dies vorbereitet:

$$
    y = e^{ln(2)x}
$$

Die Kettenregel wird angewandt

> Der Ausdruck von $\frac{dy}{dx} [ln(2)x]$ existiert noch um Schritt für Schritt erklären zu können was passiert

$$
    y' = e^{ln(2)x}\cdot \frac{dy}{dx} [ln(2)x]  
$$

> Die eine Multiplikationsregel wird angewandt mit $u' \cdot v = v' \cdot u$

$$
    y' = e^{ln(2)x}\cdot ln(2) \cdot 1  
$$

> Vereinfachen der Funktion. Für Info warum das passiert mit ln: https://socratic.org/questions/how-do-you-simplify-e-lnx-1

$$
    y' = 2^x\cdot ln(2) \cdot 1  
$$