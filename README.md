# BB26 Psychophysik - Random Dot Pattern

[TOC]

## 1 Einführung

Die Idee dieses Experimentes ist es, zu testen, wie viele Punkte einer Punktwolke sich in die gleiche Richtung bewegen müssen, damit wir diese Bewegungsrichtung auch wahrnehmen können.

Dazu verwenden wir als Stimuli sogenannte **Random Dot Pattern**.  Dies ist ein zufälliges Muster von Punkten, die sich auf einem schwarzen Hintergrund mit konstanter Geschwindigkeit in jeweils eine Richtung bewegen. Ein bestimmter Anteil der Punkte bewegt sich dabei in identischer Richtung. Diese Punkte bezeichnen wir im Folgenden als *kohärent*. 

<img src="src\Random_Dot_Pattern.gif" alt="Random_Dot_Pattern" align=center width="500" />



<br/>

## 2 Verwendete Software

### 2.1 Oracle VM VirtualBox Manager 

Als Software wird für dieses Psychophysik-Experiment lediglich der *Oracle VM VirtualBox Manager* benötigt 
- im Folgenden als *VirtualBox* bezeichnet. 
Dies ist ein praktisches Open Source-Tool, mit dem weitere Betriebssysteme in einer virtuellen Umgebung auf dem PC geladen werden können. So lässt sich auch unser bereitgestelltes **Image** (.iso) verwenden, in welchem bereits alle notwendigen Treiber & Software für die BB26-Versuche enthalten sind.



#### 2.2.1 Download

VirtualBox ist für Windows/Mac/Linux unter folgendem Link verfügbar :
https://www.virtualbox.org/wiki/Downloads

<img src="src\A_01_VirtualBox_Download.jpg" alt="A_01_VirtualBox_Download" align=center width="600"/>



#### 2.2.2 Installation

Nach dem Download gestaltet sich die **Installation** sehr einfach, die **Voreinstellungen** können nämlich einfach übernommen werden. Beispielhaft wird im Folgenden die Installation auf Windows dargestellt:

<img src="src\A_02_VirtualBox_Installation_a.jpg" alt="A_02_VirtualBox_Installation_a" align=center width="450" />

<img src="src\A_02_VirtualBox_Installation_b.jpg" alt="A_02_VirtualBox_Installation_b" align=center width="450"/>

<img src="src\A_02_VirtualBox_Installation_c.jpg" alt="A_02_VirtualBox_Installation_c" align=center width="450"/>

<img src="src\A_02_VirtualBox_Installation_d.jpg" alt="A_02_VirtualBox_Installation_d" align=center width="450" />

<img src="src\A_02_VirtualBox_Installation_e.jpg" alt="A_02_VirtualBox_Installation_e" align=center width="450"/>

<img src="src\A_02_VirtualBox_Installation_f.jpg" alt="A_02_VirtualBox_Installation_f" align=center width="450" />



#### 2.2.3 Erstellen einer Virtuellen Maschine

Um unser Image nun laden zu können, müssen wir in VirtualBox zunächst eine virtuelle Maschine - quasi ein "virtueller Computer" - erzeugen. Dafür einfach auf den Button **"Neu"** klicken.

<img src="src\B_01_Neu.jpg" alt="B_01_Neu" align=center width="600" />





Im nächsten Fenster vergeben wir einen geeigneten Namen für unsere virtuelle Maschine und legen fest, welchen **Typ** (Linux) und **Version** (Debian 64-bit) unser virtuelles Betriebssystem haben soll.
Die **Speichergröße** (RAM) wird zunächst auf 2048 MB festgelegt. Je nach verfügbarer Hardware kann diese aber beliebig verkleinert/vergrößert werden.
Zuletzt setzen wir noch den Punkt **"Festplatte erzeugen"** und drücken den Button **"Erzeugen"**.

<img src="src\B_02_VM_erzeugen.jpg" alt="B_02_VM_erzeugen" align=center width="600" />





Anschließend müssen wir im nächsten Fenster den **Dateipfad** zu unserem Image angeben.
Die **Dateigröße** lassen wir auf max. 8,00 GB, auch **Dateityp der Festplatte** und **Art der Speicherung** kann auf den Voreinstellungen belassen werden. Wieder drücken wir auf den Button **"Erzeugen"**.

