# Stundenprotokoll

[Mittwoch, 04. Dezember 2019](#1)

[Donnerstag, 05. Dezember 2019](#2)

[Dienstag, 10. Dezember 2019](#3)

[Mittwoch, 11. Dezember 2019](#4)

[Donnerstag, 12. Dezember 2019](#5)

[Dienstag, 17. Dezember 2019](#6)

[Mittwoch, 18. Dezember 2019](#7)

[Donnerstag, 19. Dezember 2019](#8)


### <a name="1"></a>Mittwoch, 04. Dezember 2019

Heute haben wir darüber nachgedacht, was wir als nächstes Projekt machen könnten. Wir hätten beide Lust, weiter mit Arduino zu arbeiten, da uns das letzte Projekt sehr viel Spaß gemacht hat und wir uns damit jetzt schon ein bisschen auskennen. Also haben wir nachgedacht und hatten mehrere Ideen. Am Ende der Stunde erschien uns eine autonome Teebeutel-Maschine vielversprechend. 


### <a name="2"></a>Donnerstag, 05. Dezember 2019

Heute  haben wir uns mit einem weiteren Bestandteil von Arduino auseinandergestzt: Den Tastern. Nach kurzem recherchieren wollten wir den Umgang praktisch üben und haben so LEDs an- und ausgeschaltet. Zuerst haben wir uns einen simplen Sketch kopiert um eine LED durch Knopfdruck anzumachen. Nach kurzer Zeit ging sie dann wieder aus. 

https://funduino.de/nr-5-taster-am-arduino

Dann wollten wir eine LED mit einem Knopf an- und mit einem anderen ausschalten. Hierzu haben wir underen ersten Sketch eigenständig angepasst. Das hat dann auch funktioniert.


![Taster LED an und aus](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LED_Taster_AN_AUS.PNG?raw=true)

![Taster_LED_Foto](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Foto_Arduino_LED_Taster_1.jpg?raw=true)


### <a name="3"></a>Dienstag, 10. Dezember 2019

Heute haben wir uns mit Motoren beschäftigt. Wir haben zuerst im Internet recherchiert, aber keine für uns sinnvollen Erklärungen gefunden, sodass wir uns selbst überlegt haben, wie wir den Motor betreiben könnten. Also haben wir einen kleinen Sketch geschrieben, in dem wir den Motor als OUTPUT definiert haben, damit der Motor das Signal zum drehen bekommt. 

![Sketch Motor](https://github.com/dennis602/Stundenprotokoll-II/blob/master/code_motor%201.PNG?raw=true)

Das hat auch funktioniert, allerdings drehte der Motor nur sehr schwach. Also haben die Hardware so verändert, dass noch ein weiteres Kabel vom 5V Anschluss des Mikrocontrollers den Motor mit Strom versorgt. Damit konnte sich der Motor sehr gut drehen. 

Als nächstes wollten wir den Motor steuern, indem er immer dreht, dann stoppt, dann wieder dreht usw. Das hat leider noch nicht geklappt.


### <a name="4"></a>Mittwoch, 11. Dezember 2019

Heute haben wir uns damit auseinander gesetzt, warum die Motorsteuerung nicht so funktoniert hat, wie wir es uns gewünscht hatten. Wir kamen darauf, dass sobald der Motor an die 5V angeschlossen immer Strom bekommt, unabhängig vom Sketch. Also haben wir versucht, den Strom über das Breadboard so zu schalten, dass die 5V den digitalen Pin nur unterstützt. Wir haben allerdings sehr schnell festgestellt, dass das nicht möglich ist. Also haben wir Herrn Buhl gefragt und haben erfahren, dass man zur Motorsteuerung ein sogenanntes Motor Shield nutzen muss. Damit werden wir uns morgen auseinandersetzen.

https://www.aeq-web.com/arduino-motor-shield-dc-motor-control/?ref=yt


### <a name="5"></a>Donnerstag, 12. Dezember 2019

Wie geplant haben wir uns heute mit dem Motor Shield auseinandergesetzt. Zuerst haben wir dafüt im Internet recherchiert. Zum einen wi man den Sketch aufbauen muss und zum anderen wie man die Hardware aufbauen muss. Für die Hardware haben wir den Motor über Anschlüsse an das Motor Shield angeschlosse. Dieses wiederum haben wir dann auf den Mikrocontroller gesteckt, sodass die 5V und jeder Pin; den wir wollten, angesteuert werdenn konnten. Für den Sketch haben wir eine vielversprechende Vorlage kopiert und diese dann an unsere Anforderungen angepasst. Leider hat das nicht funktioniert, aus einem uns unbekannten Grund konnte der Sketch nicht auf den Mikrocontroller übertragen werden. Mit der Lösung dieses Problems wollen wir uns in den kommenden Stunden bschäftigen.


### <a name="6"></a>Dienstag, 17. Dezember 2019

Heute ist der Informatikunterricht ausgefallen.


### <a name="7"></a>Mittwoch, 18. Dezember 2019

Heute haben wir uns weiterhin mit der Ansteuerung eines Motors mit externer Stromquelle beschäftigt. Zuerst probierten wir es mit einer "Anleitung" von einem älteren Informatikprojekt ohne Motorshield, sondern mit Transistor.

https://stormarnschule12.github.io/Arduino-car/

Das funktionierte aber nicht, also probierten wir den Sketch mit Motorshield, doch das gleiche Problem lag vor, und zwar, dass die Arduino-Software den Sketch nicht verarbeiten konnte, da die Bibliothek <AF_Motor.h> nicht akzeptiert wurde. Also suchten wir im Internet nach weiteren Anleitungen und fanden folgende:

https://www.arduino.cc/en/Tutorial/TransistorMotorControl

Für diese haben wir dann alle Teile herausgesucht und morgen werden wir versuchen, diese umzusetzen.


### <a name="8"></a>Donnerstag, 19. Dezember 2019

Heute haben wir die Anleitung von gestern umgesetzt, also alles aufgebaut und den Sketch auf den Mikrocontroller übertragen. 

![Sketch](https://github.com/dennis602/Stundenprotokoll-II/blob/master/code%20transistor%20kopiert.PNG?raw=true)

![Schaltplan](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Schaltplan_Transistor.PNG?raw=true)

Als Stromquelle nutzten wir eine an die Steckdose angeschlossene Stromquelle, an der wir die Spannung einstellen konnten. Die Umsetzung funktionierte. Der Motor drehte sich nach Betätigung des Tasters.
Allerdings konnten wir die Geschwindigkeit des Motors immer noch mit der Spannung der Stromquelle bestimmen. Das ist jedoch wahrscheinlich normal, schließlich ist im Schaltplan ja auch eine Batterie verwendet.
