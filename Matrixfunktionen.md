# Matrixfunktionen

## Grundprinzipien

Für Translationen in Matrixschreibweise verwendet man homogene koordinaten.
Das heißt: Jedem Punkt wird eine zusätzliche Koordinate "h" zugeordnet.
Der Punkt (x,y) würde dadurch als (x,y,h) angeschrieben werden, wobei h meist den Wert 1 annimmt.

### Matrix-Vektor Produkt

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
    a * x+ a^2 * y + a^3 * z \\
    b * x+ b^2 * y + b^3 * z \\
    c * x+ c^2 * y + c^3 * z \\
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

Verschiebt einen bestimmten Vektor / Punkt A um einen Vektor t

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
A' := M\cdot A
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

#### Drehung um Ursprung

Dreht Vektor oder Punkt um bestimmten Winkel an Ursprung ( 0 | 0 )

> Anwendung der Drehung

$$
A' := D(\alpha) * A
$$

#### Drehung um Drehungspunkt

Dreht Vektor oder Punkt um bestimmten Winkel an Drehungspunkt M

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

$$
"A = Spiegelung\ an\ x-Achse" \\
"B = Spiegelung\ an\ y-Achse"
$$

<iframe src="https://www.desmos.com/calculator/m33zy9me0d?embed" width="100%" height="400px" frameborder="0"></iframe>


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

Verlängert einen Ortsvektor um einen Skalierungswert.

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
