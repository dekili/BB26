# BB26 Psychophysik - Random Dot Pattern

## 1 Einführung

Die Idee dieses Experimentes ist es, zu testen, wie viele Punkte einer Punktwolke sich in die gleiche Richtung bewegen müssen, damit wir diese Bewegungsrichtung auch wahrnehmen können.

Dazu verwenden wir als Stimuli sogenannte **Random Dot Pattern**.  Dies sind zufällige Muster von Punkten, welche sich auf einem schwarzen Hintergrund mit konstanter Geschwindigkeit in jeweils eine Richtung bewegen. Ein bestimmter Anteil der Punkte bewegt sich dabei in identischer Richtung. Diese Punkte bezeichnen wir im Folgenden als *kohärent*. 

<img src="src\Random_Dot_Pattern.gif" alt="Random_Dot_Pattern" align=center width="500" />



<br/>

## 2 Verwendete Software

Bitte laden Sie zunächst die **Image-Datei** (.iso) herunter. Entsprechender Link wird von den BB26-Betreuern bereitgestellt.

<br/>

### 2.1 Oracle VM VirtualBox Manager 

Als Software wird für dieses Psychophysik-Experiment lediglich der *Oracle VM VirtualBox Manager* benötigt. 
Dies ist ein praktisches Open Source-Tool, mit dem weitere Betriebssysteme in einer virtuellen Umgebung auf dem PC geladen werden können. So lässt sich auch unser bereitgestelltes **Image** (.iso) verwenden, in welchem bereits alle notwendigen Treiber & Software für die BB26-Versuche enthalten sind.



#### 2.2.1 Download

VirtualBox ist für Windows/Mac/Linux verfügbar. Bitte laden Sie entsprechende **Installationsdatei** und außerdem das **Extension Pack** herunter. Beide Dateien finden Sie unter folgendem Link:
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


<br/>

#### 2.2.3 Erstellen einer Virtuellen Maschine

Um unser Image nun laden zu können, müssen wir in VirtualBox zunächst eine virtuelle Maschine erzeugen. Dafür einfach auf den Button **"Neu"** klicken.

<img src="src\B_01_Neu.jpg" alt="B_01_Neu" align=center width="600" />



<br/>

Im nächsten Fenster vergeben wir einen geeigneten Namen und Ordner für unsere virtuelle Maschine und legen fest, welchen **Typ** (Linux) und **Version** (Ubuntu 64-bit) unser virtuelles Betriebssystem haben soll.
Die **Speichergröße** (RAM) wird zunächst auf 1024 MB festgelegt. Je nach verfügbarer Hardware kann diese aber beliebig verkleinert oder vergrößert werden.
Zuletzt setzen wir noch den Punkt **"Festplatte erzeugen"** und drücken den Button **"Erzeugen"**.

<img src="src\B_02_VM_erzeugen.jpg" alt="B_02_VM_erzeugen" align=center width="600" />



<br/>

Anschließend müssen wir im nächsten Fenster den **Dateipfad** zu unserem Image angeben.
Die **Dateigröße** können wir auf den Voreinstellungen von max. 10,00 GB lassen. Je nach verfügbarem Festplatten-Speicherplatz kann diese aber auch kleiner festgelegt werden. Auch **Dateityp der Festplatte** und **Art der Speicherung** kann auf den Voreinstellungen belassen werden. Wieder drücken wir auf den Button **"Erzeugen"**.

<img src="src\B_03_VirtuelleFestplatte.jpg" alt="B_03_VirtuelleFestplatte" align=center width="600" />



<br/>

Damit ist nun unsere virtuelle Maschine fertig. Wenn alles funktioniert hat, sollte die Ansicht ungefähr so ausschauen:

<img src="src\B_04_Image_laden_a.jpg" alt="B_04_Image_laden_a" align=center width="600" />



<br/>

> Falls unter **"Massenspeicher"** bei **"[Optisches Laufwerk]"** immer noch **"leer"** steht, sollte noch einmal unser Image (.iso-Datei) als Abbild ausgewählt werden.

<img src="src\B_04_Image_laden_b.jpg" alt="B_04_Image_laden_b" align=center width="600" />

<br/> 


