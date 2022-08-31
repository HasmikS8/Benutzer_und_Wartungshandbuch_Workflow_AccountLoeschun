Diese Thematik widmet sich dem Workflow-Schritt Account löschen. 
Dabei muss ein HTTP-DELETE-Request an eine WEB-API gesendet werden, die Microsoft accounts löschen kann. 

Hierbei bietet sich die Graph API an:
Parameter|Wert
----------|------
Web API|https://graph.microsoft.com
Version|v1.0
Protokoll|HTTP
Request Typ|DELETE
URI|https://graph.microsoft.com/v1.0/user/{id| Email}
Übergabeparameter|Microsoft ID oder Email
Sicherheitssystem|OAuth 2.0

In der [[Entwicklung]] ist dieser Schritt von dem [[Custom Connector Rolle|Custom Connector]] übernommen worden, der aber vor dem [[Update 1]] fehlschlug.

Es boten sich 3 Strategien an dieses Problem zu umgehen:
1. Methode [[Custom Connector bearbeiten]]
	Dieser Option stellt sich als vergleichsweise kompliziert und sehr verbuggt bzw. fehlerbehaftet heraus.
	
2. Methode [[HTTP-Schritt]]
	Diese Methode ist funktionsfähig. Im Gegensatz zum Custom Connector ist diese Methode wesentlich einfacher einzurichten und zu warten. Das Problem hierbei besteht jedoch in einer kostenpflichtigen Variante. Dieser Schritt führt den HTTP Request aus, den bisher der Custom Connector ausgeführt hat. Es wird ein DELETE Request zur Accountlöschung an die Web-API von Graph gesendet.
	
3. Methode [[Manuelle bzw. teilautomatisierte Lösung]] 
	Um weiterhin eine kostenfreie Möglichkeit umzusetzen, bietet sich eine manuelle Löschung nach automatisierter Vorbereitung. Der Workflow soll ausgelaufene Studentenprofile in der Sharepointliste markieren. Zudem besteht die Möglichkeit die http delete befehle auszugeben und manuell an Graph zu übergeben. Dazu führt der Workflow den Account löschen Schritt nicht aus, sodass die Profile zwar nicht gelöscht werden, aber trotzdem die Sharepointliste aktualisiert wird und in der Spalte ausgelaufen gesetzte Profile in Azure manuell gesperrt bzw. I n der Spalte Nutzer angelegt nicht belegte Profile gelöscht werden können. Weiterhin kann in einer E-Mail an den Verantwortlichen eine Liste von HTTP-Request Befehlen übergeben werden, die in der Graph Umgebung ausgeführt werden können.