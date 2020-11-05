Einrichten des Administrations-Clients
======================================

Der *sphairas*-Server wird nicht über seine eigene Weboberfläche, sondern mit einer separaten Anwendung administriert. Über diese Anwendung erfolgt u. a. der Import von Schülerlisten und Unterrichten und die Steuerrung der Zugriffszeiten und -berechtigungen. 

Der *sphairas*-Administrationsclient ist eine Java-basierte Anwendung, die auf der Grundlage der `NetBeans-Plattform <https://netbeans.apache.org>`_ entwickelt wird und daher ohne Weiteres in allen gängigen Betriebssystem lauffähig ist. Komplilierte Entwicklerversionen stehen unter `<https://github.com/sphairas/sphairas-desktop/releases>`_ bereit.

Installation
------------

Das Programm kann mithilfe der Installations-Executables für Windows und Linux installiert werden. Unter Windows sind dazu Administrationsrechte erforderlich. 

Alternativ dazu kann die Datei ``sphairas.zip`` entpackt und die Anwendung über die Launcher im Unterverzeichnis ``bin`` gestartet werden. Dazu muss auf dem Arbeitsplatz Java mindestens in der Version 11 installiert sein. Wenn bei dieser Installationsvariante Java auf dem Arbeitsplatz nicht gefunden wird, kann der Switch ``--jdkhome <dir>`` verwendet werden. 

Das Programm kann mehrere Datenbanken (Mandanten) gleichzeitig administrieren. Die Authentifizierung gegenüber dem Server und damit den Datenbanken erfolgt über ein persönliches SSL-Client-Zertifikat. Das Zertifikat enthält den Namen des Nutzers mit Administrationsrechten. Für jeden Mandanten muss ein persönliches Zertifikat importiert werden. Auf diese Weise können zwar mehrere Mandanten gleicheitig verwaltet werden, es kann pro Arbeitsplatz allerdings immer nur ein Benutzer angemeldet werden. 

Das Zertifikat wird verschlüsselt im Benutzerkonto auf Betriebssystemebene abgelegt. Jeder *sphairas*-Administrator muss mit einem persönlichen Benutzerkonto auf Betriebssystemebene an dem Arbeitsplatz angemeldet sein. 

Die *sphairas*-Administratoren laden i. A. regelmäßig druckfertige Zeugnissätze und umfangreiche Zensurenlisten auf ihren Arbeitsplatz, sodass eine Bindung des *sphairas*-Administratorenkontos an ein Nutzerkonto auf Betriebssytemebene sinnvoll ist. 

Bei der ersten Installation muss der neue Nutzer bestätigen, dass es sich bei dem Arbeitsplatz um ein persönliches Benutzerkonto handelt. Außerdem muss ein Passwort festgelegt werden, mit dem gespeicherte Zertifikate ggf. wiederhergestellt werden können. Dieses Passwort sollte im Konto des Benutzers auf Betriebssystemebene gespeichert werden. In diesem Fall wird es später nur in Ausnahmefällen benötigt. 

Schlüsselimport und Anlegen eines Mandanten
-------------------------------------------

Ein Nutzerschlüssel wird an der Konsole des Servers mit erzeugt. Wenn der Server eine Docker-Installation ist, kann das Skript mit ``docker exec -it <container> generate-admin-key`` gestartet werden. Anschließend wird der Schlüssel über "Extras" > "Zertifikat/Schlüssel importieren" importiert. Der Schlüssel wird intern unter dem Mandantennamen ("provider") gespeichert. Der Mandantenname entspricht der Umgebungsvariable ``SPAIRAS_PROVIDER`` in der Serverinstallation. Wenn der Schlüssel bzw. das Zertifikat erfolgreich installiert wurde, erscheint unten links kurzzeitg eine Statusmeldung. 

Sobald ein Schlüssel importiert wurde, kann über "Datei" > "Neuer Mandant" der zugehörige Mandant angelegt werden. Dazu muss der (ggf. lokale) Servername angegeben werden. Falls der Servername nicht dem Mandantennamen entspricht, kann der Mandantenname optional unter "Schlüssel mit anderem Namen verwenden" angegeben werden. 

.. image:: /_static/images/ksnip_20200604-154022.png
    :width: 647px
    :align: center
    :alt: Schlüsselimport

Bei Erfolg erscheint wiederum kurzzeitig eine Statusmeldung. 

Jahrgänge abonnieren
--------------------

Um eine völlig neue Serverinstallation zu nutzen, sollten als nächstes Schülerdaten bzw. Klassen sowie ggf. "Unterzeichner" (Lehrinnen/Lehrer) und Unterrichte angelegt bzw. :ref:`importiert<basic-import>` werden. Danach, oder wenn der Client an ein Produktivsystem angebunden wird, können Schülerjahrgänge abonniert werden. 

Ein Jahrgang wird als Kursmappe angelegt, in dem "Datei" > "Neue Kursmappe" ausgeführt wird. Danach muss in der Kategrie "Kursmappen" ein Projekt "Jahrgang" gewählt werden (einzige Möglichkeit). 

Im nächsten Schritt wählen Sie den Mandanten und dann das Jahr aus, in dem der Jahrgang an der Schule eingeschult wurde (i. A. 1. oder 5. Klasse). Damit wird der Jahrgang abonniert und Sie können alle Unterrichte und Zensuren dieses Jahrgang sehen und verwalten.  