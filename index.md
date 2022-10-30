
1. Problema de sonido
Respuesta rápida:

>uname -a

Linux raspberrypi 5.10.103-v7+ #1529 SMP Tue Mar 8 12:21:37 GMT 2022 armv7l GNU/Linux

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

2. Instalación Ultrastar

Compilando usando make

Instalar librerias

sudo apt-get update && sudo apt-get install git automake make gcc fpc libsdl2-image-dev libavformat-dev libswscale-dev libsqlite3-dev libfreetype6-dev portaudio19-dev libportmidi-dev liblua5.3-dev libopencv-videoio-dev

Para compilar con  --with-libprojectM

sudo apt-get install g++ libprojectm-dev

Para compilar con --with-opencv-cxx-api

sudo apt-get install g++ libopencv-dev

Para Fedora con RPM Fusion: 

sudo dnf install git automake make gcc fpc SDL2_image-devel ffmpeg-devel sqlite-devel freetype-devel portaudio-devel portmidi-devel lua-devel opencv-devel

--with-libprojectM: 

sudo dnf install gcc-c++ libprojectM-devel

Clonar repositorio ultrastardx

git clone https://github.com/UltraStar-Deluxe/USDX

y seguir los siguientes pasos

cd USDX
./autogen.sh
./configure (or use autoconf)
make
sudo make install
ultrastardx

Referencias:
https://github.com/UltraStar-Deluxe/USDX#compiling-on-linuxbsd-using-make

