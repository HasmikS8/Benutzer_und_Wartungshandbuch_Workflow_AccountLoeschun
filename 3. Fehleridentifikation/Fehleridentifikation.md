Fehler:
	I Einzelne Accounts wurden trotz Fälligkeit nicht gelöscht 
		1.  Ist der Account in der Sharepointliste-Spalte Semester min 2 Semester älter als das aktuellste Semester?     
		    - Ja: Löschen Sie den Account aus der Tabelle in [[Azure]] manuell. Und löschen Sie anschließend das Tupel aus der Sharepoint-Liste. 
		    - Nein: Überprüfen Sie den Workflow in Power Automate. Führen Sie einen Testlauf durch. 
	II Der Flow hat zum fälligen Zeitpunkt nicht ausgelöst
		1.  Ist der Workflow eingeschalten?
			-> "[[Power Automate]]>>My Flows" Flow öffnen, button turn on.
		2. Ist der Auslöseschritt falsch konzipiert?
			-> Öffnen Sie den Flow in Power Automate und überprüfen Sie den Schritt 0 Auslöser.
		3. Ist ein Fehler im Workflow?
			-> [[Workflow testen]], [[Fehlermeldung im Workflow]]
		4. Sind Daten in der Sharpointliste nicht konsistent?
			-> [[Sharepoint Konsistenz]]
	III Fehlermeldung im Workflow 
		-> [[Fehlermeldung im Workflow]]
	IV Email mit Fehlermeldung
		-> [[Email Fehlermeldung 1-3]]
	V Azure Userliste und/oder Sharepoint Studentenliste wurden nicht wie gewollt verändert:
		1. Ist die Studentenliste konsistent?
			-> [[Sharepoint Konsistenz]]	

 Sollte keiner dieser Punkte hilfreich sein, sollten Sie den Workflow testen und mit den Hinweisen weitersuchen. Sie können auch den Custom Connector testen und die Sharepointliste auf Konsistenz überprüfen.
	-> [[Workflow testen]]
	-> [[Custom Connector testen]]
	-> [[Sharepoint Konsistenz]]

Die Tätigkeit vom Flow kann manuell ausgeführt werden:
	-> [[Workflowtätigkeit manuell ausführen]]

Weiterhin besteht die Möglichkeit den Microsoft Support zu kontaktieren.  
-> [Support]([https://powerautomate.microsoft.com/en-us/support/](https://powerautomate.microsoft.com/en-us/support/ "https://powerautomate.microsoft.com/en-us/support/"))
