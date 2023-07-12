---
title: "Nachbau Anleitung"
date: 2023-07-05T13:11:50+01:00
draft: false
coverImage: "../images/Ruckblick/Schwert_v3_seite.jpg"
metaAlignment: center
coverMeta: out
thumbnailImagePosition: left
---



# Blogpost: Wie es gelaufen ist


## Einleitung

Das Lichtschwert Projekt ist fertig und wir konnten es auf dem Streiflicht 2023 erfolgreich Präsentieren. In diesem Blogpost möchte ich euch einen überblick zeigen, wie ich die ganzen Wochen gearbeitet habe, und was alles gut oder schlecht lief. Dazu möchte ich meine neuen Erkenntnisse auch Dokumentieren.

Mein Projekt war ein Lichtschwert, dieses sollte diverse Funktionen haben, wie ein Soundmodul, was Sounds abspielt, sobald das Lichtschwer eingeschaltet wird. Dazu ein Bewegungssensor, der tracken kann, on das Lichtschwert bewegt wurde, und dann dementsprechend Sounds abgespielt hat.
Dazu gab es noch Infrarot Sensoren, die in der klinge versteckt waren. Mit diesen sollten Blaster Schüsse simuliert werden, die von einer selbstgebauten Fernbedienung kommen. So sollte das Schwert diese “abwehren” können und in dem Einschlag Bereich mit der vorhanden Led reagieren und dazu ein Abwehr sound abspielen.
Zum Anfang kann ich nur sagen, dass ich wieder sehr viele neue Sachen und Techniken gelernt habe, was mir im Zukunft das Arbeiten mit Microcontrollern oder auch das normaler handwerkeln zuhause vereinfachen wird. Insbesondere das 3D Modellieren konnte ich in diesem Projekt vertiefen, da ich mein Chassis komplett aus 3D Druck gebaut hab. Jedoch ist mir da aufgefallen, dass es sehr viel Zeit kosten kann, wenn man mehrere Versionen einer sache ModelliertDa. Viele veränderunen führten daszu, dass ich mein ganzes oder ein teil meines Modells häufig neu Drucken musste. Aber Mehr dazu dann in den einzelnen Abschnitten.

### Jeder Anfang ist Schwer

In der ersten Woche, gleich nach dem Pitch, konnte ich nicht viel machen. Ich habe mich Hauptsächlich darum gekümmert, dass eine Teilerliste steht, damit unser Betreuer Ali Askari, die Teile Bestellen kann. 
Dazu habe ich auch eine Roadmap entworfen, die mir beim erstellen des Projektes einen Leitfaden bietet, damit ich auch weiß was ich alles erreichen möchte. 

### Der richtige Anfang

Durch eine Empfehlung von Ali, habe ich mich in der ersten Woche gleich um das Testen der Sensoren gekümmert. Ich habe angefangen Infrarot Sensoren auszulesen und zu schauen wie diese Sich verhalten. Da die Idee ja war, dass die IR-Sensoren die Schüsse abwehren können, musste ich sie so testen, dass der Bereich den die IR-Sensoren einfangen sehr klein ist. Dies hab ich mit einfachen 3D-Modellierten Schutzvorrichtungen schaffen können.



{{< figure src="../images/Ruckblick/schutz_v1_unten.jpeg" width="60%" height="60%"  caption="Das ist der Schutz von unten" >}}


{{< figure src="../images/Ruckblick/schutz_v1_vorne.jpg" width="60%" height="60%" caption="Das ist der Schutz von Vorne">}}


Bis dahin konnte ich leider nicht viel mehr Testen, da ich keine weiteren Sensoren im Lab vorrätig hatte. Daher musste ich warten, bis die Bestellwelle kommt, und mich erstmal zurücklehnen.

### Design-Time

Nachdem ich viel Zeit mit dem Testen von dem IR-Sensor verbracht habe, habe ich mich entschlossen, an meinem Design zu Arbeiten. Das  Design finde ich sehr Modern und ich finde auch, dass das sehr gut zu meinem Lichtschwert passt. Besonders habe ich drauf geachtet, dass der Platz irgendwie reicht um meine Sachen unterzubringen. Dies sollte sich noch als ein allgemein großes Problem darstellen. Jedoch habe ich schon vorgesorgt, und eine Kappe mit einem klick Verschluss gebaut, der es mir ermöglicht, immer auf das Innere des Schwertes zuzugreifen, falls mal etwas geändert werden muss, oder irgendwas kaputt geht. Das Design sah so aus:

