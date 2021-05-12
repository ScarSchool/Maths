# Matrizen
###### tags: `Maths` `Matrix`

## Matrixalgebra und Matrixbasics
    Definition:
    Unter einer Matrix versteht man ein geordnetes Rechteckschema von Zahlen
### Grundsätzliches
Eine Matrix der 2ten Dimension kann Anhand $AxB$ beschrieben werden. $A$ gibt hierbei die Anzahl der Zeilen und $B$ die Anzahl der Spalten an
> Beispiel einer $3x3$ Matrix:

$$
Spalten\newline
A :=
	\left(
		\begin{matrix}
    \color{blue}1 & -3 & \color{purple}{2} \\
    5 & \color{blue}0.\color{purple}0 & 9 \\
    \color{purple}{-1} & 2 & \color{blue}7 \\
    \end{matrix}
	\right)
    Zeilen
$$

Die $\color{blue}{blau}$ markierte Diagonale ($[A_{1,1},A_{2,2},A_{3,3}]$) wird auch $\color{blue}{Hauptdiagonale}$ genannt.
Die $\color{purple}{lila}$ markierte Diagonale ($[A_{1,3},A_{2,2},A_{3,1}]$) wird auch $\color{purple}{Nebendiagonale}$ genannt 

Der Wert von $A_{2,3}$ der gegebenen Matrix entspricht $9$


### Spezielle Matrizen

#### Vektor
Vektoren sind spezielle Matrizen. Sie haben __exakt eine Spalte__.

> Beispiel Vektor $3ter$ Dimension:

$$
\overrightarrow b :=
	\left(
		\begin{matrix}  
        1 \\ 5 \\ -1 \\
        \end{matrix}
	\right) \rightarrow
    \left(
		\begin{matrix}  
        \overrightarrow b_{1,1} \\ 
        \overrightarrow b_{2,1} \\
        \overrightarrow b_{3,1} \\
        \end{matrix}
	\right)
$$

#### Diagonalmatrix
Alle Elemente die nicht in der $Hauptdiagonale$ liegen, haben den Wert $0$

> Beispiel $3x3$ Diagonalmatrix

$$
A :=
	\left(
		\begin{matrix}
    a & 0 & 0 \\
    0 & b & 0 \\
    0 & 0 & c \\
    \end{matrix}
	\right)
$$

#### Einheitsmatrix
Alle Elemente die in der $Hauptdiagonale$ liegen, haben den Wert $1$. Alle Restlichen betragen $0$

> Beispiel $3x3$ Einheitsmatrix

