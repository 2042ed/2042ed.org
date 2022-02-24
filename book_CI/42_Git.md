---
title: sviluppo collaborativo
parent: CI
has_children: false
nav_order: 42
---

# Piattaforme di sviluppo collaborativo

## Video
*What is GitHub?*
<https://www.youtube.com/watch?v=w3jLJU7DT5E>

## Cos'è un version control system?

Un sistema di version control system, o VCS, tiene traccia della cronologia delle modifiche mentre gli sviluppatori  e i team collaborano ai progetti insieme. Man mano che il progetto si evolve, i team possono eseguire test, correggere bug e fornire nuovo codice con la certezza che qualsiasi versione può essere ripristinata in qualsiasi momento. Gli sviluppatori possono esaminare la cronologia del progetto per scoprire:

- Quali modifiche sono state apportate?
- Chi ha apportato le modifiche?
- Quando sono state apportate le modifiche?
- Perché sono stati necessari cambiamenti?
	
## Cos'è un *distributed* version control system?

**Git** è un esempio di un **distributed** version control system (DVCS) comunemente utilizzato per lo sviluppo di software commerciale e open source. I DVCS consentono l'accesso completo a ogni file, *branch* e iterazione di un progetto e consentono a ogni utente l'accesso a una cronologia completa e autonoma di tutte le modifiche. A differenza dei sistemi di controllo delle versioni centralizzati un tempo popolari, i DVCS come Git non necessitano di una connessione costante a un repository centrale. Gli sviluppatori possono lavorare ovunque e collaborare in modo asincrono da qualsiasi fuso orario.

Senza il controllo della versione, i membri del team sono soggetti a attività ridondanti, tempistiche più lente e più copie di un singolo progetto. Per eliminare il lavoro non necessario, Git e altri VCS offrono a ciascun collaboratore una visione unificata e coerente di un progetto, facendo emergere il lavoro già in corso. Vedere una cronologia trasparente dei cambiamenti, chi li ha apportati e come contribuiscono allo sviluppo di un progetto aiuta i membri del team a rimanere allineati mentre lavorano in modo indipendente.

![](img/DVCS.jpg)

## Git

*Perché Git?*
Secondo l'ultimo sondaggio tra gli sviluppatori di [Stack Overflow](https://insights.stackoverflow.com/survey/2017#technology), oltre il 70% degli sviluppatori utilizza Git, rendendolo il VCS più utilizzato al mondo. Git è comunemente utilizzato sia per lo sviluppo di software open source che commerciale, con **vantaggi significativi **per individui, team e aziende.

- Git consente agli sviluppatori di vedere l'intera sequenza temporale delle modifiche, delle decisioni e dei progressi di qualsiasi progetto in un unico posto. Dal momento in cui accede alla cronologia di un progetto, lo sviluppatore ha tutto il contesto di cui ha bisogno per comprenderlo e iniziare a contribuire.

- Gli sviluppatori lavorano in ogni fuso orario. Con un DVCS come Git, la collaborazione può avvenire in qualsiasi momento mantenendo l'integrità del codice sorgente. Utilizzando branch, gli sviluppatori possono proporre in sicurezza modifiche al codice di produzione.

- Le aziende che utilizzano Git possono abbattere le barriere di comunicazione tra i team e mantenerli concentrati sul lavoro migliore. Inoltre, Git consente di allineare esperti in un'azienda per collaborare a progetti importanti.
    
## Cos'è un repository?

Un *repository* , o progetto Git , comprende l'intera raccolta di file e cartelle associati a un progetto, insieme alla cronologia delle revisioni di ogni file. La cronologia dei file appare come istantanee nel tempo chiamate commit e le commit esistono come una relazione di elenco collegato e possono essere organizzate in più linee di sviluppo chiamate branch . Poiché Git è un DVCS, i repository sono unità autonome e chiunque possieda una copia del repository può accedere all'intero codebase e alla sua cronologia. Utilizzando la riga di comando o altre interfacce di facile utilizzo, un repository git consente anche:

- l'interazione con la cronologia (Checkout)
- la clonazione (Clone) e il Fork
- la creazione di Branch (main, dev, feature, bugfix)
- il Commit e Push
- il Fetch, Pull e Merge
- il confronto delle modifiche tra le versioni del codice e altro ancora.
- area di Stage
- Tag / Release

