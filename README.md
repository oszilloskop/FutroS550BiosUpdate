## Futro S550 - BIOS Update (Win/Linux/OS X)

Der Futro S550 bietet ab BIOS V6.00 Release R1.12.2703.A2 das interessante Feature "Force USB Boot".  
Bei aktiviertem Feature wird **immer** von einem ggf. angesteckten USB-Stick gebootet.  
Auch ohne "F-12, 2 x runter, Enter" Gedöns.

Fujitsu bietet hier das aktuelle Futro S550 BIOS an:

http://support.ts.fujitsu.com/IndexDownload.asp  (hier nach s550 suchen)

Mit den angebotenen Tools für Windows und Unix kann eine USB-Sticks für ein BIOS Update erstellt werden.  
Um letztendlich das Update durchführen zu können, muss ein Monitor und eine Tastatur an dem Futro S550 angeschlossen sein.

---

### Worum geht es hier genau?
Auf meinen Futros waren nur sehr alte BIOS-Versionen, und mit meinem Mac hat das Erstellen des BIOS-Update-USB-Sticks nur über üble Umwege funktioniert.  
Aus diesem Grunde habe ich das aktuelle BIOS-Update-USB-Image aus einer von Fujitsu angebotenen .EXE Datei extrahiert und mal hier in Github abgelegt:  

**Download:** [USB-Image - Update Futro S550 BIOS V6.00 Release R1.16.2703.A2](https://raw.githubusercontent.com/oszilloskop/FutroS550BiosUpdate/master/2703A2R116_FD32MB.IMG)

---

### Übertragen des USB-Images auf einen USB-Stick
- unter Windows -> z.B. das Tool [Win32 Disk Imager](http://sourceforge.net/projects/win32diskimager/) benutzen
- unter Mac OS X -> z.B. das Tool [ApplePi-Baker](http://www.tweaking4all.com/hardware/raspberry-pi/macosx-apple-pi-baker) benutzen
- unter Linux -> 'dd status=progress if=2703A2R116_FD32MB.IMG of=/dev/DeinUsbDevice bs=1M' (z.B. /dev/sdb (ohne 1,2,3 etc.))

---

### Warum sollte ich das Futro S550 BIOS überhaupt aktualisieren?
Ist das neueste BIOS auf dem Futro S550 installiert und ist das Feature "Force USB Boot" aktiviert, so kann z.B. sehr einfach, auch ohne angeschlossene Tastatur, ein Gluon x86 Image auf die interne CF-Karte des Futros kopiert werden (siehe [Gluon2Futro](https://github.com/oszilloskop/Gluon2Futro)).

---

### Was gibt es zu beachten?
Ist das Feature "Force USB Boot" aktiviert, so versucht der Futro S550 wirklich **immer** von einem ggf. angeschlossenen USB-Stick zu booten.  
**Also Obacht, falls dieses nicht gewünscht ist!**
