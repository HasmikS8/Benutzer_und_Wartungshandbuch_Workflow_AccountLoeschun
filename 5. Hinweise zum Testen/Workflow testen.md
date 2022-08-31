Bei Bedarf kann ein Adminestrator die [[Workflowtätigkeit manuell ausführen]].
Der Flow sollte einen [[Funktionsumfang]] haben.

Workflow testen
	1. Übertragen Sie den Workflow in eine [[Workflow in eine andere Umgebung übertragen|Developer Umgebung]].
	2. Setzen Sie in [[Power Automate]] Workflow im Schritt "Fehler senden an" ihre Email ein. 
	3. Notieren Sie sich die Werte aus Monat und setzen Sie den Wert vorübergehend auf "6" für das aktuelle Semester Sommersemester oder "12" für Wintersemester. 
	4. Suchen Sie sich Profile in Sharepoint/Azure aus, die gelöscht bzw gesperrt werden sollen. 
	5. Sperren, entsperren und/oder stellen Sie in [[Azure]] Profile wieder her. 
		-> Zu sperrende Profile müssen entsperrt werden. 
		-> Zu löschende Profile müssen wiederhergestellt werden. 
	6. Ändern Sie in [[Sharepoint]] Werte. 
		-> Ändern Sie die Spalte Email auf eine Ihrer Emails, wenn die Benachrichtigung über Löschung/Sperrung nur an Sie geleitet werden soll.
		-> Zu sperrende Profile müssen mit folgenden Werten belegt sein. 
			- Semester=letztesSemester (zB WS21 im Fall SoSe22) 
			- Nutzer angelegt=True  
			- ausgelaufen=False  
		-> Zu löschende Profile müssen mit folgenden Werten belegt sein.  
			- Semester=letztesSemester (zB SoSe21 im Fall SoSe22) 
			- Nutzer angelegt=True  
			- ausgelaufen=True 
	7. Ändern Sie die Werte in der Studentenliste-Spalte Email auf eine Ihrer Emails, wenn Sie eine Bestätigung der Sperrung/Löschung nur an Sie senden lassen wollen. 
	8. Überprüfen Sie nach aktualisieren der Sharepointseite, ob die Spalten ausgelaufen und Nutzer angelegt korrekt gesetzt wurden.
	9. Gleichen Sie in "Azure>>Azure Active Directory>>deleted Users" die Einträge mit Sharepoint Nutzer angelegt ab. 
	10. **Setzen Sie die Werte in Power Automate Monat und Email auf die Ausgangswerte zurück.**  
	11. **Ändern Sie ggf. die Spalte Email, ausgelaufen, Nutzer angelegt in Sharepoint.**  
	12. **Stellen Sie gelöschte Profile in Azure wieder her und entsperren Sie gesperrte Profile.**

