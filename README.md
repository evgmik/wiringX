PULL REQUESTS ARE ONLY ACCEPTED TOWARDS THE REWRITE BRANCH, THIS BRANCH WILL BECOME OBSOLETE SOON
=======

wiringX
========

wiringX is a modular approach to several GPIO interfaces.
wiringX will export all common GPIO functions also found libraries such as wiringPi
and wiringHB, but when using wiringX it will automatically determine what device 
your program is running on and use the appropriate GPIO functions. So when using 
wiringX, your program will just work in regard of GPIO functionality.

The wiringPi and wiringHB are almost a direct copy of their initial library.
However, wiringX currently does not yet support all features of the
Hummingboard and Raspberry Pi I/O. Therefore, wiringPi has been
stripped so it only supports those features also supported by wiringX.

Those features currently are:
- GPIO reading, writing, and interrupts.
- IC2 reading and writing.

The supported devices are:
- Raspberry Pi
- Hummingboard
- BananaPi
- Radxa Rock 
- MIPS CI20 Creator

###Donations

donate@pilight.org

###Installation:

* Let it automatically build and generate a deb or rpm package:
```
#Make sure you have prerequisites
#For Debian based linuxes
sudo apt-get install build-essential
#For Red-Hat based linuxes
yum groupinstall "Development tools"

mkdir build
cd build
cmake ..
make
#For Debian based linuxes
cpack -G DEB
#For Red-Hat based linuxes
cpack -G RPM
```
* To install the final package run:
```
#For Debian based linuxes
dpkg -i libwiringx*.deb
#For Red-Hat based linuxes
dpkg -i libwiringx*.rpm
```

wiringX is available in the Arch Linux ARM repository. To install, simply:
```
pacman -S wiringx-git
```
Pin numbering of the Raspberry Pi, Hummingboard, BananaPi and Radxa Rock can be found here:
http://wiringx.org/
