Informacio treta per la Vercio Antiga de [Aqui](https://www.taloselectronics.com/blogs/tutoriales/camara-para-raspberry-v2).







-----------------------------(  No Se Si Funciona  )----------------------------------

 - sudo apt-get update
 - sudo apt-get upgrade -y
 - sudo apt-get install python3-pip libcap-dev -y
 - sudo pip3 install picamera2 --break-system-packages
 - 



Necesitem Vercio Moderna:
 - sudo apt-get update # Bona pràctica per actualitzar la llista abans d'instal·lar
 - sudo apt-get install libcap-dev
 - sudo apt-get install python3-pip: Per instalar el "pip3"
 - sudo pip3 install picamera2 --break-system-packages: el "--break-system-packages" ignara Atbertencies
 - sudo apt-get install libcamera libcamera-dev
 - sudo reboot: Aixo reinicia la Raspberry Pi

Necesitem Vercio Antiga (NO UTILITZAR!!!) :
  - sudo apt-get update: Per poder executar "sudo apt-get install python3-pip" sense errors
  - sudo apt-get install python3-pip: Per instalar el "pip3"
  - sudo pip3 install picamera: si no utilitzar "sudo pip3 install picamera --break-system-packages" (ignarar Atbertencies)
  - Connecta't a la Raspberry Pi per SSH.Obre l'eina de configuració:
    sudo raspi-config
  - Ves a l'opció 3 Interface Options.
  - Selecciona l'opció P1 Camera.
  - Quan et pregunti si vols habilitar la càmera, selecciona Yes.
  - Surt de raspi-config.
  - Quan et pregunti si vols reiniciar, selecciona Yes o executa manualment sudo reboot.
