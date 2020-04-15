# Eine andere Seite der Informatik - Java und OpenCV
von Cara Klimmek und Johanna Grahl  
Stormarnschule Ahrensburg  
Klasse 12g  
Schuljahr 2019/2020  

---

## Inhaltsverzeichnis

[Einleitung](#1)

[Android Studio](#2)

[OpenCV](#3)

[Das Projekt](#4)

[Fazit](#5)

---

## Einleitung <a name="1"></a>

Nachdem wir im letzten Halbjahr auf code.org mit JavaScript programmiert hatten, wollten wir uns in diesem Halbjahr mit einem für uns neuen Bereich der Informatik beschäftigen. Die Entscheidungskriterien für unser Projekt hatten wir schnell festgelegt. Wir wollten mit der Programmiersprache Java arbeiten und eine App programmieren. Die App soll auf einem Android Smartphone lauffähig sein. Android hat den Vorteil, dass man Apps ohne Nutzung eines „Stores“ installieren kann. So fiel unsere Wahl auf die Programmierumgebung Android Studio, da dort mit Java gearbeitet wird. 
Wir wollten nicht nur irgendeine App programmieren, sondern eine App, welche Gesichter erkennt. Das automatische Erkennen von Gesichtern ist hochkomplex. Um dieses nicht selbst zu programmieren, wollen wir auf eine vorhandene Bibliothek zurückgreifen. Dies muss eine Bibliothek für eine Bildverarbeitung und Bilderkennung auf Basis von Künstlicher Intelligenz (KI) sein. Unsere Wahl fiel auf OpenCV.
Aufgrund dessen, dass dieses Projekt nicht mit viel eigener Programmierung verbunden ist, liegt unser Fokus in diesem Projekt auf verschiedenen Aspekten:
Im Großen und Ganzen wollen wir eine neue Seite der Informatik kennenlernen. Wir wollen lernen, wie man sich in einer neuen Programmierumgebung zurechtfindet (Android Studio), wie man eine Bibliothek (OpenCV) mit einer Programmierumgebung verbindet und auch nutzt.  Der Großteil unseres Projektes besteht daraus, den Code welchen wir im Internet recherchieren, wieder zu verwenden und zu verstehen.

--- 

## Android Studio <a name="2"></a>

Android Studio ist freie und kostenlose Entwicklungsumgebung von Google, mit der man Android-Apps programmieren kann. Das Grundgerüst für die App wird von Android Studio automatisch generiert, sodass man auf dieser Grundlage schnell Apps selber entwickeln kann.
Obwohl Java als Programmiersprache verwendet wird und Android Studio auf Android-Software ausgelegt ist, kann die Umgebung auch für IOS Systeme von Apple verwendet werden. Allerdings kann man bei IOS Systemen die App nach dem fertigstellen nicht wie bei Android Systemen auf dem gewünschten Ziel-System installieren. Um für Apple Apps zu entwickeln und auf IOS Geräten installieren zu können, müsste man eine Entwicklerlizenz im Apple Store erwerben. Erst dann kann man IOS Apps im Apple Store einstellen und auf seinem IPhone installieren. Alternativ kann man seine IOS App in Android Studios mit Hilfe eines Emulators testen und sich anzeigen lassen. 

Da uns dies zu viel Aufwand ist und wir auch die Möglichkeit mit einem Android Smartphone hatten, haben wir diese genutzt. Um auf einem Android Smartphone eine eigene App installieren zu können, muss man hierzu auf dem Android Smartphone die Entwickleroptionen in den Einstellungen aktivieren und Debugging zulassen. Hierdurch ist es möglich, Apps (ohne den Umweg über einen Store) von einem PC über ein USB-Kabel auf das Android Smartphone zu übertragen.

Wenn man nun ein neues Projekt in Android Studio anfängt, kann man zwischen verschiedenen „*Activitys*“ unterscheiden. Hierbei geht es darum, welche Module die App schon beinhalten sollen:  z.B. eine Navigationsleiste, die sich aufklappen lässt oder dass das Bildschirm-Scrollen schon vorgesehen ist. Dies alles könnte man natürlich auch selber programmieren, über die „*Empty Activity*“. Dies ist eine Vorlage, welche nur eine Leiste mit dem Namen der App oben anzeigt.

# Foto von Android Studio

Nachdem man ein neues Projekt angefangen hat, bietet Android Studio einem viele Hilfestellungen beim Programmieren. So muss man zum Beispiel nicht das gesamte Layout des Bildschirms selber programmieren, sondern kann dies auch durch visuelles einfügen (Drag’n’Drop) von vorhandenen Widgets (Android GUI-Elemente) tun. Neben der Möglichkeit visuell Widget Elemente einzufügen, gibt es in der Entwicklungsumgebung auch eine Ansicht, auf welchem der generierte Java-Source Code angezeigt wird. Prinzipiell ist es möglich, diesen Source Code direkt einzufügen. Die Verwendung von Drag’n’Drop der Widgets ist jedoch schneller und weniger fehleranfällig.
Somit bleibt einem selber die Entscheidung überlassen, wie man programmieren möchte.
GUI-Widgets werden Event-gesteuert programmiert. So liefert das drücken eines Buttons ein Event „*onClick*“ aus. Android Studio zeigt in der Entwicklungsumgebung die von einem Widget unterstützten Events an. Dort kann man Java-Code einfügen, welcher bei Auftreten dieses Events ausgeführt werden soll:

# HIER EIN BILDSCHIRM FOTO, WIE DAS AUSSIEHT

Analog zu Events, kann man so auf Attribute von Widgets lesend und / oder schreibend zugreifen. 
Android Studio generiert automatisch mehrere Dateien, die für die Realisierung der App notwendig sind. Diese sind nicht nur Dateien für Java-Code, sondern können auch andere notwendige Dokumente z.B. in Form von XML-Strukturen sein. 
Zu den generieten Dateien gehört neben der „*activity_main.xml*“ auch die „*MainActivity.java*“, welche beide miteinander verknüpft sind, sodass man hier nur noch die eigenen Aktionen programmieren muss. Mehrere Dateien fasst Android Studio zu einem Projekt zusammen. 

Wichtig für unser Projekt ist, dass man bei Android Studio auch verschiedene Bibliotheken (z.B. OpenCV) zum Programmieren einbinden kann.

---

## OpenCV <a name="3"></a>

OpenCV oder auch Open Source Computer Vision Library, ist eine Open Source-Bibliothek, die frei verfügbar ist und sich jeder runterladen kann. Diese Bibliothek hat ihren Ursprung in der in Bildverarbeitung. Man kann sie in allen Projekten, die sich mit Bildverarbeitung, Video-Bearbeitung beschäftigen, nutzen und unterstützt auch Maschinelles Lernen (eine Form der KI).
Für unser Projekt war die Videoerfassung und das maschinelle Lernen wichtig, da wir die Bibliothek dafür nutzen wollen Gesichter zu erkennen. Die Funktion hierfür ist schon in OpenCV enthalten, sodass wir nur noch rausfinden mussten, wie wir die Funktion auch nutzen können.

Damit man OpenCV in Android Studio integrieren kann, muss man sich die Bibliothek erstmal runterladen. Danach kann man die Bibliothek als ein neues Modul in ein Projekt importieren. Hierbei tritt dann aber immer ein Fehler auf, da OpenCV einen ältere Android SDK Version nutzt, als die, die auf dem Computer installiert ist. Hierfür muss einfach nur die SDK Version im *build.gradle* auf die aktuellste Android SDK Version geändert werden. *Build.gradle* wird von Android Studio verwendet, um den Entwicklungsprozess bestehend aus Java-Code und Bibliotheken eine ausführbare App in Form einer JAR-Datei zu steuern. Nun ist die Bibliothek grundsätzlich im Projekt integriert, allerdings wird sie einem noch nicht angezeigt. Um dies zu erreichen, muss man OpenCV als neues Modul in der Projektstruktur eingebunden werden. Nun kann man die Funktionen von OpenCV in Java nutzen, in dem man entsprechende Import Strukturen zu Beginn des Source Codes angibt. 

---

## Das Projekt <a name="4"></a>

Angefangen haben wir erstmal nur mit Android Studio. Hierfür haben wir uns im Internet verschiedene Tutorials angeschaut und diese nachgebaut. Dadurch haben wir einen guten Überblick über Android Studio bekommen und gelernt wie man dort grundlegend eine App programmieren kann. Nach den Tutorials haben wir uns selber hingesetzt und die Funktionen und Möglichkeiten von Android Studio ausprobiert. Dadurch sind drei kleine Apps entstanden, die wir komplett selber programmiert haben, und damit unser Grundverständnis für Android Studios gefestigt haben.

 <details>
   <summary><h3>TestPassword</h3></summary>

  Bei dieser App geht es darum, dass wir ein festes Passwort programmiert haben, welches man in eine Textbox eingeben muss. Nach abschicken des Passwortes, wird man entweder begrüßt oder einem wird mitgeteilt, dass das Passwort falsch ist.
  
  <details>
    <summary>activity_main.xml</summary>
  
  In der *activity_main_xml* wird immer das Aussehen des Bildschirms bestimmt. Hier haben wir festgelegt, dass wir eine Textbox und einen Senden Button angezeigt bekommen wollen. Diese beiden haben wir durch die Palette auf unseren Beispiel Bildschirm festgelegt. Damit die beiden Felder nicht schlussendlich in die linke obere Ecke „springen“, weil dort der Nullpunkt ist, haben wir sie über die Attribute jeweils mit einem bestimmten Abstand zu den Rändern fixiert. Hierdurch ist es möglich, dass die App auf Android Smartphones mit unterschiedlichen Bildschirmauflösungen laufen kann. 
  
 ![activity_main xml (Textbox)_2_zeichnen](https://user-images.githubusercontent.com/54102292/79379380-25bd3900-7f5f-11ea-8739-b2eafef61742.jpg)
  
  Hier sieht man einmal unsere Textbox mit den verschiedenen Attributen an der rechten Seite. In blau sind einmal alle Attribute gekennzeichnet, welche für die Seitenabstände zuständig sind. *layout_marginTop* gibt den Abstand zum oberen Rand des Bildschirms an, dieser ist bei uns als einziger ein fester Wert, damit die Box von dem Abstand immer gleich ist. Die Abstände zu den beiden Seiten, bzw. zum Senden Button ist nicht mit einem festen, sondern mit einem Minimalwert belegt.Das heißt der Abstand zu einer Seite ist minimal 16, kann aber auch größer sein, wenn der eingegebene Text nicht so lang ist.
Damit diese Funktion auch funktioniert, haben wir die Textbox mit dem Sende Button verknüpft, sodass diese immer den gleichen Abstand zu einander haben. 
Grün markiert ist die ID, bzw. der Name der Textbox, in diesem Falle heißt sie Passwort. Passwort ist eine ID oder Identifier, über welcher im Java-Code auf die Textbox referenziert werden kann. Der Text, der innerhalb der Textbox angezeigt werden soll, wird vom Typ String (gelb) festgelegt, welche in unserem Falle *text_password* heißt. Dieser String zeigt den eigentlichen Text des Passwords in der App an. Die ID (Verweis auf die Textbox) und der String (Verweis auf den Text innerhalb der Textbox) sind direkt mit der Textbox verbunden, sodass man dies beim weitern programmieren nicht immer wieder tun muss.

![activity_main xml (Button)_2_zeichnen](https://user-images.githubusercontent.com/54102292/79379369-1fc75800-7f5f-11ea-811e-622042cafdd3.jpg)

Bei dem Senden Button haben wir die layout-Attribute (blau) genauso gesetzt wie bei der Textbox, damit sich ein einheitliches Bild ergibt und die Felder den gleichen Abstand zu den Seitenrändern haben. Hier gibt es noch zwei zusätzliche layout-Attribute (orange). Diese sind die Verknüpfung von der Textbox und dem Senden Button. Durch diese beiden Attribute wird eine Baseline von dem Senden Button zur Textbox gezogen, sodass diese beiden miteinander verbunden sind.
Auch hier haben wir wieder eine ID (grün) und einen String (gelb). Durch den String wird in der App schlussendlichen Senden angezeigt.
Zum Schluss haben wir noch das Event-Attribut *onClick* (lila). Durch dieses Event-Attribut kann man die *activity_main.xm*l mit der *MainActivity.java* verknüpfen. Dies brauchen wir, damit wenn der Senden Button gedrückt wird, die nächste Seite angezeigt werden kann.

  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  
      public void  OnClickListner (View view){
        EditText Password_eingabe= (EditText) findViewById(R.id.Password);

        if(Password_eingabe.getText().toString().equals("pass")){
            Intent Password_right = new Intent (this, Screen2.class);
            startActivity(Password_right);
        }else{
            Intent Password_wrong = new Intent (this, Screen3.class);
            startActivity(Password_wrong);
        }
    }
    
  *Public void OnClickListner()* ist eine Funktion, die ausgelöst wird, wenn auf den Senden Button gedrückt wird. Hierzu haben wir im Layout Designer beim Attribut *onClick* (violett) die Funktion *OnClickListner()* benannt, welche in der Datei *MainActivity.java* beschrieben wird. In der Funktion selber haben wir dann einen Text definiert, welcher mit dem Text belegt werden sollte, der in die Textbox geschrieben wird (*EditText Passwort_eingabe*). Hierfür haben wir die ID der Textbox mit unserer Textvariablen belegt.
  Für die eigentliche Passwortabfrage haben wir eine *if-else–Abfrage* genutzt. Wir haben definiert, dass sofern die *Passwort_eingabe* gleich dem Wort „pass“ ist, ein neuer Intent erstellt wird. Ein Intent wird dazu verwendet, verschiedene Activities zu verknüpfen. Dieser Intent heißt *Password_right* und über diesen Intent können wir die *MainActivity.java* mit einer anderen Activity verknüpfen. In unserem Falle wird diese mit der *Screen2.java* verknüpft, da dies der Bildschirm für das richtige Passwort ist

      Intent Password_right = new Intent (this, Screen2.class);
  Danach starten wir die Funktion über *startActivity(Password_right)*.
  
  Wenn der eingegebene Text falsch ist, dann wird ebenfalls ein neuer Intent erstellt (*Password_wrong*). Dieser verknüpft die *MainActivity.java* mit der Activity *Screen3.java*.
  
    Intent Password_wrong = new Intent (this, Screen3.class)
 Auch hier starten wir die Activity durch *startActivity(Password_wrong)* ,wodurch der Bildschirm angezeigt wird, wenn das Passwort falsch ist.
  
  </details>
  
  <details>
  <summary>activity_screen2.xml</summary>
  
 ![activity_Screen2 xml_2_zeichnen](https://user-images.githubusercontent.com/54102292/79379416-34a3eb80-7f5f-11ea-90aa-ce062bcf5a52.jpg)
  
  Auch hier haben wir die Seitenbegrenzungen (blau) genauso wie bei der *main_activity.xml* festgelegt. Genauso haben wir die ID mit einem entsprechenden Namen festgelegt und einen String für das Textfeld erstellt und damit verknüpft. So dass man zum Schluss auf dem Bildschirm nur den Schriftzug „*Hallo*“ erkennt.
  
  </details>
  
  <details>
  <summary>Screen2.java</summary>
  
      protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_screen2);
        Intent Password_right = getIntent();
    }
 
 Hier haben wir in die allgemeine Funktion, welche durch Android Studio automatisch erstellt wird, einen Intent erstellt. Hierdurch wird sichergestellt, dass der Intent von *MainActivity.java* verknüpft wird, so dass der Bildschirm *activity_screen2.xml* aktiviert und angezeigt wird.
  
  </details>
  
  <details>
  <summary>activity_screen3.xml</summary>

 ![activity_screen3 xml_2_zeichnen](https://user-images.githubusercontent.com/54102292/79379465-3ff71700-7f5f-11ea-9640-9c7fd3ebafe4.jpg)
 
  Bei der *activity_screen3.xml* haben wir die gleichen Einstellungen wie bei Screen2, da dies beide die Antwort-Bildschirme sind für das Passwort. Der einzige Unterschied den wir hier haben, dass wir einen anderen String (gelb) mit der Textbox verknüpft. Dieser String gibt den Text „*Your Password is wrong*“ aus.
  
  </details>
  
  <details>
  <summary>Screen3.java</summary>
  
      protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_screen3);
        Intent Password_wrong = getIntent();
    }
    
  Auch hier haben wir das gleiche gemacht wie bei Screen2. Das heißt wir haben nur die vorgegebene Funktion angepasst, indem wir gesagt haben das Intent von *MainActivity.java* ankommen soll. Dadurch wird dann der Bildschirm von *activity_screen3.xml* angezeigt.
  
  </details>
  
  <details>
 <summary>Die App</summary>
 
 ![GIF_TestPassword2](https://user-images.githubusercontent.com/54102292/79378505-c27ed700-7f5d-11ea-9f0a-9caeca990701.gif)

 </details>
 
  ---
  
</details> 

<details>
 <summary><h3>TestPasswordandUsername</h3></summary>
  
  Die App TestPasswordandUsername ist die erweiterte Version von der App TestPassword2. Wir haben sie in dem Sinne erweitert, dass wir zu dem Passwort noch einen Benutzter Namen hinzugefügt haben. Beides ist wie in der App TestPassword fest programmiert, das heißt man kann es nur im Code ändern und nicht beim Benutzten der App festlegen.
  
  <details>
  <summary>activity_main.xml</summary>
  
 ![activity_main xml_2_zeichnen](https://user-images.githubusercontent.com/54102292/79380195-610c3780-7f60-11ea-9697-512e0d8fc853.jpg)

  
  Dadurch ist der Code auch überwiegend gleich, bis auf das wir in der *activity_main.xml* noch ein weiteres Textfeld für den Benutzer Namen eingefügt haben und dieses Textfeld mit einem String (gelb) verknüpft haben, damit auf dem Bildschirm Username steht.
Die Layoutbegrenzungen und Abstände (blau) sind gleichgeblieben und die ID (grün) haben wir entsprechend des Textfeldes gewählt.

  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  
        public void  OnClickListner (View view){
        EditText Password_eingabe= (EditText) findViewById(R.id.Password);

        if(Password_eingabe.getText().toString().equals("pass")){
            Intent Password_right = new Intent (this, Screen2.class);
            startActivity(Password_right);
        }else{
            Intent Password_wrong = new Intent (this, Screen3.class);
            startActivity(Password_wrong);
        }
    }
  In der MainActivity.java hat sich im Vergleich zur App TestPassword am meisten verändert. Hier haben wir ebenfalls eine neue Funktion *public void OnClickListner()* programmiert, der die Verbindung zum Senden Button darstellt. Auch hier haben wir wieder einen Text erstellt, für die jeweiligen Textfelder. Also über die IDs der beiden Textfelder die Texte *Username_eingabe* und *Password_eingabe* verknüpft.
  
  Genauso wie bei TestPassword2 haben wir eine *if-else – Abfrage* programmiert. Diesmal allerdings mit der Voraussetzung, dass der Benutzername “*gleich*“ Johanna ist und auch die Bedingung (Passwort „*gleich*“ jojo) erfüllt sein muss.

Wenn diese beiden Bedingungen erfüllt sind, wird wieder ein neuer Intent erstellt, welcher zum *Screen2.java* führt, wodurch dann der zweite Bildschirm angezeigt wird. Dieser ist genau gleich zu dem zweiten Bildschirm aus der TestPassword-App.

Ist eine der beiden Bedingungen nicht erfüllt, wird ein Intent erstellt, wodurch *Screen3.java* aktiviert wird und man den dritten Bildschirm sieht. Dieser gleicht fast dem aus der App TestPassword, bis auf das dort steht „*Your Password or Username is wrong*“.

  </details>
  
  <details>
 <summary>Die App</summary>
 
 ![GIF_TestPasswordandUsername](https://user-images.githubusercontent.com/54102292/79380212-679aaf00-7f60-11ea-85b4-ea242c0c2008.gif)
 
 </details>
  ---
  
</details>

<details>
 <summary><h3>Dumme Sprüche</h3></summary>
  
  Unsere letzte App die wir programmiert haben, bevor wir OpenCV mit eingebunden haben, ist die App „Dumme Sprüche“. Die App ist angelehnt an schon existierende Apps, wo man auf Buttons klicken kann und dann verschiedene Sounds ertönen. Dies wollten wir als „Abschluss“ nachprogrammieren, nur mit verschiedenen Sprüchen. 

Dafür haben wir uns 8 verschiedene Sprüche rausgesucht und mit 8 passenden Bilder, die wir als Buttons benutzten wollen, verknüpft.
 
  <details>
  <summary>activity_main.xml</summary>
  
  # Bild 
  
  Das ist der Bildschirm, den man sieht, wenn man die App geöffnet hat. Jedes der acht Rechtecke stellt ein Bild (Icon) dar, welches als Button fungiert. Somit haben wir für jedes Bild die gleichen Attribute. Das heißt die Layout-Attribute (blau) sind alle so eingestellt, dass die Bilder nicht auf den 0-Punkt springen, sondern in einer Reihe bleiben. Alle Bilder die senkrecht in einer Reihe sind, sind untereinander verbunden, sodass sie alle denselben Abstand haben. Auch zu den Seitenrändern haben alle Bilder den gleichen Abstand, damit wir ein einheitliches Bild zum Schluss haben. 
Jedes Bild hat eine eigene ID (grün), entsprechend zum Spruch. Im Bild sieht man, dass dieses Bild einen Spruch mit Darth Vader enthält, weswegen die ID *darth_vader* heißt.
Ebenso ist jedes Bild mit dem Attribut *onClick* belegt, damit wir das Bild in der MainActivity.java mit einem Spruch verknüpfen können.

# Bild 

Um die Bilder in Android Studio einfügen zu können, muss man die Bilder in den Ressourcen (*res*) unter *drawable* (Ordner für alle graphischen Dateien) einfügen. Danach kann man die Bilder über das Bild-Widget einfügen und die Attribute festlegen. 

  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  
  Damit wir die Bilder auch mit einem Spruch, also einer Audio-Datei verknüpfen konnten, mussten wir diese erstmal in Android Studio einfügen.
  
  # Bild 
  
  Dies hat man, ähnlich wie die Bilder, über die Ressourcen in den *raw*-Ordner eingefügt. Hierbei muss man aber drauf achten, dass das Format der Audio-Datei auch unterstützt wird.
  
       MediaPlayer icon = new MediaPlayer();
    public void onClick(View view) {

        ImageView darth_vader = (ImageView) findViewById(R.id.darth_vader);
        if (view.equals(darth_vader)) {
            icon.stop();
            icon = MediaPlayer.create(this, R.raw.darth_vader);
            icon.start();
        }
     }
 So wurden alle Bilder mit einer Audiodatei und dem Medienplayer verbunden.
 
 Damit man die Audio-Dateien auch abspielen kann, haben wir als erstes einen *MedienPlayer* erstellt. Diesen haben wir *icon* genannt und können diesen in für alle Bilder/Sprüche verwenden. 

Da wir jedem Bild das Attribut *onClick* erstellt haben, konnten wir dies nun in unsere *onClick*-Funktion *public void onClick()* verwenden. Das heißt wenn auf ein Bild geklickt wird, wird diese Funktion aufgerufen.

Innerhalb dieser Funktion haben wir es für die Bilder jeweils ein *ImageView* mit einem Bild über die ID verknüpft (*ImageView darth_vader = (ImageView) findViewById(R.id.darth_vader)*). Um zu verhindern, dass bei jedem Drücken des Icons jeweils der Media Player gestartet wird, stellen wir in einer *if-Abfrage* sicher, dass der MediaPlayer ggfs. zuerst gestoppt wird.
Außerdem startet ein neuer Medienplayer entsprechend zum Bild
(*icon = MedienPlayer.create (this, R.raw.darth_vader)*). Hierbei wird auf die Audiodatei zugegriffen, welche wir vorher in den Ressourcen im *raw*-Ordner gespeichert haben. Zum Schluss wird der Medienplayer dann jeweils noch gestartet.

  </details>
  
  ---
  
</details>

Nachdem wir uns sicher im Umgang mit Android Studio fühlten und einige eigene Apps programmiert haben, haben wir den nächsten Schritt zum Endziel gemacht. Wir haben uns die Bibliothek OpenCV runtergeladen und mit Hilfe eines Tutorials diese in OpenCV eingebunden. 

Danach kam die nächste Hürde für uns: Für unsere App brauchten wir die Kamera. Deswegen recherchierten wir im Internet, wo wir schlussendlich auf YouTube einige gute Tutorials gefunden haben, die einem erklärt haben, wie man die Kamera in eine App einbinden kann. Da es bei OpenCV eine falsche Ausrichtung der Kamera gibt, wird diese einem immer um 90° gedreht angezeigt. Somit hatten wir bei unser ersten Testapp mit OpenCV schon Probleme mit der Kameraausrichtung, die wir aber nach einer weiteren Internetrecherche gut beheben konnten, sodass die Kamera richtig ausgerichtet war.
Nun hatten wir es geschafft die Kamera anzeigen zulassen, allerdings hatten wir noch keine Funktionen für die Gesichtserkennung. Deswegen folgte wieder eine langdauernde Recherche im Internet, wo wir dann auch fündig geworden sind und eine gute Vorlage für unsere App Face_Detection hatten. 
Im zweiten Teil des Projektes haben wir nichts mehr selber programmiert, sondern Codes aus dem Internet genutzt. Allerdings lag hier das Hauptaugenmerk darauf, dass wir diese Codes verstehen und daraus lernen wie eine solche App aufgebaut ist und wie man Bibliotheken wie OpenCV richtig nutzt.

<details>
 <summary><h3>Face_Detection</h3></summary>
  
  Diesen Code haben wir nicht selber programmiert, sondern im Internet recherchiert und genutzt um die App zu bauen. 
Damit die Kamera auch angezeigt werden kann, muss in dem Manifest der App die Erlaubnis erteilt sein, die Kamera anzuzeigen   
(*uses-permission android:name="android.permission.CAMERA"*).

  <details>
  <summary>activity_main.xml</summary>
  
  Anders als in den vorherigen Apps, haben wir das Layout bzw. die Kamera, diesmal nicht über das Designtool von Android Studio programmiert, sondern über das Texttool. 
        
        <org.opencv.android.JavaCameraView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:id="@+id/myCameraView"
        app:show_fps="true"
        />
        
  Hierbei wird die Kamera durch das Layout über den gesamten Bildschirm angezeigt (*layout_width = „match_parent“*). Ebenfalls wird eine ID der Kamera zugefügt, sodass man sie später in der MainActivity.java verknüpfen kann. Weiterhin wurde festgelegt, dass eine textuelle Anzeige über die Anzahl der Bilder pro Sekunde innerhalb des Kamerabildes angezeigt werden soll. (*show_fps =“true“*).
  
  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  
     private BaseLoaderCallback mLoaderCallback = new BaseLoaderCallback(this) {
        
        public void onManagerConnected(int status) {
            switch (status) {
                case LoaderCallbackInterface.SUCCESS:
                    initializeOpenCVDependencies();
                    break;
                default:
                    super.onManagerConnected(status);
                    break;
            }
        }
    }
    
   
ä
       
       private void initializeOpenCVDependencies() {

        try {
            // Copy the resource into a temp file so OpenCV can load it
            InputStream is = getResources().openRawResource(R.raw.lbpcascade_frontalface);
            File cascadeDir = getDir("cascade", Context.MODE_PRIVATE);
            File mCascadeFile = new File(cascadeDir, "lbpcascade_frontalface.xml");
            FileOutputStream os = new FileOutputStream(mCascadeFile);
            Log.e("OpenCVActivity", "input stream 1");

            // Load the cascade classifier
            cascadeClassifier = new CascadeClassifier(mCascadeFile.getAbsolutePath());
        } catch (Exception e) {
            Log.e("OpenCVActivity", "Error loading cascade", e);
        }
        
        // And we are ready to go
        openCvCameraView.enableView();
    }

  Als Schnittstelle zwischen den Daten der Kamera und OpenCV wird der *BaseLoaderCallback* genutzt. Dieses ist ein Video-Stream (Datenstrom). OpenCV kann aus diesem Video-Stream die einzelnen Bilder der Kamera extrahieren, um diese dann bildweise analysieren zu können.
Nach erfolgreicher Initialisierung von *BaseLoaderCallback* wird die *initializeOpenCVDependencies()* initialisiert. Hierbei wird dem *InputStream* verwiesen, wo die Daten der Kamera sind. OpenCV kann den *InputStream* analysieren und automatisch Gesichter erkennen. Dieses wird über *lbpcascade_frontalface.xml* definiert.
Im Anschluss wird der analysierte Stream mit *FileOutputStream()* verknüpft, um das Video auf dem Bildschirm anzuzeigen.  

      openCvCameraView = new JavaCameraView(this, -1);
        setContentView(openCvCameraView);
        openCvCameraView.setCvCameraViewListener(this);
        
  In einer weiteren Funktion wird die Java-Kamera, welche in der *activity_main.xml* programmiert wurde, als die OpenCV Kamera definiert. Wobei ebenfalls ein *CameraViewListner* auf die Kamera gesetzt wird.
  
  In der letzten Funktion, passiert die eigentliche Gesichtserkennung. Als erstes wird das einzelne Bild in Graustufen (*greyscale*) umgewandelt. Dieses wird dann in den *CascadeClassifier* eingebunden und auf Gesichter untersucht. Wenn Gesichter gefunden werden, wird ein grünes Rechteck in Größe des Gesichtes um das Gesicht eingeblendet. Zum Schluss wird ein Bild wieder zurückgegeben, sodass auf dem Bildschirm in der App auch das Rechteck zu sehen ist.
  
  </details>
  
</details>

---

## Fazit <a name="5"></a>

Abschließend kann man zu diesem Projekt sagen, dass es uns sehr viel Spaß gemacht hat und wir sehr viel Neues gelernt haben. Und dies nicht nur darauf bezogen, dass wir gelernt haben Apps zu programmieren. Sondern auch darauf, wie man Code im Internet richtig recherchiert und diesen dann auch versteht. Deswegen heißt es ja auch: Copy Right 
Es hat uns auch gezeigt, was man sich gut selber beibringen kann, wie zum Beispiel das Programmieren eigener kleiner App. Hierfür brauchte man keine Vorkenntnisse. Mit genügen Zeit und Interesse konnten wir uns das sehr gut selber beibringen. 
Allerdings haben wir auch gemerkt, wo man als Anfänger an seine Grenzen kommt. Unsere ersten Pläne und Ziele für unsere App waren für uns zu hochgesteckt, sodass wir diese im Laufe der Zeit unseren Fähigkeiten und unserem Zeitraum anpassen mussten. Trotzdem sind wir sehr zufrieden mit unserem Endergebnis, und sind froh darüber, dass wir dieses Projekt, trotz mancher Schwierigkeiten, durchgezogen haben.