$$
A :=
	\left(
		\begin{matrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{matrix}
	\right)
$$

#### Matrix in Dreiecksform
Alle Elemente die über bzw. unter der $Hauptdiagonale$ liegen, haben den Wert $0$.

> Beispiel $3x3$ Matrix in Dreiecksform für Werte unter der $Hauptdiagonale$

$$
A :=
	\left(
		\begin{matrix}
    a & 0 & 0 \\
    b & b^2 & 0 \\
    c & c^2 & c^3 \\
    \end{matrix}
	\right)
$$


> Beispiel $3x3$ Matrix in Dreiecksform für Werte über der $Hauptdiagonale$

$$
A :=
	\left(
		\begin{matrix}
    a & b & c \\
    0 & b^2 & b^3 \\
    0 & 0 & c^3 \\
    \end{matrix}
	\right)
$$

#### Transponierte Matrix
Werden $Zeilen$ und $Spalten$ miteinander vertauscht, so erhält man eine transponierte Matrix $A^T$

> Beispiel Transponierte Matrix $A^T$ von $3x2$ Ausgangsmatrix $A$

$$
A :=
	\left(
		\begin{matrix}
    \color{blue}1 & \color{blue}2 & \color{blue}6 \\
    \color{purple}3 & \color{purple}{-3} & \color{purple}8 \\
    \end{matrix}
	\right) \Rightarrow 
    A^T := 
	\left(
		\begin{matrix}
    \color{blue}1 & \color{purple}3 \\
    \color{blue}2 & \color{purple}{-3} \\
    \color{blue}6 & \color{purple}8 \\
    \end{matrix}
	\right)
$$

#### Symmetrische Matrix
Ist die Transponierte Matrix $A^T$ identisch zur Ausgangsmatrix $A$, so spricht man von einer Symmetrischen Matrix

> Beispiel Symmetrische Matrix $A^T$ von $3x3$ Ausgangsmatrix $A$

$$
A :=
	\left(
		\begin{matrix}
    1 & 4 & 5 \\
    4 & 2 & 6 \\
    5 & 6 & 3 \\
    \end{matrix}
	\right) \Rightarrow
    A^T :=
	\left(
		\begin{matrix}
    1 & 4 & 5 \\
    4 & 2 & 6 \\
    5 & 6 & 3 \\
    \end{matrix}
	\right) 
$$


### Multiplikation einer Matrix mit einem Skalar
Jede Zelle einer Matrix wird mit dem Skalar multipliziert.

> Beispiel Multiplikation $3x3$ Matrix $A$ mit Skalar $s$

$$
A :=
	\left(
		\begin{matrix}
    1 & -3 & {2} \\
    5 & 0 & 9 \\
    {-1} & 2 & 7 \\
    \end{matrix}
	\right);\ s = 2
$$

$$
A \cdot s \Rightarrow 
	\left(
		\begin{matrix}
    2 & -6 & 4 \\
    10 & 0 & 18 \\
    -10 & 4 & 14 \\
    \end{matrix}
	\right)
$$

### Addition zweier Matrizen
Achtung: nur möglich bei selber Spalten und Zeilenanzahl.

Jede Zelle wird mit der Zelle an der selben Koordinate addiert. 
Sprich: $A_{1,1} + B_{1,1};\ A_{2,1} + B_{2,1};\ ...$
> Beispiel Addition zweier $2x2$ Matrizen

$$
A :=
	\left(
		\begin{matrix}
    5 & 1 \\
    -2 & 3 \\
    \end{matrix}
	\right);\ B :=
	\left(
		\begin{matrix}
    0 & -1 \\
    2 & 1 \\
    \end{matrix}
	\right); 
$$

$$
    A + B \Rightarrow 
	\left(
		\begin{matrix}
    5 & 0 \\
    0 & 4 \\
    \end{matrix}
	\right); 
$$

### Matrix-Vektor Produkt
Hierfür muss die "Matrixbreite" mit der "Vektorhöhe" übereinstimmen

$$
M :=
	\left(
		\begin{matrix}
    a & a^2 & a^3 \\
    b & b^2 & b^3 \\
    c & c^2 & c^3 \\
    \end{matrix}
	\right);
\overrightarrow t :=
	\left(
		\begin{matrix}  
        x \\ y \\ h \\
        \end{matrix}
	\right)
$$

$$
M\cdot \overrightarrow t = 
\left(
    \begin{matrix}
    a * x+ a^2 * y + a^3 * h \\
    b * x+ b^2 * y + b^3 * h \\
    c * x+ c^2 * y + c^3 * h \\
    \end{matrix}
    \right)
$$

### Determinante quadratischer Matrizen
Die Determinante ist eine Zahl die aus den Elementen einer quadratischen Matrix berechnet wird.

#### Berechnung der Determinante einer $2x2$ Matrix
In diesem Fall ist es ausgesprochen einfach die Determinante zu berechnen.
Man muss lediglich die Werte der $Haupdiagonale$ sowie die Werte der $Nebendiagonale$ miteinander multiplizieren, und diese Ergebnisse daraufhin miteinander addieren.

> Beispiel Determinantenberechnung $2x2$ Matrix

$$
	\left(
		\begin{matrix}
    \color{blue}5 & \color{purple}2 \\
    \color{purple}3 & \color{blue}4 \\
    \end{matrix}
	\right); 
$$

$$
    \color{blue}{5\cdot 4} + \color{purple}{2\cdot 3} = 26
$$

#### Berechnung der Determinante mithilfe des Entwicklungssatzes von Laplace
Ist eine Matrix nicht im $2x2$ Bereich, verwendet man den Laplace-Entwicklungssatz.

> Entwickelt man nach der i-ten Zeilen, so lautet die Formel

$$
det = \sum_{j=1}^n a_{ij} \cdot (-1)^{i+j} \cdot D_{ij}
$$
> Entwickelt man nach der j-ten Spalten, so lautet die Formel

$$
det = \sum_{i=1}^n a_{ij} \cdot (-1)^{i+j} \cdot D_{ij}
$$

>[color=brown] Jetzt haben wir aber ein Problem: Wir sind PeepeePoopooMonke Brains :poop::monkey: und wissen durch das reine Ansehen der Formel nicht, was die überhaupt auf irgendeine Weise auszusagen vermag, weshalb der Vorgang jetzt doch genauer beschrieben werden muss.

##### Methodik
Gegeben ist folgende Matrix:
$$
	A = \left(\begin{matrix}
		1 & 3 & -2 \\
		-2 & 5 & 4 \\ 
		7 & 3 & 1
	\end{matrix}\right)
$$

###### Schritt 1
Bestimme nach welcher Zeile und welche Spalte entwickelt wird. 
Wir entscheiden uns hier für Zeile 1 und Spalte 2 und entwickeln der Spalte nach, aber es ist jede Kombination möglich.
>[color=green] Notiere: Es ist von Vorteil jene Zeilen und Spalten zu wählen, die die meisten 0er beinhalten. Der Grund dafür wird sich erkenntlich Zeigen.

$$
\require{cancel}
A_{det} = 
	\left(\begin{matrix}
		\cancel{1} & \color{purple}{\cancel{3}} & \cancel{-2} \\
		-2 & \color{purple}{\cancel{5}} & 4 \\ 
		7 & \color{purple}{\cancel{3}} & 1
	\end{matrix}\right)
$$
###### Schritt 2
Notiere bei jeder Zelle ob sie plus oder minus ist. Fang mit + an und wechsle dann Zeile für Zeile ab.

$$
A_{det} = 
	\left(\begin{matrix}
		\cancel1^{\color{orange}+} & \color{purple}{\cancel{3}}^{\color{orange}-} & \cancel{-2}^{\color{orange}+} \\
		-2^{\color{orange}-} & \color{purple}{\cancel5^{\color{orange}+}} & 4^{\color{orange}-} \\ 
		7^{\color{orange}+} & \color{purple}{\cancel3^{\color{orange}-}} & 1^{\color{orange}+}
	\end{matrix}\right)
$$

###### Schritt 3
Jetzt wird der Spalte nach jeder Wert mit der verbleibenden Matrix (Jene die nicht durchgestrichen ist) multipliziert.
Wenn man sich für die Entwicklung nach einer Zeile entschieden hat, muss man natürlich den Vorgang der Zeile nach durchführen.

$$
	\left(\begin{matrix}
		\cancel1^{\color{orange}+} & \bbox[yellow]{\cancel3^{-}} & \cancel{-2}^{\color{orange}+} \\
		-2^{\color{orange}-} & \color{purple}{\cancel5^{\color{orange}+}} & 4^{\color{orange}-} \\ 
		7^{\color{orange}+} & \color{purple}{\cancel3^{\color{orange}-}} & 1^{\color{orange}+}
	\end{matrix}\right)
$$

>[color=green] Notiere: Das der Zelle zugewießene Vorzeichen wird jetzt beachtet

> Ergebnis erste Spalte

$$
\bbox[yellow]{-3} \cdot
	\left|\left(\begin{matrix}
		-2 &-4 \\
		7 & 1  
	\end{matrix}\right)\right|
    =
    -3 \cdot -30
$$

Dies wird jetzt für **jede** Zeile durchgeführt, in der sich die gewählte Spalte befindet.

$$
	\left(\begin{matrix}
		1^{\color{orange}+} & \color{purple}{\cancel3^{-}} & {-2}^{\color{orange}+} \\
		\cancel-2^{\color{orange}-} & \bbox[yellow]{\cancel5^{\color{orange}+}} & \cancel4^{\color{orange}-} \\ 
		7^{\color{orange}+} & \color{purple}{\cancel3^{\color{orange}-}} & 1^{\color{orange}+}
	\end{matrix}\right)
$$
> Ergebnis der zweiten Spalte

$$
\bbox[yellow]{5} \cdot
	\left|\left(\begin{matrix}
		1 &-2 \\
		7& 1  
	\end{matrix}\right)\right|
    =
    5\cdot 15
$$

Und die letzte Zeile:

$$
	\left(\begin{matrix}
		1^{\color{orange}+} & \color{purple}{\cancel3^{-}} & {-2}^{\color{orange}+} \\
		-2^{\color{orange}-} & \color{purple}{\cancel5^{\color{orange}+}} & 4^{\color{orange}-} \\ 
		\cancel7^{\color{orange}+} & \bbox[yellow]{\cancel3^{\color{orange}-}} & \cancel1^{\color{orange}+}
	\end{matrix}\right)
$$
> Ergebnis der dritten Spalte

$$
\bbox[yellow]{-3} \cdot
	\left|\left(\begin{matrix}
		1 &-2 \\
		-2& 4  
	\end{matrix}\right)\right|
    =
    -3 \cdot 0
$$

###### Schritt 4 
Nun werden die Ergebnisse aller Spalten (oder Zeilen) miteinander addiert und man erhält die Determinante.

$$
    det= 
    -3 \cdot -30 +
    5\cdot 15 +
    -3 \cdot 0  = 165
$$

### Lösen von linearen Gleichungssystemen beliebiger Ordnung mithilfe Matrizenmultiplikation
     Die händische Matrizenmultiplikation wird nicht behandelt. 
     Bei Interesse, wie diese funktioniert bitte einfach melden.

Man kann lineare gleichungssysteme beliebiger Ordnung mithilfe von Matrizen sehr simpel lösen.

#### Methodik
Gegeben ist folgendes Gleichungssystem:
$$
\begin{matrix}
    I) & 3x &+& 2y & + & -z & = & 4\\
    II)& -2x &+& 4y & + & 3z & = & 15\\
    III)& x &+& -y & + & 5z & = & 14\\
