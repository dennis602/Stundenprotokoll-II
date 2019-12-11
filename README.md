# Stundenprotokoll

[Mittwoch, 04. Dezember 2019](#1)

[Donnerstag, 05. Dezember 2019](#2)

[Dienstag, 10. Dezember 2019](#3)

[Mittwoch, 11. Dezember 2019](#4)


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

