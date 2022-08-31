Funktionsweise
	Der Workflow soll http-delete Befehle der Studentenprofile, die nach Sharepointliste gelöscht sein müssten, in einer Email ausgeben. Diese Befehle werden anschließend in der Graph Umgebung ausgeführt.

Einrichten
1. Der Account Löschen Schritt wird aus dem Workflow entfernt
2. Es wird ein Schritt vom Typ Variable "Initialize Variable" erstellt (bespielsweise nach "Letzter Tag im letzten Semester"). Diese Variable soll ein Array von DELETE Befehlen enthalten.
3. In der Schleife Account löschen wird an die Stelle vom Custom Connector ein Schritt vom Typ Variable "Append to Array" der Wert "https://graph.microsoft.com/v1.0/users/{id}" übergeben. Anstelle der {id} wird die Id aus dem Schritt Studentenprofil abfragen übergeben.
4. Abschließend kann nach Vollendung der Schleife ein Email Schritt beigefügt werden, der eine Email an die Email aus dem Schritt "Fehler senden an" mit der Stringvariable im Body sendet.

Umsetzung
	Nachsem der Workflow ausgeführt wurde sollten Sie eine Email erhalten haben, die die http-delete befehle enthält.
	1. Öffnen Sie den [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorerGraph).
	2. Loggen Sie sich ein.
	3. Stellen Sie die Parameter der Befehlszeile um
		- DELETE
		- v1.0
	4. Übergeben Sie jeden der Http-Delete Befehle und führen Sie diese einzeln aus.
	5. In [[Azure]]>>Active Directory>>Useres>>deleted Users können Sie nun das Ergebnis überprüfen.