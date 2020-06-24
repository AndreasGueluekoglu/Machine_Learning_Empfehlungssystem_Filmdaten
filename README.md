# Machine_Learning_Empfehlungssystem_Filmdaten
Implementierung eines Empfehlungssystems für Filmdaten

## Einführung in die Thematik

Empfehlungssysteme haben Unternehmensanwendung gefunden, indem sie allen Top-Playern auf dem Online-Markt geholfen haben, explizites Feedback zu bekommen. Diese Bewertungen sind
besonders in der Unterhaltungs- und E-Commerce-Branche wichtig, da Kundenbindungen von diesen Bewertungen betroffen sind. Amazon empfiehlt Produkte basierend auf der Kauf- und Bewertungshistorie. Abgesehen davon stützt sich der Streaming-Dienstleister Netflix auf solche Bewertungsdaten, um sein Empfehlungssystem mit den besten Empfehlungen für Filme und Fernsehserien zu versorgen. Die Benutzer sollen Filme vorgeschlagen werden, die personalisiert und für den Benutzer am relevantesten sein. <br>
Dieses Projekt stellt des Aufbau eines solchen, einfachen Empfehlungssystems für eine Filmdatenbank das. Das System soll folgendes Ziel erreichen: Auf Basis der angesehenen Filme in der Vergangenheit des Benutzers sollen Filmvorschläge gemacht werden. <br>
Grundsätzlich sind Empfehlungssysteme nichts anderes als eine automatisierte Form eines „Shop Counter Guy“. Hierbei wird nicht nur das eine Produkt vorgeschlagen, nachdem gesucht wird. Vielmehr werden auch auf Basis des Kaufverhaltens die verwandten Produkten vorgeschlafen, die gekauft werden können. Im spezifischen Fall soll das System auf Basis der angesehenen Filme des Nutzers individuelle, relevant bzw. verwandte Filme vorschlagen, die noch nicht angeschaut wurden. <br>
Die Fähigkeit des Systems, personalisierte Inhalte basierend auf dem Verhalten der Vergangenheit zu empfehlen, ist unglaublich. Es macht den Kunden Freude und gibt Ihnen einen Grund, immer wieder auf die Website zurückzukehren.

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

## Wichtige Links
### Für die Ausarbeitung der Theorie und der Notebooks
- https://blog.codecentric.de/en/2019/07/recommender-system-movie-lens-dataset/
- https://grouplens.org/datasets/movielens/1m/
- https://www.analyticsvidhya.com/blog/2016/06/quick-guide-build-recommendation-engine-python/
- https://grouplens.org/datasets/movielens/
- https://analyticsindiamag.com/how-to-build-your-first-recommender-system-using-python-movielens-dataset/
- https://docs.google.com/presentation/d/1xLQKXNQfaJ-YMVB8-F1XWkyfynYy1bQRkO4NAlkRsSQ/edit?usp=sharing 
- https://analyticsindiamag.com/how-to-build-your-first-recommender-system-using-python-movielens-dataset/ 
- https://blog.codecentric.de/en/2019/07/recommender-system-movie-lens-dataset/ 
- https://github.com/oekosheri/Recommender-movie/blob/master/Recom_walk_through.ipynb 
- https://blog.codecentric.de/en/2019/07/recommender-system-movie-lens-dataset/ 
- https://heartbeat.fritz.ai/recommender-systems-with-python-part-ii-collaborative-filtering-k-nearest-neighbors-algorithm-c8dcd5fd89b2 

### Link zu der Google-Präsentation 
- https://docs.google.com/presentation/d/1xLQKXNQfaJ-YMVB8-F1XWkyfynYy1bQRkO4NAlkRsSQ/edit?usp=sharing





