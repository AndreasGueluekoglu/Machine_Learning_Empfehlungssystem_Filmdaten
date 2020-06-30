# Machine_Learning_Empfehlungssystem_Filmdaten
Implementierung eines Empfehlungssystems für Filmdaten

## Einführung in die Thematik

Empfehlungssysteme haben Unternehmensanwendung gefunden, indem sie allen Top-Playern auf dem Online-Markt geholfen haben, explizites Feedback zu bekommen. Diese Bewertungen sind
besonders in der Unterhaltungs- und E-Commerce-Branche wichtig, da Kundenbindungen von diesen Bewertungen betroffen sind. Amazon empfiehlt Produkte basierend auf der Kauf- und Bewertungshistorie. Abgesehen davon stützt sich der Streaming-Dienstleister Netflix auf solche Bewertungsdaten, um sein Empfehlungssystem mit den besten Empfehlungen für Filme und Fernsehserien zu versorgen. Die Benutzer sollen Filme vorgeschlagen werden, die personalisiert und für den Benutzer am relevantesten sein. <br>
Dieses Projekt stellt des Aufbau eines solchen, einfachen Empfehlungssystems für eine Filmdatenbank das. Das System soll folgendes Ziel erreichen: Auf Basis der angesehenen Filme in der Vergangenheit des Benutzers sollen Filmvorschläge gemacht werden. <br>
Grundsätzlich sind Empfehlungssysteme nichts anderes als eine automatisierte Form eines „Shop Counter Guy“. Hierbei wird nicht nur das eine Produkt vorgeschlagen, nachdem gesucht wird. Vielmehr werden auch auf Basis des Kaufverhaltens die verwandten Produkten vorgeschlafen, die gekauft werden können. Im spezifischen Fall soll das System auf Basis der angesehenen Filme des Nutzers individuelle, relevant bzw. verwandte Filme vorschlagen, die noch nicht angeschaut wurden. <br>
Die Fähigkeit des Systems, personalisierte Inhalte basierend auf dem Verhalten der Vergangenheit zu empfehlen, ist unglaublich. Es macht den Kunden Freude und gibt Ihnen einen Grund, immer wieder auf die Website zurückzukehren.

## Erklärung des Datensatzes 
MovieLens wird von GroupLens, einem Forschungslabor an der Universität von Minnesota, betrieben. MovieLens ist nicht kommerziell und werbefrei. GroupLens Research hat Ratingdatensätze von der MovieLens Website (http://movielens.org) gesammelt und zur Verfügung gestellt. Die Datensätze wurden über verschiedene Zeiträume gesammelt. Es stehen unterschiedliche Daten zu unterschiedlichen Größen und Zeiträumen zu Verfügung. Zu Bildungs- und Forschungszwecken wird ein kleiner und ein großer Datensatz bereitgestellt.
Die Datensätze ändern sich im Laufe der Zeit und sind für die Berichterstattung über Forschungsergebnisse nicht geeignet. Früher veröffentlichte Versionen werden nicht durch die Movielens Website archiviert, sodass eine exakte Reproduktion nicht gewährleistet werden kann. Dementsprechend sind die Daten über folgenden Link abzurufen https://workupload.com/file/svMgz6CetV4.
Der Datensatz besteht aus 100 000 Bewertungen und 3 600 Tag-Anwendung, angewandt auf 9 000 Filme von 600 Nutzern. Zum Zeitpunkt der Verarbeitung wurde der Datensatz zuletzt September 2018 durch GroupLens aktualisiert.

Die Daten liegen als CSV-Dateien vor und sind einspaltig als "comma-separated-values" gespeichert. Es werden nur Filme aufgeführt, welche mindestens ein Rating oder ein Tag verzeichnen. Ein Film-Rating wird via 0,5 Sterne Bewertung vergeben, wobei sich eine Skala von 0,5 - 5 Sternen ergibt. Bei einem Tag handelt es sich um eine kurze Beschreibung des jeweiligen Filmes, bestehend aus einem Wort oder einem kurzen Satz. Dabei wurde dementsprechend subjektiv durch einen Nutzer ein kurze Beschreibung des Films vergeben. 
Die Filme sind mit einer eindeutigen ID versehen sowie dem entsprechenden Titel, als auch Genre. Bei dem Genre können ebenfalls Kombinationen vorkommen, welche über eine Pipe "|" getrennt dargestellt sind. Deren Auflistung erfolgt alphabetisch. Folgende Genres sind in den Daten verzeichnet:
- Action
- Adventure
- Animation
- Children's
- Comedy
- Crime
- Documentary
- Drama
- Fantasy
- Film-Noir
- Horror
- Musical
- Mystery
- Romance
- Sci-Fi
- Thriller
- War
- Western
- (no genres listed)
Sämtliche Informationen liegen auf der Englischen Sprache vor.

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





