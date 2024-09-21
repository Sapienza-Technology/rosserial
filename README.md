# rosserial
Fork di rosserial fatto per cercare di risolvere il problema "unable to sync". Le modifiche presenti qui hanno risolto in alcuni casi ma non sempre.

Per installare questa versione bisogna prima rimuovere  rosserial installato, clonare la repository e buildare il workspace.
Installazione:
```
  dpkg --list|grep ros-noetic-rosserial |awk '{ print $2 }'|xargs sudo dpkg -r
  cd ~/catkin_ws/src
  git clone https://github.com/Sapienza-Technology/rosserial.git
  cd ..
  catkin build
```

Altre info riguardanti il problema "unable to sync"
- si presenta se c'è rumore sui pin tx e rx della scheda
- sembra che utilizzando i pin tx e rx e un convertitore usb-uart invece dell'usb normale l'errore non appare.
- Il comportamento è diverso da jetson e da computer.


## Original Readme

[![Build Status](https://travis-ci.org/ros-drivers/rosserial.svg?branch=melodic-devel)](https://travis-ci.org/ros-drivers/rosserial)

Please see [rosserial on the ROS wiki](http://wiki.ros.org/rosserial) to get started.
