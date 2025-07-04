The original hmlangw daemon connects a local HomeMatic radio interface (say HM-MOD-RPI-PCB attached to a Raspberry Pi) to HomeMatic software on a different machine (say a RaspberryMatic or debmatic instance).
However, the hmlangw project was discontiued - and the rather simple code does not compile unter Linux kernels > 5.15, because it uses a direct write to sysfs for changing the GPIO status.

The current code is a simple rewrite, where the sysfs calls are replaced by modern calls to the gpiod library.

Note, that this library and its headers have to be installed by<

sudo apt install libgpiod-dev gpiod


Prof.Dr. Peter A. Henning
June 2025
