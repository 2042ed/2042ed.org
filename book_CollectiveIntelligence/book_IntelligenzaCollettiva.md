---
title: Intelligenza Collettiva e Sviluppo Distribuito - da Git all'immortalità
author: Stefano Cecere
year: 2019
license: CC BY-NC-SA
---

# Intelligenza Collettiva e Sviluppo Distribuito - da Git all'immortalità
di Stefano Cecere
CC BY-NC-SA

<!--TOC-->

## Introduzione
il tuo progetto sopravviverà fino al 2042? e oltre?  
come lavorare e collaborare meglio?

- come hanno creato quell'Intelligenza Artificiale?
- come hanno bilanciato quel livello?
- come hanno scritto una tale sceneggiatura ipertestuale complessa?
- come hanno fatto quello shader?
- come ricreare quelle luci?
- come riggare quel modello per ottenere quel risultato?
- bellissima musica o suono... c'è la partitura? come è stato sintetizzato?

conveniamo che oggi i "dietro le quinte" sono degli ottimi momenti per imparare, tra la teoria e la pratica. vedere e capire i segreti del mestiere è fondamentale.
ma se nessuno condividesse nulla, o fosse accessibile solo pagando salato

per fortuna non è più così.
benvenuti nel 2019 e prepariamoci al 2042.

### Si può forse brevettare il sole?
 "A chi appartiene il brevetto?" alla quale Salk rispose "Direi alla gente. Non esiste un brevetto. Si può forse brevettare il sole?"
risposta al brevetto sul vaccino antipolio, 1952

- Internet (TCP/IP e protocolli) + Apache
- Firefox
- LibreOffice / OpenOffice
- le batterie della Tesla
- 

### Problematiche comuni nello sviluppo di progetti digitali
- l'arte e la cultura della collaborazione va studiata e messa in pratica. non nasciamo guru
- il progetto riesce bene se lavorano _tutti_ bene
  - accogliere nuovi arrivati nel progetto
  - incentivare la partecipazione e la collaborazione
  - ridurre al massimo la frustrazione personale e i colli di bottiglia
  - accelerare la risoluzione dei problemi
- DO NOT REINVENT THE WHEEL
  imparare le best practices ottenute da milioni di sviluppatori precedenti
- iniziare a creare il proprio curriculum
  - get a job
  - serve una presenza digitale di quello che si fa, non di quello che si dice di fare
- forever learning: nel nostro lavoro chi si ferma è in difficoltà
  - scoprire e cavalcare i trends di idee e tecnologie
  - nuove nicchie possono dare spunti a innovazione
  - opportunità di trovare le proprie passioni e i propri spazi
- Future Proof
  - i progetti o gli assets deperiscono in fretta
  - essere pronti e resistere al cambiamento
  - sopravvivere alla morte: cosa succede se mi muore l'hard disk, perdo la password, smetto di lavorare? un progetto reso pubblico e "open" in modo efficace e permanente va oltre noi stessi
  - che il progetto non abbia bisogno di noi che potremmo essere sostituiti
  - riapertura del progetto da parte di altri o di noi stessi fra un anno
  - necessità di definire al meglio i formati, le convenzioni e la semantica
  - come funziona... documentazione completa, aggiornata, concisa e interna al progetto stesso
  - chi ha fatto cosa e perché? changelog efficace
- non si butta via niente, il concetto di riusabilità di moduli e librerie
- C.I.: Continuous Integration: che il repository, la documentazione, le issues/milestones, le build, le notifiche e il tool di comunicazione siano integrate al massimo e accessibili a tutti i partecipanti al progetto
- intercomunicazione e aiuto reciproco fra teams, per migliorare l'Intelligenza Collettiva della company/scuola

### game designers
- necessitano di condividere al meglio gli aggiornamenti della documentazione
- testare sul progetto live nuove configurazioni o prototipi
- dare feedbacks veloci ai dev
- studiare gli altri (meccaniche interne, algoritmi)

oltre a occuparsi del gioco in sé e del giocatore,
potrebbero rendere l'esperienza stessa dello sviluppare divertente e coinvolgente: developer experience, communication, flow

