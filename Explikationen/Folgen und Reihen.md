# Folgen und Reihen
###### tags: `Maths`
## Konvergenz
$Umgangssprachlich:$ Unendliche Summe die endet heißt "konvergiert"
$Nit\ geistig\ behindert/ Mathematisch:$ Eine Reihe ist konvergent wenn ihre **Summationsglieder** eine **Nullfolge** bilden.

Also als Formel ausgedrückt:
$$
    \lim_{n\rightarrow \infty} \sum_{i=1}^n a_i = a_{Grenzwert} \Rightarrow \lim_{n\rightarrow \infty} a_n = 0
$$

    Fachsprache: 
    Für die konvergenz einer Reihe ist es notwendig eine Nullsumme aufzusummieren
    Eine Nullfolge ist NICHT hinreichend für eine konvergenz
    
### Konvergenzkriterien
Diese Kriterien sind notwendig um bei gegebener  Nullfolge der Summanden zu garantieren, dass die dadurch entstehende Reihe konvergiert.
#### Quotientenkriterium
Andere source: https://de.wikibooks.org/wiki/Mathe_für_Nicht-Freaks:_Quotientenkriterium
> Wenn man mal Jean Baptiste d'Alembert hören sollte; des hot der gmocht

Gegeben ist eine Nullfolge, welche zu einer unendlichen Reihe gemacht wird
$$
    a_n \Rightarrow \sum_{n=1}^\infty a_n
$$

Nun werden zwei Glieder der Folge mithilfe des $\lim_{n\rightarrow \infty}$ zu $\infty$ angenähert.

>[color=green] Notiere: 
>Das $\left|Betragszeichen\right|$ bedeutet, dass das der Ausdruck innerhalb des Betragszeichens   $\geq0$ ist.

$$
\begin{matrix}
    \lim_{n\rightarrow \infty} \left|\frac{a_n+1}{a_n}\right| & <& 1& \Rightarrow &absolut\ konvergent\\
    & > &1& \Rightarrow &divergent\\
    & = &1 &\Rightarrow &Keine\ Feststellung\ möglich\\
\end{matrix}
$$

#### Sidenote: Der shit mit der Unendlichkeit
Um eine beliebige Reihe oder Folge auf konvergenz überprüfen zu können, bedient man sich am Quotientenkriterium. Wenn man dieses jedoch anwendet, muss man die Mathematik der Unendlichkeit verstehen und deren Regeln kennen.

Ich werde hier nur die für uns relevanten Regeln auflisten, falls jemand Probleme mit der unendlichkeit haben sollte.

Bei einem Bruch oder einer Division, bei welcher durch mehrere Instanzen von $\infty$ gebrochen wird, zählt lediglich die höchste Instanz. Bedeutet folgendes:
$$
    \lim_{n\rightarrow \infty} (\frac{n^3}{n^3 + 3n^2 + 2n + 1}) = 1
$$

Weiters könnte man in bestimmten Fällen feststellen müssen, welches unendlich nun größer ist das andere. Hier gelten jedoch weiterhin die normalen Rechenregeln. $\infty$ ist zwar unendlich groß, jedoch ist $\infty$ relativ zu $\infty$. Bedeutet folgendes:
$$
     \infty > \infty -1\newline
     2\cdot\infty < 4\cdot \infty \newline
     \infty^2 > \infty\newline
     ...
$$

>[color=purple] Ganz interessante Beispiele zu diesem Thema sind 3.11)a) und 3.12) oder generell alle Beispiele auf S.51 im Buch der 4-5ten Klasse
## Folgen
Ordnet man jeder natürlichen Zahl $n \in \Bbb N$ eine reelle Zahl $a_n$ eindeutig zu, so entsteht eine unendliche (reelle) Folge $a_n$ Die einzelnen Werte heißen Folgenglieder und werden mit Indizes durchnummeriert.

$$
    Zahlenfolge: (a_n) = a_1, a_2, a_3, ..., a_n\newline