Lavorare nei repository mantiene i progetti di sviluppo organizzati e protetti. Gli sviluppatori sono incoraggiati a correggere bug o creare nuove funzionalità, senza timore di far deragliare gli sforzi di sviluppo principali. Git lo facilita attraverso l'uso di *branches*: puntatori ai commit nella cronologia che possono essere facilmente creati e deprecati quando non sono più necessari.

Attraverso piattaforme come GitHub, Git offre anche maggiori opportunità per la trasparenza e la collaborazione del progetto. I repository pubblici aiutano i team a lavorare insieme per creare il miglior prodotto finale possibile.

![](img/git_flow.jpg)

## Comandi Git di base

Per utilizzare Git, gli sviluppatori utilizzano comandi specifici per copiare, creare, modificare e combinare il codice. Questi comandi possono essere eseguiti direttamente dalla riga di comando o utilizzando un'applicazione come GitHub Desktop o Fork (vedi dopo i tools). Ecco alcuni comandi comuni per l'utilizzo di Git:

- `git init` inizializza un repository Git nuovo di zecca e inizia a monitorare una directory esistente. Aggiunge una sottocartella nascosta all'interno della directory esistente che ospita la struttura dati interna richiesta per il controllo della versione.

- `git clone` crea una copia locale di un progetto che esiste già in remoto. Il clone include tutti i file, la cronologia e i *branches* del progetto.

- `git add` mette in *stage* un cambiamento. Git tiene traccia delle modifiche alla base di codice di uno sviluppatore, ma è necessario mettere in *stage* e scattare un'istantanea delle modifiche per includerle nella cronologia del progetto. Questo comando esegue la gestione temporanea, la prima parte di quel processo in due fasi. Qualsiasi modifica messa in *stage* diventerà una parte della prossima istantanea e una parte della storia del progetto. Lo staging e il commit separatamente offrono agli sviluppatori il controllo completo sulla cronologia del loro progetto senza modificare il modo in cui codificano e lavorano.

- `git commit` salva l'istantanea nella cronologia del progetto e completa il processo di rilevamento delle modifiche. In breve, un commit funziona come scattare una foto. Tutto ciò che è stato messo in stage `git add` diventerà parte dell'istantanea con `git commit`.

- `git status` mostra lo stato delle modifiche come non tracciate, modificate o organizzate.

- `git branch` mostra i *branches* su cui si lavora a livello locale.

- `git merge` unisce le linee di sviluppo insieme. Questo comando viene in genere utilizzato per combinare le modifiche apportate su due *branches* distinti. Ad esempio, uno sviluppatore si fonde quando desidera combinare le modifiche da un *branch* di funzionalità al *branch* principale per la distribuzione.

- `git pull` aggiorna la linea di sviluppo locale con aggiornamenti dalla sua controparte remota. Gli sviluppatori utilizzano questo comando se un membro del team ha eseguito il commit su un *branch* remoto e vorrebbero riflettere tali modifiche nel loro ambiente locale.

- `git push` aggiorna il repository remoto con tutti i commit effettuati localmente su un ramo.

![](img/git-commit_graph.jpg)

## Alternative a Git
Hg, Perforce, SVN sono solo alcuni, ma Git sta diventando lo standard

## Git Clients
- **Fork** <https://fork.dev>
  win/mac, gratuito con licenza opzionale, veloce, completo, bello
- **GitHub Desktop** <https://desktop.github.com>
  prodotto da GitHub, molto semplice con funzioni base. win/mac, gratuito. la prima scelta per i i principianti o per chi usa pochissimo Git
- **Source Tree** <https://www.sourcetreeapp.com>
  win/mac, gratuito (necessita solo di account Atlassian), molto completo, un po' lento per progetti grossi e UI non perfetta
- **GitKraken** <https://www.gitkraken.com/>
  non gratuito per i repo privati, win/mac, completo, si integra con altri prodotti della Axosoft  

## Temi
- .gitignore
- files binari e LFS
- stash
- conflitti
- filenames: maiuscole e minuscole
- filenames: line feed -> .editorconfig
- dati sensibili


## Per approfondire
- <https://lab.github.com/courses>
- <https://www.git-tower.com/learn/git/ebook/en/desktop-gui/introduction>
