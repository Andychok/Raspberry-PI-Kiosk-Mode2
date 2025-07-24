# 🔧 Schritt-für-Schritt-Anleitung: Raspberry Pi im Kiosk-Modus

> Achte darauf, dass du mit dem Internet verbunden bist.

---

### 1. Öffne das Terminal

---

### 2. Verzeichnis Autostart-Ordner anlegen

```bash
mkdir -p "$HOME/.config/autostart"
```

---

### 3. Kiosk-Startdatei erstellen

```bash
nano "$HOME/.config/autostart/kiosk.desktop"
```

---

### 4. Inhalt der Datei einfügen:

```ini
[Desktop Entry]
Type=Application
Name=Kiosk
Exec=chromium-browser --noerrdialogs --disable-infobars --disable-pinch --overscroll-history-navigation=0 --kiosk https://example.com
Hidden=false
NoDisplay=false
X-GNOME-Autostart-enabled=true
StartupNotify=false
```

Speichern mit:
- `Ctrl + X`
- Dann `Y` drücken
- Dann `Enter` drücken

---

### 5. Neustarten und testen

```bash
sudo reboot
```
