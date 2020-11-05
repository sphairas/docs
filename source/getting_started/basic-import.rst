.. _basic-import:

Datenimport aus Listen
======================

Für die Arbeit mit *sphairas* müssen die Lehrkräfte (als "Unterzeichner" der Zensurenlisten), die Schülerinnen und Schüler mit allen für den Zeugnisdruck relevanten Daten sowie die Unterrichte im Klassen- oder Kursverband angelegt werden. Das System geht dabei davon aus, dass diese Daten aus anderen Schulverwaltungssystemen übernommen werden. Daher werden alle Daten grundsätzlich importiert. 

Ein Import ist flexibel über Listen im csv-, Open Document- oder Microsoft Excel-Format möglich. Außerdem können Daten aus SiBank Plus und Untis übernommen werden. 

Identitätsmanagement und Import-Konfiguration
---------------------------------------------

Beim Datenimport übernimmt *sphairas* grundsätzlich die Identitäten des Ursprungssystems, macht sie aber global eindeutig und unverwechselbar. Dazu wird die Identität mit einem Zusatz verstehen, der für die für die Datenidentität "zuständige Stelle" ("authority" in den Konfigurationsdateien) steht. 

Wenn beispielsweise der Datensatz für eine fiktive Schülerin Karla K. aus DaNiS exportiert und in *sphairas* importiert wird, wird die in DaNiS z. B. verwendete numerische ID 1000248762145875 übernommen und dabei mit einem Stellenteil ("authority") versehen, der z. B. "meine-schule-irgendwo.de/danis/v2015" lauten kann. Der Stellenteil besteht hier aus dem Haupt-Domänennamen der Schule und einem Bezeicher für die vewendete DaNiS-Datenbank, also z. B. das 2015 installierte System. Die vollständige Identität der Schülerin in *sphairas* wird dann ``1000248762145875@meine-schule-irgendwo.de/danis/v2015`` und diese ist global eindeutig und unverwechselbar. 

Da im Allgemeinen in einem Produktivsystem immer aus der gleichen Quelle importiert wird, wird der beim Import eingesetzte Stellenteil in der Konfiguration von *sphairas* festgelegt. Dabei sollten die Standardwerte in einem Produktivsystem vor dem ersten Import unbedingt angepasst werden. 

Auch Kurs-, Klassen- und Zensurenlisten sowie Unterrichte habe global eindeutige Identitäten. Diese müssen beim Import allerdings meistens erst erzeugt werden, weil exportierte Klassen- und Kursbezeichner i. A. nur innerhalb eines Schuljahres Gültigkeit haben. Die Namen "Klasse 6d" oder "Englisch 9a" sind i. A. nur innerhalb eines Schuljahres eindeutig. Deshalb unterscheidet *sphairas* zwischen Identität und Anzeigename. Der Anzeigename kann nach vorgegebenen, aber prinzipiell konfigurierbaren Regeln aus der Identität abgeleitet werden. Bei einer weiterführende Schule (Einschulung in Jahrgang 5) könnte die Identität der obigen Klasse z. B. "klasse-2018-d", wenn diese Klasse im Schuljahr 2019/2020 die "Klasse 6d" ist. Im Schuljahr 2022/2023 würde diese Klassen-ID zu "Klasse 9d" aufgelöst. Die vollständige Identität hat auch wieder einen Stellenbezeichner und könnte bei dieser fiktiven Klassen z. B. ``klasse-2018-d@meine-schule-irgendwo.de/v1`` sein, wobei der Stellenbezeichner auch die Regeln für die Namensauflösung identifiziert. 

Import von Unterzeichnern (Lehrkräften)
---------------------------------------

Wenn das System die IServ-Authentifizierung nutzt, können alle Lehrkräfte über eine einfache Tabelle nach folgendem Muster importiert werden: :download:`DemoLehrer.xlsx</_static/files/DemoLehrer.xlsx>`. Der Domänenteil in der E-Mail muss dabei der IServ-Domäne (hostname) entsprechen. 

Für den Import öffnen Sie über "Datenimport" > "Import aus Tabelle (Lehrer/Unterzeichner)" die Import-Tabelle. Im ersten Schritt des Importdialogs müssen Zielmandant und Schuljahrhalbjahr ausgewählt werden. Im nächsten Schritt müssen Sie die Spalten aus der Importtabelle (links) den Importkategorien zuweisen: 


