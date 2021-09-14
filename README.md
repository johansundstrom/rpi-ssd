# rpi-ssd

Notera kravlistan
* 3A adapter krävs
* PI4
* SATA adapter i USB3

Installera som vanligt

1. Ladda ned Raspberry Pi OS Lite
2. Flasha med Raspberry Pi Imager till SD
3. Lägg till en tom fil med namnet ```ssh``` i boot-partitionen
4. Starta RPi upp från SD

Uppdatera RPi

6. logga in från terminal med ```ssh pi@{ip-adress}```
7. ```sudo raspi-config```
8. Interfacing Options » SSH » Yes » Ok » Finish
9. ```sudo nano /etc/default/rpi-eeprom-update```
10. ```sudo apt update```
11. ```sudo apt full-upgrade```
12. ```sudo reboot```

Kontrollera uppdateringen

12. ```sudo rpi-eeprom-update``` (senaste versionen?)

Sätt bootordning

13. ```sudo raspi-config```
14. Advanced Options » Bootloader Version » latest » Ok
15. På frågan “Reset boot ROM to defaults” välj "Nej" (!!!) för att använda senaste boot ROM
16. Advanced Options » Boot Order » USB Boot » Ok
17. Finish » Reboot » Shut down

Hämta HASSIO till PC/Mac flash till SSD

18. https://github.com/home-assistant/operating-system/releases
19. ```haos_rpi4-64-6.X.img.xz``` för RPi4
20. Flasha med Balena Etcher till SSD (partitioner bildas)
21. Ta ut SD och sätt i SSD
22. Bevaka  http://{ip-adress}:8123
