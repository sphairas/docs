Konfiguration der Zeugnisbemerkungen
------------------------------------

Über die Weboberfläche können Klassenlehrkräfte für die Zeugnisse aus einem konfigurierbaren Satz vorformulierte Textbemerkungen auswählen. Die Auswahl und Anordnung der vorformulierten Bemerkungen erfolgt im Administrationsclient. 

Je nach installiertem Modul stehen für die Konfiguration der Zeugnisbemerkungen einerseits Sätze von länder- und schulformspezifischen Bemerkungen zur Verfügung. Andererseits können eigene Bemerkungen der Schule formuliert werden. 

Der Konfiguration der Zeugnisbemerkungen wird im Fenster "Konfigurationen" ("Fenster" > "Konfigurationen") über [Mandant >] "Zeugnisbemerkungen" geöffnet. In der Ansicht "Struktur" wird die Anordnung und Sichtbarkeit der Bemerkungen festgelegt. In der Ansicht "Texte" werden die Texte der eigenen Bemerkungen der Schule editiert. 

Anordnung und Sichtbarkeit der Bemerkungen
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die Anordnung und Sichtbarkeit der vorhandenen Bemerkungen in der Weboberfläche wird in der Ansicht "Struktur" festgelegt. 

.. image:: /_static/images/ksnip_20211208-201406.png
    :width: 1411px
    :align: center
    :alt: Zeugnisbemerkungen Struktur

Die Struktur der Bemerkungen in der Weboberfläche ist in Abschnitte gegliedert. Die Reihenfolge der Abschnitte bestimmt die Reihenfolge der Bemerkungen im Zeugnis. Sowohl die Abschnitte als auch die Bemerkungen können verschoben und (Rechtsklick) gelöscht werden. 

Aus der Palette (rechts) können neue Bemerkungen in die Struktur hineingezogen werden. Zur Auswahl stehen zwei Kategorien von Bemerkungen: Standard-Zeugnisbemerkungen für das Bundesland und die schuleigenen Bemerkungen. 

Für jeden Abschnitt kann (über Rechtsklick und "Einstellungen") festgelegt werden, ob eine Mehrfachauswahl der Bemerkungen in dem Abschnitt möglich ist oder nur eine Bemerkung des Abschnitts ausgewählt werden kann. Falls nur eine Bemerkung des Abschnitts ausgewählt werden kann, kann optional eingestellt werden, dass eine der vorgegebenen Bemerkungen obligatorisch auszuwählen ist (und damit einer der Bemerkungen des Abschnitts im Zeugnis erscheinen muss).

.. image:: /_static/images/ksnip_20211228-095317.png
    :width: 328px
    :align: center
    :alt: Zeugnisbemerkungen Einstellungen

Außerdem kann über diesen Dialog der Name des Abschnitts geändert werden. 

Änderungen müssen unbedingt gespeichert werden. 

Schuleigene Bemerkungen editieren
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Die schuleigenen Bemerkungen werden in der Ansicht "Texte" erstellt und editiert. 

.. image:: /_static/images/ksnip_20211208-204554.png
    :width: 1087px
    :align: center
    :alt: Zeugnisbemerkungen Texte

.. warning:: 
    Alle Bemerkungen in einzelnen Zeugnissen sind Referenzen auf die standardisierten Texte. Sobald ein Text mindestens einmal in einem Zeugnis verwendet (eingefügt) wurde, sollte die standardisierte Bemerkung nie wieder gelöscht werden. 

    In den xml-Dateien der Zeungnisse werden die Referenzen mit den Texten ersetzt. 

Eine neue Bemerkung wird mit (1) hinzugefügt und im Editor (2) bearbeitet. Es stehen eine Reihe von Platzhaltern zur Verfügung (3).

Änderungen müssen auch hier unbedingt gespeichert werden. 