\end{matrix}
$$

Nun fügt man die Werte auf der linken Seite des $Gleichungssystems$ in eine $Koeffizientenmatrix$ $A$ ein und die Ergebnisse dieser in einen $Konstantenvektor$ $\overrightarrow b$und bestimmt einen $Variablenvektor$ $\overrightarrow x$.

$$
    A:= \left(
\begin{matrix}
    3x  & 2y & -z & 4\\
    -2x & 4y & 3z & 15\\
     x  & -y & 5z & 14\\
\end{matrix}\right);\ 
\overrightarrow b :=\left(
\begin{matrix}
    4\\ 15\\ 14\\
\end{matrix}\right);\ 
\overrightarrow x :=\left(
\begin{matrix}
    x\\ y\\ z\\
\end{matrix}\right)
$$

Diese Werte werden in folgende Formel eingesetzt

$$
A \cdot \overrightarrow x = \overrightarrow b
$$

Welche zuerst auf $\overrightarrow x$ umgeformt werden muss, um die Ergebnisse dieser Matrix zu erhalten

$$
1\cdot \overrightarrow x = \overrightarrow b \cdot A^{-1} \Rightarrow 
\overrightarrow x =\left(
\begin{matrix}
    1\\ 2\\ 3\\
\end{matrix}\right)
$$


