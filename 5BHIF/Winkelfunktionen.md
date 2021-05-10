# Winkelfunktonen / Vermessungsaufgaben
## Fläche eines Dreiecks
### Herron Formel
Ist die Go-To Formel für ein Algemeines Dreieck. Die Formel ist trügerisch schwer aber auf genaueren Blick ist sie wirklich simpel.
Zuerst braucht man die durchschnittliche Seitenlänge:
$$
    s=\frac{a+b+c}{2}
$$

Und danach wendet man die Heron Formel an und erhält die Fläche:

$$
    A= \sqrt{s\cdot (s-a) \cdot (s-b) \cdot (s-c)}
$$

### Allgemeine Flächenformel
![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_ba59b5ff520bf9f083a719ad52df8eac.png)
Ist eine Höhe gegeben, kann man die Fläche einfach folgendermaßen errechnen:
$$
    A = \frac{c \cdot h_c}{2} = \frac{b \cdot h_b}{2} = \frac{a \cdot h_a}{2}
$$
Ist die Höhe nicht gegeben kann uns der Sinus weiterhelfen:
$$
    A = \frac{c \cdot b}{2} \cdot sin(\alpha)
$$

>[color=blue] Der Sinus hat hier die Funktion, das Dreieck so anzupassen, dass es in dieser Formel wie ein rechtwinkliges Dreieck ist. (Für eine tiefere Erklärung siehe: [mathebibel.de](https://www.mathebibel.de/flaecheninhalt-dreieck#:~:text=Das%20ursprüngliche%20Dreieck%20ist%20genau,2%20⋅%20g%20⋅%20h%20))
## Kantenkomponenten
![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_fda27efef3771b0a981c8cee49f2fd53.png)
Der Begriff "Kantenkomponente" wird hier verwendet, um die Werte eines Punktes zu beschreiben. Im oberen Bild sind alle Kantenkomponenten angegeben. 


### Liste der Kantenkomponenten eines Dreiecks:
| Punkt | Seite | Winkel |
| -------- | -------- | -------- |
| $A$     | $a$     | $\alpha$     |
| $B$     | $b$     | $\beta$     |
| $C$     | $c$     | $\gamma$     |


## Winkelfunktions-Sätze
### Sin-Satz
Der Sinus-Satz ist sonderlich praktisch, wenn man 2 "Komponenten" einer Seite / Kante und eine Komponente einer Anderen bereits bekannt sind, und die andere Komponente einer Seite zu berechnen ist.
#### Sinus Satz Verbot
Man darf mit dem Sinus Satz niemals den größten Winkel eines Dreiecks berechnen. Dies liegt an der Natur der Sinus Funktion. 
Ist ein Winkel über 90°, als Beispiel 100°, ist der Wert der Winkelfunktion in der gleiche wie der von 80°
#### Formel
$$
\frac{a}{\sin(\alpha)} = \frac{b}{\sin(\beta)} = \frac{c}{\sin(\gamma)}
$$
### Cos-Satz
Der Cosinus-Satz wird hauptsächlich dann verwendet, wenn 2 Seiten gegeben sind, und nun eine Kantenkomponente der letzten Seite berechnet werden muss.
#### Formel
$$
c^2 = a^2 + b^2 - 2ab \cdot \cos(\gamma)
$$
Der Cos-Satz ist eine Generalisierung des Satz-des-Pythagoras.
Der erweiternde Teil ist da, um den Fall eines nicht-Rechtwinkligen-Dreiecks zu kompensieren
# Berechnung am allgemeinen Dreieck
## Bekanntheitsfälle
An einem allgemeinen Dreieck sind selten alle Kantenkomponenten gegeben. Um unbekannte Werte eines Dreiecks zu berechnen, müssen mindestens 3 Kantenkomponenten bekannt sein.
Weiters ist die Konstelation der bekannten Komponenten zu beachten, sprich Bekanntheitsfäll.e

>[color=red] Bei allen Bekanntheitsfällen ist es sehr empfohlen eine entsprechende Skizze zu machen
### SSS
![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_236a17e3d823445d70312afac6371e47.png)
Hierbei sind alle 3 Seiten eines Dreiecks gegeben.

#### Schritt 1: Größter Winkel mittels Cos-Satz
Der größte Winkel ist immer der Winkel der gegenüberliegenden Seite. 
>[color=blue]Im dargestellten Beispiel ist das $\gamma$ der größte Winkel, da er gegenüber von $c$ liegt.

$$
    c^2 = a^2+b^2 - 2ab \cdot cos(\gamma)
$$
> Umgeformt ergibt das:

$$
    cos(\gamma) = \frac{a^2+b^2-c^2}{2ab}
$$

#### Weitere Schritte: Fehlende Winkel mittels Sinus-Satz
Da der Sinus Satz der weitaus simpelste ist und gut dafür geeignet ist, fehlende Komponenten eines Dreiecks auszurechnen ist er für einen solchen Fall perfekt.
$$
    \frac{sin(\alpha)}{a} = \frac{sin(\gamma)}{c}
$$
> Umgeformt ergibt das:

$$
 sin(\alpha) = \frac{sin(\gamma) \cdot a}{c}
$$

#### Geheimtipp: Der letzte Winkel lässt sich mit dem Winkelsummensatz des Dreiecks berechnen
Alle Winkel eines Dreiecks ergeben $180°$. Deshalb kann man hier folgendes machen:
$$
    \beta = 180 - \alpha - \gamma
$$
### SWS
![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_89e18136b2b60f43f283de3f76da67fb.png)
Hierbei sind 2 Seiten eines Dreiecks und der Winkel der fehlenden Seite gegeben.
>[color=blue] Diese Konstelation ist leicht zu erkennen, da der Winkel zwischen den beiden Seiten als "Eingeschlossener Winkel" gilt.

#### Schritt 1: Letzte Seite mittels Cos-Satz
Mit der SSS Konstelation ist leicht zu erkennen, welcher Winkel der größte ist (siehe SSS).

$$
    a = \sqrt{b^2+c^2-2bc\cdot cos(\alpha)}
$$

#### Schritt 2: NICHT-größten Winkel mittels Sin-Satz
Der größte Winkel ist immer der Winkel der gegenüberliegenden Seite. 
>[color=blue]Im dargestellten Beispiel ist nicht eindeutig zu erkennen, welche Seite nun am längsten ist.
>Wir gehen hier davon aus, dass b die längste Seite ist (Diese Annahme ist nur ohne eine Angabe nötig, also bitte nicht nachmachen)

$$
    sin(\alpha) = \frac{sin(\gamma) \cdot a}{c}
$$
#### Letzter Schritt: Fehlender Winkel mittels Winkelsummensatz
Alle Winkel eines Dreiecks ergeben $180°$. Deshalb kann man hier folgendes machen:
$$
    \beta = 180 - \alpha - \gamma
$$

### WSW
![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_ca275f22d0e0156af0e1a031d2d31dc7.png)
Hierbei ist 1 Seite eines Dreiecks und die anbindenden Winkel der Kantenkomponente gegeben.


#### Schritt 1: Fehlender Winkel mittels Winkelsummensatz
Alle Winkel eines Dreiecks ergeben $180°$. Deshalb kann man hier folgendes machen:
$$
    \gamma = 180 - \alpha - \beta
$$

#### Weitere Schritte: Fehlende Seiten mittels Sinus-Satz
Es ist quasi egal, welche Seite man zuerst ausrechnet, da sie in diesem Fall nicht mehr von anderen Seiten abhängig sind.

$$
    a = \frac{sin(\alpha) \cdot c}{sin(\gamma)}
$$

> Und zur Vervollständigung noch die letzte Seite

$$
    b = \frac{sin(\beta) \cdot c}{sin(\gamma)}
$$
### SSW
> Für diesen Fall gibt es kein gutes Dreieck das ich von einer Webseite klauen kann, deshalb hab ich schnell eins mit GeoGebra™ gemacht :)

![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_6d15f5866211d6110a4981a95da191fe.png)
Dies ist eindeutig die schwierigste Konstelation von allen.
Das gesuchte Dreieck kann zweideutig sein, wenn $b > c$ ist und $b != h_c$ entspricht. (Wie letzteres feststellbar ist, wird später noch geklärt)

#### Schritt 1: NICHT-eingeschlossenen (fliegenden) Winkel mittels sin-Satz
Hier wird das Sinus Satz Verbot nicht beachtet um die Möglichkeit für das zweite Dreieck offen zu halten.
>[color=blue]Würde man dem Sin-Satz Verbot folgen wäre theoretisch nur eine der 2 Dreiecke möglich, was falsch ist und als Fehler gelten würde.

$$
    sin(\gamma) = \frac{sin(\beta) \cdot c}{b}
$$

>[color=red]Würde für $\gamma$ nun exakt 90° als Ergebnis herauskommen, gäbe es nur ein mögliches Dreieck mit diesen vorgegebenen Kantenkomponenten

#### Schritt 2.1: Fehlender Winkel mittels Winkelsummensatz
Alle Winkel eines Dreiecks ergeben $180°$. Deshalb kann man hier folgendes machen:
$$
    \alpha = 180 - \beta - \gamma
$$

#### Schritt 3.1: Fehlende Seite mittels Sin-Satz
$$
    a = \frac{sin(\alpha) \cdot c}{sin(\gamma)}
$$
>[color=yellow] FRAGE: Welches a ist das nun? a1 oder a2? Und wie ist die andere Möglichkeit für a auszurechnen?

>[color=red] ANTWORT: 

![](https://codimd.s3.shivering-isles.com/demo/uploads/upload_9a78d99a27f3788dc4502b573a6894a8.png)

#### Schritt 2.2: Zweites Gamma berechnen
Wie man in diesem Bild erkennen kann, ist der gegenüberliegende Winkel von $\gamma$ ebenfalls $\gamma$.
$\gamma 2$ entspricht den fehlenden Graden eines Halbkreises, also rechnet man:
$$
    180 - \gamma = \gamma 2
$$

#### Schritt 3.2: Zweites Alpha berechnen
Da sich das $\gamma$ verändert hat, ändert sich auch der davon abhängige Winkel $\alpha$
$$
    \alpha 2 = 180 - \gamma 2 - \beta
$$

#### Letzter Schritt: Alternative unbekannte Seite mittels Sinus-Satz
Zu guter letzt kann man nun endlich die zweite Variante der unbekannten Seite berechnen und das Dreieck komplettieren.
$$
    a = \frac{sin(\alpha2) \cdot c}{sin(\gamma2)}
$$