### game developers
- il commit di codice è solo il 20% del lavoro
- studio, architettura, interoperabilità, test, debug, CI, feedback, comunicazione sono l'80%
- spesso i programmatori sono introverts, quindi migliorare comunicazione diretta e team work è indispensabile
- accesso a KnowledgeBase

### artisti e content producers
- formati accessibili
- storico e nomenclatura
- pre-test in scena
- risorse di tutoring
- sperimentazione

## Open Source
![logo_opensource](assets/logo_opensource.jpg)

Il termine "Open Source" si riferisce a prodotti progettati per essere pubblici e accessibili affinché tutti possano usarli, modificarli e condividerli.

I progetti OpenSource richiedono una collaborazione aperta, una buona comunicazione pubblica e un'adeguata qualità generale.

Collaborare pubblicamente su un progetto implica:
- più occhi e più mani
- accessibilità
- maggiore qualità

inoltre si possono usare progetti preesistenti per non dover reinventare tutto, sopratutto i bricks (mattoni) di base, spesso i più complessi.

è inoltre gratificante migliorare un progetto comune, dove altri costruiscono partendo da dove siamo arrivati noi

in un progetto Open si dà molto, è forse un po' più faticoso, ma si riceve ancora di più

### pros
- gratuito. raramente ci sono licenze
- facile da installare e maneggiare
- sviluppo in tempo reale
- indipendenza
- si modifica il necessario
- competitività
- è divertente
- crea Open Standards
- le università e gli indie lavorano qui
- grande scelta

### cons
- non sempre user-friendly
- mancanza di supporto
- necessità studio
- può essere complesso
- facilità di progetti abbandonati
- non sempre c'è qualità
- non c'è guadagno monetario diretto
- segmentazioni delle comunità

### considerazioni
- una filosofia, più che una pratica
- storia: anni 90, Linux il primo grandissimo progetto OpenSource (il cui creatore inventò Git per migliorare lo sviluppo collaborativo), big companies oggi lo adottano (Facebook, Google, Microsoft, Oracle), ROI
- intelligenza collettiva: in tanti possono partecipare e mettere il meglio di se in modalità open e meritocratica
- feedback in tempo reale con gli utenti
- possibilità di lavoro (manutenzione, customizzazione, velocità)
- il progetto sopravvive al nostro tempo e interesse. qualcun altro potrà portarlo avanti
- aprire i propri cassetti di idee e pubblicare. male non fa
- Game Jams sono i migliori eventi dove il prodotto deve essere rilasciato OpenSource. più del prodotto in sé è interessante il come è stato fatto, con chi e le referenze a futuro (portfolio)

### Licenze
fondamentalmente 3 categorie:

#### 1. closed - all rights reserved
- copyright / closed source

#### 2. share-alike - condivido ma non specularci
- Creative Commons 

#### 3. open - do whatever u want
- GPL/MIT per codice
- unlicensed

## InnerSource
l'InnerSource è il processo di sviluppo collaborativo di progetti basandosi sulle tecnologie e procedure OpenSource, ma stando all'interno di un ambiente privato, non pubblico.

l'InnerSource usa le skills degli sviluppatori abituati all'OpenSource e le porta dentro i firewalls dei progetti privati, garantendo una piattaforma interna per collaborare ai progetti.

- OpenSource dietro ad un firewall
- lavorare internamente come se fosse un progetto OpenSource
- portare le best practices dell'OpenSource nel team work
- Inner-sourcing è un mind-shift mentale

### Perché InnerSource
- la tecnologia rimane proprietaria.
- sviluppo più efficente
  - riuso del codice
  - codice più pulito
  - limit development bottleneck
- ottimizza la  collaborazione
  - improve talent retention
  - utilize talent across teams better
  - reduce tribal knowledge
- Faster development: Programmers use unit tests, code coverage, and continuous integration to remove bugs at early stages
- Complete documentation: Code is documented better, both in-code comments and less formally on discussion lists
- Code reuse: Programmers across the organization understand the code and architecture of modules developed by other teams
- Cross-team collaboration: Contributions by members outside of the team are frictionless and rarely have to be rewritten
- Development with GitHub: GitHub maintains private repositories for in-house projects as well as public repositories for open source code


