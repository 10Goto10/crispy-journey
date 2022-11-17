# Lern-Bericht
Noah Meier

## Einleitung

Ich bin gerade daran, Assembly für den 6502 Prozessor zu lernen, was mir hilft die internen Prozesse eines Computers zu verstehen.

## Was habe ich gelernt?

Ich habe gelernt, wie ich einen loop programmieren kann, der sich z.B. 5 mal wiederholt.

## Beschreibung


Ich habe gelernt, wie ich die verschiedenen Branch-Istructions des 6502 benutzen kann, um einen loop zu machen.
Jedes Computermodell, welches den 6502 verwendet, hat verschiedene Addressen, in die geschrieben werden muss, um z.B. die Farbe des Bildschirmrahmens zu ändern.
Dieses Programm ist für den Commodore VC20. Ich habe diesen Computer gewählt, da er simpler zu programmieren ist als der C64.



"Colors" ist lediglich ein sogenanntes Label, es wird schlussendlich nicht im Speicher auftauchen.
Bei der bcc-Instruktion wird es durch die Speicheradresse der inx-Instruktion ersetzt.
``

        ldx #$00      ;lade die Zahl 0 ins X-Register
        
colors                ; 

        inx           ;ändere die Zahl im X-Register um 1
        
        stx $900f     ;schreibe die Zahl im X-Register in die Speicheraddresse $900f (das $ zeigt an, dass es sich hier um eine Hexadezimale Zahl handelt)
        
        cpx #$ff      ;vergleiche X mit der zahl 255 (hex ff)
        
        bcc colors    ;falls die Zahlen nich gleich sind, wiederhole den loop
        
 ``       
        
        
![Vic20](https://user-images.githubusercontent.com/111045975/185336578-e85422a9-2b07-4ad1-b291-8d0b2d12671e.png)
        


## Verifikation

Das Bild zeigt, was passiert, wenn das oben beschriebene Programm ausgeführt wird.


# Reflektion zum Arbeitsprozess

Ich habe ziemlich schnell den Grundsatz der Assembly-Programmierung verstanden.
Das schreiben des Programmes war allerdings sehr mühsam, da es oft nicht klar ist, wo sich der Fehler Befindet.
Ich habe auch in sehr unregelmässigen Zeitabständen Programmiert.

Ich werde mir desshalb vornehmen, weniger unregelmässig zu Programmieren.
   




