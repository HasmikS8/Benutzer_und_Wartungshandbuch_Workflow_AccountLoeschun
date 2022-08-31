Vorgehen:
	1. Öffnen Sie den Custom Connector über bearbeiten in "Power Automate>>Data>>Custom Connectors".
	2. Navigieren Sie zu "5. Testen"
	3. Vergewissern Sie sich, dass eine Connection erstellt wurde.
	5. Navigieren Sie zu der zu testenden Methode.
	6. Übergeben Sie die abgefragten Parameter
	7. Testen Sie die Methode und überprüfen Sie die Ergebnisse

Zum Bsp. Account Löschen
	 - In das Feld {id | userPrincipalName} übergeben Sie eine Microsoft-Email von einem Account, den Sie in "[[Azure]]>>Azure Active Directory>>Users" oder in der Studentenliste in [[Sharepoint]] finden.
	 - Der übergebene Account sollte nach erfolgreichem Ausführen vom Test in Azure unter "Azure Active Directory>>Users>>deleted Users" zu finden sein.

Testen von Methoden in Graph
	 - Im [graph-explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) können Http-Methoden der Graph-API getestet werden.


Bei Interesse können Sie den [[Custom Connector bearbeiten]]