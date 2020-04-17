# Tutorial BB26 Psychophysik



## 1. Einführung





## 2. Oracle VM VirtualBox Manager 

Als Software wird für die BB26-Versuche lediglich der Oracle VM VirtualBox Manager benötigt. 
Dies ist ein praktisches Open Source-Tool, mit dem weitere Betriebssysteme in einer virtuellen Umgebung auf dem PC geladen werden können. So auch unser bereitgestelltes **Image** (.iso), in welchem bereits alle notwendigen Treiber & Software für die BB26-Versuche enthalten sind.



### 2.1 Download

VirtualBox ist für Windows/Mac/Linux unter folgendem Link verfügbar :
https://www.virtualbox.org/wiki/Downloads

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\A_01_VirtualBox_Download.jpg" alt="A_01_VirtualBox_Download" style="zoom: 33%;" />



### 2.2 Installation

Nach dem Download gestaltet sich die **Installation** nicht weiter kompliziert, die **Voreinstellungen** können dabei einfach übernommen werden. Beispielhaft wird im Folgenden die Installation auf Windows dargestellt:

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\A_02_VirtualBox_Installation_a.jpg" alt="A_02_VirtualBox_Installation_a" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\A_02_VirtualBox_Installation_b.jpg" alt="A_02_VirtualBox_Installation_b" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\A_02_VirtualBox_Installation_c.jpg" alt="A_02_VirtualBox_Installation_c" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\A_02_VirtualBox_Installation_d.jpg" alt="A_02_VirtualBox_Installation_d" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\A_02_VirtualBox_Installation_e.jpg" alt="A_02_VirtualBox_Installation_e" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\A_02_VirtualBox_Installation_f.jpg" alt="A_02_VirtualBox_Installation_f" style="zoom:33%;" />





### 2.3 Erstellen einer Virtuellen Maschine

Um unser Image nun laden zu können, müssen wir zunächst eine virtuelle Maschine erzeugen.
Dafür einfach auf den Button **"Neu"** klicken...

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\B_01_Neu.jpg" alt="B_01_Neu" style="zoom:33%;" />





Im nächsten Fenster vergeben wir einen geeigneten Namen für unsere virtuelle Maschine und legen fest, welchen **Typ** (Linux) und **Version** (Debian 64-bit) unser virtuelles Betriebssystem haben soll.
Die **Speichergröße** (RAM) wird zunächst auf 2048 MB festgelegt, kann aber je nach verfügbarer Hardware verkleinert/vergrößert werden.
Zuletzt setzen wir noch den Punkt **"Festplatte erzeugen"** und drücken den Button **"Erzeugen"**.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\B_02_VM_erzeugen.jpg" alt="B_02_VM_erzeugen" style="zoom:33%;" />





Anschließend müssen wir im nächsten Fenster den **Dateipfad** zu unserem Image angeben.
Die **Dateigröße** lassen wir auf max. 8,00 GB, auch **Dateityp der Festplatte** und **Art der Speicherung** kann auf den Voreinstellungen belassen werden. Wieder drücken wir auf den Button **"Erzeugen"**.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\B_03_VirtuelleFestplatte.jpg" alt="B_03_VirtuelleFestplatte" style="zoom:33%;" />





Damit ist nun unsere virtuelle Maschine fertig. Wenn alles funktioniert hat, sollte die Ansicht ungefähr so ausschauen:

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\B_04_Image_laden_a.jpg" alt="B_04_Image_laden_a" style="zoom:33%;" />





Falls unter dem Punkt **"Massenspeicher"** bei **"[Optisches Laufwerk]"** immer noch **"leer"** steht, sollte noch einmal unser Image als Abbild ausgewählt werden.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\B_04_Image_laden_b.jpg" alt="B_04_Image_laden_b" style="zoom:33%;" />





Um die virtuelle Maschine zu starten, klicken wir auf den Button **"Start"**.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\B_05_Image_starten.jpg" alt="B_05_Image_starten" style="zoom:33%;" />





