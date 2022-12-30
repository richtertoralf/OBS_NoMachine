# OBS_NoMachine
OBS Studio in der Cloud mit Ubuntu Gnome und NoMachine
```
# Hetzner Cloud Server mieten, in der Firewall den Port 4000 für NoMachine öffnen,
# anschließend als root anmelden und dann:

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