<img src="src\B_03_VirtuelleFestplatte.jpg" alt="B_03_VirtuelleFestplatte" align=center width="600" />





Damit ist nun unsere virtuelle Maschine fertig. Wenn alles funktioniert hat, sollte die Ansicht ungefähr so ausschauen:

<img src="src\B_04_Image_laden_a.jpg" alt="B_04_Image_laden_a" align=center width="600" />





> Falls unter dem Punkt **"Massenspeicher"** bei **"[Optisches Laufwerk]"** immer noch **"leer"** steht, sollte noch einmal unser Image als Abbild ausgewählt werden.
>

<img src="src\B_04_Image_laden_b.jpg" alt="B_04_Image_laden_b" align=center width="600" />





Um die virtuelle Maschine zu starten, klicken wir oben rechts auf den Button **"Start"**.

<img src="src\B_05_Image_starten.jpg" alt="B_05_Image_starten" align=center width="600" />



<br/>

### 2.2 Debian

Das virtuelle Betriebssystem wird nun automatisch hochgefahren. Alternativ kann im Bootmenü der Unterpunkt **"live"** ausgewählt werden. 

<img src="src\C_00_LiveSystem_Staten.jpg" alt="C_00_LiveSystem_Staten" align=center width="650" />





Nach kurzer Wartezeit erscheint dann der Desktop. Hier sehen wir, dass bereits ein Ordner **"BB26 (2019)"** verfügbar ist. Darin sind alle relevanten Dateien enthalten. Auch befinden sich hier später Text-Dateien, welche automatisch generiert und in denen alle Experimental-Ergebnisse gespeichert werden.

<img src="src\C_01_Desktop.jpg" alt="C_01_Desktop" align=center width="650"  />

<img src="src\C_02_BB26-Folder.jpg" alt="C_02_BB26-Folder" align=center width="650"  />

<img src="src\C_03_Psychophysik-Folder.jpg" alt="C_03_Psychophysik-Folder" align=center width="650"  />

<img src="src\C_04_Psychophysik[2020]-Folder.jpg" alt="C_04_Psychophysik[2020]-Folder" align=center width="650"  />



<br/>

### 2.3 Octave

Um die bewegten visuellen Stimuli zu erstellen, benutzen wir in diesem Experiment die Analysesoftware *Octave*. Wir müssen zum Glück nicht alles von Hand neu programmieren, sondern können auf bereits vorgeschriebene Funktionen und Funktionen der *Psychtoolbox* (www.psychtoolbox.org) zurückgreifen, welche ebenfalls bereits in unserem BB26-Image enthalten sind.

Um Octave zu starten, gehen wir im **Applications Menu** (links oben) auf den Reiter **Education** und klicken auf die **App** *GNU Octave*.

<img src="src\D_00_Octave_starten.jpg" alt="D_00_Octave_starten" align=center width="650"  />





Nach dem Start von Octave erscheint die Octave-**Oberfläche**, welche aus mehreren Fenstern besteht:

- *Command Window*: das größte, schwarz hinterlegte Feld in der Mitte; 
  dieses dient einerseits als Eingabefenster, um Befehle, Funktionen und Skripte auszuführen; andererseits werden deren Ergebnisse in diesem Fenster auch ausgegeben. 
- *File Browser*: Fenster links oben; 
  Quasi der Dateiexplorer von Octave; dient zur Anzeige des Inhalt des aktuellen Verzeichnisses; Dateioperationen wie ̈Öffnen, Löschen, Umbenennen und Kopieren sind hier ebenfalls möglich.
- *Workspace*: Fenster links unten; hier werden Größe und Typ von Objekten angegeben. 
- *Documentation*: Fenster rechts; bietet umfangreiche Informationen über Funktion, insbesondere zu ihrer Syntax.

<img src="src\D_01_Octave_Oberfläche.jpg" alt="07_Octave_Oberfläche" align=center width="650"  />



<br/>

## 3 Experiment

