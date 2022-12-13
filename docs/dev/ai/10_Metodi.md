---
title: "Introduzione e Metodi"
date: 2017-09-09T00:00:00
type: book
weight: 10
toc: true
draft: false
---

[video The Mind Game](https://www.youtube.com/watch?v=QQRqTuvBL3E)

## Introduzione alla A.I.
  - storia: inizio anni 50, turing giocare a scacchi senza computer
  - modellare l'intelligenza
  - deterministici
  - Deep Blu fine anni '90
  - Narrow/Weak AI & Strong (true) AI / AGI
  - AI e Videogiochi
	  - giocare (NPG e player)
	  - creare contenuti
	  - analizzare gameplay e modellare il giocatore
  - big data & GPU power -> ML

## AI & Videogames

![](img/ai_content_intro.webp)

AI Plays and Improves Your Game.
enhances the experience of the player.

AI può giocare con due obiettivi:
1. play **well** 
	a) il giocatore (play test e valutazione game design)
	b) gli NPC (per bilanciamento difficoltà dinamica)

2. play **believably**
	a) debug e simulazione
	b) credibilità e umanizzazione


## AI Model
![](img/AI-model.webp)

## Metodi AI nei videogiochi

### Utility
E' la funziona che misura la razionalità di una scelta.
Usata per valutare la bontà di un percorso di scelte, "campionando" lo rappresentazione dello spazio.
Ci possono essere poi funzioni euristiche per approssimare e velocizzare il calcolo, loss, cost, or error per minimizzare.

*Learning = Maximize Utility (Representation)*

### Ad-Hoc Behavior Authoring
Il metodo *classico*, e tutt'ora più usato per controllare gli NPC dei videogiochi: Finite state machines, behavior trees and utility-based AI.

#### FSM

![](img/fsm_scheme.webp)
![](img/ai.fsm.pacman.webp)

3 componenti:
1. **stati**: contiene la descrizione dello stato in cui si trova
2. **transizioni**: condizioni che fanno passare da uno stato all'altro
3. **azioni**: cosa succede durante uno stato

Pro: semplici da progettare, implementare, visualizzare e debuggare.
Cons: complessi da progettare su larga scala. Non facili da estendere, non sono flessibili nè dinamici, impossibile "evolverli" una volta consolidati.
Risultati un po' troppo prevedibili (salvo iniettare fuzzy e probabilità nelle transizioni)

#### Behavior Trees

![](img/ai.bt.webp)
![](img/ai.bt.2.webp)

Un Behavior Tree (BT) è un sistema simile al FSM, che modella la transizione tra un numero finito di insiemi di azioni (tasks, o behaviour).

Pros: rispetto agli FSM: modularità. si possono comporre comportamenti molto complessi partendo da semplici tasks.

Sono composti da Behaviour anzichè Stati in una stuttura ad albero con un nodo iniziale e n childs.
L'albero viene attraversato da sinistra a destra con una frequenza (ticks) e ogni nodo può ritornare questi valori:
1. **run** se attivo
2. **success** se completato
3. **failure** se fallisce

I Nodi sono di tre tipi
**sequence**
se figlio *succeds*, continua al seguente. *Succeds* quando finiscono tutti i figli, altrimenti *failure*

**selector**: probability o priority
si seleziona un nodo figlio. se succeds, esso stesso succeds.
se figlio failure, se ne seleziona un altro (by priority) oppure failure (probability).

**decorator**
arricchisce il nodo fliglio: ad esempio ne nega il risultato, oppure lo fa andare n volte (repeater)

