# Crazyswarm and Crazyflie

## Introduction

Crazyswarm's simulator only contains fast simulation with no (aero)dynamics.

CrazyS has dynamics included in the simulation (extension of RotorS) https://github.com/gsilano/CrazyS

## General
ubuntu: 18.04
ROS: melodic

## Crazyflie-related
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
crazyflie connection address:
cf1: 0xE7E7E7E701
cfx: 0xE7E7E7E70x

## Crazyswarm-related
python version: 2.7
conda create -n crazyswarm python=2
conda activate crazyswarm

##### crazyswarm installation
Follow instruction [here](https://crazyswarm.readthedocs.io/en/latest/installation.html) under **Physical Robots and Simulation**: 
Before Step 6, make sure you are using most updated **cmake** version as **3.10.2** will produce error.
Follow the answer with most up-votes [here](https://answers.ros.org/question/293119/how-can-i-updateremove-cmake-without-partially-deleting-my-ros-distribution/) to see a clean way of using updated cmake.