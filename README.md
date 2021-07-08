# ionic-firebase-capacitor
Repository di prova dove si vede come configurare un progetto ionic con capacitor in modo tale da ricevere push notification tramite Firebase

## Riferimenti
Per fare quanto è stato fatto all'interno di questo repository è stata seguita la guida ufficiale per le push notification con ionic + angular e capacitor disponibile al seguente link:
https://capacitorjs.com/docs/guides/push-notifications-firebase

## Step
### Creazione progetto Ionic
E' stato creato un progetto ionic con il seguente comando:
```bash
ionic new ionic-firebase-capacitor-push-notification blank
```
E sono state selezionate le opzioni per utilizzare angular e capacitor.

### Creazione progetto Firebase
Andare sul sito https://firebase.google.com/ e, dopo aver fatto login, creare un nuovo progetto Firebase.
Dopo averlo fatto bisogna collegare al progetto l'app Android creata con Ionic facendo attenzione a nominare l'app con lo stesso nome scritto nel file capacitor.config.json alla voce "appId".
Fatto questo verrà creato un file chiamato google-services.json che dovrà essere messo nella cartella android/app del progetto.

### Modifiche sul progetto
Per le modifiche sul progetto vedere direttamente i commit fatti sul repository.

## Run App Android
Per runnare l'app android sarà necessario aprire il progetto android creato da capacitor con android studio. 
Prima di farlo bisognerà provare a runnare direttamente da ionic per creare dei file necessari che non vengono creati altrimenti (il run fallirà) con il comando:
```bash
ionic capacitor run android
```
Successivamente aprire con Android studio con il comando:
```bash
ionic capacitor open android
```
E runnare direttamente da la.

## Invio prima push notification
Non appena sarà runnata l'app si vedrà un alert con il token da utilizzare per mandare un messaggio. Non utilizzeremo quello ma utilizzeremo il target di Firebase.
Quindi andare sulla console di Firebase, selezionare l'inivio di una nuova notifica, scegliere un titolo ed un corpo della notifica, aggiungere come target l'app aggiunta e procedere con l'invio della notifica seguendo le istruzioni a schermo.
Fatto ciò si dovrebbe ricevere la notifica sull'applicazione precedentemente runnata.
