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

---

## Das Projekt <a name="4"></a>

<details>
  <summary>TestPassword</summary>
  
  <details>
  <summary>activity_main.xml</summary>
  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  </details>
  
  <details>
  <summary>activity_screen2.xml</summary>
  </details>
  
  <details>
  <summary>Screen2.java</summary>
  </details>
  
  <details>
  <summary>activity_screen3.xml</summary>
  </details>
  
  <details>
  <summary>Screen3.java</summary>
  </details>
  
</details>

<details>
  <summary>TestPasswordandUsername</summary>
  
  <details>
  <summary>activity_main.xml</summary>
  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  </details>
  
</details>

<details>
  <summary>Dumme Sprüche</summary>
  
  <details>
  <summary>activity_main.xml</summary>
  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  </details>
  
</details>

<details>
  <summary>Face_Detection</summary>
  
  <details>
  <summary>activity_main.xml</summary>
  </details>
  
  <details>
  <summary>MainActivity.java</summary>
  </details>
  
</details>

---

## Fazit <a name="5"></a>