[📖 Intro to BT](https://www.gamasutra.com/blogs/ChrisSimpson/20140717/221339/Behavior_trees_for_AI_How_they_work.php)
[📽 Intro to BT](https://www.youtube.com/watch?v=uq8hnnkAxsw)
[📽 Behavior Designer](https://www.youtube.com/watch?v=T_of4_jRoJA)

#### Utility-based AI

Serve per creare sistemi di Decision-making
Ogni istanza nel gioco viene dotata di una funziona Utility che ne restituisce l'importanza.
Una funzione può misurare qualsiasi cosa di osservabile (distanza, salute) o deducibile (emozioni / minaccia)

Esempio di Behaviour Ms PacMan
![](img/utility-based.webp)

Esempio **scelta arma di un agente NPC**, si misurano: 

**Range** a seconda della distanza dell'avversario si assegna una utility all'arma. 

**Inertia** durata dell'arma corrente, per non cambiarla troppo spesso. 

**Random noise** effetto random così che non seleziona _sempre_ la stessa arma nella stessa situazione. 

**Ammo** livello attuale di munizioni

**Indoors** penalizza alcune arme all'interno di edifici (esempio granate)

L'agente controlla e chiama regolarmente la Utility di tutte le armi disponibili e seleziona la migliore

#### Random / Fuzzy / Noise
queste sono versioni base. per renderle meno deterministiche si usano tecniche di random e fuzzy.

#### Hybrid / Composition
questi metodi possono essere composti.

### Tree Search 
*Tutta la AI è fondamentalmente una ricerca* di una pianificazione, di un path, di un modello, di una funzione, etc. e gli algoritmi di ricerca sono il cuore.

#### Uninformed Search
cercano tutto lo spazio senza un goal preciso
1. Depth-first search
2. Breadth-first search

#### Best-First Search
si ha un'idea del goal finale e una funzione che ne misura la distanza

Pathfinding: **A* star**: esplora i nodi adiacenti, misurandone il costo e la distanza dal goal finale.
Funzioane bene sia in 2D che in 3D.
[intro to A*](https://www.redblobgames.com/pathfinding/a-star/introduction.html)

A* può essere usato anche per navigare negli spazi degli stti di gioco, non solo navigazione fisica. utile per il PLANNING. (vedi Mario A*)

#### Mini Max

![](img/ai.minmax.webp)

[📽 Algorithms Explained – minimax and alpha-beta pruning](https://www.youtube.com/watch?v=l-hh51ncgDI)

#### Monte Carlo Tree Search
se l'albero ha troppi rami e troppo profondo, mini max non funziona bene.

Giochi deterministici come Go, Scacchi e Dama, a informazione imperfetta come Battaglia Navale, Poker, Bridge o giochi non deterministici quali il backgammon e il Monopoly necessitano di un altro algoritmo: MCTS che si avvicina al Minimax.

Come fa MCTS a gestire forte ramificazione, mancanza di buone funzioni per la valutazioen degli stati, la mancanza di informazione e di determinismo?
1. non cerca tutti i rami, ma solo i più promettenti
2. bypassa la mancanza di funzioni, _giocando casualmente_ una partita fino a quel livello di profondità

MCTS può essere interrotto quando si vuole. necessita solo di due cose. le regole del gioco e una funzioen di valutazione dello stato finale (win, loss, draw, score)

gli steps sono:
1. Selection (si sceglie il nodo da espandere)
2. Expansion (radom si sceglie in figlio non espanso)
3. Simulation (si gioca casualmente fino alla fine)
4. Backpropagation (il reward viene propagato indietro)

![](img/ai_treesearch_montecarlo.webp)

### GOAP
vedere [[12_GOAP)

### Navigation Flocking
- **Separation**: Each boid needs to maintain a minimum distance with neighboring boids to avoid hitting them (short-range repulsion) 
- **Alignment**: Each boid needs to align itself with the average direction of its neighbors, and then move in the same velocity with them as a flock 
- **Cohesion**: Each boid is attracted to the group's center of mass (long-range attraction) 

### Evolutionary Computation / Genetic

#### Ottimizzazione
è necessaria una utility function, evaluation function o fitness function che restituisca la un valore numerico con la bontà (fitness) della soluzione, da massimizzare o minimizzare.
L'ottimizzazione è il procedimento di cercare nello *spazio di ricerca* una soluzione che abbia il massimo o minimo valure di fitness.
Si cerca di rappresentare una soluzione come un array di valori (es. le azioni per uscire da un labirinto) da modificare con tecniche prese dalla genetic evolutiva: si cambia un gene o una seguenza, casualmente

#### Local Search
**deterministic** hill climber: si cercano tutti gli adiacenti (solo per piccole variazioni)

1. Init: Se crea una soluzione *s* casuale nello spazio.
2. si generano tutti i vicini a s (un vicino è una soluzione che si discosti un minimo).
3. si valutano tutti i vicini (fitness)
4. se nessuno è migliore, si tiene s
5. Altrimenti si ricomincia con il nuovo s' -> 2

**gradient-based** hill climber: cerca il gradiente minimo o massimo di modifica della utility

1. Init: Se crea una soluzione *s* casuale nello spazio.
2. MUTAZIONE: si genera s' mutandolo
3. VALUTAZIONE di s'
4. se s' è migliore, si tiene s'
5. -> 2


![](img/ai.local_search.webp)

#### Evolutionary Algorithms
cercano nello spazio _globale_, non soltanto nella adiacenze della attuale soluzione.

SI generano molte soluzione, si buttano via quelle minori e si tengono le migliori. come nella selezione naturale o evoluzioen Darwiniana.

L'idea è che se troviamo due buon soluzioni, una soluzione che ne sia una combinazione o intermediazione potrebbe essere altrettanto buona se non migliore.

![](img/ai.local_search_evo.webp)


## Machine Learning
### i fondamentali
iniziamo con una semplice ma completa introduzione alle NN, ML, GAN. sono concetti che ci porteremo avanti per anni ed è bene conoscere l'ABC, questi 8 post di "Machine Learning è divertente" sono un ottimo inizio.

[ML parte 1](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-1-97d4bce99a06)
[ML parte 2](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-2-dec556e4855d)
[ML parte 3](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-3-deep-learning-e-convolutional-neural-network-cnns-cc106559ffa9)
[ML parte 4](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-4-c707feee1cf8)
[ML parte 5](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-5-5e9083caf8f3)
[ML parte 6](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-6-86cd682ff71a)
[ML parte 7](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-7-bbd34f905ab8)
[ML parte 8](https://medium.com/@giovannitoschi/il-machine-learning-%C3%A8-divertente-parte-8-come-imbrogliare-una-rete-neurale-9116075d5df0)

### Supervised Learning
#### Reti Neurali
![](img/ai.neuron.webp)

Explained In A Minute: Neural Networks
<https://www.youtube.com/watch?v=rEDzUT3ymw4>

![](img/ai.neuralnetwork.webp)

#### backpropagation

#### Decision Tree Learning
![](img/ai.decision_tree.webp)
![](img/ai.decision_tree_2.webp)


### Reinforcement Learning (RL)
si ispira a come imparano gli esseri viventi

![](img/ai.reinforcedlearning.webp)

A central question in RL problems is the right balance between the exploitation of current learned knowledge versus the exploration of new unseen territories in the search space

### Unsupervised Learning
#### Clustering
Good clusters are characterized by two core properties: 
1) high intra-cluster similarity, or else, high compactness
2) low inter-cluster similarity, or else, good separation.

#### Frequent Pattern Mining

due tipi sono interessanti
1) frequent itemset mining
2) frequent sequence mining