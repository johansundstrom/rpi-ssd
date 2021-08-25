# rpi-ssd

Notera...
* 3A adapter
* PI4
* SATA adapter i USB3


1. Ladda ned Raspberry Pi OS Lite
2. Flasha med Raspberry Pi Imager till SD
3. Lägg till en tom fil men namnet ```ssh``` i boot-partitionen
4. Starta upp från SD
5. logga in från terminal med ```ssh pi@<ip>```
6. ```sudo raspi-config```
7. Interfacing Options » SSH » Yes » Ok » Finish
8. ```sudo nano /etc/default/rpi-eeprom-update```
9. ```sudo apt update```
10. ```sudo apt full-upgrade```
11. ```sudo reboot```

Kontrollera uppdateringen

12. ```sudo rpi-eeprom-update``` (senaste versionen?)

Sätt bootordning

13. ```sudo raspi-config```
14. Advanced Options » Bootloader Version » latest » Ok
15. På frågan “Reset boot ROM to defaults” välj "Nej" (!!!) för att använda senaste boot ROM
16. Advanced Options » Boot Order » USB Boot » Ok
17. Finish » Reboot » Shut down

Hämta HASSIO på PC/Mac

18. https://github.com/home-assistant/operating-system/releases
19. ```haos_rpi4-64-6.X.img.xz``` för RPi4
20. Flasha med Balena Etcher till SSD (partitioner bildas)
21. Ta ut SD och sätt i SSD
22. Bevaka  http://<ip>:8123