#### 2.2.4 VirtualBox Expansion Pack

Um im virtuellen Betriebssystem auch eine **USB-Anbindung** für das Speichern der Experimental-Ergebnisse nutzen zu können, muss das **Virtual Box Extension Pack** installiert werden.
Klicken Sie im Menü "Datei" auf den Unterpunkt "Einstellungen". 



<img src="src\B_04_Datei_Einstellungen.jpg" alt="B_04_Datei_Einstellungen" align=center width="600" />



<br/> 

Anschließend wählen Sie auf der linken Seite den Punkt "Zusatzpakete".
Fügen Sie die heruntergeladene Expansion Pack-Datei mithilfe des "+"-Buttons rechts hinzu.

<img src="src\B_04_Zusatzpakete.jpg" alt="B_04_Zusatzpakete" align=center width="600" />

<br/> 

Nun startet die Installation. 



<img src="src\B_04_Installation_Extension_b.jpg" alt="B_04_Installation_Extension_b" align=center width="600" />

<br/> 

Wählen Sie danach unsere virtuelle Maschine aus und klicken Sie auf "Ändern...".

<img src="src\B_04_Aendern.jpg" alt="B_04_Aendern" align=center width="600" />

<br/> 

Gehen Sie im linken Bereich auf den Punkt "USB" und drücken Sie rechts auf den obersten Button "Leeren Filter hinzufügen".



<img src="src\B_04_Leerer_USB_Filter_a.jpg" alt="B_04_Leerer_USB_Filter_a" align=center width="600" />

<img src="src\B_04_Leerer_USB_Filter_b.jpg" alt="B_04_Leerer_USB_Filter_b" align=center width="600" />
<br/>
Abschließend mit OK bestätigen. 

### 2.3 Ubuntu

Um die virtuelle Maschine zu starten, klicken wir oben rechts auf den Button **"Start"**.



<img src="src\B_05_Image_starten.jpg" alt="B_05_Image_starten" align=center width="600" />

<br/>

Das virtuelle Betriebssystem wird nun automatisch hochgefahren. Alternativ kann im Bootmenü der Unterpunkt **"live"** ausgewählt werden. 

<img src="src\C_00_LiveSystem_Staten.jpg" alt="C_00_LiveSystem_Staten" align=center width="650" />



<br/>

Während des Hochfahrens können wir das kleine **Ausgabe-Fenster maximieren** (rechts oben, mittlerer Button). Sollte die Anzeige immer noch zu klein sein, kann im Reiter *Anzeige* entweder *Skalierter Modus* oder *Vollbildmodus* ausgewählt werden, um die Anzeige zu vergrößern.

<img src="src\B_06_Skalierte_Ansicht.jpg" alt="B_06_Skalierte_Ansicht" align=center width="650" />

<br/>

Nun sollte man sich als Benutzer einloggen. Entsprechende **Login**-Informationen werden von den BB26-Betreuern bekanntgegeben.

<img src="src\C_00_Login.jpg" alt="C_00_Login" align=center width="650" />



<br/> 

Nach kurzer Wartezeit erscheint dann der Desktop. Hier können wir doppelt auf den **Ordner Home** klicken und darin den Unter-Ordner **octave** öffnen. Hier sind alle für unser Experiment relevanten Dateien enthalten. Auch befinden sich hier später Text-Dateien, welche automatisch generiert werden und in denen die Experimental-Ergebnisse gespeichert sind.

<img src="src\C_01_Desktop.jpg" alt="C_01_Desktop" align=center width="650"  />

<img src="src\C_02_BB26-Folder.jpg" alt="C_02_BB26-Folder" align=center width="650"  />



<br/>

Um Octave zu starten, gehen wir im **Applications Menu** (links oben) auf den Reiter **Education** und klicken auf die **App** *GNU Octave*.
### 2.4 Octave

Um die bewegten visuellen Stimuli zu erstellen, benutzen wir in diesem Experiment die Analysesoftware *Octave*. Wir müssen zum Glück nicht alles von Hand neu programmieren, sondern können auf bereits vorgeschriebene Funktionen und Funktionen der *Psychtoolbox* (www.psychtoolbox.org) zurückgreifen, welche ebenfalls bereits in unserem BB26-Image enthalten sind.

