Allgemeine Hilfe
	- Der Flowchecker in Power Automate liefert bereits erste Hinweise.
	- Bei Schritten mit Connections kann unter den 3 Punkten >> my Connections die Verbindung erneuert werden.
	- Beim Flow Test können fehlerhafte Schritte erkannt werden und erste Hinweise anhand der in dem fehlerhaften Schritt beinhalteten Informationen erfasst werden.

Wo tritt der Fehler auf?
	1. Switch Monat
		- Überprüfen sie den Wert. Dieser sollte aus dem Schritt Monat übergeben werden
	2. Setze letztes/vorletztes Wintersemester/Sommersemester
		- Überprüfen Sie die Werte in Value. Diese sollten aus dem Schritt Jahr zusammensetzen 
	3. Studentenliste sperren/löschen abfragen
		Vermutlich konnte die Sharepoint Liste nicht gefunden werden.
			In diesem Fall können Sie die
				- [[Sharepointliste einrichten]] oder
				- die "Filter Query" Daten anpassen.
			- Vergewissern Sie sich, dass "Site Adress" und "List Name" in diesem Workflow mit der [[SharePoint]] Liste übereinstimmen.
			- Vergewissern Sie sich, dass die "Filter Query" Daten in diesem Workflowschritt mit den Spaltennamen in der [[SharePoint]] Liste übereinstimmen.
	4. Je Student sperren/löschen
		- Ist der Wert gleich dem Value der vorherig abgefragten Studentenliste?
		- Ist die Sharepointliste [[Sharepoint Konsistenz|konsistent]]?
		Ist in einem der Subschritte der Fehler aufgetreten?
			1. Sharepoint Profil deaktiviert/Nutzer angelegt setzen
				1. Sind die Werte der Felder "Id" und "Title" aus der Sharepoint-Liste übergeben worden? 
				2. Vermutlich konnte die Sharepoint-Liste nicht gefunden werden.
				In diesem Fall können Sie die
					- [[Sharepointliste einrichten]] oder
					- die "Filter Query" Daten anpassen.
				- Vergewissern Sie sich, dass "Site Adress" und "List Name" in diesem Workflow mit der [[SharePoint]] Liste übereinstimmen.
				- Vergewissern Sie sich, dass die "Filter Query" Daten in diesem Workflowschritt mit den Spaltennamen in der [[SharePoint]] Liste übereinstimmen.
			2. Email an Student senden 1/2
				Entstammen die Werte direkt aus dem Sharepointvalue?
			3. Email Fehler 2/3 senden
				Sind die Werte in diesem Schritt existent?
			4. Account Löschen 
			    1.  Überprüfen Sie, ob die Verbindung in Azure abgelaufen ist. [https://portal.azure.com/#home](https://portal.azure.com/#home) 
			        Ändern Sie in diesem Fall das Gültigkeitsdatum.  
			    2. Konfigurieren Sie die Verbindung von diesem Schritt erneut.
			    3. Überprüfen Sie die Konfiguration mit dem Azurezugang nach folgender [Anleitung.](https://powerusers.microsoft.com/t5/Power-Automate-Community-Blog/How-to-use-OAuth2-0-in-Power-Automate-Custom-Connector/ba-p/1260216)
			    4. Öffnen Sie in Power Automate>>Data>>Custom Connectors den verwendeten Custom Connector. Führen Sie im Schritt 5. Testen die "Account Löschen" Methode mit dem Wert von einer beliebigen MicrosoftEmail von einem Profil in [[Azure]] aus. 