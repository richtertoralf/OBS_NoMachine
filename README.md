# OBS_NoMachine
OBS Studio in der Cloud mit Ubuntu Gnome und NoMachine
```
# Hetzner Cloud Server mieten, Ubuntu 22.04 LTS auswählen, in der Firewall den Port 4000 für NoMachine öffnen,
# anschließend per SSH als Benutzer "root" anmelden und dann:

apt update && apt upgrade

# Gnome und noch bissl mehr installieren
apt install x11vnc xvfb gnome-shell ubuntu-gnome-desktop autocutsel gnome-core gnome-panel gnome-themes-standard gnome-settings-daemon metacity nautilus gnome-terminal dconf-editor gnome-tweaks yaru-theme-unity yaru-theme-gnome-shell yaru-theme-gtk yaru-theme-icon fonts-ubuntu tmux fonts-emojione

# NoMachine downloaden und installieren
wget https://download.nomachine.com/download/8.2/Linux/nomachine_8.2.3_4_amd64.deb
dpkg -i nomachine_8.2.3_4_amd64.deb

# aktuelleste OBS-Studio Version installieren
apt install ffmpeg
add-apt-repository ppa:obsproject/obs-studio
apt update && apt install obs-studio

# Benutzer ohne Adminrechte hinzufügen
adduser obsNutzer

# Dies ist keine Anleitung zum Nachmachen, da unsicher, insbesondere:
# Anmeldung als root mit Passwort

# Jetzt noch den NoMachine-Client auf deinem lokalen Rechner installieren und verbinden - Fertig!
```
Die erste Anmeldung per NoMachine erfolgt als Benutzer "root". Jetzt gegebenfalls noch die Spracheinstellungen des Desktops einstellen und dann die VM neu starten.
Ab jetzt ist die standartgemäße Anmeldung per NoMachine nur noch als normaler Benutzer möglich. Das ist aktuell der Standart bei Ubuntu. Bis hierher hat dieser Benutzer auch keine "sudo-Rechte". Einstellungen sind per SSH weiterhin als Benutzer "root" möglich.