## Piattaforme di sviluppo collaborativo (GitHub)

### Git
Git è uno strumento di Version Control.
ce ne sono altri (Hg, Perforce, SVN), ma è quello che si è imposto, per diverse buone ragioni.

parole chiave:
- Commit
- Fork
- Pull
- Push
- self contained
- branch (master, dev, feature, bugfix)
- tag / release

caldamente consigliate sono le lezioni di GitHub stessa: <https://lab.github.com/courses>
e questa guida <https://www.git-tower.com/learn/git/ebook/en/desktop-gui/introduction>

### GitHub
- GitHub è una piattaforma di sviluppo collaborativo
- Storia (nato nel 2006 è oggi la piattaforma n.1 degli sviluppatori, 40 milioni)
- Git basics <https://git-scm.com/book/it/v1/Per-Iniziare-Basi-di-Git>
- Microsoft ha comprato il tutto per 7 miliardi.
- developer community
- workflow: projects, milestones, issues
- documentazione

### tools
- Fork https://fork.dev
- GitHub Desktop https://desktop.github.com

guida completa a GitHub Desktop
<https://programminghistorian.org/en/lessons/getting-started-with-github-desktop>

## Formati e Interscambio
- Code of Conduct: regole di partecipazione e comunicazione
- changelog https://keepachangelog.com
- commit syntax https://www.conventionalcommits.org

### Markdown
in contrapposizione al markup dell'html, è stato creato il markdown dove la base è testo semplice con pochissime convenzioni che permettono al contenuto di essere convertito nei formati più utili (html, doc, pdf, ePub) garantendo un versioning perfetto e una preservazione e portabilità ottimali

GitHub ha determinato massicciamente l'adozione dello standard MarkDown per la documentazione e ormai moltissimi siti vengono generati con Static Site Generators (vedi Jekyll o Hugo) a partire da contenuti (pagine e posts) scritti in Markdown,

**links**  
- dal creatore di Markdown: https://daringfireball.net/projects/markdown/syntax
- Jekyll è il rendering engine delle GitHub pages: https://jekyllrb.com
- corso markdown: https://lab.github.com/githubtraining/communicating-using-markdown

### Cosa c'è da fare?

servono strumenti di comunicazione (Slack, Discord, Skype, Telegram, Emails)

e di tracciamento delle cose da fare e roadmap (issues, milestones), tipo GitHub Issues, Trello, Jira, Google Sheets

dove scrivere i docs: Google Docs, Microsoft 360, DropBox, offline files

come scambiarsi i files: DropBox, Box,com, LAN, Google Drive, WeTransfer, email, GitHub

### tecniche di 

## Accessibilità e Presenza
essere accessibili, ovvero non chiudersi nelle proprie mura virtuali.
parlare la stessa lingua, o almeno conoscere le lingue più utilizzate.
tenere sempre conto che stiamo parlando sia con le macchine, ma sopratutto con altri esseri umani.

oltre ai propri progetti, è bene iniziare a costruire la propria "casa" digitale, la Web Presence. 
ognuno troverà dove e come collocarsi. l'importante è iniziare

### Nickname e Avatar
se non si ha un nickname a cui ci si tiene molto e che sia "presentabile" a tutti, conviene usare NomeCognome.
mantenere uno stesso profilo su tutte le piattaforme (Twitter, GitHub, Facebook, DevianArt, Discord, Itchio, LinkedIn)

anche la propria foto/icona/avatar sarebbe meglio fosse unica.

### Language
english, please.

### CV e Portfolio
- è importante che ognuno abbia una buona presenza sul web con pubblicato quello che fa, sa fare, cosa gli interessa.
- GitHub offre la possibilità di avere un proprio sito pubblico e gratuito all'indirizzo username.github.io (eventualmente con un proprio dominio comprato a parte), e ciò sarebbe la prima cosa che oggi i vari recruiters vanno a vedere, più delle pagine LinkedIn o altro, perché i progetti/prototipi/studi pubblicati, e COME sono stati realizzati, fanno capire le reali potenzialità e peculiarità di ognuno.
- le presenze digitali fondamentali per un game developer sono:
  - GitHub
  - Twitter
  - LinkedIn
