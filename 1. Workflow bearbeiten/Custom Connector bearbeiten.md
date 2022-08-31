Vorgehen:  
1. Öffnen Sie den Custom Connector über bearbeiten in "Power Automate>>Data>>Custom Connectors".  
2. In den folgenden Schritten sind alle Parameter aus der json-Datei enthalten, sodass Sie den Json-Code nicht direkt manipulieren müssen.

Hinweise:  
- Zum Einrichten der ersten 4 Schritte befindet sich [[Custom Connector einrichten|hier]] eine Anleitung.  
- Unter 1. Definition legen wir den Namen und die Web-API fest.  
- Unter 2. Security müssen Konfigurationen mit einem Sicherheitsverfahren durchgeführt werden. Da wir mit der Graph-API arbeiten sind wir hier auf das OAuth2.0 Sicherheitsverfahren angewiesen. Weitere Informationen zu notwendigen [[Azure Zugangsdaten]].  
- Unter 3. Definition sind die Methoden vom Custom Connector enthalten, die im Workflow aufgerufen werden können. Diese senden einen Http-Request, vergleichbar mit dem Http-Connector.  
- Unter 5. Test ist die Möglichkeit Methoden vom [[Custom Connector testen|Custom Connector zu testen]] enthalten.  
- Unter "Swagger Editor" kann der Json-Code eingesehen werden.