## 3. Debian

Um das System zu hochzufahren, wählen wir im Bootmenü den Unterpunkt **"live"** aus. 

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\C_00_LiveSystem_Staten.jpg" alt="C_00_LiveSystem_Staten" style="zoom:33%;" />





Nach kurzer Wartezeit sollte dann der Desktop erscheinen. Hier sehen wir, dass bereits ein Ordner **"BB26 (2019)"** verfügbar ist. Darin sind alle relevanten Dateien enthalten.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\C_01_Desktop.jpg" alt="C_01_Desktop" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\C_02_BB26-Folder.jpg" alt="C_02_BB26-Folder" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\C_03_Psychophysik-Folder.jpg" alt="C_03_Psychophysik-Folder" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\C_04_Psychophysik[2020]-Folder.jpg" alt="C_04_Psychophysik[2020]-Folder" style="zoom:33%;" />





## 4. GNU Octave

Im Psychophysik-Versuch arbeiten wir mit der Datenanalyse-Software GNU Octave. 
Um Octave zu starten, gehen wir im **Applications Menu** (links oben) auf den Reiter **Education** und klicken auf die **GNU Octave-App**.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\D_00_Octave_starten.jpg" alt="D_00_Octave_starten" style="zoom:33%;" />





### 4.1 Octave Oberfläche

Nach dem Start von Octave erscheint die Octave-**Oberfläche**, welche aus mehreren Fenstern besteht:

- *Command Window*: das größte, schwarz hinterlegte Feld in der Mitte; 
  dieses dient einerseits als Eingabefenster, um Befehle, Funktionen und Skripte auszuführen; andererseits werden deren Ergebnisse in diesem Fenster auch ausgegeben. 
- *File Browser*: Fenster links oben; quasi der Dateiexplorer von Octave; 
  dient zur Anzeige des Inhalt des aktuellen Verzeichnisses; Dateioperationen wie ̈Öffnen, Löschen, Umbenennen und Kopieren sind hier ebenfalls möglich.
- *Workspace*: Fenster links unten; hier werden Größe und Typ von Objekten angegeben.
- *Documentation*: Fenster rechts; bietet umfangreiche Informationen über Funktion, insbesondere zu ihrer Syntax.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\07_Octave_Oberfläche.jpg" alt="07_Octave_Oberfläche" style="zoom:33%;" />





### 4.2 Random Dot Pattern

In diesem Tutorial werden wir im Wesentlichen nur eine einzige Funktion benötigen, die bereits als Skript (*DotDemo_2019.m*) im BB26-Ordner liegt. Um diese ausführen zu können, müssen wir im File Browser zunächst zu deren Ordnerpfad navigieren, wie im Folgenden dargestellt.

> Das Skript an sich muss NICHT geöffnet werden; sollte es dennoch geöffnet werden, landet man im Editor-Fenster. In diesem Fall wieder auf den Reiter "Command Window" (Mitte unten) drücken.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\08_FileBrowser_a.jpg" alt="08_FileBrowser_a" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\08_FileBrowser_b.jpg" alt="08_FileBrowser_b" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\08_FileBrowser_c.jpg" alt="08_FileBrowser_c" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\08_FileBrowser_d.jpg" alt="08_FileBrowser_d" style="zoom:33%;" />





Ihr solltet nun im Ordner des Skripts *DotDemo_2019.m* angelangt sein. Um das Skript zu starten, muss lediglich folgender **Befehl** im Command Window eingegeben und mit [ENTER] bestätigt werden:

```octave
DotDemo_2019
```

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\09_DotDemo-Command.jpg" alt="09_DotDemo-Command" style="zoom:33%;" />





Vor Beginn der Präsentation der Random Dot Pattern werden mehrere Informationen im Command Window abgefragt. 

* *Gruppe*
  Hier wird die Gruppennummer angegeben, z.B. `1234`.
