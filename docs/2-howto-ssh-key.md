# SSH Key für den Zugang ohne Kennwort einrichten


Beachte: 
- ``<username>`` bezieht sich auf den bei der Einrichtung angegebenen Benutzernamen.
- ``<hostname>`` bezieht sich auf den bei der Einrichtung angegebenen Hostnamen
- Das hier beschriebene Verfahren wurde unter der WSL auf Windows ausgeführt
- Für Details siehe zum Beispiel https://linuxize.com/post/how-to-set-up-ssh-keys-on-debian-10/

## Step 1: ssh-key generieren
````
# Achtung: standard-ausgabedatei ändern um. ~/.ssh/id_rsa nicht zu überschreiben
ssh-keygen -t rsa -b 4096 -C <username>@mydomain``
````

## Step 2: ssh-key kopieren


````
ssh-copy-id -i <ausgabedatei> <username>@<hostname>
````


## Step 3: Test Anmeldung

````
ssh -i <ausgabedatei> <username>@<hostname>
````

## Step 4: Private und Public-Key sichern

Zum Beispiel in keypass.
