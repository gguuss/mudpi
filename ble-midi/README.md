# BLE Midi scripts

Mostly in Ruby and described in this blog post:

https://neuma.studio/rpi-midi-complete.html


# Install Midi Service

```
git submodule update
sudo apt-get install -y autotools-dev libtool autoconf
sudo apt-get install -y libasound2-dev
sudo apt-get install -y libusb-dev libdbus-1-dev libglib2.0-dev libudev-dev libical-dev libreadline-dev 
sudo apt-get install glib2.0 libdbus-1-dev libudev-dev libical-dev libreadline-dev
cd bluez
./bootstrap
./configure --enable-midi --prefix=/usr --mandir=/usr/share/man --sysconfdir=/etc --localstatedir=/var
make
sudo make install
```

After you have installed the bluez service, you can start it listening
with:

```
sudo btmidi-server -v -n "RPi Bluetooth"
```

# Connecting to the device
There is a [Windows app for this](http://www.tobias-erichsen.de/software/rtpmidi/rtpmidi-tutorial.html)

Install it and then point it to the pi, the device will show up in your DAW.