Um Octave zu starten, klicken wir im Desktop auf die **App** *GNU Octave*.

<img src="src\D_00_Octave_starten.jpg" alt="D_00_Octave_starten" align=center width="650"  />



<br/>

Nach dem Start von Octave erscheint die **Octave-Oberfläche**, welche aus mehreren Fenstern besteht:

- *Command Window*: das größte, schwarz hinterlegte Feld in der Mitte; 
  dieses dient einerseits als Eingabefenster, um Befehle, Funktionen und Skripte auszuführen; andererseits werden deren Ergebnisse in diesem Fenster auch ausgegeben. 
- *File Browser*: Fenster links oben; 
  Quasi der Dateiexplorer von Octave; dient zur Anzeige des Inhalt des aktuellen Verzeichnisses; Dateioperationen wie ̈Öffnen, Löschen, Umbenennen und Kopieren sind hier ebenfalls möglich.
- *Workspace*: Fenster links unten; hier werden Größe und Typ von Objekten angegeben. 
- *Documentation*: Fenster rechts; bietet umfangreiche Informationen über Funktion, insbesondere zu ihrer Syntax.

<img src="src\D_01_Octave_Oberfläche.jpg" alt="07_Octave_Oberfläche" align=center width="650"  />



<br/>

## 3 Experiment

In diesem Tutorial werden wir im Wesentlichen nur eine einzige Funktion benötigen, die bereits als selbstgeschriebenes Script (*DotDemo_2020.m*) im Ordner *octave* liegt. Dieses Script muss <u>nicht</u> geöffnet werden. Wir müssen lediglich im Octave File Browser (links) zu dessen Ordnerpfad navigieren, wie im Folgenden dargestellt wird. Der vollständige Pfad lautet:
`home/dj0/octave`

> Sollte das Skript dennoch geöffnet werden, landet man im Editor-Fenster. 
> In diesem Fall wieder auf den Reiter "Command Window" (Mitte unten) drücken.

<img src="src\D_02_FileBrowser_a.jpg" alt="08_FileBrowser_a" align=center width="650"  />



<br/>

Nun sollten wir im Ordner des Scripts *DotDemo_2020.m* angelangt sein. Um es zu starten, muss lediglich folgender **Befehl** im Octave Command Window  eingegeben und mit [ENTER] bestätigt werden:

```octave
DotDemo_2020
```

<br/>

<img src="src\D_03_DotDemo-Command.jpg" alt="09_DotDemo-Command" align=center width="650"  />



<br/>

Vor Beginn der Präsentation der Random Dot Pattern werden mehrere Informationen der Versuchsperson im Command Window abgefragt. Diese werden ausschließlich dafür verwendet, um später automatisch die Ergebnis-Textdateien zu generieren und zu benennen.

* *Gruppe*
  Hier wird die Gruppennummer angegeben, z.B. `1`. Falls im Vorfeld keine Gruppennummern vergeben wurden, kann hier eine beliebige Nummer angegeben werden.
* *Name*
  Hier wird der Name des Teilnehmers angegeben, z.B. `ErikaMustermann` oder `MaxMustermann`. 
* *Kohärenzwert*
  Hier wird die relative Kohärenz der Bewegungsrichtung aller Dots als Dezimalzahl angegeben.
  Dieser Wert gibt an, wie groß der Anteil aller Punkte mit identischer Bewegungsrichtung ist. 
  Beachte: Das Dezimaltrennzeichen entspricht der <u>englischen Notation</u> (mit Punkt) und nicht der deutschen (mit Komma).
  Beispiel 1: im Falle von 100% Kohärenz bewegen sich alle Punkte in dieselbe Richtung. 
  Als Kohärenzwert wird der Wert `1` angegeben. 
  Beispiel 2: im Falle von 50% Kohärenz bewegt sich nur die Hälfte aller Punkte in dieselbe Richtung, die restlichen 50% nehmen zufällige Bewegungsrichtungen an. 
  Als Kohärenzwert wird der Wert `0.5` angegeben.
* *Trial-Anzahl*
  Hier wird die Anzahl der Einzelmessungen (Trial) angegeben. Pro Kohärenzwert geben wir eine Anzahl von `20` Trials vor. 

