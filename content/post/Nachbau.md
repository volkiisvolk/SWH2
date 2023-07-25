---
title: "Nachbau Anleitung"
date: 2023-07-05T13:11:50+01:00
draft: false
coverImage: "../images/Ruckblick/Schwert_v3_seite.jpg"
metaAlignment: center

coverMeta: out
thumbnailImagePosition: left
---
### Einleitung:

Mein Projekt war ein Lichtschwert, dieses sollte diverse Funktionen haben, wie ein Soundmodul, was Sounds abspielt, sobald das Lichtschwert eingeschaltet wird. Dazu ein Bewegungssensor, der tracken kann, on das Lichtschwert bewegt wurde, und dazu dann dementsprechende Sounds abspielen.
Dazu gab es noch Infrarot Sensoren, die in der klinge versteckt waren. Mit diesen sollten Blaster Schüsse simuliert werden, die von einer selbstgebauten Fernbedienung kommen. So sollte das Schwert diese “abwehren” können und in dem Einschlag Bereich mit der vorhanden LED reagieren und dazu ein Abwehr sound abspielen.

Die Idee war es zu zeigen, dass man ein Lichtschwert auch billiger selbst bauen kann. Leider kosten Lichtschwerter sehr viel und sind meist auch von Schlechter Qualität, so kann man sogar sein eigenes Design machen, und dazu auch noch viel Geld Sparen.

### Bauteile:

