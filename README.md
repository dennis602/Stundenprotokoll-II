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

[Dienstag, 04. Februar 2020](#17)

[Mittwoch, 05. Februar 2020](#18)

[Donnerstag, 06. Februar 2020](#19)

[Mittwoch, 12. Februar 2020](#20)

[Donnerstag, 13. Februar 2020](#21)

[Freitag, 14. Februar 2020](#22)

[Mittwoch, 19. Februar 2020](#23)

[Donnerstag, 20. Februar 2020](#24)

[Mittwoch, 26. Februar 2020](#25)

[Donnerstag, 05. März 2020](#26)

[Freitag, 06. März 2020](#27)

[Mittwoch, 11. März 2020](#28)

[Freitag, 13. März 2020](#29)

[Donnerstag, 19. März 2020](#30)

[Freitag, 20. März 2020](#31)

[Mittwoch, 25. März 2020](#32)


### <a name="1"></a>Mittwoch, 04. Dezember 2019

Heute haben wir darüber nachgedacht, was wir als nächstes Projekt machen könnten. Wir hätten beide Lust, weiter mit Arduino zu arbeiten, da uns das letzte Projekt sehr viel Spaß gemacht hat und wir uns damit jetzt schon ein bisschen auskennen. Also haben wir überlegt und hatten mehrere Ideen. Am Ende der Stunde erschien uns eine autonome Teebeutel-Maschine vielversprechend, da man dort zum Beispiel mit Motoren arbeiten kann.


### <a name="2"></a>Donnerstag, 05. Dezember 2019

Heute  haben wir uns mit einem weiteren Bestandteil von Arduino auseinandergesetzt: Den Tastern. Nach kurzem recherchieren wollten wir den Umgang praktisch üben und haben so LEDs an- und ausgeschaltet. Zuerst haben wir uns einen simplen Sketch kopiert um eine LED durch Knopfdruck zum Leuchten zu bringen. Nach kurzer Zeit ging sie dann wieder aus. 

https://funduino.de/nr-5-taster-am-arduino

Dann wollten wir eine LED mit einem Knopf an- und mit einem anderen ausschalten. Hierzu haben wir unseren ersten Sketch eigenständig angepasst. Das hat dann auch funktioniert.


![Taster LED an und aus](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LED_Taster_AN_AUS.PNG?raw=true)

![Taster_LED_Foto](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Foto_Arduino_LED_Taster_1.jpg?raw=true)


### <a name="3"></a>Dienstag, 10. Dezember 2019

Heute haben wir uns mit Motoren beschäftigt. Wir haben zuerst im Internet recherchiert, aber keine für uns sinnvollen Erklärungen gefunden, sodass wir uns selbst überlegt haben, wie wir den Motor betreiben könnten. Also haben wir einen kleinen Sketch geschrieben, in dem wir den Motor als OUTPUT definiert haben, damit der Motor das Signal zum drehen bekommt. 

![Sketch Motor](https://github.com/dennis602/Stundenprotokoll-II/blob/master/code_motor%201.PNG?raw=true)

Das hat auch funktioniert, allerdings drehte der Motor nur sehr schwach. Also haben die Hardware so verändert, dass noch ein weiteres Kabel vom 5V Anschluss des Mikrocontrollers den Motor mit Strom versorgt. Damit konnte sich der Motor sehr gut drehen. 

Als nächstes wollten wir den Motor steuern, indem er immer dreht, dann stoppt, dann wieder dreht usw. Das hat leider noch nicht geklappt.


### <a name="4"></a>Mittwoch, 11. Dezember 2019

Heute haben wir uns damit auseinander gesetzt, warum die Motorsteuerung nicht so funktoniert hat, wie wir es uns gewünscht hatten. Uns wurde sehr schnell klar, dass der Motor, sobald er an die 5V angeschlossen ist, immer Strom bekommt, unabhängig vom Sketch. Also haben wir versucht, den Strom über das Breadboard so zu schalten, dass die 5V den digitalen Pin nur unterstützen. Wir haben allerdings sehr schnell festgestellt, dass dies nicht möglich ist. Also haben wir Herrn Buhl gefragt und haben erfahren, dass man zur Motorsteuerung ein sogenanntes Motor Shield nutzen muss. Damit werden wir uns morgen auseinandersetzen.

https://www.aeq-web.com/arduino-motor-shield-dc-motor-control/?ref=yt


### <a name="5"></a>Donnerstag, 12. Dezember 2019

Wie geplant haben wir uns heute mit dem Motor Shield auseinandergesetzt. Zuerst haben wir dafür im Internet recherchiert. Zum einen wie man den Sketch aufbauen muss und zum anderen wie man die Hardware aufbauen muss. Für die Hardware haben wir den Motor über Anschlüsse an das Motor Shield angeschlossen. Dieses wiederum haben wir dann auf den Mikrocontroller gesteckt, sodass die 5V und jeder Pin, den wir wollten, angesteuert werden konnten. Für den Sketch haben wir eine vielversprechende Vorlage kopiert und diese dann an unsere Anforderungen angepasst. Leider hat das nicht funktioniert, aus einem uns unbekannten Grund konnte der Sketch nicht auf den Mikrocontroller übertragen werden. Mit der Lösung dieses Problems wollen wir uns in den kommenden Stunden beschäftigen.


### <a name="6"></a>Dienstag, 17. Dezember 2019

Heute ist der Informatikunterricht ausgefallen.


### <a name="7"></a>Mittwoch, 18. Dezember 2019

Heute haben wir uns weiterhin mit der Ansteuerung eines Motors mit externer Stromquelle beschäftigt. Zuerst probierten wir es mit einer "Anleitung" von einem älteren Informatikprojekt ohne Motorshield, sondern mit Transistor.

https://stormarnschule12.github.io/Arduino-car/

Das funktionierte aber nicht, also probierten wir den Sketch mit Motorshield, doch das gleiche Problem lag vor und zwar, dass die Arduino-Software den Sketch nicht verarbeiten konnte, da die Bibliothek <AF_Motor.h> nicht akzeptiert wurde. Also suchten wir im Internet nach weiteren Anleitungen und fanden folgende:

https://www.arduino.cc/en/Tutorial/TransistorMotorControl

Für diese haben wir dann alle Teile herausgesucht und morgen werden wir versuchen, diese umzusetzen.


### <a name="8"></a>Donnerstag, 19. Dezember 2019

Heute haben wir die Anleitung von gestern umgesetzt, also alles aufgebaut und den Sketch auf den Mikrocontroller übertragen. 

![Sketch](https://github.com/dennis602/Stundenprotokoll-II/blob/master/code%20transistor%20kopiert.PNG?raw=true)


Den Sketch haben wir so verstanden, dass x irgendwie die Geschwindigkeit bestimmt, mit der der Motor dreht. Also beginnt der Motor nach drücken des Knopfes durch x++ zu beschleunigen, bis er die Geschwindigkeit 255 (Umdrehungen pro Minute) erreicht. Anschließend wird er durch x-- wieder langsamer, bis er zum Stillstand kommt. 



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

![Bild Potentiometer](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Bild%20Potentiometer.jpg?raw=true)

![Sketch Potentiometer](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Unbenannt.PNG?raw=true)

Die Idee dahinter ist folgende: Man führt durch "int val" eine Variable ein, auf welcher der Wert des Potentiometers gespeichert wird. Dieser kann an einem analogen Pin des Mikrocontrollers ausgelesen werden. Mithilfe der "map" Funktion kann man diesen Wert (beim Potentiometer normalerweise 0 bis 1023) in einen Gradwinkel für den Servo (also 0 bis 180) umrechnen. Somit sollte sich der Winkel des Servos an den des Potentiometers anpassen. 

Dies hat einigermaßen funktioniert. Wir waren also theoretisch in der Lage den Drehwinkel vom Servo per Potentiometer zu steuern, leider gab es aber noch mehr Komplikationen. Der Mikrocontroller hat sich ständig vom Computer getrennt. Der Sketch lief ein paar Sekunden und dann war Stillstand. Dieses Problem wollen wir morgen beheben.


### <a name="11"></a>Donnerstag, 16. Januar 2020

Unser Erster Versuch um das Problem von gestern zu lösen war es, den Computer zu wechseln. Dann haben wir alles wieder neu aufgebaut und angefangen auszuprobieren. Wir haben herausgefunden, dass sich der Mikrocontroller nur dann trennt, wenn man einen zu hohen Wiederstand auf dem Potentiometer einstellt. Der Servo wollte sich trotzdem nicht so richtig bewegen, wir würden es gerne nocheinmal mit einem modernen und handlichem Potentiometer probieren, dies ist aber leider momentan nicht möglich. Somit werden wir das Potentiometer ersteinmal sein lassen. Wir haben immerhin gelernt, wie man eine Variable mit der map Funktion verwendet.

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

Heute haben wir den letzten Sketch mit einer zweiten if-Bedingung erweitert. Dazu muss man beide if-Bedingungen in Klammern setzten und dazwischen " && " setzten. Die zweite if-Bedingung ist ein Ultrasschallsensor, der Entfernung misst (s. Projektseite letztes Halbjahr (https://github.com/dennis602/Projektseite-Arduino-Parkhaus/blob/master/README.md#6)). Um diesen zu testen, verwendeten wir erst einen Serial Print, um uns dort die berechnete Entfernung anzeigen zu lassen. Das hat soweit auch funktioniert. Wir wollten bewirken, dass der Sketch nur dann abläuft, wenn der Ultraschallsensor eine geringe Entfernung misst, um später den Teebeutelautomaten nur zu starten, wenn auch wirklich eine Tasse dort steht. Der Taster hat also nur eine Wirkung, wenn eine geringe Entfernung gemessen wird. Wir haben wie letztes Jahr die Messung mit ins Void Loop etc. eingefügt und anschließend die zweite if-Bedingung geschrieben.

![Code mit Ultraschallsensor](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Code_motor_ultraschall%20(3).PNG?raw=true)

Das hat soweit auch funktoniert, allerdings nur das erste Mal nach dem Hochladen des Sketches. Dieses Problem werden wir nächstes Mal versuchen zu lösen.

![Foto](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Foto_Arduino_Motor_Ultraschall.jpg?raw=true)



### <a name="16"></a>Donnerstag, 30. Januar 2020

Gestern und heute ist der Informatikunterricht ausgefallen. Also hatten wir keinen Zugang zur Hardware, aber haben uns überlegt, wie wir nun weiter vorgehen werden. Wir werden noch einmal das Arduino Motorshield ausprobieren, um leistungsstärkere Motoren anzusteuern. Die entsprechende Bibliothek, die wir herunterladen müssen, haben wir schon gefunden. 
Außerdem haben wir geplant, wie wir die Idee mit dem Teebeutelautomaten im Bau umsetzten können.



### <a name="17"></a>Dienstag, 04. Februar 2020

Heute haben wir uns noch einmal mit dem Arduino Motor-Shield beschäftigt. Dazu mussten wir zuerst die dazugehörige Arduino-Bibliothek herunterladen und in das Programm einfügen. Dies lief ohne Probleme sehr schnell ab. Somit akzeptiert das Arduinoprogramm die Motorbibliothek <AFMotor.h>.

![<AFMotor.h>](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Code_motorshield_1.PNG?raw=true)

Dann haben wir uns ein Motor-Shield gesucht, einen Stepper-Motor angeschlossen und einen Sketch zur Probe aus dem Internet kopiert. Das Besondere an einem Stepper-Motor ist, dass man diesen sehr genau anhand der Schritte Steuern kann. 2048 Schritte sind gleichgesetzt mit 360 Grad, also einer Umdrehung. Dies ermöglicht also sehr präzises Arbeiten. Nachdem wir ein anderes Motor-Shield verwendet haben (Blau statt Grün) hat auch alles funktioniert und wir konnten den Motor sehr präzise mit einem relativ simplen Sketch steuern.


https://funduino.de/nr-15-schrittmotor



### <a name="18"></a>Mittwoch, 05. Februar 2020

Heute haben wir uns weiter mit dem Motorshield auseinandergesetzt. Unser Problem war, dass das Motorshield alle Ports besetzt und wir keines gefunden haben, welches die nicht vom Shield benötigten Ports nach oben durchleitet. Also entschlossen wir uns, die benötigten Ports per Kabel mit dem Motorshield zu verbinden. Nach kurzer Recherche und ausprobieren gelang es uns, die nötigen Ports zu finden.

![Verkabelung_Motorshield](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Motorshield_verkabelt.jpg?raw=true)

Anschließend haben wir begonnen, den bisherigen Sketch des Teebeutelautomatens in den des Motorshields zu übertragen.

Wir haben auch herausgefunden, dass man den Steppermotor mit dem kleinen beiligenden Shield verwenden kann. Doch wir finden die Steuerung per Motorshield sehr schön. Nur falls uns die Kabel stören, werden wir auf das kleine Shield umsteigen.


### <a name="19"></a>Donnerstag, 06. Februar 2020

Heute haben wir die Sketche in einen verbunden. Den für den normalen Motor mit Ultraschallsensor und Taster mit dem für das Motor-Shield mit dem Stepper-Motor. Wir haben den Stepper-Sketch als Grundlage genommen und den anderen dort hinein gebaut, auch um uns nocheinmal mit allen Elementen vertraut zu machen. Zwangsläufig sind somit alle Motor-Elemente des alten Sketches verschwunden, da wir diesen durch den Stepper ersetzt haben. Dann haben wir die Hardware zusammen gebaut. Einfach alle Ports des Microcontrollers zugewiesen und alle mehrfach belegten (z.B. 5V) auf das Breadboard gelegt. Die Funktionalität war leider noch nicht vollständig gegeben, der Taster wurde aus uns aktuell unbekannten Gründen nicht akzepiert. Der Rest allerdings hat einwandfrei funktioniert.

![Stepperino](https://github.com/dennis602/Stundenprotokoll-II/blob/master/stepperino.jpg)


### <a name="20"></a>Mittwoch, 12. Februar 2020

Dem Problem von letzter Stunde sind wir heute auf den Grund gegangen. Wir haben verschiedene Serial Prints und nur einzelne if-Bedingungen genutzt, um die Funktionalität der einzelnen Komponenten zu prüfen. Dabei ist uns aufgefallen, dass der Sketch jeweils ein Mal funktioniert und dann nicht mehr. Nach kurzem Überlegen kamen wir darauf, dass die Variable "i" nicht im Setup, sondern im Loop gleich 0 gesetzt werden muss, damit der Ablauf jedes Mal neu beginnt. Nachdem wir das umgesetzt haben, funktionierte alles wie gewünscht. 

![Code 12.02.2020](https://github.com/dennis602/Stundenprotokoll-II/blob/master/code_teebeutelautomat_1.PNG?raw=true)

Außerdem nutzten wir als externe Stromquelle eine an die Steckdose angeschlossene Spannungsquelle, da der Motor bei der Batterie teilweise Anlaufschwierigkeiten hatte. Das Problem haben wir aber somit in den Griff gekriegt. 

![Aufbau 12.02.2020](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Motor%20mit%20Spannungsquelle%2012.02.2020.jpg)



### <a name="21"></a>Donnerstag, 13. Februar 2020

Heute haben wir uns überlegt, wie wir weiter vorgehen wollen. Die Idee war es, nach den wiederholten Drehungen des Motors ein akustisches Signal zu senden. Hierzu benutzen wir einen Summer. 

![Bild Pieper](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Pieper.jpg?raw=true)

Wir haben einen Aufbau mit einem Transistor probiert, doch das hat noch nicht funktioniert.

https://i.ytimg.com/vi/jvlTKi9nMO0/maxresdefault.jpg

### <a name="22"></a>Freitag, 14. Februar 2020

Heute haben wir uns weiter um den Pieper gekümmert. Da der Aufbau von gestern nicht funktioniert hat, haben wir weitere Änderungen vorgenommen. Komischerweise hat der Port des Piepers dauerhaft Strom gegeben. Also haben wir einen anderen Port genommen. Außerdem haben wir im Sketch eine if Bedingung hinzugefügt. Nämlich if (i = Zahl der While Schleife). Somit piept der Pieper, wenn die While Schleife durch ist, also sozusagen wenn der Tee fertig ist. Das Ganze hat auch funktioniert.

![Code 14.02.2020](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Pieper_Code.PNG?raw=true)

Jetzt sind allerdings alle Ports verbraucht. Da wir aber noch mehr Taster nutzen möchten, haben wir uns ein Arduino Mega Bord genommen und alle Kabel umgesteckt.

![Aufbau_14.02.2020](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Arduino%20Mega%20und%20Pieper.jpg?raw=true)


### <a name="23"></a>Mittwoch, 19. Februar 2020

Wir haben jetzt einen Sketch, mit dem wir auf Knopfdruck einen bestimmten Motorablauf auslösen können. Beliebig oft drehen und dann ein Piepen. Jetzt wollen wir mehrere Taster mit verschedenen Motor-Modi einbauen. Für die Hardware haben wir einfach ein großes Breadboard genommen und drei Taster angeschlossen. Im Sketch war es ein bisschen komplizierter. Zuerst haben wir die verschiedene Taster benannt und auf drei Digitale Pins des Microcontrollers festgelegt. Dann mussten wir den Void Loop Teil, der nach dem Einsatz des Tasters abläuf, kopieren und hintereinander an die Taster hängen. Eigentlich hätte der Sketch so auf das Drücken jedes Tasters reagieren können, leider gab es aber noch mindestens einen Fehler, weshalb wir den Sketch noch nicht hochladen konnten.

![Fehlermeldung](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Fehlermeldung%20Arduino.PNG?raw=true)

Diesem Fehler werden wir uns in den nächsten Stunden widmen. 


### <a name="24"></a>Donnerstag, 20. Februar 2020

Am Anfang der Stunde haben wir uns dem gestrigen Problem mit dem Sketch gewidmet. Nachdem wir einige geschweifte Klammern anders angeordnet und die Beschreibung des Namens "GRÜN" in "GRUEN" geändert haben hat alles funktioniert. Danach haben wir noch einen vierten Taster installiert, den eine Bewegung eines Servos auslöst.

![tasterSERVO](https://github.com/dennis602/Stundenprotokoll-II/blob/master/TasterSERVO.PNG?raw=true)

![Servo](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Teebeutel_SERVO.PNG?raw=true)

Das brauchen wir am Ende des Ablaufs der Teebeutelmaschine. Wenn der Tee fertig gezogen hat, zieht der Stepper-Motor den Beutel hoch und dann fährt der Servo eine Platte mit einer Schüssel über die Tasse, in die dann der Beutel fallen kann. Soweit ist unser Plan, inwieweit sich dies realisieren lässt werden wir sehen. Für den Servo mussten wir die <Servo.h> Bibliothek einbinden, den Servo bennenen und den Pin angeben. Das hat alles gut funktioniert.



Am Freitag ist der Informatikunterricht ausgefallen.

### <a name="25"></a>Mittwoch, 26. Februar 2020

Diese Woche fällt der Informatikunterricht komplett aus. Da wir ohne Zugang zum Computerraum nicht an unserem Projekt weiterarbeiten können, haben wir mit der Projektseite begonnen. Wir planen eine ähnliche Struktur wie letztes Halbjahr.


### <a name="26"></a>Donnerstag, 05. März 2020

Auch diese Woche ist der Unterricht Mittwoch und heute ausgefallen, also haben wir an der Projektseite weitergeschrieben. Heute haben wir auch versucht, in der Stunde in den Computerraum zu gehen, aber auch der Hausmeister konnte uns nicht den Schrank öffnen. Also können wir erst morgen wieder an dem Projekt weiterarbeiten.


### <a name="27"></a>Freitag, 06. März 2020

Heute haben wir uns mit dem neu bestellten LCD Display beschäftigt. Wir haben uns sehr gefreut, dass es sich um ein I2C-LCD Display gehandelt hat, da dieses nur 4 Anschlüsse und kein Potentiometer braucht, wie es oft bei LCDs ist. Wir haben also das LCD Display angeschlossen.

https://funduino.de/nr-19-i%C2%B2c-display

Außerdem mussten wir, wie beim Motorshield, eine neue Bibliothek herunterladen. Es handelt sich dabei um die <LiquidCrystal_I2C.h> Bibliothek. Das hat problemlos funktioniert.

![LCD Bibliothek](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD%20Bibliothek.PNG?raw=true)

Jedoch hat das Display nur geleuchtet, aber nichts angezeigt. Wir haben herausgefunden, dass es zweizeilige und vierzeilige LCDs gibt. Diese muss man auch anders programmieren. 

https://funduino.de/anleitung-4x20-i%C2%B2c-lcd-modul

Das haben wir leider nicht mehr geschafft auszuprobieren. Das werden wir also nächste Woche testen.


### <a name="28"></a>Mittwoch, 11. März 2020

Heute haben wir uns mit dem LCD Display auseinandergesetzt. Wir wollten es erstmal nur schaffen, dass irgendeine Art von Text auf dem Bildschirm erscheint. Zuerst haben wir viele Anleitungen aus dem Internet studiert und dann verschiedene Sketche ausprobiert. Leider wurde immer die Wire.h Bibliothek gebraucht, wir haben es aber nicht geschafft, diese in das Programm einzubinden. Somit haben wir es noch nicht geschafft Text auf das LCD Display zu Übertagen. Dies bleibt weiterhin unser Ziel.



Donnerstag ist der Informatikunterricht ausgefallen.


### <a name="29"></a>Freitag, 13. März 2020

Heute haben wir weiterhin versucht die Wire.h Bibliothek einzubinden um so das LCD-Display ansteuern zu können. Dennis hat hierzu seinen Laptop mitgebarcht und dort alles nötige installiert. Leider hat es noch immer nicht geklappt. Es stellt sich also die Frage, ob wir das immernoch weiterverfolgen sollten. Außerdem wussten wir schon während der Stunde, dass die nächten zwei Wochen wegen Corona ausfallen werden. Deshalb haben wir unsere gesamte Hardware und ein paar zusätzliche Kabel eingesteckt, um zu Hause weiterarbeiten zu können.



### <a name="30"></a>Donnerstag, 19. März 2020

Heute haben wir uns noch einmal mit dem LCD-Display beschäftigt. Es gibt sehr viele Anleitungen dazu im Internet, doch keine konnte uns bisher helfen. Heute haben wir endlich ein sehr gutes Video inklusive Webside gefunden.

https://www.youtube.com/watch?v=NyiWH5Mc7ek

Dort wurde erklärt, dass man für die Ansteuerung eines LCD-Displays zuerst die Adresse scannen muss. Dazu gibt es einen Sketch zum Download, der im Serial Print die angeschlossenen Geräte anzeigt.

![Adressenscanner](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Adressenscanner_LCD.PNG?raw=true)

Hier kann man also ablesen, dass unser Display die Adresse 0x3F hat. In den bisherigen Sketchen war als Adresse immer 0x27 angegeben. Somit war der erste Fehler behoben.

Die Wire Bibliothek hat auf unserem privaten Laptop problemlos funktioniert. Diese ist von Arduino vorinstalliert.

Anschließend haben wir die Sketche ausprobiert, die wir bisher hatten und haben dort die Adresse des LCD-Displays entsprechend geändert.

![Code_LCD_Beispiel](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD_Beispiel.PNG?raw=true)

Nun war das Problem, dass das Display jeweils nur den ersten Buchstaben der zwei Zeilen des Displays angezeigt hat.

![Display nur 1 Zeichen](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD_Beispiel.JPG?raw=true)

Also haben wir weiter recherchiert, bis wir auf weitere Sketche gestoßen sind. Der aus dem ersten Video schien sehr gut.

https://www.aeq-web.com/i2c-display-mit-dem-arduino-uno/

![LCD_kompliziert, aber funktioniert](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD_kompliziert.PNG?raw=true)

Nach dem Updaten der <LiquidCrystal_I2C.h> Bibliothek und dem Download der NewLiquidCrystal Library (https://bitbucket.org/fmalpartida/new-liquidcrystal/downloads/) konnte auch die <LCD.h> Library eingefügt und genutzt werden. Mit "setCursor" kann man festlegen, in welcher der beiden Zeilen der Text abgebildet werden soll. Nun hat der Sketch tatsächlich endlich funktioniert. Jedoch war uns der Sketch zu unübersichtlich und wir wollten ihn vereinfachen. 

Wir haben einen ähnlichen, aber deutlich einfacheren Sketch in einem Forum gefunden.

https://www.roboternetz.de/community/threads/68468-Arduino-Mega-mit-LCD-I2C

![LCD Forum](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD_Forum.PNG?raw=true)

Dieser hat so noch nicht funktioniert. Also haben wir ihn mit dem funktionierenden Sketch kombiniert, indem wir die fehlende Definition des "Backlight-Pins" eingefügt haben. 

![Code LCD funtioniert](https://github.com/dennis602/Stundenprotokoll-II/blob/master/code_lcd_funktioniert.PNG?raw=true)

![LCD funktioniert](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD_funktioniert.JPG?raw=true)

Damit waren wir fertig.


### <a name="31"></a>Freitag, 20. März 2020

Heute haben wir das LCD-Display in den Sketch für den Teebeutelautomat eingebaut. Dazu haben wir auch dort die Libraries eingefügt und im Setup die notwendigen Informationen eingefügt (siehe gestern). Im Loop haben wir folgendes programmiert: Zunächst fordert der Bildschirm auf, eine Tasse vor den Ultraschallsensor zu stellen. Anschließend wird man aufgefordert, die entsprechende Teesorte zu wählen.

![LCD im Sketch](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD%20im%20Sketch%202.PNG?raw=true)

Nach Knopfdruck wird in der oberen Zeile des Bildschirms die Teesorte angezeigt und unten steht eine Zahl, bis zu der man warten soll. Diese Zahl entspricht der Variablen i, die in der while Schleife erreicht werden soll (s. [Mittwoch, 22. Januar 2020](#13)). Rechts davon wird durch lcd.print(i) der aktuelle Stand der Variablen angezeigt, sodass man sozusagen einen Timer hat und abschätzen kann, wie lange man warten muss.

![LCD im Sketch](https://github.com/dennis602/Stundenprotokoll-II/blob/master/LCD%20im%20Sketch.PNG?raw=true)

Am Ende sagt der Bilschirm, dass der Tee fertig ist. 

Nun müssen wir nur noch die Zeiten für die jeweiligen Tees der Realtiät anpassen. Wie das ganze aussieht, wird in einem Video auf der Projektseite zu sehen sein.




## Die folgenden Einträge sind nach Abgabe des Protokolls (24. März) entstanden.

### <a name="32"></a>Mittwoch, 25. März 2020

Heute haben wir noch eine Sache am Sketch verändert, die uns bisher gestört hatte. Wenn der Tee fertig war gab es bisher ein akustisches Signal und der Bildschirm zeigte an, dass der Tee fertig ist - jedoch nur für die festgelegte Zeit von 10 Sekunden. Wir wollten aber, dass auf dem Bildschirm "Tee fertig!" solange erscheint, bis der Benutzer den Tee genommen hat. Dazu haben wir den vierten Taster (der ursprünglich für die Bewegung des Servos war; dieser bewegt sich jetzt aber automatisch wenn eine Tasse hingestellt oder weggenommen wird) integriert. Wir wollten eine Variable einführen, die durch den Tasterdruck auf 1 erhöht wird. An der entsprechenden Stelle im Sketch schreiben wir also, dass der Bilschirm solange "Tee fertig!" anzeigen soll, wie diese Variable unter 1 ist. Zusätzlich steht auf dem Bildschirm "Druecke <fertig>", damit der Nutzer weiß, welchen Knopf er zum Beenden des Vorgangs drücken soll. Grundlage dazu war der folgende Link (Beitrag aus Forum), doch wir mussten einiges Verändern und für uns Anpassen, wie auf dem Screenshots zu sehen ist.
  
  https://www.arduinoforum.de/arduino-Thread-bei-Tastendruck-Variable-immer-1
  
  Vor dem Void Setup werden Taster und benötigte Variablen eingeführt.
  
  ![Endknopf Einführung](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Endknopf%20einf%C3%BChrung.PNG?raw=true)
  "val" ist dabei eine Variable, in der man einen Wert speichern kann. Sie kann somit die Anzahl der gedrückten Male des Tasters       speichern. Im Setup wird dann buttonState definiert, indem es = digitalWrite(switchPin) gesetzt wird. Im Loop wird zuerst die Variable "buttonPresses" = 0 gesetzt, damit die Variable jeden Ablauf erneut gleich Null ist.
  Nach dem Motorablauf und dem Piepton haben wir nun eine while Schleife genutzt, um den Bilschirm solange den gewünschten Text anzeigen zu lassen, wie die Variable "buttonPresses" unter 1 ist. Außerdem wird festgelegt, dass durch Knopfdruck die Variable um 1 erhöht wird.
  
  ![Endknopf Loop](https://github.com/dennis602/Stundenprotokoll-II/blob/master/Endknopf%20Loop.PNG?raw=true)
  
  
