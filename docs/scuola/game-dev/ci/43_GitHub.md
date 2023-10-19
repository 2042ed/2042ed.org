---
title: GitHub
date: 2022-12-23
updated: 2023-01-16
type: book
weight: 45
---
# GitHub

![](../../../assets/img/gamedev/img-ci/github_icon_192.webp)

GitHub è la principale (ma non l'unica) piattaforma online che permette di ospitare gratuitamente progetti Git, offrendo opzioni di sviluppo molto avanzate e soluzioni commerciali quando si sono raggiunti i limiti delle offerte gratuite.  
Nato nel 2008 è stato acquistato da Microsoft nel 2018 per 7 miliardi.

## Git vs GitHub vs GitHub Desktop/Git Client

**Git** è l'applicazione che gestisce Versioning System.  
**GitHub** è una piattaforma web che ospita repositories Git.  
**GitHub Desktop/Git Client** è un programma che permette di comandare Git attraverso un'interfaccia grafica.

## Features

### Repository Private / Public
I respository possono essere privati, ovvero accessibili solo a determinate persone o teams

### Personal / Teams

- Account personali
- Account Team

### Permessi
Sopratutto negli account teams si possono configurare in modo molto granularei permessi di accesso, di scritture, di gestione dei repository.

### Issues / Projects
Sitema molto avanzato di project e issue management integrato con i commit (si può referenziare una Issue direttamente dal messaggio di un commit per segnalare anche un'eventuale risoluzione e auto-chiusura).
Le issues hanno milestones, dicussioni, reactions, labels, assegnatari multipli, notifiche.
I progetti hanno vista a colonne o a righe, campi dinamici customizzabili.

### Discuss
Ogni repository può avere un vero e proprio forum pubblico dove discutere tra gli sviluppatori o semplici utenti o sviluppatori esterni.

### Releases
Un `tag` può essere convertito in una `Release` con tanto di descrizione e files da scaricare.

### Social Developers Network
la Home Page di GitHub segnala tutte le attività degli sviluppatori e progetti che si seguono.

### Download / Clone / Fork

- Un progetto può esserescaricato come pacchetto zip.
- Clonato sul proprio computer
- `forkato` nel proprio account

### Pull Request (PR)
Quando si effettua una modifica al proprio repository forkato, si può proporre all'origin di applicare la modifica con una `Pull Request`, ovvero GitHub invia il commit e lo mette nell'elenco delle Pull Requent da discutere, valutare, testare ed eventualmente implementare.

### Actions
Si possono configurare delle azioni da eseguire in automatico in caso di determinati eventi, tipo un commit su un branch, un merge, una release.

Le azioni sono script totalmente programmabili (e condivisibili con altri), ad esempio il rendering di documentazione, la compilazione, il deploy su altri sistemi.

### Webhooks
Ogni evento di attività (commit, commento, issue, release, etc) può essereagganciato ad un webhook e quindi integrare applicazioni esterni, ad esempio Slack, Discord, Teams, Unity Cloud...

### Markdown
Tutti i contenuti testuali gestiti da GitHub (readme, issues, commenti) sono nativamente in formato Markdown.

### Community / Social Coding
Ogni repo può avere una descrizione, un'immagine, dei tags che lo presentano meglio e lo rendono "trovabile" dalla comunità di developers che lavora con GitHub.
Le "stars" danno visibilità, si può decidere di tenere sotto osservazione un repository (e quindi ricevere notifiche puntuali sul suo sviluppo).

### Sponsorship
Si può configurare la possibilità di ricevere sponsorizzazioni da altri utenti GitHub, sottoforma sopratutto di contributi mensili.

### README.md
file in formato Markdown che sintetizza il progetto.

### LICENSE.md
importante sopratutto per i repository pubblici.
Cosa possono fare gli altri col il nostro repo?
Se non si mette nulla, è nostro standard copyright, altrimenti mettere MIT.

### github.dev
VS Code è stato perfettamente integrato nella piattaforma e si può usare per programmare online.

### Co-Pilot
Un potente compagno di programmazione. Una AI che ha studiato tutti i repository pubblici e sa trovare errori e proporre migliorie di codice.

### Pages
Possibilità di configurare una directory (di solito `\docs`) o un brach (`gh-pages`) che venga renderizzato automaticamente in HTML e che diventi il sito / vetrina integrato e pubblico. Tutto gratuitamente.

### Preservation
[GitHub Archive Program](https://archiveprogram.github.com/faq/)

## Alternative a GitHub

- GitLab
- Bitbucket
