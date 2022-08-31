Vorgehen
	1. Öffnen Sie [[Azure]] "Active Directory>>Users".
	2. Öffnen Sie die Studentenliste in [[Sharepoint]] im "grid View".
	3. Zu jedem Tupel der Studentenliste, dessen Werte
		- Semester = dem letzten Semester
		- ausgelaufen = False
		sind:
		1. Setzen Sie "ausgelaufen" = True.
		2. Sperren Sie das Profil mit der selben MicrosoftEmail in Azure.
	4. Zu jedem Tupel der Studentenliste, dessen Werte
		- Semester = dem **vor**letzten Semester
		- ausgelaufen = True
		- Nutzer angelegt = True
		sind:
		1. Setzen Sie "Nutzer angelegt" = False.
		2. Löschen Sie das Profil mit der selben MicrosoftEmail in Azure.