# Malaria-Erkennung-aus-Zellbildern
Dieses Projekt implementiert ein Convolutional Neural Network (CNN), um anhand von Mikroskop-Bildern von Blutzellen automatisch zu erkennen, ob die Zellen mit Malaria infiziert oder nicht infiziert sind.

# **Projektziele* 
- Aufbau einer robusten Pipeline zur Datenvorverarbeitung und Normalisierung medizinischer Bilddaten.
- Implementierung eines CNN-Modells, das in der Lage ist, Merkmale von infizierten und nicht infizierten Zellen zu unterscheiden.
- Evaluation des Modells hinsichtlich Genauigkeit und Verlustfunktion auf einem unabhängigen Testdatensatz.

# **Datensatz*
**Quelle:** TensorFlow Datasets – Malaria
**Gesamtumfang:** ca. 27.558 Bilder (RGB, 2 Klassen)
**Labelstruktur:**
  
  0 = uninfected
  1 = parasitized

# **Methodik*
**1. Datenaufbereitung:**
- Resize auf 224 × 224 Pixel
- Normalisierung der Pixelwerte auf 0–1

**2. Modellarchitektur (LeNet-inspiriert):**
- Mehrere Convolutional Layers mit Batch Normalization und MaxPooling
- Dense-Layer mit Dropout zur Regularisierung
- Sigmoid-Output für binäre Klassifikation

**Training:**
- Optimizer: Adam (Lernrate 0,001)
- Loss-Funktion: Binary Crossentropy
- Anzahl Epochen reduziert (aufgrund begrenzter Rechenressourcen in Colab)

**Evaluation:**
- Bewertung des Modells auf dem Testdatensatz
- Visualisierung der Trainings- und Validierungsmetriken
