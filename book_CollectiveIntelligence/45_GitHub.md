# GitHub
- GitHub è una piattaforma di sviluppo collaborativo
- Storia (nato nel 2006 è oggi la piattaforma n.1 degli sviluppatori, 40 milioni)
- Microsoft ha comprato il tutto per 7 miliardi.
- developer community
- workflow: projects, milestones, issues
- documentazione

## I vantaggi di GitHub 
GitHub è un hosting di repository  Git che fornisce agli sviluppatori strumenti per fornire un codice migliore tramite funzionalità della riga di comando, problemi (discussioni in thread), richieste pull, revisione del codice o l'uso di una raccolta di app gratuite e acquistabili nel Marketplace di GitHub. Con livelli di collaborazione come il flusso GitHub, una comunità di 15 milioni di sviluppatori e un ecosistema con centinaia di integrazioni, GitHub cambia il modo in cui viene costruito il software.

## Come funziona GitHub
GitHub integra la collaborazione direttamente nel processo di sviluppo. Il lavoro è organizzato in repository, in cui gli sviluppatori possono delineare requisiti o direttive e definire aspettative per i membri del team. Quindi, utilizzando il flusso GitHub, gli sviluppatori creano semplicemente un ramo per lavorare sugli aggiornamenti, eseguire il commit delle modifiche per salvarli, aprire una richiesta pull per proporre e discutere le modifiche e unire le richieste pull quando tutti sono sulla stessa pagina.

# Il flow di GitHub
Il flusso GitHub è un flusso di lavoro leggero, basato su rami, costruito attorno ai principali comandi Git utilizzati dai team di tutto il mondo.

Il flusso GitHub ha sei passaggi, ciascuno con vantaggi distinti quando implementato:

1.  **Create a branch:**  i rami degli argomenti creati dal ramo di distribuzione canonica (di solito main) consentono ai team di contribuire a molti sforzi paralleli. I rami tematici di breve durata, in particolare, mantengono i team concentrati e si traducono in navi veloci.
2.  **Add commits:** Snapshots dello statuo di sviluppo all'interno di un ramo creano punti sicuri e reversibili nella cronologia del progetto.
3.  **Open a pull request:**  le pull request pubblicizzano gli sforzi in corso di un progetto e danno il tono a un processo di sviluppo trasparente.
4.  **Discuss and review code:** i team partecipano alle revisioni del codice commentando, testando ed esaminando le pull request aperte. La revisione del codice è al centro di una cultura aperta e partecipativa.
5.  **Merge:** dopo aver fatto clic su unisci, GitHub esegue automaticamente l'equivalente di un'operazione di  `git merge` locale. GitHub mantiene anche l'intera cronologia dello sviluppo del ramo sulla richiesta pull unita.
6.  **Deploy:** i team possono scegliere i cicli di rilascio migliori o incorporare strumenti di integrazione continua e operare con la certezza che il codice nel ramo di distribuzione sia passato attraverso un flusso di lavoro affidabile.

## Modelli per lo sviluppo collaborativo

Esistono due modi principali in cui le persone collaborano su GitHub:

1. Repository condiviso
2. [Fork](https://help.github.com/articles/about-forks/) and [pull](https://help.github.com/articles/using-pull-requests)

Con un repository condiviso, _shared repository_, sviluppatori e team sono esplicitamente designati come contributori con accesso in lettura, scrittura o amministratore. 

Per un progetto open source o per progetti a cui chiunque può contribuire, la gestione delle autorizzazioni individuali può essere impegnativa, ma un modello _fork and pull_ consente a chiunque possa visualizzare il progetto di contribuire. Un fork è una copia di un progetto sotto l'account personale di uno sviluppatore. Ogni sviluppatore ha il pieno controllo del proprio fork ed è libero di implementare una correzione o una nuova funzionalità. Il lavoro completato nelle forche viene mantenuto separato o riportato al progetto originale tramite una  pull request. Lì, i maintainer possono rivedere le modifiche suggerite prima che vengano unite.

