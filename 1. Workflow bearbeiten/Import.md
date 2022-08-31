Vorgehen 
	*Stellen Sie Sicher, dass Sie die Dateien aus dem Schritt [[Export]] vollständig erhalten haben. Sie benötigen die Exportdatei vom Workflow und Custom Connector.*
	1.  Connectoren erstellen 
		1. Öffnen Sie [[Power Automate]] und navigieren Sie zu "Data>>Connections".
		2. Erstellen Sie Connectorions für:
			- Azure AD
			- Sharepoint
			- Office 356 Users
			- Office 365 Outlook
	2. Teams Connector importieren 
		[[Custom Connector einrichten]]
	3. Workflow [[Import Workflow|importieren]] 
	4. [[Sharepoint]] Liste erstellen
	5. [[Azure]] konfigurieren
		1. Geben Sie dem Custom Connector einen Zugang zu ihrer Umgebung und zugehörigen [[Berechtigung Custom Connector|Berechtigungen]].
	6. Workflow speichern 
		1. Navigieren Sie in der Flow Oberfläche zu Flowchecker. Dieser zeigt Fehler im Workflow an.
		2. Belegen Sie Schritte mit den Connectoren, die diese erfordern.
		3. Bestimmen Sie die Email im Schritt "Fehler senden an" auf eine Ihrer Emails.
		4. Ändern Sie in den Schritten "Studentenliste sperren/löschen abfragen", sowie "Sharepoint Profil deaktiviert/Nutzer angelegt setzen" "Site Adress" und "List Name" auf die Studentenliste in Sharepoint.
		5. Sollten weitere Fehler im Flowchecker angezeigt werden, beheben Sie diese.
		6. Sollte der Workflow getestet werden, beachten Sie folgende [[Workflow testen|Anweisung]].
		7. Speichern Sie abschließend den Workflow.
	7. Workflow aktivieren 
		1. Navigieren Sie zu "My Flows >> (aktueller) Flow". Klicken Sie auf die 3 Punkte und "Turn On".  Ihr Workflow 
	8. Workflow testen