## Matrixfunktionen
Dieses Dokument behandelt Matrixfunktionen im 2 Dimensionalen Raum.

Für weitere Informationen:
https://www.grund-wissen.de/mathematik/lineare-algebra-und-analytische-geometrie/matrizen.html
https://www.cg.tuwien.ac.at/courses/CG1/textblaetter/02%20Geometrische%20Transformationen.pdf


#### Reihenfolge von Aktionen

$$
Rückaktion \cdot Aktion \cdot Voraktion = Neuer Vektor \\
Rückaktion = Voraktion^-1\ ( in\ meisten Fällen)
$$

### Operations-Matrizen

Für Transformationen in Matrixschreibweise verwendet man homogene koordinaten.
Das heißt: Jedem Punkt wird eine zusätzliche Koordinate "h" zugeordnet.
Der Punkt (x,y) würde dadurch als (x,y,h) angeschrieben werden, wobei h meist den Wert 1 annimmt.


#### Translationsmatrix

Verschiebt einen bestimmten Ortsvektor A um einen Vektor t
<iframe src="https://www.geogebra.org/calculator/v5f22hmx?embed" width="800" height="400" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

$t = translationsvektor; A = Ausgangspunkt; A' = Punkt nach translation$

> Translationsmatrixvariablen

$$
\overrightarrow t := \left(
		\begin{matrix}
    x \\
    y \\
    \end{matrix}
	\right);
