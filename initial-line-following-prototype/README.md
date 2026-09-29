# Prototype initial de suivi de ligne

Ces sources correspondent à la première phase expérimentale du véhicule : déplacement, suivi de ligne par caméra, commande de direction et de vitesse, mesure ultrason et interface locale.

## Modules

- `traitement_image.py` : acquisition Picamera2, traitement OpenCV, détection de lignes et calcul de l'angle de direction ;
- `servo_controller.py` : commande de la direction avec pigpio ;
- `acceleration_controller.py` : commande PWM et sens de déplacement ;
- `ultrason.py` : mesure de distance ;
- `threads.py` : threads d'outils, état partagé et watchdog ;
- `gui.py` et `spinbox.py` : interface CustomTkinter ;
- `main.py` : initialisation et boucle principale.

## Environnement historique

Le code cible un Raspberry Pi avec caméra, GPIO, pigpio et capteur ultrason. Les dépendances Python connues sont listées dans `requirements.txt`.

Ce dossier documente un prototype réellement retrouvé. Il ne représente pas encore l'architecture cible LiDAR/IMU décrite dans le README principal et n'a pas été validé sur le matériel depuis sa récupération.
