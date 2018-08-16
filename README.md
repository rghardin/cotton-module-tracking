### The mercury library is open source code from Github from contributor gotthardp.
### This code active RFID associate with GPS and record RFID info with GPS in raspberry pi.

Download this package first and unpack it at root folder of raspberry pi

### Mercury library installation on raspberry pi 3

Open the terminal on your RPi 3 and type the following cmd line:

```bash
apt-get install patch xsltproc gcc libreadline-dev python-dev
```

Go to the folder where you unpacked the package, and build the module simply by running
```bash
cd python-mercuryapi
make
```
This will download and build the [Mercury API SDK](http://www.thingmagic.com/index.php/manuals-firmware)
and then it will build the Python module itself.


Then, install the module by running
```bash
sudo make install
```
which is a shortcut to running
```bash
sudo python setup.py install
```

To access ports like `/dev/ttyUSB0` as a non-root user you may need to add this
user to the `dialout` group:
```bash
sudo usermod -a -G dialout $USER
```
