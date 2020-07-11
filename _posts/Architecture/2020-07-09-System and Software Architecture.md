# Cost Analyser Application -- System and Software Architecture




**Entwickeln Sie ein einfaches Architekturmodell für Ihren UseCase!**

![Architekturmodell](./image/Architektur_Modell.png)


**Welche Architektur würden Sie wählen, warum?**

Wir haben uns für die Microservice Architecture entschieden. Wir glauben, dass diese Architektur ihren Zweck bei unserer Anwendung gut erfüllen kann und ist darüber hinaus sehr übersichtlich. Wie man es der oberen Abbildung entnehmen kann ist unser Architektur sehr einfach, wir wollen mit unserer Anwendung im Prinzip zwei Services dem Kunden anbieten, einmal ist es die Möglichkeit seine Geldbewegungen von verschiedenen Banken in einem Ort strukturiert zu speichern und darüber hinaus wollen wir ihr/ihm anbieten diese Daten auf einer einfache und effektive Art auszuwerten (Uploading Services +Anlaytical Services). Wir glauben, dass für diese Ziele die dargestellte Microservice Architektur gut geeignet ist.

**Welche Art von Schnittstellen wären notwendig? Welche denkbar? Welche möglich?**

Für unseren Projekt haben wir uns entschieden für die REST API Schnitstelle. Alternativ könnte man SOAP und WDL wählen. Die Nutzung von Rest-API bietet die Möglichkeit eine sehr hohe Skalierbarkeit zu erreichen, da Client und Server voneinander entfernt sind.  Ein weitere Vorteil von Rest-API besteht darin, dass man es einfacher in vorhandener Website integrieren kann ohne die Webseite-Infrastruktur zu verändern.  


**Wie können Sie „Messaging" nutzen?**

Man könnte zum Beispiel das asynchrone Messaging nutzen, bei den Analytischen Anwendungen und zwar so, dass der Kunde nue Analyse anfordert, die es benötigt ein komplexeres Modell zu trainieren und die Anfrage wird zuerst in „Que“ gespeichert und zu einem günstigen Zeitpunkt umgesetzt. 


**Welche Informationen können Sie aus „Log"-Dateien extrahieren?**

In unserem Anwendungsbeispiel würden wir gerne die Zeitstempeln von den Uploads, den Banknamen, den Usernamen extrahieren. Darüber hinaus sollen jeglicher Art von Fehler die während der Benutzung der App aufgetreten sind protokoliert werden. Des weiteren sollen die TimeStamps protokolliert werden wann der Kunde eine Anfrage anfragte und wann er die Antwort erhalten hat. Wir würden auch gerne die Zeit, die der Kunde jedes Mail in der App verweilt aus den „Log“-Dateien ablesen und wie oft er die App benutzt. 


**Wie könnten Sie über „Internationalisierung stolpern" --(nicht nur Kunden aus diversen Ländern)?**

Wir gehen davon aus, dass wir nicht über die Internationalisierung stolpern werden , da unsere Requirements präzise definiert sind.
Theoretisch könnte man sich folgende Probleme vorstellen (Wir gehen zuerst davon aus, dass unsere App nur in dem deutschsprachigen Raum und in GB + USA zur Verfügung stehen wird);
Folgende Issues können zu Problemen führen:
	- verschiedene rechtliche Anforderungen in den jeweiligen Ländern;
	- verschiedene Währungen;
	-  verschiedene Zeitzonen; 
	- Metrische Systeme sind unterschiedlich- Formatierung!;
	- verschiedene Buchstaben, Umlaute;
