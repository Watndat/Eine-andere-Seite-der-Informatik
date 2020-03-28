# Eine andere Seite der Informatik - Java und OpenCV
von Cara Klimmek und Johanna Grahl  
Stormarnschule Ahrensburg  
Klasse 12g  
Schuljahr 2019/2020  


Einleitung:
-  wie haben wir uns für das Projekt entschieden
- was wollen wir damit lernen / Intention warum wir das gemacht haben
-> wollten was anderes machen, als ein Spiel programmieren und JavaScript 
-> wollten expliziet Java lernen und uns damit beschäftigen wie man eine app programmiert
-> lernen, wie man mit einer Bibliothek arbeitet und diese mit der Programmierumgebung verknüpft



























































## Inhaltsverzeichnis

<details>
    <summary>Projektbeschreibung</summary>
    
[Unser Projekt](#1)
</details>

<details>
    <summary>Programmierumgebung und OpenCV</summary>

[Android Studios](#2)

[OpenCV](#2.5)
</details>

<details>
    <summary>AndroidStudios</summary>
    
[My first App](#3)
   
[Test_2](#4)

[Test_3](#5)

[Test_Password](#6)

[TestPassword2](#7)

[TestPasswordandUsername](#8)

[Dumme Srprüche](#9)
    </details>
    
<details>
    <summary>OpenCv</summary>
    
[Test_OpenCv](#11)

[Display_Camera_2](#12)

[Face_Detection](#13)
</details>

<details>
    <summary>Ein paar nette Worte zum Schluss</summary>
    
[Schlusswort](#14)
    </details>
    
### Android Studios <a name="2"></a>

Android Studios ist ein Programm mit dem jeder eigene Apps für Android Handys programmieren kann. Aufh Appel nutzer können damit arbeiten, das man sich eine Vorschau der App anzeigen lassen kann. Das Programm hat eine auf JetBrains IntelliJ IDEA basierte Software und setzt dementsprechend auf Java als Programmiersprache.

---

### OpenCV <a name="2.5"></a>

Open CV ist eine öffentliche Bibliothek, die für Programmierer geschaffen wurde.

---

### Unser Projekt <a name="1"></a>

Nach dem wir im letzten Halbjahr über Code.org ein eigenes Spiel programmiert hatten und dadurch JavaScript als Programmiersprache kennengelernt hatten, wollten wir uns dieses Halbjahr an was neuem probieren. 
Wie programmiert man mit Java? Wie arbeitet man mit einer neuen Programmierumgebung und erstellt Apps? Und zu guter letzt noch wie arbeitet man mit einer Bibliothek?
All diese Frage bilden unser Projekt fürs zweite Halbjahr. Ein Halbjahr wo wir viel lernen wollen, um die unterschiedlichen Seiten der Informatik kennenzulernen.
Begonnen haben wir mit AndroidStudios und haben dort einige Apps erst durch Tutorials programmiert und später dann selber. Als wir uns sicher genung mit AndroidStudios fühlten und wir Java auch gut verstanden haben, sind wir zum zweitern und deutlich schwierigern Teil unseres Lernprozesses übergegangen. Wir haben die Bibliothek OpenCV in AndroidStudios eingbunden. Um mit der Bibliothek zu arbeiten, haben wir uns überlegt eine App zubauen, welche Gesichter erkennt. Die Funtkionen dafür sind in der Bibliothek schon vorhanden. Hierbei müssen wir nur lernen, wie wir diese Funktionen aus der Bibliothek aufrufen und Code aus dem Internet raussuchen und verwenden können, damit die App am Ende auch funktioniert.

---

## AndroidStudios


### My first App <a name="3"></a>

(Test_2)
Dies ist die erste App welche wir programmiert haben. Hierbei sind wir einem Tutorial
(https://developer.android.com/training/basics/firstapp ) gefolgt, mit dem wir "Hello World" programmiert haben. Hierbei haben wir auch den ersten Überblick bekommen, wie AndroidStudios aufgebaut ist. Diese App wurde im Tutorial soweit von Hello World umprogrammiert, dass wir ein Textfeld am Ende hatten, in den man eine Nachricht eingeben konnten. Danach konnte man auf Senden drücken, um die eingetippte Nachricht auf dem Bildschirm anzeigen zulassen. 

BILD DER APP (Videos)

CODE -> hierbei haben wir die onClick funktion kennengelernt und nichts selber gelernt, weil Tutorial

<details>
    <summary>activity_main.xml</summary>
     Hier haben wir durch die Widgets die zwei Felder "Write a message" und der "Send" Button auf den Bildschirm eingefügt. Diese haben wir dann miteinander und mit den Ränder verknüpft, damit diese nicht auf auf den Ursprung also 0/0/0 (oben links in der Ecke) springen.
Außerdem haben wir beim "Send" Button die Aktion onClick definiert. Diese haben wir mit sendMessage belegt, welche die Verknüpfung zu MainActivity.java darstellt. 
    
![MyfirstApp_1](https://user-images.githubusercontent.com/54102292/74930037-15fcfa80-53dd-11ea-9a7a-d4f30fe29c1f.png)

(Bild von activity_main.xml)
</details>

<details>
    <summary>MainActivity.java</summary>
In der MainActivity.java ist die Verknüpfung zwischen dem Bildschirm, also was der Nutzer bei der App sieht, und den Aktionen die in unserem Fall zum Beipsiel aus dem Send-Button besteht.
    Da wir im activity_main.xml den Button mit onClick sendMessage belegt haben, wird dies in der MainActivity.java ausgeführt. Dies wird in einer öffentlichen Klasse (public class) ausgeführt. Diese ist die allgemeine Klasse, welche alle zugreifen können, und nicht geschützt ist. 
In der allgemeinen public class, in der alle anderen Funktionen sind, haben wir die sendMessage Funktion auch als public void definert. Diese hat den Name sendMessage, damit dieser mit dem Send Button verknüpft ist.
Als erstes haben wir einen neuen Intent erstellt. Diesen brauchen wir um dieses Activity (MainActivity) mit einer zweiten Activity (NewScreen) zuverknüpfen, wo später der eingegebene Text angezeigt wird.
Um den Text zu erkennen, welcher eingegeben werden kann, wird der Text einmal als editText definiert. Dieser wird über findViewById mit dem Text belegt, welcher eingegeben wurde. 
Um den Text an die andere Activity übergeben zu können, wurde mit dem String message gesagt, das der Text zum String gebracht werden soll. Um die message dann zum Intent gebracht wird, welcher mit der Activity NewScreen verknüpft ist. 
Mit startActivity wird die ganze Aktion gestartet.
    
    public void sendMessage (View view){
        Intent intent = new Intent(this, NewScreen.class);
        EditText editText = (EditText) findViewById(R.id.editText);
        String message = editText.getText().toString();
        intent.putExtra(EXTRA_MESSAGE, message);
        startActivity(intent);
    
</details>

<details>
    <summary>/activity_new_screen.xml</summary>
    
    
    
</details>
    
<details>
    <summary>NewScreen.java</summary>
    
    
 </details>
 
 ---
 
### TestPassword2 <a name="7"></a>
...
BILDER DER APP
CODE -> was haben wir gelernt und was haben wir selber geschrieben

---

### TestPasswortandUsername <a name="8"></a>
...
BILDER DER APP
CODE -> was haben wir gelernt und was haben wir selber geschrieben

---

### Dumme Sprüche <a name="9"></a>
...
BILDER DER APP
CODE -> was haben wir gelernt und was haben wir selber geschrieben

---

## OpenCV

### Test_OpenCV <a name="11"></a>
...
BILDER DER APP
CODE-> was haben wir gelernt und was haben wir selber geschrieben

---

### Display_Camera_2 <a name="12"></a>
...
BILDER DER APP
CODE -> was haben wir gelernt und was haben wir selber geschrieben

---

### Face_Detection <a name="13"></a>
...
BILDER DER APP
CODE -> was haben wir gelernt und was haben wir selber geschrieben

---

## Schlusswort <a name="14"></a>

Abschließend können wir zu unserem Projekt sagen, dass es uns sehr viel Spaß gemacht hat. Dabei haben wir viel gelernt und nochmal einen weiteren Teil der Informatik kennengelernt. Allerdings muss man sagen, dass vielleicht der letzte Teil des Projektes mit dem Face_Detection zu schwierig für Anfänger wie uns war. Trotzdem muss man auch da sagen, obwohl dieser Teil des Projektes aus viel Code aus dem Internet raussuchen und verstehen bestand und dies oft Stunden in Anspruch genommen hat und man nicht wirklich das Gefühl hatte, das man etwas schaffen würde, hatten wir auch daran sehr viel Spaß. Und dieses Projekt hat uns gezeigt wie viel Schichtig die Informatik ansich ist und das man nicht nur stumm vorsich hin programmiert, sondern auch viel mit Recherche und verstehen zutun hat.


















































# Projektbeschreibung

[Die Idee!]

[Das Programm]

[Der Weg zur App]

[Die App]

[Schlusswort]

## Die Idee <a name="1"></a>

Nach dem wir im letzten Halbjahr auf Code.org mit JavaScript programmiert hatten, wollten wir uns dieses Halbjahr mit einem für uns neuen Bereich der Informatik beschäftigen. Hierbei liegt der Fokus nicht auf dem selberprogrammieren, sondern eine neue Programmierumgebung (Android Studios) kennenzulernen. Aber auch mit einer neuen Programmiersprache zurechtzukommen (Java) und eine Bibliothek (OpenCV) zuverstehen und diese in das Programm mit einzubinden. 
So kamen wir auf die Idee eine App mit Gesichtserkennung zuprogrammieren im bestenfalle so sie die Gesichter auch benennen können. Da wir diesen Code natürlich nicht selber schreiben könne, besteht dieses Projekt viel aus einzelne Codestücke im Internet finden und zu verstehen, sowie die einzelne unterschiedlichen Codestücke zusammenzusetzten.
Aufgrunddessen, dass wir voher noch nie mit Android Studios gearbeitet haben, begann unser zweites Halbjahr damit erstmal kleinere Apps in Android Studios zuerstellen und somit die Programierumgebung kennenzulernen. In diesem Zuge sind dann kleinere Apps entstanden wie "Hello World" oder auch Apps wo man eine Nachricht schreiben kann, die dann widerum auf dem Bildschirm angezeigt wird. Auch haben wir uns damit beschäftig wie man ein Passwort in einer App setzt, mit Benutzername und Passwort.
Der nächste Schritt um unserem Ziel näher zukommen, war OpenCV als Bibliothek in Android Studios zu integrieren. Dafür haben wir uns im Internet verschiedene Tutorials angeschaut, bis wir schließlich eins gefunden haben, um mit diesem dann auch ein Beispielprojekt ausprobieren zukönnen. Nachdem dies alles funktionierte musste wir natürlich auch verstehen, was wir dort eigentlich gemacht hatten. Darausfolgte das wir den Code für uns auseinander genommen haben und angefangen haben Stück für Stück den Code zuverstehen. 
Nachdem wir unser Beispielprojekt aus dem Tutorial verstanden hatten, wollten wir nun endlich mit unserem eigentlich Projekt anfangen. Darausfolgte das wir uns entschieden ersteinmal rauszufinden, wie wir die Kamera in unserer App anzeigen können. Auch hier haben wir uns im Internet für uns geigneten Code rausgesucht und diesen kopiert. Darauf folgte wieder eine lange Zeit wo wir den Code verstehen mussten, da hierbei auch schon die Bibliothek OpenCV verwendet wurde. 

Wir haben mit Android Studios gearbeitet. Eine Entwicklungsumgebung, die einem eine App generiert, welche man dann nach seinen Wünschen programmieren kann. 
So haben wir angefangen mit einem "Hello World", einem Tutorial welches man meistens zu Beginn einmal fertigstellt. Durch verschiedene Vorgaben an Buttons und Textfeldern, welche man theoretisch gesehen auch selber programmieren könnte, kann man erste eigene Apps entwickeln. Begonnen haben wir erstmal mit einer App angefangen, wo man einen Text eingibt und diesen dann durch senden auf dem Bildschirm anzeigen lässt. Dadurch lernt man die verschiedenen Seiten (MainActivity.xml und MainActivity.java) kennen und lernt wo was programmiert wird. Dadruch



Plan: 
- Cara: Design Icon
- Jojo: Kamera drehen; Java durchlesen

Fokus:
- anderer Bereich Informatik 
-> wie arbeitet man mit Java und Entwicklungsentgebung (Apps vom Anfang und dort erklären was wir dort selber gemacht haben, vielleicht auch Dumme Sprüche)
-> wie arbeitet man mit einer Bibliothek 
-> wie findet man code im Internet
=> über anfangsapps zeigen wie man sich damti auseinandergesetzt hat.


## Das Programm <a name="2"></a>

## Der Weg zur App <a name="3"></a>

1. My first App (Hello World, was schreiben und dann schicken das steht dann da)
    Um Android Studios kennen zulernen und erste App per tutorial programmmiert
2. Passwort (TestPassword2)
    Weiter an Android Studios gearbeitet, und selber durch geklickt und anfgefangen Apps selber zu programmieren. Angefangen mit       Passwort festlegen und dann zwei Screens danach einmal mit Hallo anderes mit "Your Password is wrong"
3. Username + Passwort (TestPasswortundUsername)
    Immer noch mit Android Studios gearbeitet, selber beigebracht wie man Username und Passwort programmiert
4. Dumme Sprüche (komplett selber, Weihnachten)
    Bevor man mit OpenCv angfängt, nochmal eine App selber programmiert. Bilder eingefügt, wenn man auf die klickt, wird eine Audiodatei abgespielt. Wenn man auf den nächsten drückt, wird die vorherige datei gestoppt und die neue wird abgespielt. Hierbei haben wir gelernt, wie man Appicon und farben in der App die voher voreingestellt waren ändern kann.
5. Beispiel OpenCV (Test_OpenCV -> vom Tutorial Farben erkennen)
    Tutorial wie 
6. Kamera anzeigen (Display_Camera_2 -> Inder)

## Die App <a name="4"></a>

6. Gesichter erkennen (Face_Detection -> Internet)


## Schlusswort <a name="5"></a>

