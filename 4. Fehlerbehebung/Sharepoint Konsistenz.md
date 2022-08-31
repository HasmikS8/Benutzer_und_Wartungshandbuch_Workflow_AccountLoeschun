Konsistenz überprüfen
	1. Öffnen Sie [[SharePoint]] und navigieren Sie zu über Site zu der Studentenliste.
	2. Überprüfen Sie die Spaltentypen und die Namen der Spalten. Gleichen Sie diese mit den Namen in dem [[Power Automate]] Flow Schritt "Studentenliste sperren/löschen abfragen" Feld "Filter Query" ab. 
		- Number: Matrikelnummer
		- Single Line of Text: Vorname
		- Single Line of Text: Nachname
		- Single Line of Text: Email
		- Single Line of Text: Microsoft-Email
		- Single Line of Text: Semester
		- Single Line of Text: Datenschutzerklärung
		- Yes/No: Nutzer angelegt
		- Yes/No: ausgelaufen
	3. Überprüfen Sie die Existenz von Tupels:
		*Öffnen Sie [[Azure]] "Active Directory>>Users" und überprüfen Sie die Existenz aller Profile in der Sharepointliste, sowie die Anzahl der Tupels. zu jedem Eintrag in der Azure Liste soll genau ein Eintrag in der Sharepointliste enthalten sein. Sharepointeinträge, die nicht in der Azure zuzuordnen sind, sind zu entfernen.*
	4. Überprüfen Sie die Werte in den Tupels:
		Für den flow unrelevante Spalten:
			- Matrikelnummer: entspricht der Matrikelnummer 
			- Vorname: entspricht dem Vornamen vom Studenten.
			- Nachname: entspricht dem Nachnamen vom Studenten.
			- Datenschutzerklärung
		Für den Flow relevante Spalten:
			- Email: entspricht einer Email vom Studenten bzw zu Testzwecken einer eigenen Email.
			- Microsoft-Email: entspricht der Microsoftemail vom Studentenaccount. Diese kann in Azure "Active Directory>>Users" abgeglichen werden.
			- Semester: entspricht dem Semester, in dem die Datenschutzerklärung das letzte Mal aktualisiert wurde. Der Wert setzt sich aus "SoSe"/"WS" und den letzten 2 Ziffern aus der Jahreszahl zusammen. (zB "SoSe22")
			- Nutzer angelegt: entspricht nein (ja), wenn sich der Benutzer (nicht) in Azure "Azure Active Directory>>Users>>deleted Users" befindet
			- ausgelaufen: entspricht ja (nein), wenn das Profil (nicht) gesperrt ist 
	5. Werden die Daten im Power Automate Flow konsistent aus den Abfragen verwendet?
		*Die Namen der Sharepoint Dynamic Contents sollten den Spaltennamen der Sharepointliste entsprechen.*