- se non sulle proprie pagine, i propri progetti possono/devono essere pubblicati su https://itch.io/

- corso GitHub pages: https://lab.github.com/githubtraining/github-pages

## Preservazione e Immortalità

Progetti Self Contained
Ultima versione di _ogni_ risorsa da preservare.
Archiviazione (anche 1000 anni)

## Marketing ed Economia

- auto promozione
- fare esperienza
- vendere consulenza e customizzazioni
- bacino di utenza
- vendere addons

## Appendici e Risorse

### Links
- <https://opensource.org/osd>
- http://innersourcecommons.org/
- https://github.com/InnerSourceCommons

- [How to create an internal InnerSource community](https://opensource.com/life/16/11/create-internal-innersource-community)
- video [InnerSource Journey with GitHub](https://www.youtube.com/watch?v=MhhBi7o9z90)
- video [GitHub: InnerSource: Reaping the Benefits of Open Source, Behind Your Firewall](https://www.youtube.com/watch?v=sDKN-xyqcNc)
- video [GitHub Satellite 2017 - Global Software Development with InnerSource](https://www.youtube.com/watch?v=64gaATwzXvE)

### progetti OpenSource
- OpenSource projects finder: <https://www.findbestopensource.com>
- OpenSource games: <https://en.wikipedia.org/wiki/List_of_open-source_video_games>
- open Game Dev tips and tools <https://opensource.com/article/17/12/how-to-gaming-jam-development>
- <https://wiki.creativecommons.org/wiki/Games_using_CC_licensed_assets>
- [contro le licenze CC nei videogiochi](https://www.gamasutra.com/blogs/StephenMcArthur/20160112/262962/Creative_Commons_is_Not_a_Smart_Source_for_Video_Game_Assets.php)

### tools per GameDev
- Godot game engine https://godotengine.org/
- Phaser JS game engine https://phaser.io/
- Blender 3D engine (con la nuova 2.8 UI) sempre più usato anche dai big studios https://www.blender.org/
- Audacity audio editor http://www.audacityteam.org/download/linux/
 
### Esempi
- progetti grossi:
  - https://github.com/microsoft/vscode

- Unity projects
  - https://unitylist.com
  - https://github.com/QianMo/Unity-Design-Pattern
  - https://github.com/mob-sakai/UIEffect
  - https://bitbucket.org/Unity-Technologies/

- frameworks per giochi narrativi
  - https://github.com/snozbot/fungus
  - https://github.com/Siccity/xNode
  - https://github.com/inkle
  - https://github.com/e-ucm/uAdventure

- developers
  - https://github.com/keijiro/
  - https://github.com/ncase

## Home-Works per settimana prossima
1. completare il progetto Team 1920.2, con propria foto, nome cognome, corso e progetto, link a propria pagina GitHub

2. ognuno finisca la propria pagina personale username.github.io
(non badare al tema e stile) 
scrivere una sintesi dei propri interessi in ambito di game dev/design

3. trovare un progetto OpenSource di proprio interesse e forkarlo sul proprio account

---

## Unity Game Project
Integrazione progetto Unity -> GitHub -> Unity Cloud Build -> Discord -> Issues -> Documentazione

- organizzare un progetto con metodologia InnerSource: strumenti, comunicazione e best practices
- progetti delle cumulative, polishing, docs, interscambi, cross issues, moduli, custom web site, changelog, Cloud Build e CI
- se si pensa subito al dopo e si lavora con lo sguardo a dopodomani, ci si guadagna tutti

- nomenclatura (codici, files)
- organizzazione degli strumenti (scegliere bene)
- CGL
- ruoli
- organizzare progetto Unity
- sorgenti dei files -> deployed
- formati files (formati multipiattaforma e opensource the best)
- dati sensibili
- conoscere i propri strumenti
- usiamo Discord: etiquette
- documentazione (artistica, design, tecnica)
  - spiegare PERCHE' si sono fatte determinate scelte
- devlog (sito di progetto / twitter / FB)
- changelog
- backup / ridondanza / archivio

- personal marketing: GitHub + Twitter, pensare alla propria presenza pubblica lavorativa e artistica. nel dubbio: NomeCognome e non fare cose di cui pentirsi.
 
