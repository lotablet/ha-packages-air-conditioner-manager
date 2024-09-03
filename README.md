# package-gestione-condizionatore  
Questi sono 2 package di gestione del condizionatore (sia smart che non-smart) con notifiche su alexa in caso di apertura delle finestre.

Prima cosa da fare è creare la cartella package all'interno del nostro server di home assistant.
Si puo utilizzare [Samba share](https://github.com/home-assistant/addons/blob/master/samba/DOCS.md) o l'addon [File Editor](https://github.com/home-assistant/addons/blob/master/configurator/README.md) per creare la cartella.

Successivamente, una volta inserito il file .yaml all'interno della cartella, seguire le istruzioni all'interno.


+++++PACKAGE PER CONDIZIONATORI NON SMART+++++

Questo package crea un condizionatore virtuale, comandabile tramite un telecomando universale come Broadlink, Tuya etc.
Per non complicare il codice ho preferito usare delle scene, quindi assicurarsi che il nostro telecomando universale sia installato e funzionante su Home assistant e quindi creare delle scene come segue:

scene.caldo ----> creare una scena che invia il comando IR al condizionatore impostandolo su Caldo
scene.freddo ----> creare una scena che invia il comando IR al condizionatore impostandolo su Freddo
scene.auto ----> creare una scena che invia il comando IR al condizionatore impostandolo su Auto
scene.deumidificatore ----> creare una scena che invia il comando IR al condizionatore impostandolo su Deumidificatore
scene.spegni_condizionatore ----> creare una scena che invia il comando IR che spegne il condizionatore

La prima cosa da fare è installare [Template Climate](https://github.com/jcwillox/hass-template-climate) da [HACS](https://github.com/hacs/integration), scaricare l'addon e riavviare.

Successivamente configurare il package seguendo le istruzioni al suo interno.

