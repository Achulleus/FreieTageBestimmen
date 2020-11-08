# FreieTageBestimmen
Für dieses Programm werden folgende Librarys benötigt:
- mysql-connector-java-8.0.2 1.jar
- jason-20200518.jar
- javafix.media.jar
- javafix.graphics.jar
- javafix.fxml.jar
- javafix.controls.jar
- javafix.base.jar
- commons-io-2.8.0.jar

Dieses Programm ist für die Bestimmung der Tage andenen Frei ist. Dies kann in verschiedenen Problemstellungen hilfreich sein z.B.: wenn man wissen möchte an welchem Tag es am Besten ist nicht zu arbeiten.

Der erste Teil besteht in der Bestimmung der Tage an deinen frei ist. Dies habe ich mit einer ArrayList Feiertage gelöst. Als erstes werden die statischen Feiertage in die ArrayList hinzugefügt (in der Methode FeiertageBestimmen). Danach ist die List DynamischeFeiertage der Methode getWert übergeben worden und in dieser Methode werden die Dynamischen Feiertage aus der API geholt und zur ArrayList feiertage hinzugefügt. Abschließend wird die Methode tagUeberpruefen() aufgerufen, in der die ArrayList Feiertage überprüft wird welche Tage diese Daten haben. Somit wird gespeichert wie viele Tage jedes Wochentages von der angegebenen Zeitspanne Feiertage sind. Die Zeitspanne wird beim ausführen des Programms abgefragt und der Benutzer kann das Anfangsjahr und Endjahr bestimmen.

Der zweite Teil besteht in der Visualisierung durch javafx. Ich habe mich hier für einKuchendiagramm entschieden, da ich finde das man hier denn prozentuellen Anteil der verschiedenen Wochentage am einfachsten und schnellsten erkennen kann. Dies ist mit der Methode start gelöst.

Der dritte Teil besteht in der Speicherung der Abfragen in eine Datenbank. Dies ist sehr hilfreich wenn man im späteren Verlauf alle Abfragen noch einmal gesammelt sehen will. Die erste wichtige Methode ist das erstellen der Tabelle, dies geschieht in der Methode tabelleErstellen(). Zuerst wird versucht eine Verbindung mit dem Treiber herzustellen. Anschließend mit der Datenbank. Hier wird nun mit dem Statement eine Tabelle erstellt. Danach muss in diese Tabelle die verschiedenen Einträge gespeichert werden. Dies geschieht in der Methode datenbankeingabe(). Es wird wieder die Verbindungen hergestellt und anschließend ein INSERT INTO Befehl ausgeführt in dem die Daten in der zuvor erstellten Tabelle gespeichert werden. Die dritte Methode wird anschließend zur Ausgabe der Tabelle verwendet. Diese Methode ist die Datenbankausgabe() in der wieder die Verbindungen erstellt werden und im Anschluss die Dateien mit einem ResultSet Objekt aus der Datenbank geholt und formatiert werden. Anschließend werden diese noch ausgegeben.