In diesem Tutorial werden wir im Wesentlichen nur eine einzige Funktion benötigen, die bereits als selbstgeschriebenes Script (*DotDemo_2019.m*) im BB26-Ordner liegt. Dieses Script muss <u>nicht</u> geöffnet werden. Wir müssen lediglich im Octave File Browser (links) zu dessen Ordnerpfad navigieren, wie im Folgenden dargestellt wird.

> Sollte das Skript dennoch geöffnet werden, landet man im Editor-Fenster. 
> In diesem Fall wieder auf den Reiter "Command Window" (Mitte unten) drücken.

Der vollständige Pfad lautet:
`home/dj0/Desktop/BB 26 (2019)/Psychophysik/Psychophysic Toolbox [2019]`

<img src="src\D_02_FileBrowser_a.jpg" alt="08_FileBrowser_a" align=center width="650"  />

<img src="src\D_02_FileBrowser_b.jpg" alt="08_FileBrowser_b" align=center width="650"  />

<img src="src\D_02_FileBrowser_c.jpg" alt="08_FileBrowser_c" align=center width="650"  />

<img src="src\D_02_FileBrowser_d.jpg" alt="08_FileBrowser_d" align=center width="650"  />





Nun sollten wir im Ordner des Scripts *DotDemo_2019.m* angelangt sein. Um es zu starten, muss lediglich folgender **Befehl** im Octave Command Window  eingegeben und mit [ENTER] bestätigt werden:

```octave
DotDemo_2019
```

<img src="src\D_03_DotDemo-Command.jpg" alt="09_DotDemo-Command" align=center width="650"  />





Vor Beginn der Präsentation der Random Dot Pattern werden mehrere Informationen der Versuchsperson im Command Window abgefragt. Dies dient später zur Generierung der Ergebnis-Textdateien.

* *Gruppe*
  Hier wird die Gruppennummer angegeben, z.B. `1234`.
* *Name*
  Hier wird der Name des Teilnehmers angegeben, z.B. `ManfredMustermann`.
* *Kohärenzwert*
  Hier wird die relative Kohärenz der Bewegungsrichtung aller Dots als Dezimalzahl angegeben.
  Dieser Wert gibt an, wie groß der Anteil aller Punkte mit identischer Bewegungsrichtung ist. 
  Beachte: Das Dezimaltrennzeichen entspricht der <u>englischen Notation</u> (mit Punkt) und nicht der deutschen (mit Komma).
  Beispiel 1: im Falle von 100% Kohärenz bewegen sich alle Punkte in dieselbe Richtung. 
  Als Kohärenzwert wird der Wert `1` angegeben. 
  Beispiel 2: im Falle von 50% Kohärenz bewegt sich nur die Hälfte aller Punkte in dieselbe Richtung, die restlichen 50% nehmen zufällige Bewegungsrichtungen an. 
  Als Kohärenzwert wird der Wert `0.5` angegeben.
* *Trial-Anzahl*
  Hier wird die Anzahl der Einzelmessungen (Trial) angegeben, z.B. `20`. 

Jeder Eingabe ist mit der Taste [ENTER] zu bestätigen.

<img src="src\D_04_Gruppennummer_angeben.jpg" alt="10_Gruppennummer_angeben" align=center width="650"  />

<img src="src\D_05_Teilnehmer-Name_angeben.jpg" alt="11_Teilnehmer-Name_angeben" align=center width="650"  />

<img src="src\D_06_Kohärenzwert_angeben.jpg" alt="12_Kohärenzwert_angeben" align=center width="650"  />

<img src="src\D_07_Trial-Anzahl_angeben.jpg" alt="12_Trial-Anzahl_angeben" align=center width="650"  />





Nun wird eine **Bestätigung** (`y` = yes, `n` = no) der vorher getätigten Eingaben verlangt. Zudem wird der Dateiname angegeben, in dem die Ergebnisse automatisch als Excel-Datei abgespeichert werden.
Falls alles richtig eingegeben wurde, drücken wir im Command Window die Taste `y` und bestätigen wieder mit [ENTER]. Damit startet die Dot Demo.

