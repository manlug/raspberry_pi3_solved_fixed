
1. Problema de sonido
Respuesta rápida:

>less /home/pi/.asoundrc
defaults.pcm .card 1
defaults.pcm.device 0
defaults.ctl.card 1

Referencias:
https://forums.raspberrypi.com/viewtopic.php?t=175233
https://www.alsa-project.org/wiki/Setting_the_default_device
https://www.linuxquestions.org/questions/linux-software-2/default-sound-card-specification-in-alsa-conf-files-903046/

Descripción problema:
Tras instalar Ultrastar en la raspberry pi 3, y tras una actualización del sistema operativo, dejo de funcionar.