* *Name*
  Hier gebt wird der Namen des Teilnehmers angegeben, z.B. `ManfredMustermann`.
* *Kohärenzwert*
  Hier wird die relative Kohärenz der Bewegungsrichtung aller Dots als Dezimalzahl angegeben, z.B. `0.3`. Zu beachten: das Dezimaltrennzeichen entspricht der <u>englischen Notation</u> (mit Punkt) und nicht der deutschen (mit Komma).
  Beispiel 1: im Falle von 100% Kohärenz bewegen sich alle Punkte in dieselbe Richtung. 
  Als Kohärenzwert wird der Wert `1` angegeben. 
  Beispiel 2: im Falle von 50% Kohärenz bewegt sich nur die Hälfte aller Punkte in dieselbe Richtung, die restlichen 50% nehmen zufällige Bewegungsrichtungen an. 
  Als Kohärenzwert wird der Wert `0.5` angegeben.
* *Trial-Anzahl*
  Hier wird die Anzahl der Einzelmessungen (Trial) angegeben, z.B. `20`. 

Jeder Eingabe ist mit [ENTER] zu bestätigen.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\10_Gruppennummer_angeben.jpg" alt="10_Gruppennummer_angeben" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\11_Teilnehmer-Name_angeben.jpg" alt="11_Teilnehmer-Name_angeben" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\12_Kohärenzwert_angeben.jpg" alt="12_Kohärenzwert_angeben" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\12_Trial-Anzahl_angeben.jpg" alt="12_Trial-Anzahl_angeben" style="zoom:33%;" />





Nun wird eine **Bestätigung** (y = yes, n = no) der vorher getätigten Eingaben verlangt. Zudem wird der Dateiname angegeben, in dem die Ergebnisse automatisch als Excel-Datei abgespeichert werden.
Falls alles richtig eingegeben wurde, `y` drücken und wieder mit [ENTER] bestätigen. 
Damit startet die Dot Demo.

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\13_Bestätigen.jpg" alt="13_Bestätigen" style="zoom:33%;" />





Die Darstellung sollte wie im folgenden Fenster aussehen. Dabei sind folgende Bestandteile des Stimulus zu erkennen:

* *Fixationspunkt* (roter Punkt): auf diesen Punkt soll der Partizipant während der gesamten Durchführung des Experiments schauen. Die Position des Fixationspunkt bleibt über alle Trials hinweg gleich. 
* *Bewegungsrichtung 1 & 2* (blauer & grüner Punkt): zu einer dieser beiden Punkten bewegen sich die kohärenten weißen Dots. Die Bewegungsrichtungen ändern sich zwischen den Messungen zufällig.
* *Random Dots* (weiße Punkte): diese Punkte können sich je nach Kohärenzwert in eine Richtung bewegen. Bei einer Kohärenz von 100% würden sich somit alle weißen Punkte entweder zum blauen oder grünen Punkt hin bewegen. Bei Kohärenzwerten von < 100% bewegt sich entsprechend nur eine Teilmenge von Punkten in eine dieser beiden Richtungen, der Rest schlägt zufällige Bewegungsrichtungen ein. 
  WICHTIG: der Partizipant soll <u>nicht</u> die weißen Punkte fixieren, sondern sich ausschließlich auf den roten Punkt konzentrieren!

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\14_DotDemo_durchführen.jpg" alt="14_DotDemo_durchführen" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\14_nach_DotDemo_CommandWindow.jpg" alt="14_nach_DotDemo_CommandWindow" style="zoom:33%;" />

<img src="C:\Users\kilian\Desktop\Docs\TUD\Systems Neurophysiology\Lehrveranstaltungen\BB26[E-Learning]\Psychophysik E-Learning\Tutorial\Markdown\src\TEMP\15_ErgebnisMatrix.jpg" alt="15_ErgebnisMatrix" style="zoom:33%;" />





...





## 5. Ergebnisse

...



## 6. Abschluss

...