T :=
	\left(
		\begin{matrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{matrix}
	\right);
A :=
	\left(
		\begin{matrix} 
        a \\ b \\
        \end{matrix}
	\right)
$$

> Anwendung der Translation

$$
A' := M_{\overrightarrow t}\cdot A
$$

> Aufgelöste Translation

$$
A' = 
\left(
    \begin{matrix}
    1 & 0 & x \\
    0 & 1 & y \\
    0 & 0 & 1 \\
    \end{matrix}
    \right) \cdot
\left(
    \begin{matrix}
    a \\ b \\ 1
    \end{matrix}
    \right) =
\left(
    \begin{matrix}
    1*a+0*b+c*x \\ 
    0*a+1*b+y*1 \\ 
    0*a+0*b*1*1
    \end{matrix}
    \right)=
\left(
    \begin{matrix}
    a+c*x \\ 
    b+y \\ 
    1
    \end{matrix}
    \right)
$$

#### Drehungsmatrix

> Allgemeine Drehungsmatrixvariablen

$$
D(\alpha) = 
\left(
    \begin{matrix}
    cos(\alpha) & -sin(\alpha) & 0 \\
    sin(\alpha) & cos(\alpha) & 0 \\
    0 & 0 & 1 \\
    \end{matrix}
    \right) ;
A = 
\left(
    \begin{matrix}
     x \\ y
    \end{matrix}
    \right) ;
$$


<iframe src="https://www.geogebra.org/calculator/qettnmbg?embed" width="800" height="400" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

$M = Ursprung; A = Ausgangspunkt; A' = Punkt nach angewandter Drehung$
##### Drehung um Ursprung

Dreht Ortsvektor um bestimmten Winkel $\alpha$ an Ursprung ( 0 | 0 )

> Anwendung der Drehung

$$
A' := D(\alpha) * A
$$

##### Drehung um Drehungspunkt
 
Dreht Ortsvektor um bestimmten Winkel $\alpha$ an Drehungspunkt M

> Zusätzliche Drehungsmatrixvariablen für Drehungspunkt M

$$
M := 
\left(
    \begin{matrix}
     x \\ y
    \end{matrix}
    \right) ;
\overrightarrow t := M^{-1} = \left(
    \begin{matrix}
     -x \\ -y
    \end{matrix}
    \right) ;
T :=
	\left(
		\begin{matrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{matrix}
	\right);
$$

> Translationsmatrix wird konfiguriert

$$
T = \left(\begin{matrix}
    1 & 0 & -x \\
    0 & 1 & -y \\
    0 & 0 & 1 \\
    \end{matrix}
	\right);
$$

> Punkt translatiert zum Ursprung, wird gedreht und wird zum Drehungspunkt zurücktranslatiert

$$
A' = T^{-1} \cdot D(\alpha) \cdot T \cdot A
$$

#### Spiegelungsmatrix

Spiegelt Vektor oder Punkt um die x- oder y-Achse

<iframe src="https://www.geogebra.org/calculator/japetadg?embed" width="800" height="400" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

$A = Spiegelung\ an\ x-Achse; B = Spiegelung\ an\ y-Achse$

> Allgemeine Spiegelungsmatrixvariablen

$$
A:= \left(\begin{matrix}
    x \\ y
    \end{matrix}
	\right);
$$

##### Spiegelung an x-Achse

> Operationsmatrix für Spiegelung um x-Achse

$$
SP_x:= \left(\begin{matrix}
    1 & 0 & 0 \\
    0 & -1 & 0 \\
    0 & 0 & 1
    \end{matrix}
	\right);
$$

> Anwendung der Spiegelung um x-Achse

$$
A' := SP_x \cdot A
$$

> Aufgelöste Spiegelung

$$
A' =  \left(\begin{matrix}
    1 & 0 & 0 \\
    0 & -1 & 0 \\
    0 & 0 & 1
    \end{matrix}
	\right) \cdot 
\left(\begin{matrix}
    x \\ y \\ 1
    \end{matrix}
	\right) = 
\left(\begin{matrix}
    1*x + 0*y + 0*1 \\
    0*x + -1*y + 0*1 \\
    0*x + 0*y + 1*1
    \end{matrix}
	\right) =
\left(\begin{matrix}
    x \\
    -y\\
    1
    \end{matrix}
	\right)
$$

##### Spiegelung an y-Achse

> Operationsmatrix für Spiegelung um y-Achse

$$
SP_y:= \left(\begin{matrix}
    -1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1
    \end{matrix}
	\right);
$$

> Anwendung der Spiegelung um y-Achse

$$
A' := SP_y \cdot A
$$

> Aufgelöste Spiegelung

$$
A' =  \left(\begin{matrix}
    -1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1
    \end{matrix}
	\right) \cdot 