Jeder Eingabe ist mit der Taste [ENTER] zu bestätigen.

<img src="src\D_04_Gruppennummer_angeben.jpg" alt="10_Gruppennummer_angeben" align=center width="650"  />

<img src="src\D_05_Teilnehmer-Name_angeben.jpg" alt="11_Teilnehmer-Name_angeben" align=center width="650"  />

<img src="src\D_06_Kohärenzwert_angeben.jpg" alt="12_Kohärenzwert_angeben" align=center width="650"  />

<img src="src\D_07_Trial-Anzahl_angeben.jpg" alt="12_Trial-Anzahl_angeben" align=center width="650"  />



<br/>

Nun wird eine **Bestätigung** (`y` = yes, `n` = no) der vorher getätigten Eingaben verlangt. Zudem wird der Dateiname angegeben, in dem die Ergebnisse automatisch als Excel-Datei abgespeichert werden.
Falls alles richtig eingegeben wurde, drücken wir im Command Window die Taste `y` und bestätigen wieder mit [ENTER]. Damit startet die Dot Demo.

<img src="src\D_08_Bestätigen.jpg" alt="13_Bestätigen" align=center width="650"  />



<br/>

Die Stimulus-Präsentation sollte etwa wie im folgenden Fenster aussehen. Dabei sind folgende **Bestandteile des Stimulus** zu erkennen:

* *Fixationspunkt* (roter Punkt): auf diesen Punkt soll der Partizipant während der gesamten Durchführung des Experiments schauen. Die Position des Fixationspunkt bleibt über alle Trials hinweg gleich. 
* *Bewegungsrichtung 1 & 2* (blauer & grüner Punkt): zu einer dieser beiden Punkten bewegen sich die kohärenten weißen Dots. Die Position beider Punkte ändert sich zwischen den Trials zufällig.
* *Random Dots* (weiße Punkte): diese Punkte können sich je nach Kohärenzwert in eine Richtung bewegen. Bei einer Kohärenz von 100% würden sich somit alle weißen Punkte entweder zum blauen oder grünen Punkt hin bewegen. Bei Kohärenzwerten von < 100% bewegt sich entsprechend nur eine Teilmenge von Punkten in eine dieser beiden Richtungen, der Rest schlägt zufällige Bewegungsrichtungen ein. 
  WICHTIG: die Testperson soll <u>nicht</u> die weißen Punkte fixieren, sondern sich ausschließlich auf den roten Punkt konzentrieren!

<img src="src\D_09_DotDemo_durchführen.jpg" alt="14_DotDemo_durchführen" align=center width="650"  />

<br/>

Nach jedem Trial stoppt die Anzeige und es wird eine **Eingabe der Testperson** erwartet:

- Wird eine Bewegung zum grünen Punkt hin wahrgenommen, drücken wir die Taste `g`
- Wird eine Bewegung zum blauen Punkt hin wahrgenommen, drücken wir die Taste `b`

Dies wiederholen wir solange, bis alle Trials für einen einzelnen Kohärenzwert (z.B. 0.1) durchgelaufen sind. 

> Beachte: Octave limitiert die Ausgabe von langem Output auf wenige Zeilen. Es ist somit notwendig, durch Drücken der Taste `f` in der Ausgabe weiter zu scrollen. Alternativ kann dieses Verhalten auch abgestellt werden, in dem man nach dem Öffnen der Octave-App den Command `more on` ausführt.

<img src="src\D_10_nach_DotDemo_CommandWindow.jpg" alt="14_nach_DotDemo_CommandWindow" align=center width="650"  />

<br/>

Nach Durchführen aller Trials sollten wir folgende **Ergebnismatrix** im Command Window angezeigt bekommen. Diese ist folgendermaßen aufgebaut:

