# Machine_Learning_Empfehlungssystem_Filmdaten
Implementierung eines Empfehlungssystems für Filme basierend auf dem MovieLens-Dataset

## Grundlegendes
### Einführung in die Thematik

Empfehlungssysteme haben Unternehmensanwendung gefunden, indem sie allen Top-Playern auf dem Online-Markt geholfen haben, explizites Feedback zu bekommen. Diese Bewertungen sind
besonders in der Unterhaltungs- und E-Commerce-Branche wichtig, da Kundenbindungen von diesen Bewertungen betroffen sind. Amazon empfiehlt Produkte basierend auf Kauf- und Bewertungshistorie der Kunden. Abgesehen davon stützt sich der Streaming-Dienstleister Netflix auf solche Bewertungsdaten, um sein Empfehlungssystem mit den besten Empfehlungen für Filme und Serien zu versorgen. Den Benutzern sollen Filme vorgeschlagen werden, die für den individuellen Benutzer am relevantesten sind. <br>
Dieses Projekt stellt den Aufbau eines solchen, einfachen Empfehlungssystems für Filme aus dem MovieLens-Dataset (siehe 'Wichtige Links') dar. Das System soll folgendes Ziel erreichen: Auf Basis der angesehenen Filme in der Vergangenheit sollen Filmvorschläge gemacht werden. <br>
Grundsätzlich soll das System auf Basis der angesehenen Filme des Nutzers  ähnliche bzw. verwandte Filme vorschlagen, die noch nicht angeschaut wurden. <br>

