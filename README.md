# Neuronale Netzwerke

Ein neuronales Netzwerk ist ein **mathematisches Modell**, das vom menschlichen Gehirn inspiriert ist. 
Es besteht aus miteinander verbundenen **Neuronen**, die ähnlich wie Nervenzellen zusammenarbeiten.
Das Netzwerk wird trainiert, indem es aus **Beispieldaten** lernt, Muster zu erkennen, und wird dadurch in der Lage, komplexe Probleme zu lösen.

## Einsatzgebiete

Neuronale Netzwerke finden in vielen Bereichen Anwendung. Hier ein paar Beispiele:

* **Computer Vision**
    * Informationen und Erkenntnisse aus Bildern / Videos gewinnen
        * Gesichtserkennung (z.B. in Smartphones)
        * Klassifizierung von handgeschriebenen Zahlen
        * Erkennung von Verkehrszeichen für selbstfahrende Autos

* **Spracherkennung**
    * Analyse menschlicher Sprache
        * Videos / Aufzeichnungen automatisch mit Untertiteln versehen
        * Gespräche in Textdokumente umwandeln (z.B. Meeting-Protokolle)
    * Verwendet von virtuellen Assistenten wie **Amazon Alexa** oder **Siri**

* **Natürliche Sprachverarbeitung (Natural Language Processing, NLP)**
    * Bedeutung und Erkenntnisse aus Texten extrahieren
        * Chatbots, die auf Kundenfragen antworten
        * Zusammenfassung von Dokumenten / Generieren von Artikeln

* **Empfehlungsmodule**
    * Persönliche Empfehlungen basierend auf Benutzeraktivitäten 
        * **Netflix** oder **Amazon Prime**

## Neuron

Ein **Neuron** ist die grundlegende Baueinheit eines neuronalen Netzwerks und entspricht in gewisser Weise einer Nervenzelle im menschlichen Gehirn. Es hat die Aufgabe, Eingabewerte zu verarbeiten, eine Berechnung durchzuführen und basierend auf dieser Berechnung ein Signal weiterzugeben. 
Ein Neuron besteht im Wesentlichen aus **einem einzigen Wert**, der als **Aktivierung** bezeichnet wird.

### Funktionsweise

1. **Eingaben empfangen**
    * Jedes Neuron empfängt Eingaben von anderen Neuronen / Eingabedaten des Netzwerks
    * Eingaben $x_i$ sind die Features einer Observation
        * Stellen die Werte dar, die das Neuron verarbeiten muss
    * Beispiel:
        * Bilder (28x28 Pixel) sollen klassifiziert werden
        * Jeder Pixel hat einen gewissen Farbwert, der dem Wert eines Neurons entspricht
        * Eingabeschicht hat also 784 Neuronen 

2. **Gewichte anwenden**
    * Jede Eingabe $x_i$ wird mit einem **Gewicht** $w_i$ multipliziert
    * Gewichte bestimmten die Wichtigkeit jeder Eingabe für das Neuron
        * Je höher dieses ist, desto mehr Einfluss hat die Eingabe auf das Ergebnis
    * Gewichtete Eingabewerte werden addiert:
        * $z = (w_1 \cdot x_1) + (w_2 \cdot x_2) + \dots + b$
    * Der **Bias b** passt das Ergebnis zusätzlich an und hilft, das Modell **flexibler** zu machen

3. **Aktivierungsfunktion anwenden**
    * Der zuvor berechnete Wert z wird durch eine **Aktivierungsfunktion** transformiert
    * Entscheidet, ob ein Neuron aktiviert wird
        * Ob Signal weitergeleitet wird oder nicht

4. **Signal weiterleiten**
    * Berechneter Wert wird weitergegeben, wenn Neuron durch die **Aktivierungsfunktion** aktiviert wird
    * Dieses dient als Eingabe für die Neuronen der nächsten Schicht

## Aufbau

Ein neuronales Netzwerk besteht aus mehreren Schichten, die zusammenarbeiten:

* **Eingabeschicht (Input Layer)**
    * Nimmt Rohdaten auf und schickt diese an die nächste Schicht weiter

* **Verborgene Schicht (Hidden Layer)**
    * Hier passiert die eigentliche Verarbeitung
    * Jedes Neuron bekommt die Werte der vorherigen Schicht
        * Multipliziert diese Werte mit **Gewichten** und addiert einen **Bias**
    * Anschließend wird eine **Aktivierungsfunktion** angewendet

* **Ausgabeschicht (Output Layer)**
    * Liefert das Ergebnis
    * Hat genau so viele Neuronen wie mögliche Ausgaben (Klassen)

## Lernen 

Das neuronale Netzwerk lernt, indem es die Fehler korrigiert:


Neuron -> Thing that holds a number

The value inside the neuron is called activation. For example, if we have a hand-written digit
that is represented by 28x28 pixels, each pixel is a neuron that contains the grey-scale of that pixel.

So 28 x 28 is 784, which is the number of neurons of the first layer.

The last layer of the neural networks represents the end results. So, if we should classify hand-written digits from 0 to 9 there are 10 neurons at the end. Each neuron represents a result value from 0 to 9.

These neurons also have a value between zero and one. It is the value the system things a given image will corresponde most with. 

Between the first layer and the last layer there are some hidden layers.

Between these neurons, each connection gets a weight. These weights are all numbers.

Activations should be between 0 and 1.

Learning means that the weights and biases will be changed to find the optimal settings.