{{< figure src="../images/Ruckblick/Schwert_v3_seite.jpg" width="60%" height="60%" caption="Das Schwert von Vorne">}}

{{< figure src="../images/Ruckblick/Schwert_v3_Oben.jpg" width="60%" height="60%" caption="Das Schwert von Oben">}}

{{< figure src="../images/Ruckblick/Schwert_v3_Kappe.jpg" width="60%" height="60%" caption="Die Kappe des Schwertes">}}

Persönlich war ich sehr Zufrieden mit dem Design, jedoch war das Design nicht fertig, da ich z. B den Button noch nicht Designed hatte. Und ich hatte noch keine Vorrichtung, die holz Klinge oder das PVC zu Verschrauben. Diese Verbesserungen habe ich dann in Zukunft vorgenommen.

Daraufhin habe ich auch eine Schutzvorrichtung für meine Teile im Inneren angefangen zu Designen. Diese habe ich so gemacht, dass man die Boards in ruhe einbauen kann ohne diese zu Schaden zu bringen.


{{< figure src="../images/Ruckblick/KastenFrBoards_v5_Hinten.jpeg" width="60%" height="60%" caption="Der Kasten von Hinten">}}

{{< figure src="../images/Ruckblick/KastenFrBoards_v5_Vorne.jpeg" width="60%" height="60%" caption="Der Kasten von Vorne">}}

Hinten hab ich es so aufgebaut, dass ich in ruhe ein USB-Kabel einstecken kann, und auch den LED-Strip durchstecken kann.

{{< figure src="../images/Ruckblick/Button.jpeg" width="60%" height="60%" caption="Der Button mit der Schiebe vorrichtung">}}

Der hintere Teil ist dazu, dass ich einen Schieberegler einstecken kann, und dieser dann fest im rahmen sitzt. Bei dem vorderen, ist ein Loch, damit ich den Kopf des Schiebereglers rein kleben kann. Dadurch hat man dann einen Button der sich nach oben und unten bewegen kann, sobald das hintere fest geklebt wurde.



{{< figure src="../images/Ruckblick/vh1zc7vp.gif" width="60%" height="60%" caption="Das sind Verschiedene Versionen von meinem Schwert">}}



### Die Platine

Nachdem das Design stand, ging es daran, die Teile von der Bestellung zu Testen. Als erstes hab ich mich gleich mal an den Vibrationssensor gemacht und gleich gemerkt, dass die leider nicht gut Funktionieren. Daher habe ich nach dem Testen die Vibrationssensoren gleich mal verworfen. Daraufhin hab ich mich entschieden den Bewegungssensor, also den MPU-6050 anzusteuern. Das hat für den Anfang gut funktioniert. Dazu später mehr. Darüber hinaus hab ich dann angefangen, den DFPlayerMini anzusteuern. Das hat auch sehr gut funktioniert. 

Nach dem ich die meisten meiner Teile getestet habe, war es Zeit die Platine zu Designen. Dazu habe ich das Fritzing Tool genutzt. So konnte ich mir mein Design schon Planen und schauen wie klein ich die Platine machen kann. Da ich ja sowieso Platz Probleme habe.


{{< figure src="../images/Ruckblick/Untitled_Sketch_Steckplatine.jpg" width="60%" height="60%" caption="Hier mein Schaltplan den ich in Fritzing erstellt habe">}}


{{< figure src="../images/Ruckblick/IMG_2299.jpg" width="60%" height="60%" caption="Meine Hauptplatine">}}

Jeder platz der nicht zum Wiring gehört wurde bei mir weggeschnitten. Da ich nur wenig Platz im Schwert habe, musste ich drauf achten, dass es so klein wie möglich gemacht wird.

### Meine Probleme