<img src="src\D_08_Bestätigen.jpg" alt="13_Bestätigen" align=center width="650"  />





Die Stimulus-Präsentation sollte etwa wie im folgenden Fenster aussehen. Dabei sind folgende **Bestandteile des Stimulus** zu erkennen:

* *Fixationspunkt* (roter Punkt): auf diesen Punkt soll der Partizipant während der gesamten Durchführung des Experiments schauen. Die Position des Fixationspunkt bleibt über alle Trials hinweg gleich. 
* *Bewegungsrichtung 1 & 2* (blauer & grüner Punkt): zu einer dieser beiden Punkten bewegen sich die kohärenten weißen Dots. Die Position beider Punkte ändert sich zwischen den Trials zufällig.
* *Random Dots* (weiße Punkte): diese Punkte können sich je nach Kohärenzwert in eine Richtung bewegen. Bei einer Kohärenz von 100% würden sich somit alle weißen Punkte entweder zum blauen oder grünen Punkt hin bewegen. Bei Kohärenzwerten von < 100% bewegt sich entsprechend nur eine Teilmenge von Punkten in eine dieser beiden Richtungen, der Rest schlägt zufällige Bewegungsrichtungen ein. 
  WICHTIG: die Testperson soll <u>nicht</u> die weißen Punkte fixieren, sondern sich ausschließlich auf den roten Punkt konzentrieren!

<img src="src\D_09_DotDemo_durchführen.jpg" alt="14_DotDemo_durchführen" align=center width="650"  />



Nach jedem Trial stoppt die Anzeige und es wird eine **Eingabe der Testperson** erwartet:

- Wird eine Bewegung zum grünen Punkt hin wahrgenommen, drücken wir die Taste `g`
- Wird eine Bewegung zum blauen Punkt hin wahrgenommen, drücken wir die Taste `b`

Dies wiederholen wir solange, bis alle Trials für einen einzelnen Kohärenzwert (z.B. 0.1) durchgelaufen sind.

> Beachte: Octave limitiert die Ausgabe von langem Output. Es ist somit notwendig, durch Drücken der Taste `f` in der Ausgabe weiter zu scrollen. Alternativ kann dieses Verhalten auch abgestellt werden, in dem man direkt nach dem Öffnen der Octave-App den Command `more on` ausführt.

<img src="src\D_10_nach_DotDemo_CommandWindow.jpg" alt="14_nach_DotDemo_CommandWindow" align=center width="650"  />



Nach Durchführen aller Trials sollten wir folgende **Ergebnismatrix** im Command Window angezeigt bekommen. Diese ist folgendermaßen aufgebaut:

* *Angabe korrekt/falsch* (linke Spalte): dies ist die wichtigste Spalte. Hier wird für jeden Trial angezeigt, ob die wahre Bewegungsrichtung der Punkte von der Versuchsperson richtig (1) oder falsch (0) erkannt wurde. 
* *Relative Kohärenz* (mittlere Spalte): hier wird für jeden Trial die relative Kohärenz als Dezimalzahl angegeben. Dieser Wert sollte über alle Trials konstant bleiben.
* *Antwortdauer [in Sekunden]* (rechte Spalte): hier wird die Zeit abgetragen, die nach der Präsentation des Trials bis zur Antwort der Versuchsperson (Drücken der Taste `b` oder `g`) verstrichen ist.

<img src="src\D_11_ErgebnisMatrix.jpg" alt="15_ErgebnisMatrix" align=center width="650"  />



<br/>

## 4. Ergebnisse

Die Ergebnisse werden nach jedem erfolgreichen Abschluss des Commands `DotDemo_2019` in einer separaten Text-Datei (.txt) gespeichert. Alle Text-Dateien befinden sich im selben Ordnerpfad wie auch das Script *DotDemo_2019.m* . Benannt sind diese wie im folgenden Beispiel: 

`Not_adaptive_moving_dot_Gruppe1_ManfredMustermann_0.5_Kohaerenz_20_Apr_2020_14_00_00.txt`



