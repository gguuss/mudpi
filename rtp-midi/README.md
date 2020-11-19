# Install services to pi


```
sudo apt update
sudo apt install snapd
sudo reboot
sudo snap install avahi
sudo apt-get install avahi-utils libavahi-client-dev
```

# Install reveloxmidi
```
pushd pimidi/raveloxmidi 
sh ./autogen.sh
./configure
make
sudo make install
popd
```

# Run raveloxmidi
```
raveloxmidi -c raveloxmidi.config
```
