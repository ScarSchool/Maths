
# Differentialrechnung
###### tags: `Maths` `differential calculation`
## Grundsätzliches
Das Ziel der Differentialrechnung ist es, lokale Veränderungen in Funktionen darstellen und bemessen zu können.
> Als Beispiel ist die erste Ableitung einer Funktion die "Steigung" an einem gewissen Punkt, ist diese Steigung 0, gibt es an diesem Punkt keine Veränderung, weshalb die untersuchte Stelle als 'Extremum' gilt (Mehr dazu später)
## Ableitungsregeln
> WIP (I hob meine olten Mitschriften noch nit dabei lmao)
## Integrationsregeln
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
    \color{lime}{2y} + \color{blue}{3x^2} + \color{black}{y^3} = \color{purple}{x+y}
$$
##### Schritt 1 
Ableitungsregeln anwenden, als wären die Variablen bereits isoliert.
$$
    \color{lime}{2\cdot} \color{gold}{1} \color{lime}{\cdot y'} + \color{blue}{3 \cdot 2 \cdot x} + \color{gold}{3\cdot y^2} \color{black}{\cdot y'} = \color{purple}{1+} \color{gold}{1} \color{purple}{\cdot y'}
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

## Differentialgleichung
Kommen in einer Gleichung Funktionen $f(x)$ und ihre Ableitungen $f'(x), f''(x), f'''(x)$ vor, so spricht man von einer Differentialgleichung.

Differentialgleichungen entstehen, wenn man den Zusammehang einer Funktion und deren Änderungsraten als Gleichung formuliert.

    Bemerkung:
    
    y ... Funktion
    
    y' ... Änderungsrate
    
    y'' ... Änderungsrate der Änderungsrate

### Einteilungen von Differentialgleichungen
> Nähere Info unter https://www.uni-due.de/imperia/md/content/materialtechnik/vmath124.pdf und http://micbaum.y0w.de/uploads/DGLGrundbegriffe.pdf

* Ordnung
    * Darunter versteht man die höchste vorkommende Ableitung
* Grad einer Differentialgleichung
    * Entspricht der höchsten vorkommenden Potenz der höchsten Ableitung

> DGL 2. Ordnung
$$
    \color{gold}{y''} + ay = 0
$$

> DGL 4. Ordnung
$$
    \color{gold}{y''''} + 3yy''^3-7y'x^2+2y^2sin(x) = e^{-x}
$$

### Lösen von Differentialgleichungen
#### Integrieren
Das Integrieren ist wohl die einfachste Methode eine Diff. Gleichung aufzulösen.
$$
    y' = 5x^2 + 2x + 1 \rightarrow y = \int{5x^2 + 2x + 1}
$$


Damit dies aber möglich ist, darf die Funktion keine 2 unbestimmten aber konkreten Variablen haben.
Konkret bedeuted das, wenn $\frac{dy}{dx} = y' = f(x)$ der Fall ist, in der funktion f(x) keine Abhängigkeit von $y$ bestehen darf.

##### Beispiel
Gegeben:
$$
    y' = 2x
$$

> Integrierung wird durchgeführt

$$
\require{cancel}
    \int{y'} = \int{2x*dx} \rightarrow y =  \frac{\cancel{2}x^2}{\cancel{2}} + c
$$

    Bemerkung:
    c stellt die Anfangsbedingung dar.
    Durch Wahl einer Anfangsbedingung/Randbedingung durch Punkt P oder gegebenes c,
    wird aus einer allgemeinen Lösung eine partikuläre Lösung ausgewählt

#### Trennen von Variablen
Das Integrieren ist in folgendem Fall nicht sofort möglich.

Im folgenden allgemeinen Fall muss man nun die Ausdrücke voneinander trennen um daraufhin ein Integral bilden zu können:
$$
    y' = f(x) \cdot g(y)
$$

##### Schritt 1
Differentialschreibweise bilden
$$
\frac{dy}{dx} = f(x) \cdot g(y) 
$$

##### Schritt 2
Formel umformen, sodass $dy$ und $dx$ mit den dazugehörigen Ausdrücken isoliert sind.

$$
    dy = f(x) \cdot g(y) \cdot dx
$$

$$
    \frac{1}{g(y)} \cdot dy = f(x) \cdot dx
$$

##### Schritt 3
Integral bilden und auflösen

$$
   \int \frac{1}{g(y)} \cdot dy = \int f(x) \cdot dx
$$


$$
    ln(g(y) + c_1 = \frac{f(x)^2}{2} + c_2
$$

> Beliebige Randbedingungen auf gemeinsame Seite bringen und zusammenfassen. 
> Da sie ja beliebig sind darf man das

$$
    ln(g(y))  = \frac{f(x)^2}{2} + c
$$

> Potenzieren mit $e$ als Basis da $ln$ der konkrete Logarithmus von der $eulerschen\ Zahl$ ist.

$$
    e^{ln(g(y))}  = e^{\frac{f(x)^2}{2} + c}
$$

$$
    g(y)  = e^{\frac{f(x)^2}{2}} \cdot e^{c}
$$

> Da c beliebig wählbar ist und $e$ eine Konstante Zahl ist, einfach c runter nehmen aus der Potenz

$$
    g(y)  = e^{\frac{f(x)^2}{2}} \cdot c
$$


### Differentialgleichung mit Störfunktion
Eine Störfunktion/Ein Störglied ist ein Anteil einer DGL, der nicht von der gesuchten Funktion und ihren Ableitungen, sondern **nur von der/den unabhängigen Variablen abhängt**. Diesen Anteil gilt es isoliert auf eine Seite zu bringen.
> Das Störglied beschreibt in der Regel die äußere Anregung eines Systems.

#### Methodik
Als Beispiel haben wir folgende Funktion mit Störglied:
> Man bemerke, dass die Störfunktion bereits isoliert auf der rechten Seite zu sehen ist.

$$
    y' + 2y = 4x-5
$$

##### Schritt 1
Bilden der homogenen Differentialgleichung
> Störfunktion auf 0 setzen

$$
    y_h' + 2y_h = 0
$$

##### Schritt 2
Lösen des entstandenen Gleichungssystems mit Integral (Für Schritt für Schritt Erklärungen siehe [Trennen von Variablen](https://demo.hedgedoc.org/s/kJPo7QV5V#Trennen-von-Variablen)

$$
    \frac{dy_h}{dx} = - 2y_h
$$

$$
    dy_h = - 2y_h \cdot dx
$$

$$
    \frac{1}{y_h} \cdot dy_h = - 2 \cdot dx
$$

$$
    \int\frac{1}{y_h} \cdot dy_h = - \int 2 \cdot dx
$$

$$
    ln(y_h) \cdot ln(c) = - 2 x
$$

$$
    y_h \cdot c = e^{- 2 x}
$$

##### Schritt 3
Bilden der partikulären Differentialgleichung

> Der partikuläre Teil wird veralgemeinert. Hier folgt dieser dem Format einer linearen Funktion

$$
    \color{blue}{y_p} =  Ax + B
$$

$$
    \color{purple}{y_p'} =  A
$$

##### Schritt 4
Partikulären Teil in Ursprungsfunktion einsetzen

$$
    \color{purple}{y'} + 2 \cdot \color{blue}{y} = 4x-5
$$

> Wird zu

$$
    \color{purple}{A} + 2\cdot (\color{blue}{Ax + B}) = 4x-5
$$


##### Schritt 5
Partikuläre Funktion dem vorhin erkannten Format nach umformen (hier lineare Funktion)

$$
    A + 2\cdot (Ax + B) = 4x-5
$$

$$
    A + 2\cdot Ax + 2\cdot B = 4x-5
$$

>Im nächsten Ausdruck folgt die linke Seite dem gewünschten Muster.

$$
    \color{blue}{[2\cdot A]}x + \color{purple}{[A + 2\cdot B]} = \color{blue}{4}x\color{purple}{-5}
$$

> Jetzt werden die im Muster an der selben Stelle stehenden Werte gleichgesetzt. 
> (Blau wird mit Blau gleichgesetzt und Lila mit Lila)

$$
    2\cdot A = 4;\newline
    A + 2\cdot B = -5
$$
> Gleichungssysteme werden aufgelöst

$$
    A = 2
$$

$$
    2 + 2B = -5\newline
    B = -3.5
$$

##### Schritt 6
"Mustervariablen" im Muster einsetzen
$$
    \color{blue}{A} = 2;\ \color{purple}{B} = -3.5 
$$

$$
    {y_p} =  \color{blue}{A}x + \color{purple}{B}
$$


$$
    {y_p} =  \color{blue}{2}x + \color{purple}{(-3.5)}
$$


##### Schritt 7
Homogene als auch partikuläre Funktionen in Formel eintragen
> Formel

$$
    y = \color{blue}{y_h} + \color{purple}{y_p}
$$

> Formel mit eingesetzten Werten

$$
    y = \color{blue}{e^{- 2 x} \cdot c} +\color{purple}{2x + (-3.5)}
$$