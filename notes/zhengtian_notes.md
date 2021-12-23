# Crazyswarm and Crazyflie

Crazyswarm's simulator only contains fast simulation with no (aero)dynamics.

CrazyS has dynamics included in the simulation (extension of RotorS) https://github.com/gsilano/CrazyS

python version: 3.7
conda create -n crazyflie python=3.7

USB permission:
https://www.bitcraze.io/documentation/repository/crazyflie-lib-python/0.1.9/usb_permissions/

##### crazyflie-firmware
1. Clone repo git clone --recursive https://github.com/bitcraze/crazyflie-firmware.git
2. Compiling `make PLATFORM=cf2`
3. Flash firmware (need to setup crazyradio, cfclient, crazyflie in bootloader mode) make cload


##### crazyradio-firmware
1. Clone repo
2. Build firmware https://github.com/bitcraze/crazyradio-firmware#building-the-firmware
3. Flash firmware (need to use python3 commands) https://github.com/bitcraze/crazyradio-firmware#flashing-the-firmware


##### cflib (required for GCS)
1. install dependencies of cflib https://github.com/bitcraze/crazyflie-lib-python/blob/master/docs/installation/install.md#install-cflib-dependencies

2. install cflib https://github.com/bitcraze/crazyflie-lib-python/blob/master/docs/installation/install.md#developing-for-the-cflib

##### GCS (crazyflie-client): 
https://github.com/bitcraze/crazyflie-clients-python/blob/develop/README.md
crazyflie-clients-python
1. clone the repo https://github.com/bitcraze/crazyflie-clients-python
2. install https://github.com/bitcraze/crazyflie-clients-python/blob/develop/README.md#launching-the-gui-application
3. python bin/cfclient
