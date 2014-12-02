Miniproject2-FMSE
=================

Das Programm liegt zum Ausf�hren als jar-Datei vor.
Die Jar muss im selben Ordner liegen wie der graphiz-Ordner,
damit Graphen zur visualisierung gezeichnet werden k�nnen.


Wie k�nnen Eingaben gemacht werden?
In einer CSV-Datei, welche als LTS �ber die Buttons 'load LTS1/LTS2' geladen werden kann.
Das Format ist hierbei wie folgt:

F�r einen Startzustand:  
I,[name][,AP1 ... ,APn]  
F�r einen anderen Zustand:  
S,[name][,AP1 ... ,APn]  
F�r eine Transition:  
T,[from],[to],[name]  

Hierbei m�ssen zun�chst Zust�nde und anschlie�end Transitions definiert werden. Wichtig ist au�erdem, dass f�r den composition operator Zust�nde nicht den selben Namen haben d�rfen! (auch nicht, wenn sie aus einem anderen LTS stammen)
Au�erdem sind die atomaren propositionen f�r einen Zustand optional.


Wie kann eine parallele Komposition erstellt werden?
Sobald �ber beide load-Buttons zwei LTS geladen wurden kann �ber den Button 'create parallel composition' die parallele Komposition erstellt werden, welche dadurch auch als Graph angezeigt wird und im Ordner in welchem sich auch die Jar befindet als png-Datei gespeichert wird. Zur weiterverarbeitung kann die parallele Komposition auch �ber den Button 'save parallel composition' als CSV-Datei gespeichert werden.
Die zuvor geladenen LTS k�nnen ebenfalls als png durch die Buttons 'show graph LTS1/LTS2' angezeigt werden.


Wie k�nnen die LTS gegen eine CTL-Formel gepr�ft werden?
Sobald wenigstens ein LTS geladen wurde kann dieses gegen eine CTL-Formel gepr�ft werden, indem sie in die Textbox eingegeben wird und durch den 'check CTL' Button ausgef�hrt werden kann.
Sollte ein LTS die Formel erf�llen, erscheint am unteren Rand der GUI ein gr�ner Punkt hinter dem entsprechenden LTS (LTS1, LTS2, LTS1||LTS2). Sollte das LTS die Formel nicht erf�llen, erscheint ein roter Punkt.
M�gliche Eingaben f�r eine Formel sind hierbei wie folgt:

EX ...  
EG ...  
EF ...  
E[ ... U ...]  
AX  
AG  
AF  
(... AND ...)  
(... OR ...)  
NOT  
TRUE  
FALSE  

Hierbei m�ssen f�r AND und OR Klammern gesetzt werden. Zudem k�nnen beliebig weitere Klammern gesetzt werden, um die Lesbarkeit f�r den Nutzer zu verbessern (nur runde Klammern).
Eingaben k�nnen beliebig gro� oder klein geschrieben werden.
Alle Worte, die nicht unter den aufgelisteten auftreten werden als atomare Proposition interpretiert.