$$

### Arithmetische Folgen
Arithmetische Folgen $AF$ sind Zahlenfolgen, welche eine konstante differenz $d$ innerhalb der Folgenglieder aufweißen. 
#### Formeln
Berechnung eines bestimmten Glieds $a_n$ in der Folge mit bekannter differenz $d$ und erstem Folgenglied $a_1$:
$$
    a_{n} = a_1 + + (n-1) \cdot d 
$$

Berechnung eines bestimmten Glieds $a_n$ in der Folge mit 2 bekannten Folgengliedern:
$$
    a_n = \frac{a_{n+1} + a_{n-1}}{2}
$$

Berechnung der Differenz $d$ mithilfe 2 bekannter Folgenglieder $a_n$ und deren indize $n$
$$
    d_i = \frac{a_2-a_1}{n+1}
$$
### Geometrische Folgen
Geometrische Folgen $GF$ sind Zahlenfolgen, welche einen Quotienten $q$ aufweist, der auf 2 aufeinander Folgenden Gliedern konstant ist. 
#### Formeln
Allgemeine Gesetzlichkeit von Geometrischen Folgen:
$$
    \frac{a_{n+1}}{a_n} = q
$$
Bildungsgesetz:
$$
    a_n = a_1 \cdot q^{n-1}
$$

Berechnung eines bestimmten Glieds in der Folge:
$$
    a_n = \sqrt{a_{n+1} \cdot a_{n-1}}
$$
Will man zwischen zwei Werten $a_1$ und $a_2$ insgesamt $n$ weitere Zahlen als eine geometrische Folge einfügen, so gilt dabei für alle Quotienten der einzelnen Folgenglieder:
$$
    q_i = \sqrt[n+1]{\frac{a_2}{a_1}}
$$
## Reihen
Wenn man alle Glieder einer Folge aufsummiert, nennt man dies eine Reihe. Wenn man fancy ist kann man diesen Fall folgendermaßen beschreiben:
$$
   s_n = \sum_{i=1}^n a_i = a_1 + a_2 + a_3 + ... + a_n
$$
Hierbei wird unterhalb des Summenzeichens die Untergrenze und oberhalb die Obergrenze des Index $i$ angegeben, wobei die Summengrenzen jeweils ganze Zahlen sind. Im obigen Fall werden alle Folgenglieder $a_{\mathrm{i}}$ somit von $i=1$ bis $i=n$ aufsummiert.
### Arithmetische Reihen
Addiert man alle Glieder einer arithmetischen Folge, also eine Folge von Zahlen, die sich untereinander stets um den gleichen Wert d unterscheiden, so ergibt sich eine arithmetische Reihe.
$$
    s_n = \sum_{i=1}^n (a1 + (i-1) \cdot d) = n\cdot a_1 + \frac{n\cdot (n-1)}{2}\cdot d
$$
### Geometrische Reihen
Addiert man alle Glieder einer geometrischen Folge, also eine Folge von Zahlen, die sich untereinander stets um den gleichen Faktor $q$ unterscheiden, so ergibt sich eine geometrische Reihe. Der Wert $s_{n}$ einer endlichen geometrischen Reihe lässt sich folgendermaßen berechnen:
$$
    s_n = \sum_{i=1}^n a_1\cdot q^{i-1} = a_1 \cdot \frac{q^n-1}{q-1}
$$

Ob eine unendliche geometrische Reihe konvergiert, hängt vom Wert von q ab. Ist |q| > 1, so divergiert die Reihe; ist hingegen |q|<1, so konvergiert die Reihe, und es gilt:

$$
    \lim_{n\rightarrow \infty} a_1 \cdot \frac{q^n-1}{q-1} = \frac{a_1}{1-q}
$$

### Potenzreihen
Eine Potenzreihe ist im Prinzip ein unendlich langes Polynom.
Sie folgen dieser Form:
$$
    P(x) = \sum_{n=0}^\infty c_n (x-x_0)^n