* *Angabe korrekt/falsch* (linke Spalte): dies ist für uns die wichtigste Spalte. Hier wird für jeden Trial angezeigt, ob die wahre Bewegungsrichtung der Punkte von der Versuchsperson richtig (`1`) oder falsch (`0`) erkannt wurde. 
* *Relative Kohärenz* (mittlere Spalte): hier wird für jeden Trial die relative Kohärenz als Dezimalzahl angegeben, z.B. `0.5` für 50 % Kohärenz. Dieser Wert entspricht unserem Eingabewert und sollte über alle Trials konstant bleiben.
* *Antwortdauer [in Sekunden]* (rechte Spalte): hier wird die Zeit abgetragen, die nach der Präsentation des Trials bis zur Antwort der Versuchsperson (d.h. nach Drücken der Taste `b` oder `g`) verstrichen ist.

<img src="src\D_11_ErgebnisMatrix.jpg" alt="15_ErgebnisMatrix" align=center width="650"  />



<br/>

> **Beachte:**
>
> Alle angegeben Schritte sind **für jeden der acht Kohärenzwert** (0%, 5%, 10%, 15%, 20%, 30%, 40%, 50%) **in zufälliger Reihenfolge** (z.B. 10%, 30%, 20%, 50%, 0%, 15%, 5%, 40%) zu wiederholen!



## 4. Ergebnisse

Die Ergebnisse werden nach jedem erfolgreichen Abschluss des Commands `DotDemo_2020` in einer separaten Text-Datei (.txt) gespeichert. Alle Text-Dateien befinden sich im selben Ordnerpfad `home/dj0/octave` und sind wie im folgenden Beispiel benannt: 

`Not_adaptive_moving_dot_Gruppe1_MaxMustermann_0.5_Kohaerenz_27_Apr_2020_9_35_46.txt`



<img src="src\E_01_Ergebnis-txt_a.jpg" alt="E_01_Ergebnis-txt_a" align=center width="650" />

<img src="src\E_01_Ergebnis-txt_b.jpg" alt="E_01_Ergebnis-txt_b" align=center width="650" />

<br/>

Die Ergebnisse lassen sich nach Abschluss aller Experimente auf einem **USB-Laufwerk speichern**. Nach dem Einlegen sollte auf dem Ubuntu-Desktop ein entsprechendes Icon erscheinen. Klicken Sie doppelt auf dieses, um das Laufwerk im Explorer zu öffnen. Die Textdateien lassen sich dann wie gewohnt auf das Laufwerk kopieren, z.B. mittels Drag&Drop.

In einem beliebigen **Office-Programm** (z.B. Excel oder LibreOffice) lassen sich die Textdateien auf dem eigenen PC weiter verarbeiten. Im Folgenden wird gezeigt, wie die Ergebnisse in LibreOffice Calc eingefügt werden. Dazu sind folgende Schritte notwendig:

* Ergebnismatrix aus einer der Text-Dateien kopieren, z.B. mit Tastenkombination [STRG]+[C] 
* Ergebnisse in Libre Office Calc einfügen, z.B. mit Tastenkombination [STRG]+[V] 
* Im Menü *Text Import*  die im Bild gezeigten Einstellungen verwenden. Damit werden die einzelnen Ergebnisse gleichmäßig in Spalten aufgeteilt.



<img src="src\E_03_Ergebnismatrix_einfügen.jpg" alt="E_03_Ergebnismatrix_einfügen" align=center width="650" />

<br/>

Es sollten nun die Ergebnisse in drei Spalten aufgeteilt worden sein. Der Vollständigkeit halber wurden im folgenden Bild die Tabellenspalten mit Bezeichnungen versehen.

<img src="src\E_04_Interpretation_a.jpg" alt="E_04_Interpretation_a" align=center width="650"  />



<br/>


<br/>

## 5. Abschluss

> **BITTE DRINGEND BEACHTEN!**
>
> Wenn die VirtualBox geschlossen werden soll, dann im Fenster "Beenden der virtuellen Maschine" unbedingt den Punkt "**den Zustand der virtuellen Maschine speichern**" auswählen. Andernfalls wird das Image auf den Ursprungszustand zurückgesetzt und alle Ergebnisse sind nicht mehr verfügbar.



<img src="src\F_01_VirtuelleMaschine-Beenden.jpg" alt="F_01_VirtuelleMaschine-Beenden" align=center width="650"  />

<br/>

## 6. Zusammenfassung

Anbei noch einmal eine Zusammenfassung der wesentlichen Schritte:

