Studentenliste in [[Sharepoint]] erstellen
	1. Site erstellen
		1. Navigieren Sie zu Sharepoint. 
		2. Klicken Sie auf "+Create Site".
		3. Wählen Sie "Team Site".
			![[Sharepoint_Seite erstellen.png]]
		4. Belegen Sie den Namen und merken Sie sich diesen für die Konfiguration im Workflow.
	2. Liste erstellen
		1. Wählen Sie die soeben erstellte Site aus. 
			![[Sharepoint_Liste erstellen.png]]
		2. Klicken Sie auf "+New>>List".
			![[Sharepoint_Liste erstellen_2.png]]
		3. Wählan Sie "Blank List".
			![[Sharepoint_Liste importieren.png]]
		4. Geben Sie der Liste einen Namen.
			![[Sharepoint_Liste erstellen_3.png]]
		5. Klicken Sie auf "Create".
	3. Spalten erstellen
		Erstellen Sie folgende Spalten mit "New Column"
			![[Sharepoint Liste.png]]
			- Number: Matrikelnummer
			- Single Line of Text: Vorname
			- Single Line of Text: Nachname
			- Single Line of Text: Email
			- Single Line of Text: Microsoft-Email
			- Single Line of Text: Semester
			- Single Line of Text: Datenschutzerklärung
			- Yes/No: Nutzer angelegt
			- Yes/No: ausgelaufen
		*Achten Sie auf korrekte Zeichensetzung der Namen. Sollten Sie andere Namen vergeben wollen, so muss in [[Power Automate]] Schritt "Studentenliste sperren/löschen abfragen" das Feld "Filter Query" angepasst werden.*
	4. Einträge hinzufügen
		Der Workflow benötigt korrekte Werte aus diesen Spalten:
			- Email
			- Microsoft-Email
			- Semester
			- Nutzer angelegt
			- ausgelaufen
		Der Workflow benötigt korrekte Werte aus diesen Spalten **nicht**:
			- Matrikelnummer
			- Vorname
			- Nachname
			- Datenschutzerklärung
		1. Erstellen Sie Einträge zu allen/ausgewählten Accounts ihrer Microsoft Umgebung. 
			1. Öffnen Sie [[Azure]] und navigieren sie zu "Azure Active Directory>>Users". Entnehmen Sie von dort Microsoft-Email und Vor-/Nachname
			2. Erstellen Sie für die ausgewählten Accounts neue Zeilen in der Studentenliste mit den Daten aus Azure. 
			3. Ergänzen Sie in diesen Tupels folgende Daten:
				- Email: eine Email vom Studenten oder zu Testzewcken Ihre Email.
				- Semester: "SoSe"/"WS"+Jahr (zB "SoSe22"). In diesem Feld befindet ich das letzte Semester, in dem Sich zurückgemeldet wurde.
				- Nutzer angelegt: True
				- ausgelaufen: False (sollte der Account deaktiviert sein: True)
				- opt. Matrikelnummer, Datenschutzerklärung
			-> Stellen Sie sicher, dass die eingegebenen Daten [[Sharepoint Konsistenz|konsistent]] sind.
	