### Erklärung des Datensatzes 
MovieLens ein Empfehlungssystem für Filme und wird von GroupLens, einem Forschungslabor an der Universität von Minnesota, betreut. MovieLens ist nicht kommerziell und werbefrei. GroupLens Research hat Ratingdatensätze von der MovieLens Website (http://movielens.org) gesammelt und zur Verfügung gestellt. Die Datensätze wurden über verschiedene Zeiträume gesammelt. Es stehen Datensätze in unterschiedlichen Größen und von unterschiedlichen Zeiträumen zur Verfügung. Zu Bildungs- und Forschungszwecken wird ein kleiner und ein großer Datensatz bereitgestellt.
Die Datensätze und werden im Laufe der Zeit angepasst. Früher veröffentlichte Versionen werden nicht durch die Movielens Website archiviert, sodass eine exakte Reproduktion nicht gewährleistet werden kann. Dementsprechend sind die Daten über folgenden Link abzurufen https://workupload.com/file/svMgz6CetV4.
Der Datensatz besteht aus 100 000 Bewertungen (Ratings) und 3 600 Tags vergeben von rund 600 Nutzern, angewandt auf 9 000 Filme. Zum Zeitpunkt der Verarbeitung wurde der Datensatz zuletzt  im September 2018 durch GroupLens aktualisiert.

Die Daten liegen im CSV-Format vor. Es werden nur Filme aufgeführt, welche mindestens ein Rating oder ein Tag verzeichnen. Ein Film-Rating wird mittels Skala von 0 bis 5 mit einer Schrittweite von 0,5 vergeben. Bei einem Tag handelt es sich um Key Word(s), welche die Nutzer dem Film zugewiesen haben. 

Die Filme sind mit einer eindeutigen ID, dem entsprechenden Titel und zutreffenden Genres versehen. Bei dem Genre können ebenfalls Kombinationen vorkommen, welche über eine Pipe "|" getrennt dargestellt sind. Deren Auflistung erfolgt alphabetisch. Folgende Genres sind in den Daten verzeichnet:
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

Sämtliche Informationen liegen in Englischer Sprache vor.
## Datenvorbereitung
- Die allgemeine Vorverarbeitung ist im Notebook DataVisualisation hinterlegt. Die jeweiligen Vorverarbeitungsschritte der einzelnen Algorithmen unterscheiden sich von der allgemeinen Vorverarbeitung. 

## Überblick über die Vorgehensweise 
Grundsätzlich wird bei der Implementierung eines Empfehlungssystems für Filmdaten zwischen zwei unterschiedlichen Vorgehensweisen unterschieden. Beide Verfahren können mittels unterschiedlicher Algorithmen implementiert werden.
1. Collaborative Filtering <br>
   1.1 KNN-Algorithmus <br>
2. Content-Based-Filtering <br> 
   2.1 TFIDF-Vectorizing <br> <br> 
![alt text](https://miro.medium.com/max/998/1*O_GU8xLVlFx8WweIzKNCNw.png)

Für jeden Algorthmus ist eine individuelle Datenvorbereitung erforderlich, welche in den ensprechenden Notebooks genauer erläutert wird.


### Collaborative Filtering
- Idee des Verfahrens anhand eines Beispiels: Wenn Person 1 die Filme "A", "B" und "C" und Person 2 die Filme "B", "C" und "D" mag, dann weisen die Personen ähnliche Interessen auf. Demnach sollte Person 1 den Film "D" und Person 2 den Film "A" mögen.
- Dieser Algorithmus basiert vollständig auf den vergangenen Verhaltensweisen einer Person. Hierbei ist der Kontext nicht von Bedeutung. Diese Vorgehensweise führt dazu, dass das Verfahren einer der am häufigsten verwendeten Algorithmen ist. Es ist nicht abhängig von zusätzlichen, externen Informationen.

#### K-Nearest-Neighbors-Algorithmus (KNN)
##### Allgemeine Beschreibung
Der KNN-Algorithmus trifft keine Annahmen über die zugrundeliegende Datenverteilung. Stattdessen stützt sich das Verfahren auf die Ähnlichkeit der Elementmerkmale. Wenn der KNN-Algorithmus eine Vorhersage über einen Film trifft, berechnet er den "Abstand" zwischen dem Zielfilm und jedem anderen Film in der Datenbank. Hierbei können unterschiedliche Distanzarten herangezogen werden. Anschließend wird eine Rangfolge der Abstände erstellt und die k- nächstgelegenen Nachbarfilme als die ähnlichsten Filmempfehlungen zurückgegeben.

##### Ergebnisse der Durchführung
Die Ergebnisse des KNN-Algorithmus sind im Notebook KNN dargestellt.

### Content-Based-Filtering
- Idee des Verfahrens anhand eines Beispiels: Wenn einer Person bestimmte Filme gefallen, dann sollen dieser Person Filme mit ähnlichem Inhalt vorgeschlagen werden.
- Demnach basiert das Verfahrens auf der Ähnlichkeit des Inhalts der empfohlenen Filme.
- Das Verfahren findet im Allgemeinen Anwendung, wenn Inhalt und Genre der Filme bekannt sind

#### TF-IDF-Vectorizing
##### Allgemeine Beschreibung
TF-IDF ist ein Verfahren, um anhand von Key Words den Inhalt eines Textes zu bestimmen. Dazu werden zwei Metriken verwendet: TF (term frequency) und IDF (inverse document frequency). TF beschreibt die Häufigkeit eines Keywords in einem Text, IDF bezieht sich auf die Häufigkeit eines Key Words in einem Text im Vergleich zu anderen Texten. Diese Kennzahlen werden in einen Vektor umgewandelt. Ähneln sich zwei Vektoren, so ist davon auszugehen, dass sich auch der Inhalt der zugehörigen Texte ähnelt.

##### Beschreibung des Anwednungsfalls MovieLens
Bei einem Content-Based-Filtering basiert ein Empfehlungssystem auf Information über den Inhalt eines Films. In diesem speziellen Anwendungsfall liegen von den Usern vergebene Tags und Genres vor, welchen die einzelnen Filme zugeordnet werden können. Diese Tags und Genres werden zu einem String zusammengefasst und durch TF-IDF-Vectorizing ein einen Vektor umgewandelt. Ist dieser Vektor ähnlich zu anderen Vekotoren, so kann mit hoher Wahrscheinlichkeit angenommen werden, dass sich die entsprechenden Filme inhaltlich ähneln. Der inhaltliche Zusammnehang wird durch die zugewiesenen Tags und Genres prognostiziert

##### Ergebnisse der Durchführung
Die Ergebnisse des TF-IDF´-Vectorizing sind im Notebook TFIDF-Vectorizing dargestellt.