- **[ARDUINO NANO Arduino Nano V3, ATmega 328, Mini-USB](https://www.reichelt.de/arduino-nano-v3-atmega-328-mini-usb-arduino-nano-p142943.html?search=arduino+nano)**
- [**ARD DFPAYER MINI Arduino - DFPlayer Mini**](https://www.reichelt.de/arduino-dfplayer-mini-mp3-wav-microsd-karte-ard-dfpayer-mini-p289897.html?PROVID=2788&gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_lauymmJG6foTYR4S60vDFAvxTd4eXJdaEbhaLEvOirMdMszOFgqpIaAuxTEALw_wcB)
- **[DEBO SENS 3AXIS Entwicklerboards - Beschleunigung & Gyroskop, 3-Achsen, MPU-6050](https://www.reichelt.de/entwicklerboards-beschleunigung-gyroskop-3-achsen-mpu-6050-debo-sens-3axis-p253987.html?&trstct=pos_0&nbc=1)**
- **[TRU COMPONENTS OS-1838 IR-Empfänger Sonderform axial bedrahtet 38 kHz 940 nm 35](https://www.conrad.de/de/p/tru-components-os-1838-ir-empfaenger-sonderform-axial-bedrahtet-38-khz-940-nm-35-1572283.html?hk=SEM&WT.mc_id=google_pla&gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_maTnqIvHTeHBTAy4BtaBlcn2rTZQi3uw5wHjULBRk7KYJzj7ZYzgoaArVIEALw_wcB)**
- **[BTF-LIGHTING WS2812 1M 60 LEDs/Pixels/m WS2812B Schwarz PCB RGB adressierbare Strip mit 5050 SMD LEDs NichtWasserdicht IP30 Stripes](https://www.amazon.de/BTF-LIGHTING-WS2812B-adressierbare-Streifen-NichtWasserdicht/dp/B01CDTED80/ref=asc_df_B01CDTED80/?tag=googshopde-21&linkCode=df0&hvadid=232051979945&hvpos=&hvnetw=g&hvrand=639957698393931961&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9042139&hvtargid=pla-352730111509&psc=1&th=1&psc=1)**
- **[T 215 Schiebeschalter-Miniatur, Lötanschluss, 1x UM](https://www.reichelt.de/schiebeschalter-miniatur-loetanschluss-1x-um-t-215-p19975.html?PROVID=2788&gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_kdDB-FjAaenwBwjS9DW-n429PRygjb-4YvHcWYDhvgP3eQ2128itsaAtgaEALw_wcB)**
- **[PAM8403 digitaler Mini Audio Verstärker 2x 3 Watt DC 5V Leistungsverstärkerplatine mit Potentiometer für DIY Lautsprecher und Kopfhörer](https://www.az-delivery.de/products/pam8403-digitaler-mini-audio-verstarker-2x-3-watt-dc-5v-leistungsverstarkerplatine-mit-potentiometer-fur-diy-lautsprecher-und-kopfhorer-inklusive-ebook?variant=39436364808288&utm_source=google&utm_medium=cpc&utm_campaign=16964979024&utm_content=136656817158&utm_term=&gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_mpHrvP_YCuHzHyAviBLaSbbcWSZcFBldpY4ow8QXjyHZSZzAZRg64aAnk-EALw_wcB)**
- **[VIS 2802 Kleinlautsprecher K 20, 1,0W, 8 Ohm](https://www.reichelt.de/kleinlautsprecher-k-20-1-0w-8-ohm-vis-2802-p248245.html?&trstct=pol_5&nbc=1)**
- [**PowerBank**](https://www.amazon.de/dp/B089SV6513?ref=nb_sb_ss_w_as-reorder-t1_k5_1_9&amp=&crid=2TIVUFEDLJFF6&amp=&sprefix=powerbank)

### Hardware:

- **[Konsta Rundstab Buche roh Ø 14 mm L:1000 mm](https://www.hornbach.de/p/konsta-rundstab-buche-roh-o-14-mm-l1000-mm/5485761/)**
- **[PVC Rohr transparent 32 mm 1 m (+/- 0,5%)](https://www.mcm-systeme.de/PVC-Rohr-transparent-32-mm-1-m?utm_source=google&utm_medium=cpc&utm_campaign=alle-kampagnen&gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_myyVQDZGUfBONZAuGsfkdw7LnlukGsfqTTURiJGi4xZl8gjYxI23UaAre-EALw_wcB)**
- [**M2.5 Heat-Set Inserts**](https://www.amazon.de/s?k=M2.5+x+0.45+mm+Thread+Size%2C+3.4+mm&geniuslink=true&tag=ocrlab0d-21)
- **[M2.5 Socket Head Screws](https://www.amazon.de/s?k=M2.5+x+3-20mm+Bolts+and+Nuts&geniuslink=true&tag=ocrlab0d-21)**
- **[JD79 Spanplattenschraube 3x20 mm galv. verzinkt gelb chromatiert, 200 Stück](https://www.hornbach.de/p/jd79-spanplattenschraube-3x20-mm-galv-verzinkt-gelb-chromatiert-200-stueck/3834785/?wt_mc=de.paid.sea.google.alwayson_assortment.eis.pla.766104886.102189377754.&wt_cc1=766104886&wt_cc2=102189377754&wt_cc3=425722128162&wt_cc4=&wt_cc6=3834785&wt_cc7=&gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_mN_R7JmC-P-3wzTwovaPfd67Pip6GnUHjU1LUrDgMLJJOKnJ2vvC0aAplfEALw_wcB)**
- [**Lochrasterplatte Kit**](https://www.amazon.de/Doppelseitig-Prototype-Lochrasterplatte-Verschiedene-Kompatibel/dp/B0734XYJPM/ref=asc_df_B0734XYJPM/?tag=googshopde-21&linkCode=df0&hvadid=231998698971&hvpos=&hvnetw=g&hvrand=8740646829613995993&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9042139&hvtargid=pla-422876697783&psc=1&th=1&psc=1)
- Kupferkabel
- Fernbedienung(Egal welche)

### 3D-Printing

- [**PLA Filament**](https://filamentworld.de/?gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_mW7CpIHpozFgtgrZiYBRDKRAuODnh8dGeytAu-99RMPw9C4AdLTjIaAq9xEALw_wcB)
- [**Alle anderen teile für einen 3D Druck**](https://filamentworld.de/?gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_mW7CpIHpozFgtgrZiYBRDKRAuODnh8dGeytAu-99RMPw9C4AdLTjIaAq9xEALw_wcB)

### Fertigstellung

- [**Sandpapier**](https://www.amazon.de/LANHU-sortiert-K%C3%B6rnung-Schleifpapier-St%C3%BCck/dp/B07BGWRD56/ref=sr_1_1_sspa?keywords=sandpapier&qid=1689165623&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1)
- [**Acrylfarbe**](https://www.amazon.de/s?k=acrylfarbe&__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1C12UUO5AOJ9&sprefix=acrylfarbe%2Caps%2C102&ref=nb_sb_noss_1)
- [**Backpapier**](https://www.amazon.de/TOPINCN-Pergamentpapier-doppelseitige-Lebensmittel-Backpapier/dp/B07MGQW21N/ref=asc_df_B07MGQW21N/?tag=googshopde-21&linkCode=df0&hvadid=318194190204&hvpos=&hvnetw=g&hvrand=10954467689500785012&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9042139&hvtargid=pla-657354737722&psc=1&th=1&psc=1&tag=&ref=&adgrpid=60869609462&hvpone=&hvptwo=&hvadid=318194190204&hvpos=&hvnetw=g&hvrand=10954467689500785012&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9042139&hvtargid=pla-657354737722)
- [**Wolle**](https://www.hornbach.de/p/bastelwatte-1000-g-weiss/5987925/?wt_mc=de.paid.sea.google.alwayson_assortment.inn.pla.766105607.128661085896.&wt_cc1=766105607&wt_cc2=128661085896&wt_cc3=551982025096&wt_cc4=&wt_cc6=5987925&wt_cc7=&gclid=Cj0KCQjwnrmlBhDHARIsADJ5b_mdizGCB-E5EOSkJMzyUrj8R5UuQDkGjiHhYxgazhqtjF3LTeaX7YMaAt9dEALw_wcB)

### Tools

3D Drucker

Lötstation

Löt-Tisch

Schraubendreher

Kabel

Flux und Lötzinn

Kabel-Knipser

### Schritt 1: Design und Drucke dein Lichtschwert

Ihr habt die Möglichkeit ein eigenes Design zu erstellen, oder ihr benutzt meine STL´s. Natürlich kann man auch da immer wieder Veränderungen vornehmen.
Die letzte STL ist der Button und die Halterung, auch diese kann man noch anders designen. Aber sie sind so gebaut, dass sie perfekt in mein Projekt passen.


<a href="../post/Nachbau_assets/MainBody_First.stl" download= "MainBoady.stl">MainBody_First STL zum Downloaden</a>

<a href="../post/Nachbau_assets/MainBody_Second.stl" download>MainBody_Second STL zum Downloaden</a>

<a href="../post/Nachbau_assets/Stabhalterug_Final.stl" download>Stabhalterung STL zum Downloaden</a>

<a href="../post/Nachbau_assets/MainBody_First.stl" download>BodyButton STL zum Downloaden</a>


### Schritt 2: Anfangen mit dem Löten und Verkabelung

Fang erstmal damit an, deinen Arduino Nano zu löten. Dieser sollte an das kleinste Lochraster mit der Größe 4x6 rangelötet werden. Achte drauf, dass ihr den Nano soweit am Rand wie möglich lötet, dann ist es möglich gleich dran noch ein Teil zu löten. Arbeite so, dass die Lötstellen zu sind, und keine Kalte Lötstellen entstehen. Sich zeit zu lassen ist Gold wert.

Daraufhin fangt an den DFPlayerMini an das gleiche Board nebendran zu Löten. Wenn ihr aufgepasst habt und den Nano ganz in die Ecke Platziert habt, habt ihr noch genau genug Platz um den DFPlayerMini neben dran zu Löten. Platz Management ist bei diesem Projekt sehr wichtig!

Auf einem Extra Board was wieder die gleiche größte hat, löten wir dann den MPU-6050 dran. Auch hier achten wir drauf, dass wir das so Löten, dass es ganz an dem Rand ist. Achte dabei, dass du oben und unter dem MPU noch Platz frei haltest, damit du dort eine Reihe von 5V und GND mit Kupferkabel ziehen kannst.

Das sollte dann ungefähr so aussehen

{{< figure src="../Nachbau_assets/Schwert_Steckplatine.jpg" width="auto" height="auto" caption="Das ist die Steckplatine in Fritzing Designed">}}



Wie auch schon beschrieben sollen die Lochplatinen dann bei den Pinkenkabeln mit einer säge oder mit einem Clipser kaputt gemacht werden. 

Die 5V Reihe zieht man am Besten mit einem Kupferkabel, an dem man in ruhe ran löten kann.
Das gleiche dann mit einer Reihe von Ground.

Die Verkabelung kann theoretisch anders verlaufen, aber die Analog pins, sollten genau so gelötet werden, da dort eine I2C Kommunikation stattfindet.

### Schritt 4: Button befestigen.

Da wir ja jetzt genau zwei hälften haben, können wir jetzt ganz einfach den Button installieren.
Dafür müssen wir einfach nur zwischen einen USB-Kabel einen Schalter verlöten. Dafür müssen wir drauf achten, dass die Kontakte sich nicht berühren. und dass wir nur die roten kabel trennen und in den Schalter verlöten. Ist der Schalter Oben so werden diese kurzgeschlossen und es fließt Strom.

In dem gedruckten Button ist ein Loch. In dieses passt der Schalter perfekt rein. Ich würde empfehlen diesen zu Kleben. Man muss nur noch den button an die gewollte stelle mit einer M2 Schraube und der dazugehörigen Mutter befestigen. So sitzt dann der Button fest.

### Schritt 5: LED Stab herstellen

Als nächstes nehmen wir den LED Strip den wir haben, und befestigen diese rundherum am Stab. Den Abstand, kann man so variieren wie man möchte. Man sollte aber schonmal Platz frei halten für die Infrarot-Sensoren. 
Das Sieht dann ungefähr so aus:


{{< figure src="../Nachbau_assets/IMG_2397.jpeg" width="auto" height="auto" caption="Der Stab mit der LED und den IR-Sensoren">}}

Die LED´s haben genau 3 Löt Stellen und einen kleinen Pfeil, der die Richtung der LED anzeigt.

{{< figure src="../Nachbau_assets/Untitled.jpg" width="auto" height="auto" caption="Hier eine Beispiel LED.">}}

5V steht natürlich für den Strom und GND für Ground. Das Mittlere Din und Do ist für Digitalinput und Digitaloutput. Der Pfeil ist wichtig, da die LED nur in die Richtung des Pfeiles Strom fließen lässt.

Gleich daraufhin kann man auch die Infrarot-Sensoren anschließen und auf dem Stab kleben.

{{< figure src="../Nachbau_assets/i3.jpg" width="auto" height="auto" caption="Der VS183B und ihr Pinning">}}

Hier kann man sehen wie wir die Infrarot zu Wiren haben. Davon sollte man so ungefähr 3 stück nehmen und im Abstand von 10cm verkabeln und verkleben.

Wichtig ist dass wir die ganzen Kabel durch den Kopf des Lichtschwertes bekommen. Dafür gibt es vorgefertigte Tunnel die wir dafür nutzen können.


{{< figure src="../Nachbau_assets/halterung.jpg" width="auto" height="auto" caption="Hier ein Bild von der Vorrichtung">}}

Das innere Loch ist dazu, dass man den Holz Stab befestigen kann. Der Äußere dann später für die PVC Röhre.

### Schritt 7: Weiteres Verlöten.

Nachdem die Kabel durch den Kopf durchgesteckt wurden, muss man diese mit den Schon Board Verlöten. 
Dafür habe ich bei der LED den Port D2 Verwendet, und für die Infrarot-Sensoren D4-D6.
Stromkabel werden wieder mit dem 5V-Kupferkabel verlötet und GND mit dem GND-Kupferkabel.
Nachdem dies erledigt ist, war es das mit dem Löten für dieses Projekt. Dafür mal ein Glückwunsch 🥳

### Schritt 8: Die Klinge fertigstellen

Die PVC röhre muss nun fertiggestellt werden. Dazu benutzen wir Sandpapier damit eine Diffusion stattfindet. Ich hab 100 Sandpapier verwendet und dazu eine Schleifmaschine. Man kann da aber viel herumtesten. 
Daraufhin habe ich in das innere noch Backpapier befestigt und die LED´s dann mit Watte beklebt. Bei der richtigen Farbe funktioniert die Diffusion ganz gut.

### Schritt 9: Der Code

Den Code habe ich selbst geschrieben und in dem Code funktionieren alle Funktionen.
Ich habe Folgende Libraries verwendet

- ****Adafruit BusIO by Adafruit****
- ****Adafruit NeoPixel by Adafruit****
- ****DFRobotDFPlayerMini by DFRobot****
- ****IRremote by Armin Joachimsmeyer****
- ****MPU6050_tockn by tockn****

```arduino
#include <Arduino.h>
#include <Adafruit_NeoPixel.h>
#include <IRremote.h>
#include <Wire.h>
#include <SPI.h>
#include <SoftwareSerial.h>
#include <DFRobotDFPlayerMini.h>
#include <MPU6050_tockn.h>

#define PIN 2
#define IR_Pin_1 4
#define IR_Pin_2 5
#define IR_Pin_3 6

int angehen = 1;
int istAn = 2;
int moveing_1 = 3;
int moveing_2 = 4;
int moveing_3 = 5;
int ausgehen = 6;

int begining = 0;

float accBeginX = -30;
float accBeginY = 90;
float accBeginZ = -30;

/*
MPU Zeugs
*/
MPU6050 mpu(Wire);

static const uint8_t Pin_MP3_TX = 11;
static const uint8_t Pin_MP3_RX = 12;

DFRobotDFPlayerMini player;
SoftwareSerial swserial(Pin_MP3_RX, Pin_MP3_TX);

const int vibration_pin = 3;
const int MPU_ADDR = 0x68;

IRrecv IR_1(IR_Pin_1);
IRrecv IR_2(IR_Pin_2);
IRrecv IR_3(IR_Pin_3);

int accCounter = 0;

int16_t accelerometer_x, accelerometer_y, accelerometer_z; // variables for accelerometer raw data
int16_t gyro_x, gyro_y, gyro_z;                            // variables for gyro raw data
int16_t temperature;                                       // variables for temperature data
int counter = 1;                                           // counter for the Pixels
decode_results results;                                    // result from decode not necessery.
char tmp_str[7];                                           // temporary variable used in convert function
unsigned long inistart;                                    // milis start

float calcAverageX = 0;
float calcAverageY = 0;
float calcAverageZ = 0;
int done = -1;

// Sachen für den Vibrationssensor
boolean vibrating = false;
boolean ini = true;
unsigned long vibration_previousMillis = 0;
const int vibration_interval = 1000;

// Strip initialisierung
Adafruit_NeoPixel strip = Adafruit_NeoPixel(1, PIN, NEO_GRB + NEO_KHZ800);

// converts int16 to string. Moreover, resulting strings will have the same length in the debug monitor.
char *convert_int16_to_str(int16_t i)
{
  sprintf(tmp_str, "%6d", i);
  return tmp_str;
}

// Brightens the LED. int a, int b int c are RGB Values.
void brighten(int a, int b, int c)
{
  uint16_t i;
  for (i = 0; i <= strip.numPixels(); i++)
  {
    strip.setPixelColor(i, a, b, c);
  }
  strip.setBrightness(255);
  strip.show();
  delay(0.5);
  // delay(1500);
}

void movement()
{
  mpu.update();

  if (accCounter <= 50)
  {
    Serial.println(calcAverageX);
    Serial.println(mpu.getGyroY());
    Serial.println(mpu.getGyroZ());
    Serial.println("Neue Daten");
    float gyroX = mpu.getGyroX();
    float gyroY = mpu.getGyroY();

    if (gyroX < 0)
    {
      gyroX = gyroX * -1;
      calcAverageX += gyroX;
    }
    else
    {
      calcAverageX += gyroX;
    }

    // GYRO FOR Y
    if (gyroY < 0)
    {
      gyroY = gyroY * -1;
      calcAverageY += gyroY;
    }
    else
    {
      calcAverageY += gyroY;
    }
    calcAverageZ += mpu.getGyroZ();
    accCounter++;
  }

  if (accCounter == 50)
  {
    if (calcAverageX > 9000 || calcAverageY > 9000)
    {
     Serial.print("Moved");
    player.play(moveing_1);
    delay(1000);
    player.play(istAn);

    }
    
    accCounter = 0;
    calcAverageX = 0;
    calcAverageY = 0;
  }

  Serial.println("Counter");
  Serial.println(accCounter);
}

void setup()
{

  // MPU SETUP
  Wire.begin();
  mpu.begin();

  // Start of the SerialMonitor
  Serial.begin(115200);
  swserial.begin(9600);
  player.begin(swserial);
  player.volume(30);
  player.play(angehen);
  delay(200);
  inistart = millis();

  // Set pinMOde to output. I think not necessery anymore
  pinMode(8, OUTPUT);
  // Infrared things
  IR_1.begin(IR_Pin_1, false);
  IR_2.begin(IR_Pin_2, false);
  IR_3.begin(IR_Pin_3, false);

  // PinMode for VibrationSensor
  pinMode(vibration_pin, INPUT); // Vibration Sensor pin Mode

  // Start and show of the Strip
  strip.begin();
  strip.show(); // initialize all pixels to "off"
}

// Detects Vibrations
void vibration()
{
  unsigned long vibration_currentMillis = millis();
  if (digitalRead(vibration_pin) == HIGH)
  {
    vibration_previousMillis = vibration_currentMillis;
    if (vibrating == false)
    {
      vibrating = true;
      Serial.println("Vibration detected!");
      delay(150);
    }
  }
  else if (digitalRead(vibration_pin) == LOW)
  {
    if (vibrating == true)
    {

      brighten(255, 255, 0);
      delay(1000);
      vibrating = false;
      Serial.println("Vibration stopped!");
    }
  }
}

void loop()
{

  // vibration(); // Look if Vibration detected

  // if any irRecived lockated, then the color should change
  if ((IR_1.decodedIRData.decodedRawData, DEC) == 16)
  {
    player.play(4);
    Serial.print("Hey");
  }

  if ((IR_2.decodedIRData.decodedRawData, DEC) == 16)
  {
    player.play(5);
  }

  if ((IR_3.decodedIRData.decodedRawData, DEC) == 16)
  {
    player.play(3);
  }

  if (IR_1.decode())
  {
    Serial.print("BrightHit");
    brighten(0, 0, 255);
    delay(500);

    IR_1.resume();
  }

  if (IR_2.decode())
  {
    Serial.print("Hit");
     brighten(0, 0, 255);
    delay(500);
    IR_1.resume();
  }
  if (IR_3.decode())
  {
    Serial.print("Hit"); 
    brighten(0, 0, 255);
    delay(500);
    IR_1.resume();
  }

  // Each gets colored. So it lookes like a transision.
  if (counter < 120)
  {
    counter += 1;
  }
  strip.updateLength(counter);
  brighten(0,255, 0);

  if (millis() - inistart >= 2000)
  {
    done++;
  }

  if (done == 0)
  {
    player.play(istAn);
    done++;
  }
  movement();
}
```

Der Code sollte Verständlich genug sein. Falls es fragen gibt, kann man sich jederzeit an mich wenden.

### Schritt 10: Zusammen Bauen.

Wenn die Kabel stehen, gilt es die Boards direkt unter den Kopf zu legen.
{{< figure src="../Nachbau_assets/halterung_unten.jpg" width="auto" height="auto" caption="Die Halterung von unten">}}

Hier ist noch genug Platz um das Board wenigstens Teilweise unterzubringen. Wir können dann die zwei einzelnen teile des Lichtschwerts so zusammenlegen , dass wir den Kopf perfekt reinstecken können

{{< figure src="../Nachbau_assets/Schwert_links.jpg" width="auto" height="auto" caption="Der VS183B und ihr Pinning">}}

{{< figure src="../Nachbau_assets/Schwert_rechts.jpg" width="auto" height="auto" caption="Der VS183B und ihr Pinning">}}

Wie man bei dem Modell sehen kann, sind an den seiten Löcher um dort schrauben durch zu Stecken. Davor müssen wir die Löcher von Innen noch mit Muttern der gleichen Größer zukleben, damit wir die Schrauben auch reindrehen können. Ist die Technik nun verstaut, und die Schrauben drinnen, ist das Lichtschwert so gut wie Fertig.

Wir müssen jetzt noch die PVC-Röhre die wir vorhin geschliffen haben einarbeiten. Diese Drücken wir durch das Äußere Loch.
Jetzt müssen wir nur noch die Schrauben nehmen, und darauf achten, dass wir durch das Holz und der Röhre Bohren. Wir müssen aber drauf achten, dass wir dadurch keine Kabel kaputtmachen.

Wenn auch dies geschafft ist, muss man nur noch die Kappe die wir ganz am Anfang gedruckt haben befestigen. Diese hält durch ein Klickverschluss den ich extra dafür gemacht habe.

Die Stromversorgung wird durch eine Powerbank gesteuert, aber eine 9V Batterie würde das auch schaffen.

### Schritt 11: Sein Lichtschwert bewundern.

Du hast es geschafft dein Lichtschwert zusammen zu Bauen, darauf kannst du Stolz sein! Ich hoffe die Anleitung war verständlich und man konnte jeden Schritt gut folgen. Ich würde dich um ein Feedback bitten. Sei dabei bitte so kritisch wie es geht, damit auch der Post so gut wie möglich wird.


<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons Lizenzvertrag" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Dieses Werk ist lizenziert unter einer <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Namensnennung 4.0 International Lizenz</a>.


