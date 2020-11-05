Eingabeberechtigungen
---------------------

Um Listen für die Eingabe im Webinterface zu öffnenn und wieder zu schließen, müssen entsprechende Berechtigungen angelegt werden. Ohne gültige Berechtigungen können Unterzeichner/Lehrkräfte ihre Listen im Webinterface nur einsehen, jedoch keine Eintragungen vornehmen. 

Es gibt verschiedene **Berechtigungstypen** mit unterschiedlicher Reichweite.  Durch die Reichweite ist festgelegt, für welche Schüler/Schülerinnen Eintragungen gemacht werden können. Möglich sind folgende Typen mit entsprechender Reichweite.

+---------------------+---------------------------------------------------------------------------+
| Berechtigungstyp    | Reichweite der Berechtigung                                               |
+=====================+===========================================================================+
| Klassenberechtiung  | Alle Schülerinnen/Schüler einer ganzen Klasse in allen Fächern und Kursen | 
+---------------------+---------------------------------------------------------------------------+
| Listenberechtigung  | Alle Schülerinnen/Schüler eines einzelnen Kurses/Unterrichts              |
+---------------------+---------------------------------------------------------------------------+
| Schülerberechtigung | Ein Schüler/eine Schülerin in allen Fächern und Kursen                    |
+---------------------+---------------------------------------------------------------------------+

Eingabeberechtigungen gelten immer nur für das aktuelle Halbjahr. 

Die Berechtigungen sind zudem an Löschtermine mit Datum und Uhrzeit gebunden. Wenn der Termin erreicht ist, erlischt die Berechtigung automatisch und eine Eingabe über das Webinterface ist nicht mehr möglich. 

Berechtigungen einsehen und löschen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Aktuelle Berechtigungen werden im Administrationsclient in einem separaten Fenster angezeigt. Das Fenster kann über "Fenster" > "Kursverwaltung" > "Berechtigungen" geöffnet werden und zeigt die Berechtigungen im Kontext des gerade aktiven Elements an. Wenn z. B. im Fenster "Kursmappen" eine Klasse aktiv gewählt wird, werden alle im Kontext der Klasse angelegten Berechtigungen angezeigt. 

Eine Berechtigung kann direkt im Fenster "Berechtigungen" gelöscht werden.

.. image:: /_static/images/ksnip_20200623-133309.png
    :width: 745px
    :align: center
    :alt: Löschtermin

Neue Berechtigungen anlegen
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Berechtigungen werden über Kontextfunktionen (Rechtsklick) des jeweiligen Elements angelegt. 

Klassenberechtigung
"""""""""""""""""""

Im Fenster "Kursmappen" wird durch Rechtsklick auf die Klasse das Kontextmenü geöffnet und dann "Neue Berechtigung" ausgeführt. Der erste Schritt des Dialogs kann hier übersprungen werden. Im nächsten Schritt können optional einzelne Schülerinnen/Schüler der Klasse ausgewählt werden, für die die Berechtigung *nicht* gelten soll. Für diese Schüler/Schülerinnen können dann keine Eintragungen vorgenommen werden. 

Als letztes wird im Dialog der :ref:`Löschtermin festgelegt<set-ticket-event>`. 

​Listenberechtigung
"""""""""""""""""""

Im "Navigator"-Fenster werden einen oder mehrere Kurse/Unterrichte ausgewählt und dann wird über das Kontextmenü "Neue Berechtigung" ausgeführt. Im ersten Schritt des Dialogs kann optional die Berechtigung auf einzelne Schülerinnen/Schüler des Kurses/Unterrichts eingeschränkt werden. 

Im zweiten Schritt wird der :ref:`Löschtermin festgelegt<set-ticket-event>`.

Schülerberechtigung
"""""""""""""""""""

In der Auswahlbox oben im "Navigator"-Fenster wird zunächst "Schülerinnen/Schüler" ausgewählt. Dann können ein/eine oder mehrere Schüler/Schülerinnen ausgewählt werden; dann wird über das Kontextmenü die Funktion "Neue Berechtigung" ausgeführt. Der erste Schritt des Dialogs wird übersprungen, im zweiten Schritt wird der Löschtermin festgelegt.

---------

.. _set-ticket-event:

Im letzten Schritt des Dialogs zum Erstellen einer neuen Berechtigung wird der **Löschtermin festgelegt**. Dieser Schritt ist für alle Berechtigungstypen gleich. Es muss der Zeitpunkt gewählt werden, zu dem die Berechtigung ungültig wird. 

Es wird entweder ein neuer Termin (Kalendereintrag) festgelegt oder die Berechtigung wird einem schon vorhandenen, noch in der Zukunft liegenden Termin hinzugefügt. Dazu müssen Datum und Uhrzeit sowie eine Zusammenfassung (z. B. "Eintragungsschluss Sommer 2019" o. Ä.) eingegeben werden. 

.. image:: /_static/images/ksnip_20200623-132806.png
    :width: 678px
    :align: center
    :alt: Löschtermin