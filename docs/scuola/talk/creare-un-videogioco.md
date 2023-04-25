---
title: Creare un videogioco
date: 2023-04-24
updated: 2023-04-25
summary: "arti, tecnologie, scienze, psicologia, economia, strumenti e idee per chi volesse guardare dietro lo schermo di un videogioco e provare a creare"
tags: [videogiochi]
categories: [talk]

width: 1280
height: 720
maxScale: 1.0
---

### Input / Output

![](img_dentro_vg/hardware_porte.webp)

---

# Creare un videogioco
_arti, tecnologie, scienze, psicologia, economia, strumenti e idee per chi volesse guardare dietro lo schermo e provare a creare._

![](img_dentro_vg/banner_talk.webp)

---

## Chi sono e perché

### Stefano Cecere

![Stefano Cecere](../../assets/img/stefano/stefanocecere_pixel.webp)

- ho iniziato ad hackerare i computer a 10 anni, primo VG in terza Liceo[^giochi-liceo].
- Sviluppo videogiochi educativi @ **[Videogames Without Borders](https://vgwb.org)**
- Ricercatore nell'uso di giochi e tecnologia a Scuola @ **[Future Education Modena](https://fem.digital)**
- Docente Game A.I. / XR / OpenSource / Giochi applicati @ **[TheSign Academy](https://thesign.academy)**

[^giochi-liceo]: vedi [videogiochi per Amiga](https://cecere.xyz/project/amiga-videogames/)

---

### Perché sono qui a parlare di VG?

1. perché mi piace condividere quello che so.
2. il digitale e l'interattività immersiva sono rivoluzionarie.
3. dopo il libro, la radio, il cinema, il videogioco è il medium del presente (e sempre più del futuro).

---

### Creatività multimediale

![multimedialità](../game-dev/g4c/img/creative_multimedia.webp){: style="height:400px"}

I videogiochi sono medium multimediali e multidisciplinari.
Danno soddisfazione ad essere giocati, ma ancora di più ad essere creati.

---

### Economia e lavoro

Ci sono più di 3 miliardi di videogiocatori nel mondo.
Nel 2022 ci sono stati 203 miliardi di ricavi. E' un'industria in crescita costante. Anche in Italia crescono gli studi che producono, chi gioca (anche in modo professionale), le scuole che insegnano.

Potrebbe essere interessante lavorare con i videogiochi.

![](img_dentro_vg/GTA5-image.webp)
_GTA 5 è costato 137 milioni per svilupparlo, e altri 128 per commercializzarlo._

---

### Ikigai
L'invito è sapere che esiste una strada che porta all'Ikigai, concetto giapponese che rappresenta:
![IKIGAI](../game-dev/g4c/img/ikigai.webp)

---

## Il Digitale

![](img_dentro_vg/digi_love.webp)

Non si può parlare di videogiochi se prima non diciamo due parole sul mondo digitale.

**Digit** = cifra, numero
**Digitale** è tutto ciò che viene rappresentato e gestito in modo numerico.

---

### Codice Binario

![](img_dentro_vg/digi_binario.webp)

Usiamo i numeri binari, a base 2, con i **Bit** che possono essere intesi come interruttori spenti o accesi, dal valore 0 o 1.

E' facile costruire qualsiasi numero decimale con una sequenza di bit.

![](img_dentro_vg/digi_conversione.webp)

### Informatica
E' la scienza dell'informazione.  
Si occupa anche della codifica, memorizzazione, elaborazione, decodifica dell'informazione digitalizzata.

_Ogni_ tipo di informazione può essere codificata in numeri:

- **Testo**

![](img_dentro_vg/digi_binary_text.webp)

- **Immagini**

![](img_dentro_vg/digi_binary_image.webp)

- **Video** (immagini in movimento)
- **Modelli 3D**
- **Suoni** (campionamento)

![](img_dentro_vg/digi_binary_audio.webp)

- **Procedure logiche** (codice di programmazione)
- Tutto ciò che è misurabile e riconducibile ad un numero (temperatura, pressione, forze...)

### CPU

![](img_dentro_vg/digi_cpu_board.webp)

Dentro ogni dispositivo digitale c'è un "cuore" che elabora i dati: la CPU (Central Processing Unit).

Riceve dati in ingresso, li elabora seguendo delle istruzioni date (il programma, il software), li memorizza e li restituisce.

![CPU](img_dentro_vg/digi_cpu.webp)

---

### Codice
Le istruzioni delle procedure da seguire sono codificate in codice macchina, oggi scritto con linguaggi simili all'inglese, o rappresentanti da diagrammi di flusso logico.

![](img_dentro_vg/code_if_then.webp)

---

## Cosa è un videogioco

E' un gioco veicolato da un dispositivo _digitale_.
Può essere considerato un Medium, un veicolatore di esperienze multimediali dove il giocatore è il protagonista che agisce.

--- 

### Hardware e Software

![](img_dentro_vg/digi_hardware-software.webp)

Un videogioco è il software, il codice di programmazione che gestisce gli elementi multimediali, che viene eseguito da un Hardware specifico. A volte un videogioco è la combinazione indissolubile di HW (Hardware) e SW (Software)

---

### Piattaforme
Gli hardware più comuni per videogiocare sono

#### Computer
fisso o portatile. si sta seduti a casa. tastiera e mouse, controllers.

#### Mobile
Smartphone o Tablet. In viaggio. Touch.

#### Console
Massimo rapporto qualità/prezzo. Dedicate al gioco. Titoli AAA.

#### Arcade Cabinet
Sono console dedicate installate nelle sale giochi

#### VR / AR / XR
Nuova frontiera

#### Altro

- wearable
- audio only
- robot

---

### Interattività
![](../game-dev/g4c/img/interactive.webp){: style="height:400px"}
E' la virtù principale dei videogiochi, ed è permessa dalla CPU che elabora le azioni del giocatore in tempo reale e reagisce in modo autonomo, preprogrammato o imprevedibile, permettendo esperienze non-lineari.

---

### Un medium umano-centrico

![humanist_player](img/humanist_player.webp){: style="height:40%"}

Il Videogioco è pensato, confezionato ed eseguito intorno al giocatore e alle sue azioni. Il giocatore è al centro. Si può considerarlo un *medium umanista*.

---

### Il circuito

![Circuito dei Videogiochi](img/vg-circuit.webp){: style="height:400px"}

Il giocatore, consideriamolo umano per il momento, è al _centro_ del circuito, come un agente senziente e intelligente che percepisce, elabora decisioni e le attua andando a modificare l'ambiente e ottenendo risultati e sensazioni, l'esperienza di gioco appunto.

A differenza dei giochi a "turni" (tipo gli scacchi) dove il tempo è sospeso tra una decisione e l'altra, quasi sempre i videogiochi si svolgono in tempo reale, ovvero si gioca immersi nel tempo con l'effetto di una maggiore e costante tensione, coinvolgimento intellettuale, emotivo e motorio. Il giocatore vive all'interno di un *flusso* non solo spaziale, ma anche temporale.

Questo circuito di interattività in tempo reale differenzia il medium videogioco da tutti gli altri medium "passivi", ovvero dove si è solo spettatori.

Ultimamente i videogiochi sono sviluppati per rendere l'esperienza ludica il più  coinvolgente possibile, anche adattando i contenuti di gioco (difficoltà, ambientazioni, elementi grafici e sonori, comportamento dei personaggi, addirittura la storia) in funzione della diversità fisica, culturale, psicologica, delle capacità e delle scelte del giocatore.

Per _cucire_ al meglio le esperienze intorno ai giocatori, come fossero dei sarti multimediali, i creatori di videogiochi sono sempre più attenti alla psicologia, alla sociologia, alla filosofia e alla fisiologia umana.

![](img_dentro_vg/game_human-hw-sw-circuit.webp)

---

### VIrtù dei videogiochi

- sono una forma di divertimento -> procurano _piacere_
- sono una forma di gioco -> generano _coinvolgimento_
- hanno regole -> hanno _struttura_
- hanno obiettivi -> stimolano la _motivazione_
- sono interattivi -> necessitano _azioni, scelte_
- si adattano -> innescano un _flow mentale_
- danno risultati e feedback -> c'è _apprendimento_
- hanno una vincita ->  procurano _gratificazione_
- hanno conflitti/antagonisti/sfide -> _adrenalina_
- richiedono capacità di problem solving -> sviluppano _creatività_
- hanno interazioni tra pari -> costruzione _gruppi sociali_
- hanno personaggi e storie -> procurano _emozioni_

---

## Come si crea un VG

### Definizione degli obiettivi
Si parte da un'idea dell'esperienza che si vuole far vivere al giocatore, con tanto di sfide e difficoltà da superare, storia da raccontare, ambientazione, personaggi.  

![](https://www.wikihow.com/images/thumb/d/dd/Design-a-Video-Game-Step-01-Version-3.jpg/v4-728px-Design-a-Video-Game-Step-01-Version-3.jpg.webp)

### Pubblico
Per chi lo sto creando? Chi lo giocherà? Saranno bambini, giovani, professionisti, gente che gioca ogni tanto?

![](https://www.wikihow.com/images/thumb/b/bd/Design-a-Video-Game-Step-02-Version-3.jpg/v4-728px-Design-a-Video-Game-Step-02-Version-3.jpg.webp)

### Gameplay
Che genere e che meccanica di gioco prevedo? quali azioni dovrà compiere il giocatore?

![](https://www.wikihow.com/images/thumb/1/15/Design-a-Video-Game-Step-04-Version-3.jpg/v4-728px-Design-a-Video-Game-Step-04-Version-3.jpg.webp)

### Prototipo
Solitamente si inizia con un semplice **prototipo** per capire se le meccaniche di gioco funzionano facendolo testare a diverse persone.

![](https://miro.medium.com/v2/resize:fit:1400/0*Nk_M39HXtYEn6x7r)

![](https://theglobalgaming.com/assets/images/article/prototype-2.jpg)

### Flusso di produzione
![](img_dentro_vg/gamedev-fasi.webp)


### Team di sviluppo
Ci sono persone che riescono a creare videogiochi in solitario, ma solitamente ci sono 3 (+2) figure chiave:

- il game designer
- il programmatore
- l'artista
- il produttore
- il marketing

### Game Designer
E' lo sceneggiatore del gioco.

![](https://www.wikihow.com/images/thumb/b/b9/Design-a-Video-Game-Step-08-Version-3.jpg/v4-728px-Design-a-Video-Game-Step-08-Version-3.jpg.webp)
Bilancia i vari elementi

- Sviluppa la trama, i retroscena dei personaggi e i dialoghi

![](https://www.wikihow.com/images/thumb/d/d0/Design-a-Video-Game-Step-11-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-11-Version-4.jpg.webp)

- Sviluppo del gameplay, delle regole e del sistema di punteggio

![](https://www.wikihow.com/images/thumb/c/c8/Design-a-Video-Game-Step-07-Version-3.jpg/v4-728px-Design-a-Video-Game-Step-07-Version-3.jpg.webp)
- Determinazione del livello di difficoltà e gli incentivi

![](https://www.wikihow.com/images/thumb/a/a2/Design-a-Video-Game-Step-06-Version-3.jpg/v4-728px-Design-a-Video-Game-Step-06-Version-3.jpg.webp)

- Costruisce i livelli e determina gli ostacoli e oggetti
- Può definire il comportamento dei personaggi non giocanti / boss

![Game Design Scheme](../game-dev/g4c/img/playgamedesign.webp)

#### Storia e personaggi

![](https://www.wikihow.com/images/thumb/0/0b/Design-a-Video-Game-Step-28-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-28-Version-4.jpg.webp)

#### Level Design

![](https://www.wikihow.com/images/thumb/5/5f/Design-a-Video-Game-Step-12-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-12-Version-4.jpg.webp)

![](https://www.cgspectrum.com/hs-fs/hubfs/CGSpectrum_November2019%20Theme/images/UE4-placeholder-assets-soul-cave.jpg)

![](https://www.cgspectrum.com/hs-fs/hubfs/CGSpectrum_November2019%20Theme/images/UE4-placeholder-asset-pack-soul-cave.jpg)

---

### Arte
il 75%/90% del budget di produzione va nell'arte

#### Concept Artists

Definiscono l'aspetto grafico e la personalità, del mondo e dei personaggi

![](https://www.wikihow.com/images/thumb/9/9e/Design-a-Video-Game-Step-10-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-10-Version-4.jpg.webp)

![](https://www.wikihow.com/images/thumb/5/5c/Design-a-Video-Game-Step-13-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-13-Version-4.jpg.webp)  

![](https://www.cgspectrum.com/hubfs/Starcraft2_KoreaBillboard_Small_brian_huang.webp)

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*lrZMO82H6bjZb4Pq.png)

Definiscono l'estetica
![](https://www.wikihow.com/images/thumb/a/ab/Design-a-Video-Game-Step-16-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-16-Version-4.jpg.webp)

#### Interfaccia Utente (UI)

![](https://www.wikihow.com/images/thumb/6/62/Design-a-Video-Game-Step-15-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-15-Version-4.jpg.webp)

#### 3D modelers

![](https://theglobalgaming.com/assets/images/article/3d-modelling.jpg)

![](https://miro.medium.com/v2/resize:fit:1400/0*dLPbkVsId7CIDBzG)

![](https://www.cgspectrum.com/hs-fs/hubfs/CGSpectrum_November2019%20Theme/images/vfx-pipeline-3d-modeling-interview-victoria-passariello-image-02-1-768x746.jpg)

#### animators

![](https://theglobalgaming.com/assets/images/article/The-Division-img.1.jpg)

#### FX artists

![](https://www.cgspectrum.com/hs-fs/hubfs/CGSpectrum_November2019%20Theme/images/Assasins-Creed-Odyssey-Landscape-Ubisoft-600x338.jpg)


#### Musicisti

![](https://www.wikihow.com/images/thumb/e/ec/Design-a-Video-Game-Step-23-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-23-Version-4.jpg.webp)

#### Audio

![](https://www.wikihow.com/images/thumb/0/08/Design-a-Video-Game-Step-20-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-20-Version-4.jpg.webp)

![](https://www.wikihow.com/images/thumb/5/59/Design-a-Video-Game-Step-21-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-21-Version-4.jpg.webp)

![](https://www.wikihow.com/images/thumb/2/25/Design-a-Video-Game-Step-22-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-22-Version-4.jpg.webp)

### Programmazione

![](img_dentro_vg/game_programming.webp)

Tutta la tecnologia digitale, la logica, l'interfacciamento tra hardware e software.
Il programmatore è la figura più ingegneristica con le maggiori competenze tecnologiche. Deve trovare le soluzioni conoscendo bene l'hardware e il software.

SOno necessarie passione per la logica, matematica, la fisica, il pensare bene, l'ottimizzare, statistica.

![](img_dentro_vg/visual-scripting2.webp)

![](img_dentro_vg/visual-scripting.webp)


Ci sono molti linguaggi che possono essere usati, e si va dal "visual scripting" al Javascript, al C# al C++ (in ordine di complessità).

- Creazione di un motore di base personalizzato per il gioco
- Porgrammazione delle interazioni
- Gestione della fisica (ad es. differenze di gravità in un gioco ambientato nello spazio)
- La resa grafica
- Intelligenza Artificiale negli avversari
- Aggiunta di effetti sonori, musica e voci fuori campo
- Implementare la logica e la meccanica del gioco
- Creazione dell'interfaccia utente
- Consentire ai giocatori di competere o cooperare tramite LAN o Internet
- Sviluppo di strumenti personalizzati

### Produzione

- Nei giochi medio/grandi è essenziale la figura del **Produttore**, che tiene le fila di tutte le persone che stanno lavorando insieme.
- Controllo qualità, verifica i bug (errori e problemi)
- Scrittura (dei testi, della storia)
- Traduzioni (la maggior parte dei videogiochi sono in inglese più le lingue native)
- Attori (per registrare le voci)

### Marketing
Si preoccupa di "vendere" il videogioco, facendo analisi di mercato (giochi simili, concorrenti) e curando la comunicazione, la diffusione, la community dei giocatori, la visibilità nei negozi.

## Categorie e casi studio

### Azione

#### Assassin's Creed 2

<https://www.youtube.com/watch?v=AzEEwKcuEng>

### Arcade
I giochi Arcade sono quei giochi, nati negli anni ’80, con meccaniche e caratteristiche semplici. Lo scopo principale dei giochi arcade, visto anche che nascono per le sale giochi, è quello di cercare di superare e superarsi con punteggi sempre più alti.
Tramite questo tipo di videogiochi il giocatore aumenta la destrezza oculo-motoria e velocizza l’individualizzazione di strategie per poter superare il punteggio stabilito. Ad oggi il genere degli arcade, vista la quasi totale scomparsa delle sale giochi, ha ancora vita nei giochi per smartphone. Tra gli esempi più noti del genere abbiamo il sempreverde Pac-Man e Space Invaders.



### Audio game
Giochi sviluppati soprautto per i non-vedenti, ma interessanti e godibili da tutti.
E' qui che si sviluppato e trovano le più avanzate tecnologie di spazialità.
Anche una narrativa solo audio è molto interessante per stimolare l'immaginazione, avvicinandoci al libro.

### Avventura
Il videogiocatore, in questo genere, si ritrova libero di esplorare aree di gioco sempre nuove, panorami sempre diversi risultando libero di interagire con i vari scenari e personaggi secondari.

#### The Legend of Zelda: Breath of the Wild

### Avventura Platform / Puzzle 

#### Portal
![](../../assets/img/played/videogame/portal.webp)

### Avventura Punta e Clicca

#### 7 FRAMES
![](https://play-lh.googleusercontent.com/vbnSW_DVLmu-gR2hBETt3fdaJWEzltceP4uSTU8Zro9PZBfhTBxs3OktD46kvXqokA=w526-h296-rw)
videogioco realizzato da 7 ragazzini, sotto la mia supervisione, in 3 giorni.
<https://2042ed.org/2042/jam/7-frames/>

#### Thimbleweed Park
![](https://cdn.akamai.steamstatic.com/steam/apps/569860/ss_1a90833d40cb29fe1a13ef72f154b36f5fe0d2a5.1920x1080.jpg)

### Combattimento

#### Street Fighter
![](https://www.stuff.tv/wp-content/uploads/sites/2/2021/08/street_fighter.jpg)

### Corse
#### Assetto Corsa
![](https://www.gamereactor.it/media/58/assettocorsaps4_1845873b.jpg)

### Casual
Giochi di breve durata, spesso giocati su smartphone e tablet durante gli spostamenti o negli intermezzi della vita quotidiana.

#### Fancade

![](../../assets/img/played/videogame/fancade.webp)
Fancade is a huge collection of simple games. Play them instantly, or make your own game using drag-n-drop building blocks!
website: [fancade.com](https://www.fancade.com)

### Educativi
Nel mondo della scuola e dell'educazione in generale, si è scoperto quanto i videogiochi possano essere utilissimi per determinati scopi didattici, a volte molto più coinvolgenti e immediati delle tecniche normali. Che siano esperienze in Realtà Virtuale o Aumentata per esplorare l'astronomia o la meccanica, o giochi strategici per rivivere la Storia, giochi che ti fanno imparare lingue straniere o risolvere problemi scientifici, la EdTech (così si chiama in gergo l'uso delle nuove tecnologie per fini educativi) è già tra noi.

#### Antura and the Letters
![](../../assets/img/played/videogame/antura.webp)

### ExerGame
Quando l'interazione con il gioco è con il movimento fisico, dal semplice camminare (*PokemonGO*) al correre perché inseguiti da zombies virtuali (*Zombie Run*), dal fare addominali e flessioni per combattere un mostro (*Ring Fit Adventure*) al ballare in coreografia perfetta (*Just Dance*).

#### Ring Fit Adventure
![](../../played/videogame/img/ringfit_adventure.webp)

### FPS / Sparatutto
I giochi in prima persona (First Person Shooter) o terza persona.
Di solito sono giochi violenti: da soli o in team si combattono gli avversari impiegando armi da fuoco. Spesso l'ambiente circostante è visto dalla prospettiva del proprio personaggio di gioco.

#### Fortnite
![](../../assets/img/played/videogame/fortnite.webp)
![](https://theglobalgaming.com/assets/images/article/Fortnite-gameplay-img.1.png)

### Gestionali / Manageriali
Si deve gestire una città, un mondo, una squadra di calcio, uno studio di videogiochi, una fabbrica, un Governo!, una ditta edile.. oggi qualsiasi cosa necessiti un manager nel mondo reale, ha la sua controparte nel mondo videoludico, e spesso con dettagli e procedure talmente precise, che i videogiochi non solo formano i nuovi Manager, ma vengono usati per migliorarsi, formare giovani leve, e simulare scenari alternativi. Davvero: ci sono scuole di business che usano i videogiochi anche per decidere chi assumere e chi no.
Ma il "management" potrebbe essere anche solo il giardino di casa o il proprio allevamento di draghi pollo, il principio è lo stesso: imparo a gestire sistemi complessi, facendo crescere qualcosa di mio, in un ambiente simulato, sicuro e divertendomi.

#### Anno 1800
![](https://assets.rockpapershotgun.com/images/2020/01/Anno-1800-Best-Management-Games.jpg)

### Musicali
Due sono le componenti estetiche fondamentali per un gioco: la grafica e la musica.
E qualche videogioco ha fatto della musica la componente principale, facendo giocare direttamente con la propria colonna sonora, con canzoni e con i suoni.

#### Beat Saber
![](https://i.ytimg.com/vi/3ehSPtWoiuc/maxresdefault.jpg)

### Platform

#### Braid
![](../../assets/img/played/videogame/braid.webp)

### Puzzle
#### Monument Valley

![](../../assets/img/played/videogame/monumentvalley.webp)

### RPG
Gli RPG (Role-Playing Game) sono un genere videoludico basato principalmente sul fantasy e che vede la sua origine tramite i classici GDR (Dungeons and Dragons). In questo genere di giochi il giocatore prende il controllo di un personaggio e lo potenzia fino a raggiungere il livello massimo disponibile modificando a piacimento i vari parametri. Riguardo al genere bisogna fare una distinzione tra il JRPG (di stampo giapponese) e l’RPG occidentale. Le differenze riguardano solo le tematiche. Inizialmente il genere prevedeva battaglie a turni ma questo stile è stato via via abbandonato per delle dinamiche più action. Tra gli esempi abbiamo la saga di *Final Fantasy* e di *Dragon Quest*.

#### Final Fantasy serie
![](../../assets/img/played/videogame/finalfantasy.webp)

### Sandbox
#### Minecraft

### Simulazioni
I videogiochi di simulazione cercano di simulare il più possibile la vita reale. Sono utilizzati anche da piloti per esercitarsi nell’uso di alcuni mezzi di trasporto. Lo scopo principale è quello di permettere al giocatore di fare cose che nella vita reale non potrebbe fare (come pilotare un aereo, fare gare clandestine con le macchine, essere una capra!) 

#### Kerbal Space Program
![](../../assets/img/played/videogame/kerbal.webp)

Take charge of the space program for the alien race known as the Kerbals. You have access to an array of parts to assemble fully-functional spacecraft that flies (or doesn’t) based on realistic aerodynamic and orbital physics. Launch your Kerbal crew into orbit and beyond (while keeping them alive) to explore moons and planets in the Kerbol solar system, constructing bases and space stations to expand the reach of your expedition.  
website: [kerbalspaceprogram.com](https://www.kerbalspaceprogram.com)


### Sportivi
Tutti nella vita abbiamo giocato ad un videogioco sportivo, chi per passione, chi per divertimento con gli amici ma una partita a FIFA o a PES (ma anche ad NBA, o gli altri sport) l’abbiamo fatta. Lo scopo è quello di simulare l’esperienza reale della gestione della squadra e quindi di utilizzare e creare le strategie adatte per vincere.

#### NBA
![](../../assets/img/played/videogame/nba.webp)
**Curricular connections:** Social Studies; biomechanics; economics; biometrics; management **Possible skills taught:** Systems thinking; collaboration; decision-making; critical gaming vocabulary; critical thinking; historical awareness

### Strategia 
Se i Giochi da Tavolo sviluppano un senso della strategia a turni sequenziali, ovvero decido la mia mossa in previsione di quella dei miei prossimi avversari e delle mie prossime mosse, il videogioco permette una ricerca di strategia in Tempo Reale, ovvero mentre tutti gli altri giocatori e avversari stanno giocando le loro mosse.
Il tipo di gioco si chiama appunto RTS (Real Time Strategy).
E il bello è che possiamo giocare tanto contro altri giocatori online, tanto contro le Intelligenze Artificiali più brave al mondo.
Come con i giochi manageriali, anche quelli che richiedono una forte strategia sviluppano molto la capacità di analisi e di previsione a futuro in funzione dello situazione attuale e alla storia precedente.

#### Civilization 
![](../../assets/img/played/videogame/civilization.webp)

#### StarCraft: Brood War
![starcraf](https://ftw.usatoday.com/wp-content/uploads/sites/90/2021/12/starcraft-brood-war.png)

## Idee e strumenti per iniziare

### Consigli

![](https://www.wikihow.com/images/thumb/0/08/Design-a-Video-Game-Step-32-Version-4.jpg/v4-728px-Design-a-Video-Game-Step-32-Version-4.jpg.webp)

- segnatevi i videogiochi che vi piacciono di più, e iniziate a studiarli, ovvero domandatevi: come lo avranno realizzato? andate a cercare dei video che lo spiegano.
- tenete sempre a portata di mano un quadernino dove registrare le idee che vi vengono in mente su giochi che vi piacerebbe creare.
- guardate qualche video di persone che creano videogiochi (ad esempio [Brackeys](https://www.youtube.com/@Brackeys))
- provate a creare qualcosa partendo da modelli già fatti e modificateli / hackerateli (io ho iniziato così)

Ecco alcuni strumenti con cui iniziare:

### Usare framework dedicati
Sono soluzioni che consentono di partire da un gioco fatto e finito, e poterlo modificare o crearne uno simile (tipo un'avventura punta e clicca o un platform)

### Super Mario Maker 2
Per la Nintendo Switch. Semplicissimo creare livelli platform.
Level Design.

![](../../assets/img/played/videogame/supermariomaker.webp)


### Portal 2 editor
Creare un livello di Portal è un'esperienza a 360 gradi.

### Twine
Per creare storie interattive. Gratuito.
<https://twinery.org/>

### Scratch
Molto semplice, "visuale", è indicato per il bambini ma può essere un primo passo per tutti i neofiti.
<https://scratch.mit.edu/>

### Code.org
Un vero e proprio ambiente per imparare a programmare videogiochi. anche in Italiano. gratuito. online.
<https://code.org/>

### MakeCode Arcade
Una versione evoluta di Code.org, per programmare giochi più complessi (multiplayer, avventure, da giocare poi su hardware dedicato)
<https://arcade.makecode.com/>

### Unity

![](https://miro.medium.com/v2/resize:fit:1256/format:webp/0*unSpFPROhQMKZ6XZ.jpg)

Strumento estremamante professionale, ma molto accessibile, e gratuito per creare giochi anche grande qualità (la metà dei videogiochi del mondo è creata con Unity). Ha moltissime risorse per imparare, e una serie di progetti di esempio da studiare (microgames).  
<https://learn.unity.com/project/start-learning-1>

## Approfondimenti

![2042ed](../../assets/img/logo/header_2042ed.webp)

Nel mio sito [2042ed.org](https://2042ed.org/) ci sono diverse risorse per approfondire il mondo dei giochi e dei videogiochi, sia da giocatori che da sviluppatori.

### Scuole
Se questo mondo ti piace e ti interessa, ti invito a contattarmi e provare a valutare delle scuole di sviluppo videogiochi, magari andando agli open day.

- [TheSign Academy](https://thesign.academy/) (scuola dove insegno io) open day venerdì 5 maggio
- [Università di Firenze](https://www.unifi.it/index.php?module=ofform2&mode=1&cmd=3&AA=2022&afId=598918) inizia ad avere esami di Game Design.

### Video

- How to program in C# - BASICS - Beginner Tutorial
<https://www.youtube.com/playlist?list=PLPV2KyIb3jR6ZkG8gZwJYSjnXxmfPAl51>

### Articoli

- <https://www.wikihow.it/Creare-un-Videogioco> (da cui sono tratte alcune immagini di questa pagina)

### Libri

- Jesse Schell – The Art of Game Design. A Book of Lenses
- Le professioni del videogioco (Marco Accordi Rickards e Paola Frignani)

### Film da vedere

- Tetris (2023, Apple TV)
- Wargames (1983)
- Ralph Spaccatutto (2012)
- Free guy (2021)
- Ready Player One (2018)
- The Super Mario Bros (2023)

### Documentari

- La storia di Minecraft: <https://www.youtube.com/watch?v=1rOUfNa7dxM>
