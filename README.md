# Stundenprotokoll

[Mittwoch, 04. Dezember 2019](#1)

[Donnerstag, 05. Dezember 2019](#2)

[Dienstag, 10. Dezember 2019](#3)

[Mittwoch, 11. Dezember 2019](#4)

[Donnerstag, 12. Dezember 2019](#5)

[Dienstag, 17. Dezember 2019](#6)

[Mittwoch, 18. Dezember 2019](#7)

[Donnerstag, 19. Dezember 2019](#8)

[Donnerstag, 09. Januar 2020](#9)

[Mittwoch, 15. Januar 2020](#10)

[Donnerstag, 16. Januar 2020](#11)

[Dienstag, 21. Januar 2020](#12)

[Mittwoch, 22. Januar 2020](#13)

[Donnerstag, 23. Januar 2020](#14)

[Dienstag, 28. Januar 2020](#15)

[Donnerstag, 30. Januar 2020](#16) 


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


Den Sketch haben wir so verstanden, dass x in irgendwie die Geschwindigkeit bestimmt, mit der der Motor dreht. Also beginnt der Motor nach drücken des Knopfes durch x++ zu beschleunigen, bis er die Geschwindigkeit 255 erreicht. Anschließend wird er durch x-- wieder langsamer, bis er zum Stillstand kommt. 



![Schaltplan](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Schaltplan_Transistor.PNG?raw=true)

Als Stromquelle nutzten wir eine an die Steckdose angeschlossene Stromquelle, an der wir die Spannung einstellen konnten. Die Umsetzung funktionierte. Der Motor drehte sich nach Betätigung des Tasters.
Allerdings konnten wir die Geschwindigkeit des Motors immer noch mit der Spannung der Stromquelle bestimmen. Das ist jedoch wahrscheinlich normal, schließlich ist im Schaltplan ja auch eine Batterie, also eine konstante Spannung, verwendet.

### <a name="9"></a>Donnerstag, 09. Januar 2020

Die erste Woche des neuen Jahres ist der Unterricht ausgefallen, weshalb wir uns zu Hause über die weitere Vorgehensweise Gedanken gemacht haben. Wir möchten uns nun mit dem sogenannten Potentiometer (eine Art Drehregler) auseinandersetzten, um einen Servo und anschließend eventuell auch den Motor damit steuern zu können. Bei dem Potentiometer handelt es sich um einen drehbaren Widerstand. Mithilfe einer Variable im Sketch kann die Drehbewegung in einen Wert umgerechnet werden, welcher dann zum Beispiel einem Winkel entspricht, den sich ein Servo bewegen soll. 

https://www.youtube.com/watch?v=aAxbp507B9I

Dieses Video bietet dazu eine gute Grundlage.

Zudem möchten wir den Motor nochmal mithilfe des Transistors ganz einfach ansteuern, indem wir ihn (ohne Taster) einfach als Output bezeichnen und durch ganz schnelles an- und ausschalten die Geschwindigkeit regulieren. Der Transistor soll es ermöglichen, diesen einfachen Sketch zu verwenden und die Stromversorgung trotzdem extern zu gewährleisten.



### <a name="10"></a>Mittwoch, 15. Januar 2020

Heute wollten wir mit einem Potentiometer einen Servo ansteuern. Leider hatten wir nicht die nötige Hardware zur Hand, also mussten wir improvisieren. Das Ergebnis war ein sehr altes und sehr großes Potentiometer, mit dem wir es dann versucht haben. 

![Sketch Potentiometer](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Unbenannt.PNG?raw=true)

Die Idee dahinter ist folgende: Man führt durch "int val" eine Variable ein, auf welcher der Wert des Potentiometers gespeichert wird. Dieser kann an einem analogen Pin des Mikrocontrollers ausgelesen werden. Mithilfe der "map" Funktion kann man diesen Wert (beim Potentiometer normalerweise 0 bis 1023) in einen Gradwinkel für den Servo (also 0 bis 180) umrechnen. Somit sollte sich der Winkel des Servos an den des Potentiometers anpassen. 

Dies hat einigermaßen funktioniert. Wir waren also theoretisch in der Lage den Drehwinkel vom Servo per Potentiometer zu steuern, leider gab es aber noch mehr Komplikationen. Der Mikrocontroller hat sich ständig vom Computer getrennt. Der Sketch lief ein paar Sekunden und dann war Stillstand. Dieses Problem wollen wir morgen beheben.


### <a name="11"></a>Donnerstag, 16. Januar 2020

Unser Erster Versuch um das Problem von gestern zu lösen war es, den Computer zu wechseln. Dann haben wir alles wieder neu aufgebut und angefangen auszuprobieren. Wir haben herausgefunden, dass sich der Mikrocontroller nur dann trennt, wenn man einen zu hohen Wiederstand auf dem Potentiometer einstellt. Der Servo wollte sich trotzdem nicht so richtig bewegen, wir würden es gerne nocheinmal mit einem modernen und handlichem Potentiometer probieren, dies ist aber leider momentan nicht möglih. Somit werden wir das Potentiometer ersteinmal sein lassen. Wir haben immerhin gelernt, wie man eine Variable mit der map Funktion verwendet :)

Also werden wir uns nächste Woche weiter mit dem Drehmotor beschäftigen. Unser Ziel ist es, ihn vorwärts und rückwärts laufen zu lassen, um eventuell doch am Ende noch den Teeautomaten als Endprojekt erreichen zu können.


### <a name="12"></a>Dienstag, 21. Januar 2020

Heute haben wir uns also wieder mit dem Motor beschäftigt. Zur einfachen Umsetzung, die es erlaubt, den Motor vorwärts und rückwärts drehen zu lassen, nutzen wir folgende Quelle:

https://starthardware.org/motorsteuerung-direkt-per-arduino/

Um den Arduino nicht zu überlasten, nahmen wir statt des 5V Anschlusses des Mikrocontrollers eine externe Stromquelle hinzu. 

![Motor](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Motor_Arduino.jpg?raw=true)

Unser Sketch sah folgendermaßen aus:

![Code Motor](https://github.com/dennis602/Stundenprotokoll-II/blob/master/code_motor_funktioniert.PNG?raw=true)

Das hat auch alles so funktioniert. Der Motor drehte erst vorwärts, stoppte und drehte anschließend rückwärts. Das Ganze ist dadurch möglich, dass wir an beide Pole des Motors einen OUTPUT angeschlossen haben und somit jeweils der andere Pol den Stromkreis wieder schließt. Der Motor wird also umgepolt. Nun können wir daran weiterarbeiten, den Motor individuell zu steuern.


### <a name="13"></a>Mittwoch, 22. Januar 2020


Heute haben wir einen Weg gesucht, wie man bestimmte Abläufe einfach gezielt oft ablaufen lassen kann, um das auch beim Motor durchführen zu können. Nach kurzer Recherche sind wir auf die While-Schleife gestoßen.

https://www.youtube.com/watch?v=QlDH2SApocM

Bei dieser setzt man eine Variable zu Anfang auf 0, um sie in einer While-Schleife nach jedem Durchgang des Ablaufs um 1 zu erhöhen. Vorher legt man fest, bis zu welchem Wert die Variable ansteigen darf. So haben wir den Sketch geschrieben und das ganze mit einer LED ausprobiert.

![While Schleife](https://github.com/dennis602/Stundenprotokoll-II/blob/master/While%20Schleife.PNG?raw=true)

Die LED geht also an, nach einer Sekunde wieder aus, die Variable erhöht sich um den Wert 1 und die Schleife beginnt von vorn. Das bedeutet, dass die LED fünf Mal blinkt und dann für 3 Sekunden aus bleibt. Dann beginnt das Ganze von vorne. Das hat auf Anhieb funktioniert. Als nächstes werden wir diese Funktion mit Motor und Taster verknüpfen.


### <a name="14"></a>Donnerstag, 23. Januar 2020

Heute haben wir unsere drei großen Bausteine miteinander verknüpft: Motor, Taster und While-Schleife mit Variable. Als Ausgangsbasis haben wir den Motor-Sketch genommen und in diesen den Taster-Sketch eingefügt. Dass der Motor sich einmal vor und danach zurück dreht, soll also nur noch passieren, wenn wir vorher auf den Taster gedrückt haben. Wird der Taster nicht gedrückt, passiert gar nichts. Als nächstes haben wir die While-Schleife eingebaut. Dieses Vor- und Zurückdrehen soll durch das Mitzählen und erhöhen der Variable auf drei Mal begrenzt werden. Danach ist Schluss und es muss erneut der Taster betätigt werden. Dies hat bei der praktischen Umsetzung sofort funktioniert.

![Motor Taster While 1](https://github.com/dennis602/Stundenprotokoll-II/blob/master/23.01.20_1.PNG?raw=true)


![Motor Taster While 2](https://github.com/dennis602/Stundenprotokoll-II/blob/master/23.01.20_2.PNG?raw=true)


### <a name="15"></a>Dienstag, 28. Januar 2020

Heute haben wir den letzten Sketch mit einer zweiten if-Bedingung erweitert. Dazu muss man beide if-Bedingungen in Klammern setzten und dazwischen " && " setzten. Die zweite if-Bedingung ist ein Ultrasschallsensor, der Entfernung misst (s. Stundenprotkoll letztes Halbjahr). Um diesen zu testen, verwendeten wir erst einen Serial Print, um uns dort die berechnete Entfernung anzeigen zu lassen. Das hat soweit auch funktioniert. Wir wollten bewirken, dass der Sketch nur dann abläuft, wenn der Ultraschallsensor eine geringe Entfernung misst, um später den Teebeutelautomaten nur zu starten, wenn auch wirklich eine Tasse dort steht. Der Taster hat also nur eine Wirkung, wenn eine geringe Entfernung gemessen wird. Wir haben wie letztes Jahr die Messung mit ins Void Loop etc. eingefügt und anschließend die zweite if-Bedingung geschrieben.

![Code mit Ultraschallsensor](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Code_motor_ultraschall%20(3).PNG?raw=true)

Das hat soweit auch funktoniert, allerdings nur das erste Mal nach dem Hochladen des Sketches. Dieses Problem werden wir nächstes Mal versuchen zu lösen.

![Foto](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Foto_Arduino_Motor_Ultraschall.jpg?raw=true)



### <a name="16"></a>Donnerstag, 30. Januar 2020

Gestern und heute ist der Informatikunterricht ausgefallen. Also hatten wir keinen Zugang zur Hardware, aber haben uns überlegt, wie wir nun weiter vorgehen werden. Wir werden noch einmal das Arduino Motorshield ausprobieren, um leistungsstärkere Motoren anzusteuern. Die entsprechende Bibliothek, die wir herunterladen müssen, haben wir schon gefunden. 
Außerdem haben wir geplant, wie wir die Idee mit dem Teebeutelautomaten im Bau umsetzten können.








https://funduino.de/nr-15-schrittmotor







