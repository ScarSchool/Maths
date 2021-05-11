# Matrixfunktionen
#### tags: `Maths` `Matrix`

Dieses Dokument behandelt Matrixfunktionen im 2 Dimensionalen Raum.

Für weitere Informationen:
https://www.grund-wissen.de/mathematik/lineare-algebra-und-analytische-geometrie/matrizen.html
https://www.cg.tuwien.ac.at/courses/CG1/textblaetter/02%20Geometrische%20Transformationen.pdf

## Grundprinzipien

Für Transformationen in Matrixschreibweise verwendet man homogene koordinaten.
Das heißt: Jedem Punkt wird eine zusätzliche Koordinate "h" zugeordnet.
Der Punkt (x,y) würde dadurch als (x,y,h) angeschrieben werden, wobei h meist den Wert 1 annimmt.

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

### Reihenfolge von Aktionen

$$
Rückaktion \cdot Aktion \cdot Voraktion = Neuer Vektor \\
Rückaktion = Voraktion^-1\ ( in\ meisten Fällen)
$$

## Operations-Matrizen

### Translationsmatrix

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

### Drehungsmatrix

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
#### Drehung um Ursprung

Dreht Ortsvektor um bestimmten Winkel $\alpha$ an Ursprung ( 0 | 0 )

> Anwendung der Drehung

$$
A' := D(\alpha) * A
$$

#### Drehung um Drehungspunkt
 
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

> Punkt transponiert zum Ursprung, wird gedreht und wird zum Drehungspunkt zurücktransponiert

$$
A' = T^{-1} \cdot D(\alpha) \cdot T \cdot A
$$

### Spiegelungsmatrix

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

#### Spiegelung an x-Achse

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

#### Spiegelung an y-Achse

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

### Skalierungsmatrix

> KOMMT NICHT ZUR SCHULARBEIT [color=red]

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