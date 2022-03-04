# Einrichtung einer headless raspberry 4 node 

## Step 1:Raspberry Pi imager installieren

1. Herunterladen von https://downloads.raspberrypi.org/imager/imager_latest.exe
2. Installation ausführen

## Step 2: Betriebssystem herunterladen

1. Auswahl über https://www.raspberrypi.com/software/operating-systems/
2. Raspberry Pi OS Lite (32 Bit) von hier heruntergeladen: https://downloads.raspberrypi.org/raspios_lite_armhf/images/raspios_lite_armhf-2022-01-28/2022-01-28-raspios-bullseye-armhf-lite.zip
3. .zip Datei entpacken -> ``.img``-Datei

## Step 3: SD Card vorbereiten
1. SD Card einlegen
2. Windows->Einstellungen->Datenträgerverwaltung
3. SD-Card Identifizieren
4. Alle Partitionen löschen

## Step 4: Betriebssystem Image auf SD Card schreiben

1. Raspberry Pi Imager starten
2. ``.img.``-Datei auswählen
3. SD Card auswählen
4. Einstellungen wählen
5. ``Overscan deaktivieren`` nicht aktiviert
6. Hostname setzten
7. SSH aktivieren (Password zur Authentifizierung verwenden)
8. Benutzername und Kennwort setzen
9. Wifi nicht aktiviert
10. Spracheinstellungen festlegen: Zeitzone=Europe/Berlin, Tastaturlayout=de
11. ``Einrichtungsassistent überspringen`` nicht aktiviert
12. Schreiben

## Step 5: Starten (DHCP Server im Netz vorhanden)

1. SD Karte in Raspi einlegen
2. Netzwerkkarte anschließen
3. (optional) HDMI Monitor für Kontrolle anschließen
4. Strom einschalten
5. Warten (Größenordnung 2 Minuten) + ``ping <hostname>``; Eventuell Monitor anschließen und Fehlermeldungen beachten.
6. Anmelden: ``ssh <benutzername>@hostname``


