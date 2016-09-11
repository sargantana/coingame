# coingame
gui driven network game



Jeder Spieler erhält 50 Münzen. Ziel ist es 3 Punkte zu bekommen, dadurch hat man Gewonnen.
In jeder Runde setzen die Spieler mindestens 0 Münzen, wissen dabei aber nicht was der andere setzt. 
Der erste der fertig Gesetzt hat betätigt einen Schalter, danach kann er an seinen Münzen nichts mehr Ändern.
Der zweite hat nun noch 10 Sekunden zeit um Fertig zu setzen. Nach ablauf der Zeit vergleicht der Computer die
gesetzten Stapel, der Spieler mit dem größeren bekommt einen Punkt. 
Die gesetzten Münzen werden aus dem Spiel entfernt.
Das ganze wird solange wiederholt bis der erste 3 Punkte hat. Wenn die Spieler gleich viele Münzen setzen 
bekommt niemand einen Punkt, die Münzen werden trotzdem aus dem Spiel entfernt.


Not implemented:
Die Software besteht aus Server und Clienten. Beim start betritt man eine art Lobby in der man sich mit anderen
Spielern unterhalten kann und wenn zwei sich gefunden haben kann man über das Komanndo "!@nickname" 
mit dem Nicknamen des jeweils anderen eine Spielinstanz starten. Ab diesem Punkt startet eine GUI die aus einer
5*10 Matrix und den Buttons "+","-","Setzen","Bereit" besteht, sowie einem Punktindikator der den derzeitigen Punktestand
der beiden Teilnehmer anzeigt.   

Nun setzen die Spieler über +/- die Anzahl ihrer Punkte. Wenn der erste Fertig ist drückt er auf Setzen. 
Dadurch wird an dem Server die Anzahl der gesetzten Münzen, sowie der Nickname des Gegenspielers übermittelt.
Der Server schickt daraufhin ein Countdown Kommando an den Gegenspieler wodurch auf seinem Bildschirm ein Countdown 
startet. Nach ablauf der Zeit Sendet der Gegenspieler die Anzahl seiner Gesetzten Münzen an den Server, dieser 
Vergleicht beide Werte und Sendet an beide den Punktestand welcher auf beiden Clientrechnern angezeigt wird.
Bei Gleichstand bleiben die Punkte unverändert. 
Dieser Ablauf wiederhohlt sich bis ein Spieler 3 Punkte hat. Darauf hin Gewinnt er das Spiel und die Spielinstanz
wird beendet. 

