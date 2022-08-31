![[Übersicht Workflow Tätigkeit.png]]

Der Workflow löst Ende jeden Semesters aus und setzt sich hierbei die Aufgabe ausgelaufene Studentenprofile zu sperren bzw. Zu löschen. 

In den Vorbereitungsschritten wird dabei die aktuelle Zeit und die Email, an die Fehlermeldungen gesendet werden sollen, abgefragt. Daraufhin werden die Parameter letzes und vorletztes Semester ermittelt. 

Die Spalte Semester in der Sharepointliste wird mit den Werten letzets und vorletztes Semester abgeglichen und übereinstimmende Accounts gelöscht bzw. gesperrt und in sharepoint der Wert der Spalte "Nutze angelegt" auf "False" bzw Nutzer "ausgelaufen" auf "True" gesetzt. 

Der Student erhält bei Sperrung bzw Löschung eine Benachrichtigung per Email.  

Sollte der Workflow mit dem falschen Monatswert gestartet werden oder die löschen/sperren Schritte fehlschlagen, erhält der Zuständige eine Email.