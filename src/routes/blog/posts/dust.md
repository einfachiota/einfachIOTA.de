---
title: Was ist die "Dust-Protection"?
date: "2021-03-15"
---

der sicherheitsmechanismus gegen Staub einfach erklärt!


<!-- more -->

Da IOTA "feeless", also gebührenfrei ist, und man Mikrotransaktionen senden kann also zum Beipsiel 1 IOTA, können Angreifer damit das Netzwerk sehr einfach "zuspammen". Dies bezeichnen wir als "Dust", also "Staub". Um dies zu vermeiden, erlauben wir nur Mikrotransaktionen unter 1Mi IOTA-Token an eine andere Adresse, wenn Sie bereits mit mindestens 1Mi aufgaladen wurde.

## Wie funktioniert das?
Die Dust Protection ist fest im Kernprotokoll verankert.
 
Jede Node muss den Kontostand jeder einzelnen adresse (abgesehen von null wert adressen) - kennen. Ansonsten könnte man ja mehr Geld ausgeben als man hat, der klassische `double spent`. 

Diesen Umstand könnte man jedoch als Angriffsvektor nutzen, in dem man einfach ganz viele Adressen mit jeweils 1i value "auflädt", denn dann müssten alle diese Adressen vom gesamten Netzwerk gespeichert werden, und so würde der Speicherbedarf den jede Node grundsätzlich braucht (selbst ohne die aktuelle Historie aller Transaktionen zu sichern) bereits ins Unermessliche wachsen. Um das Ganze noch einmal zu verdeutlichen, mit 1Mi (gegenwert zum zeitpunkt dieses Artikels in etwa 1,40$) - könnte man bereits eine Million adressen mit jeweils einem iota "Dusten", und diese müssten für immer alle von allen Nodes gesichert werden. Dies wird deutlich teuerer für einen Angreifer - und somit faktisch nicht "bezahlbar" mit der einführung einer "minimum balance", also einem minimalem Guthaben das jede Adresse haben muss nach Chrysalis. Genau genommen liegt dieser Wert bei mindestens einem Mega Iota pro Adresse. 

Jedoch wird es dadurch nicht unmöglich auch kleinere Beträge zu senden. Denn sobald eine Adresse diese minimale Anzahl an Wert besitzt, kann man damit 10 kleinere Transaktionen von beliebiger höhe empfangen, bis man wieder den Mindestwert aufladen muss. Jedoch ist hierfür noch weiterer Handlungsbedarf nötig - man muss so genannte `"SigLockedDustAllowanceOutputs"` freischalten.

[RFC Link (auf English)](https://github.com/iotaledger/protocol-rfcs/pull/32)

