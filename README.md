# PiParty

Pure Data improv patch for Raspberry Pi.

Tested on a Raspberry Pi 4B + PiSound.

**TigerVNC**

Flash SD card with default Raspberry Pi OS.

TigerVNC can be used to screenshare with the Pi.

```sh
sudo apt update && sudo apt upgrade
sudo apt install tigervnc-standalone-server
sudo nano /etc/tigervnc/vncserver-config-mandatory
```

Change `$localhost = "no";`

```sh
sudo tigervncpasswd
tigervncserver
```

Note that `tigervncserver` needs to be run every time after boot to allow screenshare.

Raspberry Pi can be reach from client machine pointed at `raspberry-pi-ip:5901`.

**Pure Data**

Install Pure Data with

```sh
sudo apt-get update
sudo apt-get -y install git puredata
pd -version
```

**Controls**

Buttons work in combination to momentarily or persistently enable each effect.

| Numb | FX | Knob | Slider |
| -- | -- | -- | -- |
| 1 | Delay | Time | Gain |
