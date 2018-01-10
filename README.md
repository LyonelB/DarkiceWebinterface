# DarkiceWebinterface

Le fichier run.py a été modifié pour pouvoir accéder à l'interface depuis n'importe quel navigateur du réseau local.

## Préparation

    $ sudo apt-get install python3-pip python-dev git
    $ sudo pip3 install flask flask-wtf
   
## Installation

    $ git clone https://github.com/nvalis/DarkiceWebinterface.git
    $ cd DarkiceWebinterface
    $ pip install -r requirements.txt
    $ python3 run.py

## Auto-start

    $ sudo nano darkice.sh
    
Copiez le texte suivant :

    #!/bin/sh

    cd DarkiceWebinterface
    python3 run.py

    exit 0

Enregistrez et quittez

    $ crontab -e
   
Et ajoutez la ligne suivante :

    */5 * * * * /bin/bash /home/pi/darkicewebinterface.sh > /home/pi/dwi.log 2>&1

## Présentation

A simple Flask webinterface for configuring and running [DarkIce](http://darkice.org/) ([Github](https://github.com/rafael2k/darkice)).

## Captures d'écran

![Screenshot Overview](/screenshot_overview.png?raw=true "Screenshot")

![Screenshot Config](/screenshot_config.png?raw=true "Screenshot")