* Bereitgestellte Image-Datei (.iso) herunterladen
* Auf eigenem Rechner das Programm *Oracle VM VirtualBox Manager* installieren
* In Virtual Box: virtuelle Maschine erstellen, Image-datei (.iso) einladen und starten
* In Ubuntu: App "GNU Octave" öffnen
* In Octave File-Manager zum Ordnerpfad des Scripts *DotDemo_2020.m* navigieren. Das Script an sich muss nicht geöffnet werden.
  Pfad: `home/dj0/octave`
* Folgende Schritte **für jeden der acht Kohärenzwert** (0%, 5%, 10%, 15%, 20%, 30%, 40%, 50%) wiederholen **in zufälliger Reihenfolge** (z.B. 10%, 30%, 20%, 50%, 0%, 15%, 5%, 40%):

  1. Im Octave Command Window den Befehl `DotDemo_2020` ausführen

  2. Gruppennummer, Namen, Kohärenzwert und Anzahl der Trials (20 Trials pro Kohärenzwert) festlegen und mit `y` bestätigen

  3. Experiment durchführen, bis alle Trials für den ausgewählten Kohärenzwert abgeschlossen wurden

  4. Mit nächstem Kohärenzwert weitermachen
* Ergebnisse werden nach jedem Trial automatisch im selben Ordnerpfad als .txt-Datei gespeichert. Diese können dann zur weiteren Verarbeitung auf einen USB-Stick gespeichert und in einem beliebigen Office-Programm wie Excel oder LibreCalc weiter verarbeitet werden.
* **WICHTIG!**
  Wenn die VirtualBox geschlossen werden soll, dann im Fenster "Beenden der virtuellen Maschine" unbedingt den Punkt "**den Zustand der virtuellen Maschine speichern**" auswählen. Andernfalls wird das Image zurückgesetzt und alle Ergebnisse sind nicht mehr verfügbar.



## 7. Frequently Asked Questions (FAQ)

**Q: Beim Starten des virtuellen Betriebssystems tritt ein Fehler auf. Die Fehlermeldung beinhaltet einen der folgenden Begriffe: VT-x, VT-d, AMD-V, Virtualisierung. Beispiel: "VT-x is disabled in the BIOS for all CPU modes".**

**A:** Dies liegt an einer deaktivierten **Virtualisierungs-Einstellung** eures Rechners. 
Bei vielen neueren PCs ist diese von Vorneherein aktiviert. In Windows kann dies im Task Manager überprüft werden. Dazu [STR]+[ALT]+[ENTF] (bzw. noch besser: [STR]+[SHIFT]+[ESCAPE]) drücken. Im Task Manager auf den Reiter "Leistung" klicken und links auf "CPU". Rechts sollte nun unter "Virtualisierung" bestenfalls "Aktiviert" stehen, wie z.B. in folgendem Bild: 

<img src="src\FAQ_TaskManager_Virtualisierung.jpg" alt="FAQ_TaskManager_Virtualisierung" align=center width="450" />

Sollte das nicht der Fall sein, muss diese Einstellung im BIOS bzw. UEFI aktiviert werden. 
Wie ihr an eurem Rechner in das BIOS / UEFI Menü gelangt, ist von System zu System unterschiedlich - dazu könnt ihr die Google-Suche bemühen (z.B. "Lenovo Ideapad Bios"). 
Seid ihr erst einmal im BIOS / UEFI angelangt, müsst ihr in den Security-Einstellungen (bzw. CPU-Einstellungen) nach einem Unterpunkt suchen, der die Begriffe "Virtualisierung", "VT-x", "VT-d", oder "AMD-v" beinhaltet. Diese Einstellung muss aktiviert werden, damit ihr VirtualBox ohne Fehler ausführen könnt. Nachdem ihr die Virtualisierung im BIOS Menü aktiviert habt, speichert ihr die Änderungen und startet den Rechner neu. 
Eine ausführlichere Anleitung findet ihr unter folgendem Link: 
https://support.bluestacks.com/hc/de/articles/115003174386-Wie-kann-ich-Virtualisierung-VT-auf-meinem-PC-aktivieren-#%E2%80%9C3%E2%80%9D

