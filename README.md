# AIR CONDITIONER MANAGER - Gestione Condizionatore Smart e non-Smart

Questo è il mio primo package perciò siate clementi nel caso incontriate difficoltà di comprensione/funzionamento :D

Questi 2 package comprendono la gestione di un condizionatore smart e non-smart, gestendo l'accensione e lo spegnimento in caso di apertura di una o piu finestre, e avere delle notifiche su alexa quando viene spento o riacceso il condizionatore.

Prima cosa da fare prima i procedere con l'installazione del package, bisogna creare la cartella package all'interno del nostro server di home assistant:
  
  Si puo utilizzare gli addon [Samba share](https://github.com/home-assistant/addons/blob/master/samba/DOCS.md) o [File Editor](https://github.com/home-assistant/addons/blob/master/configurator/README.md) per creare la cartella.
  

<b>PACKAGE PER CONDIZIONATORI NON SMART</b>

*INSTALLAZIONE PACKAGE*

  - Per non complicare il codice ho preferito usare delle scene, quindi assicurarsi che il nostro telecomando universale sia installato e funzionante su Home assistant e quindi creare delle scene come segue:

        scene.heat ----> creare una scena che invia il comando IR al condizionatore impostandolo su Caldo
        scene.cool ----> creare una scena che invia il comando IR al condizionatore impostandolo su Freddo
        scene.auto ----> creare una scena che invia il comando IR al condizionatore impostandolo su Auto
        scene.dry ----> creare una scena che invia il comando IR al condizionatore impostandolo su Deumidificatore
        scene.aircon_off ----> creare una scena che invia il comando IR che spegne il condizionatore

    Una volta create le scene assicurarsi che le entità delle scene si chiamino esattamente come sopracitato.

  - Installare [Template Climate](https://github.com/jcwillox/hass-template-climate) da [HACS](https://github.com/hacs/integration), scaricare l'addon e riavviare.
  - Scaricare "air_conditioner_manager_non_smart.yaml" ed inserire il file nella cartella package
  - Configurare il package seguendo le istruzioni al suo interno.


<b>PACKAGE PER CONDIZIONATORI SMART</b>
*INSTALLAZIONE PACKAGE*

  - Scaricare "air_conditioner_manager_smart.yaml" ed inserire il file nella cartella package
  - Compilare la sezione IMPOSTAZIONI e successivamente riavviare
