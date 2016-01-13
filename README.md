##Futro S550 - BIOS Update (Win/Linux/OS X)

Das neueste Futro S550 BIOS V6.00 Release R1.16.2703.A2 bietet das interessante Feature "Force USB Boot".  
Das Feature wird seit BIOS V6.00 Release R1.12.2703.A2 unterstützt.  
Bei aktiviertem Feature wird **immer** von einem ggf. angesteckten USB-Stick gebootet.  
Auch ohne "F-12, 2 x runter, Enter" Gedöns.

Fujitsu bietet das Futro S550 BIOS hier an:

http://support.ts.fujitsu.com/Download/ShowFiles.asp?LNG=DE&LNID=5958&intlevel2=24334&intFehlercode=0&NavIDs=

Mit den angebotenen Tools für Windows und Unix kann eine USB-Sticks für ein BIOS Update erstellt werden.  
Um letztendlich das Update durchführen zu können, muss ein Monitor und eine Tastatur an dem Futro S550 angeschlossen sein.

---

###Worum geht es hier genau?
Mit meinem Mac hat das Erstellen des Bios-Update-USB-Sticks nur über üble Umwege funktioniert.  
Aus diesem Grunde habe ich das Bios-Update-USB-Image aus der von Fujitsu angebotenen .EXE Datei extrahiert und hier mal in Github gepackt:  

Download: [USB-Image - Update Futro S550 BIOS v6.00.1.16](https://raw.githubusercontent.com/oszilloskop/FutroS550BiosUpdate/master/2703A2R116_FD32MB.IMG)

---

###Übertragen des USB-Images auf einen USB-Stick
- unter Windows -> z.B. das Tool [Win32 Disk Imager](http://sourceforge.net/projects/win32diskimager/) benutzen
- unter Linux/OS X -> 'dd if=2703A2R116_FD32MB.IMG of=/dev/DeinUsbDevice bs=1m' (z.B. /dev/sdb (ohne 1,2,3 etc.))

---

###Warum sollte ich das Futro S550 BIOS überhaupt aktualisieren?
Ist das neueste BIOS auf dem Futro S550 installiert und ist das Feature "Force USB Boot" aktiviert, so kann z.B. sehr einfach, auch ohne angeschlossene Tastatur, ein Gluon x86 Image auf die interne CF-Karte des Futros kopiert werden (siehe [Gluon2Futro](https://github.com/oszilloskop/Gluon2Futro)).

---

###Was gibt es zu beachten?
Ist das Feature "Force USB Boot" aktiviert, so versucht der Futro S550 immer von einem angeschlossenem USB-Stick zu booten.  
**Also Obacht, falls dieses nicht gewünscht ist!**