\left(\begin{matrix}
    x \\ y \\ 1
    \end{matrix}
	\right) = 
\left(\begin{matrix}
    -1*x + 0*y + 0*1 \\
    0*x + 1*y + 0*1 \\
    0*x + 0*y + 1*1
    \end{matrix}
	\right) =
\left(\begin{matrix}
    -x \\
    y\\
    1
    \end{matrix}
	\right)
$$

#### Skalierungsmatrix

Verlängert einen Ortsvektor um einen Skalierungswert. 

<iframe src="https://www.geogebra.org/calculator/dhpb7ptb?embed" width="800" height="400" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

> Skalierungsmatrix variablen

$$
A_{ska} =  \left(\begin{matrix}
    \lambda & 0  \\
    0 & \lambda 
    \end{matrix}
	\right) ;
 \overrightarrow p :=  \left(\begin{matrix}
    x \\ y
    \end{matrix}
	\right) ;
$$

> Anwendung der Skalierung

$$
\overrightarrow{p}' = \overrightarrow p * A_{ska}
$$

> Aufgelöste Skalierung

$$
\overrightarrow p' =  \left(\begin{matrix}
    \lambda & 0  \\
    0 & \lambda 
    \end{matrix}
	\right) \cdot 
\left(\begin{matrix}
    x \\ y
    \end{matrix}
	\right) =
\left(\begin{matrix}
    \lambda* x + 0*y \\ 
     0*y + \lambda*y
    \end{matrix}
	\right) =
\left(\begin{matrix}
    \lambda* x \\ 
     \lambda*y
    \end{matrix}
	\right)
$$