.. image:: /_static/images/ksnip_20200608-124310.png
    :width: 653px
    :align: center
    :alt: Import von Unterzeichnern

Im letzten Schritt wählen Sie die zu importierenden Lehrerinnen und Lehrer aus und klicken dann auf "Fertigstellen". Im Fenster "Ausgabe - Import" sehen Sie, wie viele Lehrkräfte erfolgreich importiert wurden. 


Import von Schülerinnen/Schülern und Klassen
--------------------------------------------

Schülerinnen und Schüler können über eine Tabelle nach folgendem Muster importiert werden: :download:`DemoSchülerInnen.ods</_static/files/DemoSchülerInnen.ods>`. Für den Import öffnen Sie über "Datenimport" > "Import aus Tabelle (Klassen)" die Import-Tabelle. 

Im ersten Schritt des Importdialogs müssen wieder Zielmandant und Schuljahrhalbjahr ausgewählt werden. Im nächsten Schritt müssen Sie die Spalten aus der Importtabelle (links) den Importkategorien zuweisen. Dabei muss der Klassenname (Tabellenspalte) als Schlüssel ausgewählt werden, nach dem die Schülerinnen/Schüler (Tabellenspalten) grupiert werden.

.. image:: /_static/images/ksnip_20200607-192647.png
    :width: 653px
    :align: center
    :alt: Import von Schülerinnen/Schülern

Im nächsten Schritt wählen Sie die Klassen, die tatsächlich importiert werden sollen, aus. Dabei wird auch die generierte ID ("Gruppe") und der entsprechende Anzeigename gezeigt. 

.. image:: /_static/images/ksnip_20200609-101956.png
    :width: 894px
    :align: center
    :alt: Import von Schülerinnen/Schülern - Klassenbezeichner

Im letzten Schritt wählen Sie die zu importierenden Schülerinnen und Schüler aus und klicken dann auf "Fertigstellen". Im Fenster "Ausgabe - Import" sehen Sie, wie viele Schülerinnen/Schüler erfolgreich importiert wurden. 

Unterrichte
-----------

Unterricht kann über eine Tabelle nach folgendem Muster importiert werden: :download:`Unterrichtsverteilung.xlsx</_static/files/Unterrichtsverteilung.xlsx>`. Für den Import öffnen Sie über "Datenimport" > "Import aus Tabelle (Unterricht/Kurse)" die Import-Tabelle. 

Im ersten Schritt des Importdialogs müssen wieder Zielmandant und Schuljahr ausgewählt werden. Im nächsten Schritt müssen Sie auch wieder die Spalten aus der Importtabelle (links) den Importkategorien zuweisen:

.. image:: /_static/images/ksnip_20200609-095404.png
    :width: 626px
    :align: center
    :alt: Import von Unterricht

Im nächsten Schritt können die Vorgaben für die Unterrichte angepasst und ergänzt werden. Wählen Sie dabei aus, welche Unterrichte tatsächlich importiert werden sollen (1):

.. image:: /_static/images/ksnip_20200609-095730.png
    :width: 1434px
    :align: center
    :alt: Import von Unterricht - Unterrichtseinstellungen

Sie können die Gruppe (hier: Klasse), für die der Unterricht angelegt wird, ändern und es wird der aktuelle Anzeigename der Gruppe angegeben (2). 

Für die Schülerinnen und Schüler der entsprechenden "Gruppenliste" (hier: Klasse) werden in der "Zensurenliste" für das gewählte Halbjahr Einträge angelegt. Aus der Gruppen-Identität und dem gewählten Unterrichtsfach (3) ergibt sich der Name der Zensurenliste (4), in der für das gewählte Halbjahr für alle Schülerinnen und Schüler der Gruppe Einträge angelegt werden. 

In den Standardeinstellungen wird ein "?"-Eintrag angelegt, wenn ein Fachlehrer/eine Fachlehrerin (Listen-Unterzeichner) angegeben ist (5); wenn keine Lehrkraft angegeben wird, wird ein "n.e."-Eintrag erzeugt. Das Standard-Notensystem der Liste sollte ebenfalls ausgewählt werden (6). 

Klicken Sie dann auf "Fertigstellen". Im Fenster "Ausgabe - Import" sehen Sie wieder, welche Kurslisten erfolgreich importiert wurden. 