Die Ergebnisse lassen sich nach Abschluss aller Experimente in einem Office-Programm wie z.B. Excel oder LibreOffice weiter verarbeiten. Im Folgenden wird gezeigt, wie die Ergebnisse in LibreOffice Calc eingefügt werden. Dazu sind folgende Schritte notwendig:

* Ergebnismatrix aus einer der Text-Dateien oder direkt aus dem Octave Command Window kopieren, z.B. mit Tastenkombination [STR]+[C] 
* LibreOffice Calc im Applications Menu öffnen
* Ergebnisse einfügen, z.B. mit Tastenkombination [STR]+[V] 
* Im Menü *Text Import*  die im Bild gezeigten Einstellungen verwenden



<img src="src\E_01_LibreOffice-Calc_starten.jpg" alt="E_17_LibreOffice-Calc_starten" align=center width="650"/> 	

<img src="src\E_02_LibreOffice-Calc_Oberfläche.jpg" alt="E_02_LibreOffice-Calc_Oberfläche" align=center width="650" />

<img src="src\E_03_Ergebnismatrix_einfügen.jpg" alt="E_03_Ergebnismatrix_einfügen" align=center width="650" />



Es sollten nun die Ergebnisse in drei Spalten aufgeteilt worden sein. Der Vollständigkeit halber wurden im folgenden Bild die Tabellenspalten mit Bezeichnungen versehen.

<img src="src\E_04_Interpretation_a.jpg" alt="E_04_Interpretation_a" align=center width="650"  />



Gespeichert werden kann die Tabelle dann mit [STR]+[S] oder wie im folgenden Bild per Menü:

<img src="src\E_05_Speichern-Ergebnisse.jpg" alt="E_05_Speichern-Ergebnisse" align=center width="650"  />



<br/>

## 5. Abschluss

> **BITTE DRINGEND BEACHTEN**
>
> Wenn die VirtualBox geschlossen werden soll, dann im Fenster "Beenden der virtuellen Maschine" unbedingt den Punkt "**den Zustand der virtuellen Maschine speichern**" auswählen. Andernfalls wird das Image zurückgesetzt und alle Ergebnisse sind nicht mehr verfügbar.



<img src="src\F_01_VirtuelleMaschine-Beenden.jpg" alt="F_01_VirtuelleMaschine-Beenden" align=center width="650"  />

<br/>

## 6. Zusammenfassung

Anbei noch einmal eine Zusammenfassung der wesentlichen Schritte:

* Auf eigenem Rechner das Programm *Oracle VM VirtualBox Manager* installieren

* In Virtual Box: virtuelle Maschine erstellen, BB26-Debian-Image (.iso) einladen und starten

* In Debian: App "GNU Octave" öffnen

* In Octave File-Manager zum Ordnerpfad des Scripts *DotDemo_2019.m* navigieren. Das Script an sich muss aber nicht geöffnet werden.
  Pfad: `home/dj0/Desktop/BB 26 (2019)/Psychophysik/Psychophysic Toolbox [2019]`

* Folgende Schritte **für jeden der acht Kohärenzwert** (0%, 5%, 10%, 15%, 20%, 30%, 40%, 50%) wiederholen, am besten in zufälliger Reihenfolge (z.B. 10%, 30%, 10%, 50%, 0%, 15%, 5%, 20%):

  1. Im Command Window den Befehl `DotDemo_2019` ausführen

  2. Gruppennummer, Namen, Kohärenzwert und Anzahl der Trials (n=20) festlegen und mit `y` bestätigen

  3. Experiment durchführen, bis alle Trials für den ausgewählten Kohärenzwert abgeschlossen wurden

  4. Mit nächstem Kohärenzwert weitermachen

* Ergebnisse werden nach jedem Trial automatisch im selben Ordnerpfad als .txt-Datei gespeichert. Diese können dann zur weiteren Verarbeitung in einem Office-Programm wie Excel oder LibreCalc genutzt werden.

* **WICHTIG**
  Wenn die VirtualBox geschlossen werden soll, dann im Fenster "Beenden der virtuellen Maschine" unbedingt den Punkt "**den Zustand der virtuellen Maschine speichern**" auswählen. Andernfalls wird das Image zurückgesetzt und alle Ergebnisse sind nicht mehr verfügbar.