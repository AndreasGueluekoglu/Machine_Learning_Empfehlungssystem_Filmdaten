# Machine_Learning_Empfehlungssystem_Filmdaten
Empfehlungssystem für Filmdaten

## Einführung in die Thematik
Dieses Projekt stellt einen Aufbau eines  einfachen Empfehlungssystems für eine Filmdatenbank das. Dieses System soll folgendes Ziel erreichen: Auf Basis der angesehenen Filme in der Vergangenheit des Benutzers sollen Filmvorschläge gemacht werden. <br>
Grundsätzlich sind Empfehlungssysteme nichts anderes als eine automatisierte Form eines „Shop Counter Guy“. Dieser wird nach einem bestimmten Produkt. Hierbei wird nicht nur das eine Produkt vorgeschlagen, nachdem gesucht wird. Vielmehr werden auch auf Basis des Kaufverhaltens die verwandten Produkten vorgeschlafen, die gekauft werden können. Im spezifischen Fall soll das System auf Basis der angesehenen Filme des Nutzers individuelle, relevant bzw. verwandte Filme vorschlagen, die noch nicht angeschaut wurden. 

## Erklärung des Datensatzes 

## Überblick über die Vorgehensweise 

## Vorverarbeitung und Präparation von den ausgewählten Daten 

## Data Preparation - Machine Learning
- Daten selektieren: 
    - Welche Daten sind verfügbar?
    - Welche Daten sind nicht verfügbar?
    - Welche Daten sind nicht erforderlich, um die Frage zu beantworten?
    - Nur bei kleinen Problemstellungen ist die Vorauswahl der Daten bereits getroffen
- Daten vorbereiten:
    - Formatting: Daten in ein geeignetes Format bringen
    - Cleaning: Löschen oder ergänzen von fehlenden Daten
    - Sampling: Große Datenauswahl vs. Laufzeit des Algortihmus -> Representatives Datenset
- Daten transformieren: 
    - Scaling: Daten weisen verschiedene Einheiten auf (z. B. KG, Euro). ML Algorithmen können mit Attributen mit normalisierten Werten besser umgehen
    - Decomposition:Komplexe Attribute sollten in ihre Bestandteile heruntergebrochen werden, da ML Algortihmen damit besser zurechtkommen. (z. B. Datum und Uhrzeit in zwe Felder  aufteilen
    - Aggregation: Verschiedene “Features” können in ein “Feature” zusammengefasst warden. (z. B. ein Eintrag pro Kundenlogins -> Anzahl der Logins


## Was soll programmiert werden?
- Supervised Learning mit 2 Algorithmen, z.b. KNN, K-Means (Trennung von Training- und Testdaten); Optional: Deep Learning mit Tensorflow
- Korrelationsanalyse mit Numpy (Regression); Optional: 3D-plotting mit matplotlib
- Datenstrukturierung/-manipulation mit Pandas
- Netzwerkanalyse mit networkx
- Visualisierung der Ergebnisse (Scatter Plots, Heatmap, Sankey, etc.)

## Aufgaben
- Jupyter Notebook inkl. Kommentaren & Erklärung zur Auswahl der Methode & Interpretation der Ergebnisse
- Zusammenfassung der Ergebnisse (Beispielsweise in einer READ.me Datei)
- Projektpräsentation mit max. 5 Folien (30 min Präsentation und 10 min Fragen)