Probleme hatte ich leider einige beim Arbeiten an diesem Projekt.
Ich hab wohl am Anfang, eine schlechte Library für den Bewegungssensor also den MPU-6050 genutzt. Daher hatte ich eine sehr lange Zeit gewisse Probleme mit meinen LED´s. Da der MPU beim ansteuern in dieser Library einen großen delay verursacht hat, sind meine LED´s nicht richtig aufgeleuchtet, dadurch hatte ich ewig viele Code Fehler die ich erst gegen Ende des Projekts verbessern konnte, wo ich gemerkt habe, dass es an der Library liegt.
Ich habe ja schon oft erwähnt, dass Platz einer der großen Herausforderungen war. Da das Lichtschwert nicht zu dich werden durfte war es wichtitg dass alles klein und sparsam ist. Dadurch habe ich leider auch einen Kurzschluss verursacht, beidem mein Arduino Nano den Geist aufgegeben hat. Zu dem hab ich durch das rein drücken von meiner Platine wohl einmal einen DFPlayerMini kaputt gemacht, da ich wohl kleine Teile abgerissen habe während dem Reindrücken.

Wie auch schon gezeigt, habe ich viele Design Veränderungen an meinem Schwert vornehmen müssen. Da das auch nicht auf anhieb geklappt hat. Oft war es so, dass der Platz nicht gereicht hat. Die klinge nicht gehalten hat. Ich z. B bei einem Design gar nicht mehr den Button reinbekommen habe, oder einmal war es so, dass der Kopf vom Lichtschwert zu wenig halt beim Kleben hatte, und dadurch der Kopf abgerissen ist.

Auch beim Löten gab es wieder Challenges. Was ich am schlimmsten fand, war das löten eines USB-Kabels an meiner Stromversorgung. Das Problem war, dass ich ein USB-Kabel benötigt hab um meine Stromversorgung mit einer PowerBank zu Powern. Das USB-Kabel war leider aber so anfällig auf risse, dass es mindestens 20 mal gerissen ist, und ich es häufig nach löten musste. Dies hat ewig viel Zeit gekostet.
Das Restliche Löten, lief sehr gut. Durch das Projekt vom letzten Semester konnte ich viel im Löten üben, und hatte daher kaum Probleme bis auf das Problem von Oben.

### Fazit

Das Lichtschwert sollte also Schüsse abwehren können mit IR-Sensoren. Sounds abspielen können mit einem Amplifire und einem Lautsprecher und Bewegungen erkennen können mit einem Accelometer.

Das Lichtschwert hatte leider bei der Abschlusspräsentation einige Fehler, die nicht so gewollt waren. Die LED hat aufgehört richtig zu Arbeiten und das einzige was zuverlässig funktioniert hat war der Bewegunssesnor und das Soundmodul. Die LED und den Infrarotsensoren habe ich aber nach der Präsentation wieder hingerichtet. Daher Funktioniert jetzt eigentlich jeder Funktionalität die ich wollte.

Die meisten Ideen die ich von anfang an hatte, habe ich auch so lösen können wie ich es mir Vorgestellt habe. Jedoch habe ich im nachhinein bessere Hardware gefunden, die meine Arbeit definitv vereinfacht hätte. Aber auch dies ist eine neue Sache die ich durch das Projekt gelernt habe.


Das Lichtschwert-Projekt war also eine herausfordernde, aber auch äußerst lohnende Erfahrung. Es hat mir nicht nur ermöglicht, meine Fähigkeiten im Bereich der Mikrocontroller und des 3D-Modellierens zu erweitern, sondern auch wertvolle Erkenntnisse über den Prozess der Projektentwicklung zu Erlangen.

Während des Projekts stieß ich auf verschiedene Herausforderungen, darunter Platzprobleme, Defekte von Bauteilen und Probleme mit Libraries. Diese Hindernisse erforderten Geduld und Durchhaltevermögen, führten aber auch zu wertvollen Lernmomenten. Ich musste oft Designänderungen vornehmen, um sicherzustellen, dass das Lichtschwert funktional und ästhetisch meinen Vorstellungen entsprach.

Während des Projekts habe ich auch wertvolle Lektionen gelernt, wie die Bedeutung der Wahl der richtigen Libraries, die sorgfältige Verarbeitung von Bauteilen und die beharrliche Problemlösung. Diese Erkenntnisse werden mir in zukünftigen Projekten und im Umgang mit Mikrocontrollern und handwerklichen Tätigkeiten von großem Nutzen sein.

Alles in allem war das Lichtschwert-Projekt eine wertvolle Erfahrung, die meine Fähigkeiten erweitert und mich dazu ermutigt hat, neue Herausforderungen anzunehmen. Ich freue mich darauf, mein erworbenes Wissen und meine Fähigkeiten in zukünftigen Projekten weiter anzuwenden und zu verbessern.