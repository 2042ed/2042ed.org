# Introduzione e Metodi

![[ai_content_intro.png]]

## Introduzione alla A.I.
  - storia: inizio anni 50, turing giocare a scacchi senza computer
  - modellare l'intelligenza
  - deterministici
  - Deep Blu fine anni '90
  - AI e Videogiochi
	  - giocare (NPG e player)
	  - creare contenuti
	  - analizzare gameplay e modellare il giocatore
  - big data & GPU power -> ML

## Machine Learning
### i fondamentali
iniziamo con una semplice ma completa introduzione alle NN, ML, GAN. sono concetti che ci porteremo avanti per anni ed è bene conoscere l'ABC

[ML parte 1](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-1-97d4bce99a06)
[ML parte 2](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-2-dec556e4855d)
[ML parte 3](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-3-deep-learning-e-convolutional-neural-network-cnns-cc106559ffa9)
[ML parte 4](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-4-c707feee1cf8)
[ML parte 5](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-5-5e9083caf8f3)
[ML parte 6](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-6-86cd682ff71a)
[ML parte 7](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-7-bbd34f905ab8)
[ML parte 8](https://medium.com/@giovannitoschi/il-machine-learning-%C3%A8-divertente-parte-8-come-imbrogliare-una-rete-neurale-9116075d5df0)

## Metodi AI nei videogiochi

### Utility
E' la funziona che misura la razionalità di una scelta.
Usata per valutare la bontà di un percorso di scelte, "campionando" lo rappresentazione dello spazio.
Ci possono essere poi funzioni euristiche per approssimare e velocizzare il calcolo, loss, cost, or error per minimizzare.

*Learning = Maximize Utility (Representation)*

### Ad-Hoc Behavior Authoring
Il metodo *classico*, e tutt'ora più usato per controllare gli NPC dei videogiochi: Finite state machines, behavior trees and utility-based AI.

#### FSM

![[fsm_scheme.png]]
![[fsm_pacman.jpg]]

3 componenti:
1. **stati**: contiene la descrizione dello stato in cui si trova
2. **transizioni**: condizioni che fanno passare da uno stato all'altro
3. **azioni**: cosa succede durante uno stato

Pro: semplici da progettare, implementare, visualizzare e debuggare.
Cons: complessi da progettare su larga scala. Non facili da estendere, non sono flessibili nè dinamici, impossibile "evolverli" una volta consolidati.
Risultati un po' troppo prevedibili (salvo iniettare fuzzy e probabilità nelle transizioni)

#### Behavior Trees

![[bt_scheme.png]]

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

[introduction to BT](https://www.gamasutra.com/blogs/ChrisSimpson/20140717/221339/Behavior_trees_for_AI_How_they_work.php)
[video](https://www.youtube.com/watch?v=uq8hnnkAxsw)

#### Flocking
- **Separation**: Each boid needs to maintain a minimum distance with neighboring boids to avoid hitting them (short-range repulsion) 
- **Alignment**: Each boid needs to align itself with the average direction of its neighbors, and then move in the same velocity with them as a flock 
- **Cohesion**: Each boid is attracted to the group's center of mass (long-range attraction) 


### TreeSearch / Pathfinding

### Evolutionary Computation / Genetic

### Supervised Learning
### Reinforcement Learning
### Unsupervised Learning


### Random / Fuzzy / Noise

