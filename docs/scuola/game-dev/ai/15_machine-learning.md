---
title: Machine Learning
date: 2023-01-10
updated: 2023-01-10
---
# Machine Learning

> How to construct computer programs that automatically improve with experience. (Tom Mitchell)

> Addestrare le macchine a trovare la soluzione migliore ad un problema imparando dai dati e dai propri errori.

**Come si insegna ad una macchina a riconoscere un gatto?**  
<https://www.youtube.com/watch?v=LrGdHmHkfUk>  
<iframe loading="lazy" title="Come si insegna ad una macchina a riconoscere un gatto?" src="https://www.youtube.com/embed/LrGdHmHkfUk?feature=oembed" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" width="500" height="281" frameborder="0"></iframe>

---

## Introduzione
Iniziamo con una semplice ma completa introduzione al 

- Machine Learning (ML)
- apprendimento supervisionato (Supervised Learning)
- apprendimento non supervisionato (Unsupervised Learning)
- Reti Neurali / Neural Network (NN)
- Generative Adversial Network (GAN)

Sono concetti che ci porteremo avanti per anni ed è bene conoscerne l'ABC.  

![](../../../assets/img/gamedev/ai-symbolism-vs-connectivism.webp)

### Slides

![Dati di una banana matura, con il suo grado di giallo e la sua morbidezza](https://www.alessiopomaro.it/content/images/2022/12/addestramento-modello-machine-learning-fase-1-2.webp){: style="height:200px"}
![Dati della seconda banana matura, con il suo grado di giallo e la sua morbidezza](https://www.alessiopomaro.it/content/images/2022/12/addestramento-modello-machine-learning-fase-2.webp){: style="height:200px"}
![Dati delle prime tre banane mature per la fase di training del modello di Machine Learning](https://www.alessiopomaro.it/content/images/2022/12/addestramento-modello-machine-learning-fase-3.webp){: style="height:200px"}
![Nel diagramma delle misurazioni indichiamo la prima banana acerba (pallino verde)](https://www.alessiopomaro.it/content/images/2022/12/addestramento-modello-machine-learning-fase-4.webp){: style="height:200px"}
![Il diagramma delle misurazioni con valori di banane mature e acerbe](https://www.alessiopomaro.it/content/images/2022/12/addestramento-modello-machine-learning-fase-5.webp){: style="height:200px"}
![Il diagramma completo delle misurazioni di addestramento del modello di Machine Learning](https://www.alessiopomaro.it/content/images/2022/12/addestramento-modello-machine-learning-fase-6.webp){: style="height:200px"}
![Il confine decisionale derivante dai dati di addestramento del modello di Machine Learning](https://www.alessiopomaro.it/content/images/2022/12/addestramento-modello-machine-learning-fase-linea-decisionale.webp){: style="height:200px"}
![Le previsioni del modello di Machine Learning addestrato](https://www.alessiopomaro.it/content/images/2022/12/previsioni-modello-machine-learning-addestrato.webp){: style="height:200px"}
![Un diagramma delle misurazioni con dei dati più verosimili](https://www.alessiopomaro.it/content/images/2022/12/diagramma-misurazioni-dati-reali.webp){: style="height:200px"}
![Un modello di Machine Learning più verosimile: il confine decisionale non è più una retta](https://www.alessiopomaro.it/content/images/2022/12/modello-di-machine-learning.webp){: style="height:200px"}
![Machine Learning: il fenomeno dell'overfitting](https://www.alessiopomaro.it/content/images/2022/12/machine-learning-overfitting.webp){: style="height:200px"}
![I dati di training per il modello che dovrà stimare il prezzo delle case](https://www.alessiopomaro.it/content/images/2022/12/machine-learning-dati-training-prezzo-immobile-1.webp){: style="height:200px"}
![Due modelli di Machine Learning che prendono vita dai dati di addestramento](https://www.alessiopomaro.it/content/images/2022/12/machine-learning-dati-training-prezzo-immobile-modello.webp){: style="height:200px"}

![Le fasi di apprendimento del modello di Machine Learning](https://www.alessiopomaro.it/content/images/2022/12/machine-learning-come-viene-creato-il-modello.webp){: style="height:200px"}

### Machine Learning è divertente
Questi 8 post di "Machine Learning è divertente" sono un ottimo inizio:

- [ML parte 1](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-1-97d4bce99a06)
- [ML parte 2](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-2-dec556e4855d)
- [ML parte 3](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-3-deep-learning-e-convolutional-neural-network-cnns-cc106559ffa9)
- [ML parte 4](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-4-c707feee1cf8)
- [ML parte 5](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-5-5e9083caf8f3)
- [ML parte 6](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-6-86cd682ff71a)
- [ML parte 7](https://medium.com/botsupply/il-machine-learning-%C3%A8-divertente-parte-7-bbd34f905ab8)
- [ML parte 8](https://medium.com/@giovannitoschi/il-machine-learning-%C3%A8-divertente-parte-8-come-imbrogliare-una-rete-neurale-9116075d5df0)

## Reti Neurali
![](img/ai.neuron.webp)

<https://www.youtube.com/watch?v=rEDzUT3ymw4>  
<iframe loading="lazy" title="Explained In A Minute: Neural Networks" src="https://www.youtube.com/embed/rEDzUT3ymw4?feature=oembed" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" width="500" height="281" frameborder="0"></iframe>

## Supervised Learning

![](../../talk/img/ml-supervised.webp)

Ricordate che per molti anni sul web, per confermare l'invio di una form, ci chiedevano di leggere una parola o dei numeri dentro una foto (sembravano parole di un libro o i numeri civici delle case)? Ultimamente ci chiedono di riconoscere le strisce pedonali o i semafori, o Facebook ci chiedeva di taggare gli amici nelle foto.  
Sapete cosa abbiamo fatto negli ultimi 15 anni, e stiamo ancora facendo?  
Avete intuito bene: abbiamo creato una mole di dati "etichettati" correttamente, affinché le macchine potessero imparare la corrispondenza tra un'immagine e il suo contenuto. Così oggi le macchine sono bravissime a riconoscere i testi scritti o le auto a guida autonoma sono sempre più precise nel riconoscere quello che vedono, e Facebook ora sa riconoscere chi sono i nostri amici nelle foto.

![](../../talk/img/comic-captcha.webp)

## Reinforcement Learning (RL)

![](../../talk/img/ml-reinforced.webp)

Prendiamo un "agente" ovvero un'entità dotata di sensori e attuatori e lo mettiamo in un ambiente, ad esempio dentro un campo da tennis virtuale e gli diciamo: questa è una palla e se la fai cadere due volte nel tuo campo, perdi, ma se la fai cadere due volte oltre la rete, vinci. Puoi solo spostarti e colpire la palla per farla rimbalzare. Vai.  
Non diremmo così a nostro figlio, vero? Però se il nostro "agente" virtuale avesse molto tempo per fare qualche milione di partite tentando a caso e ricevendo premi o punizioni e cercando di ripetere quei movimenti che portano con maggiore probabilità ai premi, allora potrebbe imparare.
E il bello è che impara, e anche in modo sorprendente!
(Vi lascerò dei link per vedere qualche esempio pratico)

![](img/ai.reinforcedlearning.webp)

#### Imitation Learning

![](../../talk/img/ml-imitation.webp)

A nostro figlio faremmo vedere come si gioca, vero? e gli diremmo: “fai come me. colpisci la palla in questo modo, muoviti così etc.”  
Possiamo quindi programmare le AI per osservare il comportamento umano, registrarlo e analizzarlo insieme all'ambiente e ai risultati, e poi imitarlo.  
Funziona. E molto bene. Osservandoci e imitandoci.

## Unsupervised Learning

![](../../talk/img/ml-unsupervised.webp)

![](img/ai.neuralnetwork.webp)

## Sintesi

![Machine Learning: le diverse tipologie di apprendimento](https://www.alessiopomaro.it/content/images/2023/01/machine-learning-tipologie-apprendimento.webp)


![](https://www.alessiopomaro.it/content/images/2023/01/AI-ML-DL-cosa-sono.webp)


## Approfondimenti
### Video
Car training  
<https://www.youtube.com/watch?v=Aut32pR5PQA>
<https://www.youtube.com/watch?v=5lJuEW-5vr8>

Mario plays  
<https://www.youtube.com/watch?v=qv6UVOQ0F44>

Snake  
<https://www.youtube.com/watch?v=3bhP7zulFfY>

Number recognizion  
<https://www.youtube.com/watch?v=aircAruvnKk>
