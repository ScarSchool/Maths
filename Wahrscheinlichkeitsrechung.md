# Wahrscheinlichkeitsrechnung
#### tags: `Maths` `Probability`


## Wiederholung Kombinatorik
> Nicht zurücklegen; Reihenfolge wird beachtet: [color=orange]

$$
     nCr \rightarrow V_{n,k} = \frac{n!}{(n-k)!} 
$$

> Nicht zurücklegen; Reihenfolge wird nicht beachtet [color=orange]

$$
    nPr \rightarrow V_{n,k} = \frac{n!}{(n-k)!} 
$$

## Laplace - Experiment
### Grundsätzliches
Trifft zu wenn alle folgenden Anforderungen zutreffen:

* Jedes Ergebnis hat die selbe chance zuzutreffen
* Das Experiment ist beliebig oft wiederholbar
* Chance für eintritt konstant

$$
    P = \frac{Anzahl\ günstiger\ Fälle}{Anzahl\ mögliche\ Fälle}
$$

### Darstellung als Baum


![Poissonverteilung / Binom. Verteilung](https://www.mathematik.de/images/Erste_Hilfe/Stochastik/urneBR1_4.svg)

### Formel
> Variablen [color=orange]

$$
    n = Wie\ viele\ werden\ gezogen?; k = Wie\ oft\ wird\ gezogen?; \\p = Wahrscheinlichkeit\ günstiger\ Fall 
$$

> Wahrscheinlichkeitsberechnung für günstiger Fall [color=orange]
> > Bei $\left(	\begin{matrix}
> > n \\ k
> > \end{matrix}\right)$ müssen nCr oder nPr entsprechend gewählt werden

$$
    W =
    \left(\begin{matrix}
    n \\ k
    \end{matrix}\right)
    \cdot p^k \cdot (1-p)^{n-k}\\
$$


## Binomialverteilung
### Grundsätzliches

> To Be Added [color=red]

### Darstellung in einem Diagramm

<iframe src="https://www.geogebra.org/classic/n8764kzb?embed" width="800" height="400" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

### Formel

> Wahrscheinlichkeitsberechnung für günstiger Fall [color=orange]
> > Bei $\left(	\begin{matrix}
> > n \\ k
> > \end{matrix}\right)$ müssen nCr oder nPr entsprechend gewählt werden

$$
    W =
    \left(\begin{matrix}
    n \\ k
    \end{matrix}\right)
    \cdot p^k \cdot (1-p)^{n-k}\\
$$



## Gaus'sche Normalverteilung
Weitere Informationen:
https://www.mathematik.de/algebra/86-erste-hilfe/stochastik/andere-verteilungen/1497-die-normalverteilung

### Grundsätzliches
Vereinfacht ausgedrückt entsteht die Gaus'sche Normalverteilung aus der Binomialverteilung wenn die Stichprobengröße $n \rightarrow \infty$ wandern lässt

> Die Glockenkurve nähert sich der x-Achse asymptotisch [color=orange]


### Formeln

> Erwartungswert / Mittelwert [color=orange]
> > Setzt bei der Wahrscheinlichkeitsfunktion den "Mittelpunkt" der durch den begrenzungsvariablen definierten Fläche 


$$
\mu = n \cdot p
$$

> Standardabweichung [color=orange]
> > Bestimmt unter anderem die "Breite" bzw. "Schlankheit" der Glockenkurve 

$$
\sigma = \sqrt{n\cdot p \cdot(1-p)} = \sqrt{\mu \cdot(1-p)}
$$

> Wahrscheinlichkeitsfunktion [color=orange]
> > Die Funktion für das erhalten der Wahrscheinlichkeit für jeden Wert x
$$
    f(x) = \frac 1{\sqrt{2\pi}\cdot \sigma} \cdot e^{-\frac12{(\frac{x-\mu}{\sigma})^2}}
$$

### Darstellung der Wahrscheinlichkeitsfunktion
> Probiere es aus: [color=blue]
> > Setze den Wert $\sigma$ und beobachte wie die Kurve schrumpft/wächst 
> (Achte auf die Angabe auf der x-Achse)> 
> 
> > Setze den Wert $\mu$ und beobachte wie das Zentrum der Fläche verändert wird.
> 
> > Setze die begrenzungsvariablen und beobachte wie sich die Fläche der Funktion verändert. (Bei P(-1<x<1) die 1 bzw -1 verändern ändern oder schwarze Pfeile auf x-Achse ziehen)

<iframe src="https://www.geogebra.org/classic/yums9kev?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

### Beispiele für Wahrscheinlichkeitsfunktionen
#### Angabe vom Maximalwert
> Die blaue Fläche ($f(x)$) entspricht der Wahrscheinlichkeit, dass die Zufallsvariable $x$ __höchstens__ den Wert $x_0=(0.5)$ annimmt [color=purple]

![Maximalbegrenzung Normalverteilung](https://codimd.s3.shivering-isles.com/demo/uploads/upload_364b65b75e0e4b75f3fe8cd752a93fbc.png)

#### Angabe vom Minimalwert
> Die blaue Fläche ($1-f(x)$) entspricht der Wahrscheinlichkeit, dass die Zufallsvariable $x$ __mindestens__ den Wert $x_0=(-0.5)$ annimmt [color=purple]

![Minimalbegrenzung Normalverteilung](https://codimd.s3.shivering-isles.com/demo/uploads/upload_05c9d5ec2153780ec76e463276f06a39.png)

#### Angabe von Minimal- als auch Maximalwert!
> Die blaue Fläche ($1-f(x)$) entspricht der Wahrscheinlichkeit, dass die Zufallsvariable $x$ einen Wert  __zwischen__ $x_0=(-1)$ und $x_1=(1)$ annimmt  [color=purple]



![Doppelwertbegrenzung Normalverteilung](https://codimd.s3.shivering-isles.com/demo/uploads/upload_790d46dd5a1e423f735661683b3b8baf.png)

> Nehmen $x_0$ und $x_1$ den selben Wert an, nennt man diesen $a$. 
> Im oberen Beispiel wäre $a=1$ [color=yellow]
> 
> Die weißen Flächen des Graphen lassen sich für die linke mit $F(\mu - a)$ und die rechte mit $F(\mu + 
> a)$ berechnen (Es kommt der selbe Wert heraus)

### Die Standardisierte Normalverteilung
Als __standardisiert__ gilt eine Normalverteilung wenn $\mu = 0$ gesetzt ist
 
Das bedeutet für $f'(x)=0$, was den Höhepunkt des Graphen beschreibt, dass $x$ den Wert 0 annimmt.

Kurzgesagt ist der Höhepunkt der Funktion nun in der Mitte des Graphen 
($\mu=0;f'(x)\rightarrow x=0$) (sprich standardisiert)

#### Berechnung
> Standardisieren [color=orange]
> > Der standardisierte Wert $z$ wird dann in die standardisierte Wahrscheinlichkeitsfunktion $\Phi(z)$ eingesetzt.
> > 
> > $z$ wird daraufhin in der Standardnormalverteilungs-Tabelle gesucht und der gefundene Wert entspricht daraufhin der Wahrscheinlichkeit.
> > 
> > Die Tabelle ist zu finden unter: 
> > http://www.analysis-schmeisser.uni-jena.de/matia2media/Baaske/Schaden/tabelle.pdf

$$
    z= \frac{x-\mu}{\sigma}
$$

> Beispiel [color=blue]

$$
    \mu = 5; \sigma = 2\\
    F(x) = ?\\
    z= \frac{6-2}{2} = 0.5\\
    F(6) = \Phi(z=0.5) \rightarrow 0.5\ in\ Tabelle\ nachschauen \rightarrow \Phi(0.5)= 0.6915\\
    Die\ Wahrscheinlichkeit\ ist\ \underline{69.15\%}
$$

> Gutes Beispiel für Zuhause: Ü9.64 (Lösung in eurem Buch nachschauen oder bei mir nachfragen) [color=yellow]

### Rechenbeispiel Überbuchung
https://a.hpthek.at/ebook/164/?page=233
#### Ü 9.80

> Globale Angaben

$$
    p = 0.8; n = 400;
$$

##### 1) a)
$$
    k = 90; n_{bin} = 100;
$$

> Mit nCr

$$
     W =
    \left(\begin{matrix}
    100 \\ 90
    \end{matrix}\right)
    \cdot 0.8^{90} \cdot (0.2)^{10} = 0.00336 \rightarrow
    \underline{0.336\%}
$$
##### 1) b)
$$
    \mu := 400 \cdot 0.8 = 320;
    \sigma := \sqrt{400 \cdot 0.8 \cdot 0.2} = 8
$$

$$
    F(310 < x < 325) = F(325.5) - F(309.5)
$$

$$
    z_1 = \frac{309.5-320}{8} = -1.3125; 
    z_2 = \frac{325.5-320}{8} = 0.6875;
$$

> z-Werte in der Tabelle dementsprechend nachschauen

$$
    \Phi(-1.3125) = 1-\Phi(1.31) = 1 - 0.9049 = 0.0951 \rightarrow 9.51\%\\
    \Phi(0.6875) = \Phi(0.69) = 0.7549 \rightarrow 75.49\%
$$

$$
    F(325.5) - F(309.5) = 75.49 - 9.51 = \underline{65.98\%}
$$

##### 2)

> Was bedeutet die Angabe?

$$
    W(z) = 0.0001; n_{ges} = ?
$$

$$
    P(x>400) = 1 - P(x<401) < 0.0001 \rightarrow\\
    P(x<400) > 0.9999
$$
> Also:

$$
    F(n_{ges};0.8;400) > 0.9999
$$

$$
    \Phi(\frac{400-n_{ges}\cdot 0.8+0.5}{\sqrt{n_{ges}\cdot 0.8\cdot 0.2}}) > 0.9999
$$

> _0.9999 nachschauen in Tabelle_

$$
    z := 3.59 < \frac{400-n_{ges}\cdot 0.8+0.5}{\sqrt{n_{ges}\cdot 0.8\cdot 0.2}} / * \sqrt{...}
$$

$$
    3.59 \cdot \sqrt{n_{ges}\cdot 0.16} < 400.5-0.8\cdot n_{ges} \ /ロ^2
$$ 

$$
    3.59^2 \cdot n_{ges}\cdot 0.16 < (400.5-0.8\cdot n_{ges})^2 /Binom\ auflösen
$$ 

$$
    3.59^2 \cdot n_{ges}\cdot 0.16 < 400.5^2 - 2\cdot (400.5\cdot 0.8\cdot n_{ges}) + 0.64n_{ges}^2\ /-( 3.59^2 \cdot n_{ges}\cdot 0.16)
$$ 

$$
    0 < 0.64n^2_{ges} - 640.8n_{ges} - 3.59^2\cdot 0.16n_{ges} + 400.5^2\\
    0 < 0.64n^2_{ges} - 642.86n_{ges}+ 400.5^2
$$

> Anwendung von Mitternachtsformel

$$
    x_{1,2} = \frac{-b+/-\sqrt{b^2-4ac}}{2a}\\
    x_{1,2} = \frac{642.86-\sqrt{-642.86^2-4\cdot 0.64 \cdot 400.5^2}}{2\cdot 0.64} = \underline{462.04}
$$

