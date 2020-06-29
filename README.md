# StromerAPI

StromerV120530.exe\
XC800_fload.exe\
Stromer_866_V075.hex

XC886/888CLM\
8-Bit Single Chip Microcontroller

![Screenshot](https://raw.githubusercontent.com/ErwinMeulman/StromerAPI/master/CazpYLG.png)

![Screenshot](https://electricbikereview.com/forums/attachments/stromer-wiring-jpg.25682/)


S11-XXXXX > Serie 2011
S13-XXXXX > Serie 2013
S18-XXXXX > Serie 2018

Für die die noch mehr Informationen wollen:
500W TCDM 
Hall Sensor SS461R von Honeywell, reagiert auf Magnet Nord
Batterie Auswertung (Ladezustand) 
36V zu 5V DC Converter
Auswertung TMM4 Sensor sowie Sinus generierung durch 8 Bit Prozessor Infineon XC-866
Kommunikation mit dem Display via UART Rx/Tx 
12 x Mosfet Transistor

5 Poliger Sensor Kabel für Display:
Blau - 36V OUT Battery (Signalisiert dass die Batterie angeschlossen ist am Display) Wenn keine verbindung / Kablebruch NO_BATT
Weiss - 36V IN KEY (Signalisiert dass das Display Ready ist und nicht LOCKED)
Grün - TXD (UART) Wenn keine verbindung / Kablebruch NO_COM, falsche kommunikation ICURR
Gelb - RXD (UART) Wenn keine verbindung / Kablebruch NO_COM[b], [/b]falsche kommunikation ICURR
Schwarz - GND (-)


2 Pol (Programmierstecker): Wenn verbunden geht der Prozessor in Flash Modus!
Schwarz - GND
Schwarz-weiss - MBC


3 Pol (TMM Kabel):
Rot - 5V
Braun - GND
Orange - Signal


Mit Infineon XC-866 verbinden (UART)
1. Blau und Weiss verbinden
2. Grün - TXD, Gelb - RXD, Schwarz - GND am USB RS232 verbinden
3. Batterie anschliessen
4. Infineon Memtool öffnen
5. Baudrate auf 57600 setzten
6. verbinden
7 Daten auslesen (Maschinencode)