$$
> mit einer beliebigen Folge $(a_{n})_{n\in \Bbb{N}_{0}}$ reeler oder komplexer Zahlen
> mit dem Entwicklungspunkt $x_0$ der Potenzreihe

#### Konvergenzradius
Der Konvergenzradius bestimmt in welchem Bereich um $x_0$ die Potenzreihe konvergiert.
Hier ein visuelles Beispiel eines Konvergenzradianten der Größe 1.
![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_44c1a091f0bdbbf6e228b546ded6c50b.png)
Wir haben uns aber nur für die reelle Achse zu interessieren, da die Matura davon ausgeht, dass wir PeepeePoopoo Brains sind die nicht mit imaginären Zahlen rechnen können.

Es gilt also folgender Sachverhalt:
$$
    \{-|r|\leq x^n \leq |r|\ \in konvergent\}
$$

##### Berechnung Konvergenzradius
Die Formel ist zu verwechseln ähnlich zu der des Quotientenkriteriums, nur ist hierbei das nächste Glied der Folge/Reihe im Nenner
$$
    r=\lim_{n\rightarrow \infty} \left| \frac{c_n}{c_{n+1}} \right|
$$

###### Beispiel
$$
    \sum_{n=1}^\infty \frac{x^n}{n} = \frac{x}n + \frac{x^2}2 + \frac{x^3}3 + ...
$$

$$
    r= \lim_{n\rightarrow \infty} \left|\frac{\frac{1}{n}}{\frac{1}{n+1}}\right| = \lim_{n\rightarrow \infty} \left|\frac{n+1}{n}\right|\newline
    l'hospital\Rightarrow\frac{\infty}{\infty};\ \infty \neq \infty \rightarrow \frac{f'(x)}{g'(x)}\newline
     r= \lim_{n\rightarrow \infty} \left|\frac{1}{1}\right| \Rightarrow r=1
$$

### Der Satz von Taylor / Taylor Reihen
> Für eine andere oder tiefere Erklärung siehe [Wikipedia zum Thema Taylorreihe](https://de.wikipedia.org/wiki/Taylorreihe)

Der Satz von Taylor gestattet es jede Funktion $y=f(x)$ an eine beliebige Stelle $x_0$ (meistens $x_0=0$) in eine sogenannte Taylor Reihe zu entwickeln. 
Für eine graphische Veranschaulichung einer Taylor Reihe in korellation mit einem Graphen siehe: [Graph von Wikipedia](https://de.wikipedia.org/wiki/Datei:Logarithm_GIF.gif)

Prinzipiell gilt für die Taylor Reihe: Umso mehr Glieder aufsummiert werden, desto mehr ähnelt die Reihe der gegebenen Funktion.

Das Bildungsgesetz der Taylor Reihe sieht wiefolgt aus:
$$
    T_{f(x;a)} = \sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!} \cdot (x-a)^n = \newline
    f(a) + f'(a)(x-a)+\frac{f''(a)}{2}(x-a)^2 + \frac{f'''(a)}{6}(x-a)^3 + ...
$$


#### Beispiel anhand von $y=cos(x)$
Entwickle die Funktion $f$ $y=cos(x)$ an der Position $x_0 = 0$ nach der Taylor Reihe.
$$
\begin{matrix}
    Allgemein & Bei\ Punkt\ 0 \\
    y    = cos(x)  & y   (0) = 1 \\
    y'   = -sin(x) & y'  (0) = 0 \\
    y''  = -cos(x) & y'' (0) = 1 \\
    y''' = sin(x)  & y'''(0) = 0 \\
    y^{(4)} = cos(x) & y^{(4)}= 1\\
    ... & ...
    \end{matrix}
$$

Also lautet diese Taylor Reihe:

$$
    cos(x) = \sum_{n=0}^\infty (-1)^n\frac{x^{2n+1}}{(2n+1)!} = \newline
    = 1 - \frac{x^2}{2} + \frac{x^4}{24} - ...
$$