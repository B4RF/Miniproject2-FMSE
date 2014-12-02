Miniproject2-FMSE
=================

Das Programm liegt zum Ausführen als jar-Datei vor.
Die Jar muss im selben Ordner liegen wie der graphiz-Ordner,
damit Graphen zur visualisierung gezeichnet werden können.


Wie können Eingaben gemacht werden?
In einer CSV-Datei, welche als LTS über die Buttons 'load LTS1/LTS2' geladen werden kann.
Das Format ist hierbei wie folgt:

Für einen Startzustand:  
I,[name][,AP1 ... ,APn]  
Für einen anderen Zustand:  
S,[name][,AP1 ... ,APn]  
Für eine Transition:  
T,[from],[to],[name]  

Hierbei müssen zunächst Zustände und anschließend Transitions definiert werden. Wichtig ist außerdem, dass für den composition operator Zustände nicht den selben Namen haben dürfen! (auch nicht, wenn sie aus einem anderen LTS stammen)
Außerdem sind die atomaren propositionen für einen Zustand optional.


Wie kann eine parallele Komposition erstellt werden?
Sobald über beide load-Buttons zwei LTS geladen wurden kann über den Button 'create parallel composition' die parallele Komposition erstellt werden, welche dadurch auch als Graph angezeigt wird und im Ordner in welchem sich auch die Jar befindet als png-Datei gespeichert wird. Zur weiterverarbeitung kann die parallele Komposition auch über den Button 'save parallel composition' als CSV-Datei gespeichert werden.
Die zuvor geladenen LTS können ebenfalls als png durch die Buttons 'show graph LTS1/LTS2' angezeigt werden.


Wie können die LTS gegen eine CTL-Formel geprüft werden?
Sobald wenigstens ein LTS geladen wurde kann dieses gegen eine CTL-Formel geprüft werden, indem sie in die Textbox eingegeben wird und durch den 'check CTL' Button ausgeführt werden kann.
Sollte ein LTS die Formel erfüllen, erscheint am unteren Rand der GUI ein grüner Punkt hinter dem entsprechenden LTS (LTS1, LTS2, LTS1||LTS2). Sollte das LTS die Formel nicht erfüllen, erscheint ein roter Punkt.
Mögliche Eingaben für eine Formel sind hierbei wie folgt:

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

Hierbei müssen für AND und OR Klammern gesetzt werden. Zudem können beliebig weitere Klammern gesetzt werden, um die Lesbarkeit für den Nutzer zu verbessern (nur runde Klammern).
Eingaben können beliebig groß oder klein geschrieben werden.
Alle Worte, die nicht unter den aufgelisteten auftreten werden als atomare Proposition interpretiert.