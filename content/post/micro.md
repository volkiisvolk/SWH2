---
title: "Microcomputer mit Arudino´s"
date: 2022-12-05T14:04:47+01:00
description: "Arudino Mechanik"
draft: false
coverImage: "../images/Ardu_Nano.jpg"
metaAlignment: center
coverMeta: out
thumbnailImagePosition: left
---

## Mein erstesmal mit einem Microcontroller
Am Mittwoch den 23.11.2022 hatte ich die Möglichkeit, meinen ersten Microcontroller in der Hand zu halten. Anfangs hatte ich Angst, irgendwelche Fehler zu machen und so etwas zu beschädigen, doch durch ein wenig Probieren und der Vorlesung wurde mir die Angst genommen.


## Versuch 1: Es Werde Licht

Nachdem wir unsere ersten Arduinos erhalten haben, wurden auch schon breadboards und verkablungen verteilt. Unser erste Aufgabe war es LED´s zum leuchten zu bringen. Dies war sehr einfach, denn es genügte den Ground Port vom Arduino mit dem - pol vom Breadboard zu verbinden und einen GPIO port mit dem + Pol. Dazu musste man natürlich auch noch zwischenverkablungen zur LED legen und in der Arduino IDE den Port programmieren.




{{< figure src="../images_micro/led.jpeg"  width="60%" height="60%">}}


Gleich nachdem wir die erste LED eigebaut haben, habe ich versucht, eine zweite dazu zu schalten. Disese haben dann abwechselnd geleuchtet.

## Versuch 2:Es wird Lauter

Hier hab ich gleich mal mit Sensoren herumgespielt. Der erste war einer der Geräausche macht. Die Lautstärke ließ sich letztendlich auch einstellen.


{{< figure src="../images_micro/sound.jpeg"  width="60%" height="60%">}}



## Versuch 3: Displays sind schwerer als gedacht.

So selbstbewusst wie ich nach meinen ersten erfolgen war, habe ich mich gleich mal an so ein Display gewagt. Nach langem hin und her musste ich dann leider der Wahrheit ins Auge sehen, und akzeptieren, dass das wohl doch zu voreilig war. Alleine das zusammenstecken war nicht leicht, das Programmieren jedoch war für meinen jetzigen Standpunkt, noch zu schwer.

{{< figure src="../images_micro/dis.jpeg"  width="60%" height="60%">}}


## Versuch 4: Serielle Kommunikation
In der Seriellen Kommunikation habe ich mich an einer LED Matrix dran gesetzt. Das hier ist mein Code


{{< highlight go "linenos=table,hl_lines=8 15-17,linenostart=199" >}}

#include "LedControl.h"

LedControl lc=LedControl(12,11,10,1);

void setup() {
  lc.shutdown(0,false);

  lc.setIntensity(0,8);

  lc.clearDisplay(0);
}

void writeArduinoOnMatrix() {
 
  byte a[5]={B01111110,B10001000,B10001000,B10001000,B01111110};

  lc.setRow(0,0,a[0]);
  lc.setRow(0,1,a[1]);
  lc.setRow(0,2,a[2]);
  lc.setRow(0,3,a[3]);
  lc.setRow(0,4,a[4]);
}


{{< / highlight >}}

Dadurch hab ich es geschafft, dass meine LED Matrix ein A Anzeigt

## Was genau ist I2C Serielle Kommunikation

{{< figure src="../images_micro/matrix.jpeg"  width="60%" height="60%">}}

Der I2C (Inter-Integrated Circuit) ist ein serieller Kommunikationsbus, der es ermöglicht, mehrere elektronische Geräte miteinander zu verbinden und miteinander zu kommunizieren. Es handelt sich um einen Master-Slave-Bus, bei dem ein einzelnes Gerät als Master fungiert und die Kommunikation kontrolliert, während die anderen Geräte als Slaves agieren und auf Anfragen des Masters reagieren.

Der I2C-Bus verwendet zwei Leitungen: eine Datenleitung (SDA - Serial Data Line) und eine Taktleitung (SCL - Serial Clock Line). Diese Leitungen sind bidirektional, was bedeutet, dass sowohl der Master als auch die Slaves Daten über die Leitungen senden und empfangen können.

Die Kommunikation auf dem I2C-Bus erfolgt durch Übertragung von Datenpaketen, die als "Nachrichten" bezeichnet werden. Jede Nachricht besteht aus einem Adressbyte, das angibt, welches Gerät die Nachricht empfangen soll, gefolgt von Datenbytes, die die eigentlichen Informationen enthalten. Der Master initiiert die Kommunikation, indem er die Adresse des Slaves sendet, mit dem er kommunizieren möchte, gefolgt von den Daten oder Befehlen.

Ein Vorteil des I2C-Busses ist die Fähigkeit, mehrere Geräte mit nur zwei Leitungen zu verbinden. Jedes Gerät auf dem Bus hat eine eindeutige Adresse, die vom Master erkannt wird. Dadurch können bis zu 128 Geräte an einem einzigen I2C-Bus angeschlossen werden.

Der I2C-Bus wird in verschiedenen Anwendungen eingesetzt, insbesondere in der Elektronik und der Mikrocontroller-Programmierung. Er ermöglicht die einfache Integration von Sensoren, Aktoren, Displays und anderen elektronischen Komponenten in ein System.


