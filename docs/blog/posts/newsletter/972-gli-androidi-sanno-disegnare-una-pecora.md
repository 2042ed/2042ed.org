---
title: 972. Gli androidi sanno disegnare una pecora?
date: 2023-11-05
updated: 2024-03-19
type: 
categories:
  - newsletter
tags:
  - newsletter
description: "Un'introduzione alla AI creativa"
permalink: /2042/nl/972
rating: 
publish: 
---
# 972. Gli androidi sanno disegnare una pecora?

Questa settimana sono un po’ preso e condivido questa presentazione che feci qualche mese fa. e noto come alcuni paragrafi sarebbero già da aggiornare! Però i fondamenti teorici sono sempre validi e credo possa essere utile per chi non mastica AI tutti i giorni. Ci vediamo questo fine settimana a Modena per il [Learning More](https://learningmorefestival.it/)! Buona settimana.

> **Durata**: 15 min  
> **Pubblico**: tutti  
> **Interesse**:
> 
> - cosa c'è alla base della capacità creativa delle AI?
>     
> - cosa possono creare oggi (maggio 2023) le AI?
>     

```
Piccolo quiz preliminare: il titolo cela due opere del XX secolo. Quali?
```

[Leave a comment](https://2042.substack.com/p/972/comments)

## Introduzione

Un aspetto particolarmente interessante, per qualcuno utile, per altri "disruptive" (ovvero che sta cambiando radicalmente la nostra società) dell'Intelligenza Artificiale è la sua capacità di creare nuovi contenuti. Tecnicamente si chiama _Generative AI_, o **GenAI**.  
Per comprenderne le potenzialità, i limiti ed eventuali preoccupazioni, è bene fare un accenno alla teoria e alla tecnologia che la sottende. _Dobbiamo studiare un po'_ :)

Iniziamo con una domanda: **Cosa è una pecora?**

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40c9060c-c94d-4405-ad04-02478e0b7938_960x575.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F40c9060c-c94d-4405-ad04-02478e0b7938_960x575.webp)

## Come costruire il modello

Nella nostra mente potremmo iniziare ad elencare tutte le caratteristiche che conosciamo di una pecora, costruendo un **modello simbolico**. Fossimo dei programmatori scriveremmo:

- genere: animale
    
- classe: mammifero
    
- arti: 4
    
- superficie: pelosa
    
- colore: chiaro
    
- peso: medio
    
- dimensioni: medie
    
- ... e così via altre variabili che riteniamo utili alla classificazione
    

Oppure potremmo osservare centinaia di foto di animali, con il relativo nome, e dire: deduciamo e memorizziamo le caratteristiche comuni, i "patterns" che vediamo nelle foto etichettate con "Pecora". Questo è il **modello supervisionato**.

Oppure possiamo dire: ecco tutta la conoscenza umana, testi e immagini. Vediamo di trovare tutto quello che possiamo associare alla parola "pecora". Questo è il **modello non supervisionato**.

_Spoiler: un misto delle tre sarà il **il modello GPT**._

## Machine Learning

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9dd3086-f1fd-4046-9ed0-cfca206ff59f_1024x908.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9dd3086-f1fd-4046-9ed0-cfca206ff59f_1024x908.webp)

Il Machine Learning è un sottoinsieme dell'Intelligenza Artificiale, che si preoccupa di **come le macchine possano imparare da sole**, per la precisione come possano riconoscere dei **pattern** nei **dati** e fare **previsioni** e prendere buone **decisioni** a partire da essi.

Non entreremo ora nei dettagli tecnici ma è importante sapere:

- come funziona? (rete neurale)
    
- come impara? (training)
    
- cosa può fare? (output)
    

## Come funziona?

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F334277d0-068b-4549-a079-3c2c9cb8aad7_1024x965.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F334277d0-068b-4549-a079-3c2c9cb8aad7_1024x965.webp)

### Rete Neurale Artificiale (ANN)

La Rete Neurale Artificiale si ispira alla struttura del nostro cervello, ed è composta da una rete di neuroni connessi tra loro che elaborano le informazioni in ingresso e restituiscono una risposta.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56f8f5e7-d8f8-422c-a23c-9f8ae8c29f9d_1280x720.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F56f8f5e7-d8f8-422c-a23c-9f8ae8c29f9d_1280x720.webp)

Il nostro cervello ha circa 85 miliardi di neuroni che comunicano tra loro attraverso segnali elettrici e chimici (sinapsi), segnali che seguono milioni ci connessioni accendendo diverse sequenze di neuroni. Ma il cervello è in grado di modificare le proprie connessioni (plasticità).

La versione artificiale parte dalla simulazione di un singolo neurone:

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63465200-1634-48ea-9871-69233d5dfea0_720x540.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63465200-1634-48ea-9871-69233d5dfea0_720x540.webp)

e li connette con una serie di livelli (layers) verticali. C'è un primo livello di Input, dove entrano i dati, i segnali. Tutta una serie di n (potenzialmente tanti. tantissimi) livelli intermedi "nascosti", ed infine un livello di neuroni in uscita (output). Ogni Neurone ed ogni connessione tra neuroni ha dei parametri che determina come i segnali si muovono e si trasformano.

In input potremmo avere un testo, un'immagine, i parametri di velocità della propria auto, tutto quello che vedo intorno a me.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3a20bead-15cc-4cc1-b33f-c47d10045d30_1000x649.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3a20bead-15cc-4cc1-b33f-c47d10045d30_1000x649.webp)

## Come impara?

La configurazione della Rete Neurale, ovvero la definizione di tutti i parametri, i pesi, dei nodi e delle connessioni, si chiama **Training** ed avviene analizzando grandi quantità di dati con diverse tecniche e metodi:

### Supervised learning

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67ba6e78-4cb2-4e36-be87-8f1f8f1b9b2b_1024x530.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F67ba6e78-4cb2-4e36-be87-8f1f8f1b9b2b_1024x530.webp)

La rete sa cosa le viene dato in input, e aggiorna il suo modello per avvicinarsi il più possibile alle risposte più corrette, con meno errori. Quando l'errore medio sarà inferiore ad una soglia che decidiamo noi, il modello sarà pronto per essere usato.

#### Captcha

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F987b2b91-616d-4163-b200-c27a7a876071_1104x260.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F987b2b91-616d-4163-b200-c27a7a876071_1104x260.webp)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5cf4098b-d9d6-4460-a4da-b3997c21f68a_1120x636.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5cf4098b-d9d6-4460-a4da-b3997c21f68a_1120x636.webp)

Sapete cosa abbiamo fatto negli ultimi 20 anni, rispondendo prima alla lettura di parole dei libri, poi numeri civici, poi insegne, targhe e poi semafori, idranti e tutto quanto?

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81ddd621-866d-4231-879d-79378f94947b_1024x742.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F81ddd621-866d-4231-879d-79378f94947b_1024x742.webp)

### Unsupervised Learning

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb09661ff-2ab7-4865-aca9-660fe9d13173_1024x366.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb09661ff-2ab7-4865-aca9-660fe9d13173_1024x366.webp)

Il modello non supervisionato cerca di trovare caratteristiche comuni nei dati in ingresso. correlazioni, raggruppamenti. Non sa bene cosa significhino, però ad esempio potrebbe scoprire che alcune immagini sono diverse da altre (tipo cani e gatti), che dopo un "ciao" spesso segue un "come stai?", che una appartamento le cui coordinate sono centrali rispetto alla città, ha un costo per mq più alto, e così via.

### Semi-Supervised Learning

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29bd9241-5c96-4230-bdf2-ce6468fd6a6b_1280x720.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29bd9241-5c96-4230-bdf2-ce6468fd6a6b_1280x720.webp)

Questo è un misto tra il Supervised e l'Unsupervised.

#### Big Data

Sebbene la teoria informatica avesse diversi decenni, tutto il Machine Learning ha iniziato a funzionare bene a partire dal 2010, dopo la grandissima disponibilità di dati digitalizzati e potenza di calcolo.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8df3786-478b-41a3-9f59-fd9e266f3a95_700x467.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8df3786-478b-41a3-9f59-fd9e266f3a95_700x467.webp)

[book](https://books.google.com/)

### Reinforced Learning

> Ottimo lavoro!

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5f7bb67-35a6-43de-bc76-b0f2f10b0399_1024x548.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5f7bb67-35a6-43de-bc76-b0f2f10b0399_1024x548.webp)

Impara a tentativi, aggiornato dal feedback e premi o penalità.  
Prendiamo due "agenti" ovvero un'entità dotata di sensori e attuatori e lo mettiamo in un ambiente e diciamo: voi squadra rossa dovete acchiappare la squadra blu per vincere. Voi blu non dovete farvi prendere da quelli rossi per vincere. Pronti?

👉🏼 video [Multi-Agent Hide and Seek](https://youtu.be/kopoLzvh5jY?t=5)

Caso speciale: **RLHF** (reinforcement learning with human feedback) dove gli umani danni indicatori di bontà della risposta.

### Imitation Learning

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8b78300c-32ac-436d-84b0-e3c7f770543b_1024x742.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8b78300c-32ac-436d-84b0-e3c7f770543b_1024x742.webp)

l'AI osserva e memorizza il comportamento umano, ne deduce i pattern e lo memorizza nelle ANN.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cadf126-09ce-4141-92d0-040d32fcc81e_960x960.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0cadf126-09ce-4141-92d0-040d32fcc81e_960x960.jpeg)

### Deep Learning

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa0e293c5-727e-4144-b0d9-14f1de7de74e_1450x948.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa0e293c5-727e-4144-b0d9-14f1de7de74e_1450x948.webp)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6be1420-8600-41ab-b07f-706ab1fdc60e_994x534.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff6be1420-8600-41ab-b07f-706ab1fdc60e_994x534.webp)

Si mettono diversi livelli di reti neurali, specializzate magari per analizzare diverse caratteristiche di un'immagine, per poi essere combinate.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5cf9bf2-c0fa-4a0f-ba5b-26d880c3a507_2048x1524.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff5cf9bf2-c0fa-4a0f-ba5b-26d880c3a507_2048x1524.webp)

La velocità di ricerca e scoperta di nuove soluzioni è impressionante.

## Cosa può fare?

### Predizione

- Uber: predice il traffico
    
- Ambito medico: anticipare problemi di salute, potenziali tumori
    

### Classificazione

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49f030d6-2ac2-4ac7-8ee1-2663268f79ca_1010x456.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F49f030d6-2ac2-4ac7-8ee1-2663268f79ca_1010x456.webp)

Analisi del "**sentimento**"

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdebc11ff-e702-4dd6-9554-74fda22aa75e_1200x402.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdebc11ff-e702-4dd6-9554-74fda22aa75e_1200x402.webp)

### Creazione: Generative AI

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdf47fd7c-05fd-4739-8b2f-5f8f389eb290_1000x327.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdf47fd7c-05fd-4739-8b2f-5f8f389eb290_1000x327.webp)

In pratica il modello di Deep Learning generativo:

- crea nuovi dati simili a quelli su cui si è allenato.
    
- conosce la distribuzione dei dati e quanto un dato esempio è simile
    
- predice la prossima parola in una frase.
    

#### Immagini

Le tecniche più usate sono la

- **GAN** (Generative Adversial Network)  
    Dove un modello crea degli esempi di immagini e un discriminatore vede se riesce a capire se sono reali o no
    

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f8e511f-556b-4fa7-b76b-f841551acc65_1400x520.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1f8e511f-556b-4fa7-b76b-f841551acc65_1400x520.webp)

- **Diffusion**
    

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9776599-bc16-49a6-bf69-926fc4eacb29_820x255.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa9776599-bc16-49a6-bf69-926fc4eacb29_820x255.webp)

#### testo

Il Natural Language Processing permette di comprendere il linguaggio umano.  
Large Language Models, sempre più grandi.

**LLM** **Year** **By** **Size (neurons)**

BERT 2018 Google 340 million

GPT-2 2019 OpenAI 1.5 billion

GPT-3 2020 OpenAI 175 billion

PaLM 2022 Google 540 billion

LLaMA 2023.2 Meta 65 billion

GPT-4 2023.3 OpenAI 1 trillion

PaLM 2 2023.5 Google 340 billion

## Cosa creano?

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F028e812f-b921-4320-85a2-1606a185e420_1000x405.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F028e812f-b921-4320-85a2-1606a185e420_1000x405.webp)

**Contesti applicativi**

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74ebe8ce-5100-4ec3-ba34-d3e2bd101c83_1426x598.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74ebe8ce-5100-4ec3-ba34-d3e2bd101c83_1426x598.jpeg)

Ci sono già centinaia di strumenti disponibili, ogni settimana ne esce qualcuno. Rimandiamo a questo sito: [Generative AI Landscape](https://ai-collection.org/) o [AI Tools Club](https://www.aitoolsclub.com/)

### Testo

- Chatbot: agenti di conversazione guidati dall'intelligenza artificiale per il cliente assistenza, domande frequenti e altro ancora.
    
- Creazione di contenuti: generazione di articoli, post sui social media, o scrittura creativa.
    
- Traduzione: conversione di testo tra lingue mentre preservando il significato.
    
- Riassunti: condensare un testo lungo in uno più breve, riassunti digeribili.
    
- Gestione della conoscenza: organizzazione, recupero, e analizzare le informazioni da grandi volumi di dati di testo.
    
- Quiz e Corsi
    
- Programmi di fitness
    
- Programmi di viaggi
    
- Ricette
    

Esempi:

**[ChatGPT – 4.0](https://openai.com/product/gpt-4)**  
by OpenAI (con [i plugin](https://www.marktechpost.com/2023/05/21/how-to-use-third-party-plugins-in-chatgpt-80-plugins-just-added-by-chatgpt-for-public/) fa praticamente tutto). Ha superato tutti i test di ammissione alle università americane senza un training preliminare.

**Creatività**  
può generare, modificare e iterare con gli utenti su attività di scrittura creativa e tecnica, come comporre canzoni, scrivere sceneggiature o apprendere lo stile di scrittura di un utente.

**Multimodale**  
accetta immagini come input e genera didascalie, classificazioni e analisi.

**Input**  
Accetta fino a 32k token, ovvero circa 43.000 parole (circa la metà di 120 pagine di un libro)

**Output**  
è in grado di gestire oltre 25.000 parole di testo (circa 60 pagine di un libro)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe83ff759-3d8d-4437-bc02-967d0f30ed7d_812x797.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe83ff759-3d8d-4437-bc02-967d0f30ed7d_812x797.webp)

👉🏼 [prompt examples](https://github.com/f/awesome-chatgpt-prompts/)

Alternative equivalenti:

- [Bing Chat](https://www.bing.com/chat) by Microsoft
    
- [Bard](https://bard.google.com/) - by Google
    

#### Knowledge Management

- [Notion](https://www.notion.so/)
    

#### Presentazioni

[TOME](https://tome.app/)  
generative storytelling

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecc561ec-9227-4ead-9380-a69b3f17cbd7_1370x679.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fecc561ec-9227-4ead-9380-a69b3f17cbd7_1370x679.webp)

- [Beautiful AI](https://www.beautiful.ai/)
    
- [SlideGPT](https://slidesgpt.com/)
    

#### Materiale didattico

[Aidemia](https://aidemia.co/)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f3750ac-4683-46a2-8e37-5899de2c40b1_711x787.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8f3750ac-4683-46a2-8e37-5899de2c40b1_711x787.webp)

#### Contenuti social

[Jasper](https://www.jasper.ai/)  
crea contenuti social

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1fb4385-6df4-4fbf-bd8e-35429f311742_1415x846.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1fb4385-6df4-4fbf-bd8e-35429f311742_1415x846.webp)

### Immagini

- Arte: creazione di opere d'arte uniche, generate dall'intelligenza artificiale o assistenza artisti con ispirazione visiva.
    
- Design: generazione di loghi, idee prodotto, siti web
    
- Gioco: produzione di risorse di gioco, trame o personaggi
    
- Sintesi testo-immagine: generazione di immagini fotorealistiche da descrizioni di testo o input di bassa qualità, aiutando a visualizzazione o prototipazione.
    
- Pubblicità e media: creazione di contenuti visivi su misura basato su suggerimenti testuali per campagne di marketing, social media e scopi di intrattenimento.
    

Esempi:  
[Midjourney](https://midjourney.com/)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd6dba6a-beff-43c3-8379-f44e295f0409_1476x959.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd6dba6a-beff-43c3-8379-f44e295f0409_1476x959.webp)

[DALL-E](https://openai.com/product/dall-e-2)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb7c6f0f1-a6cb-4f78-9350-7fcfd1ee789b_735x734.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb7c6f0f1-a6cb-4f78-9350-7fcfd1ee789b_735x734.jpeg)

Adobe Firefly

### Video

- Entertainment: film, programmi TV e pubblicità, riducendo costi e tempi di produzione.
    
- Realtà Virtuale (VR) e Realtà Aumentata (AR): ambienti realistici e personaggi
    
- Istruzione e formazione: simulazione di scenari realistici per scopi formativi ed educativi, viaggi didattici, simulazioni mediche o esercitazioni di sicurezza.
    
- Pubblicità: video personalizzati per indirizzare dati demografici specifici o preferenze individuali, aumentando l'efficacia e il coinvolgimento degli annunci.
    

Esempi:  
[Runway ML](https://runwayml.com/)  
dai creatori di Stable Diffusione,

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd400079e-e92f-499c-9601-ad995653b949_1000x282.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd400079e-e92f-499c-9601-ad995653b949_1000x282.webp)

vedi esempio 👉🏼[Gen-1](https://research.runwayml.com/gen1)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b714482-4d37-450f-8992-26710a12986f_1200x858.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b714482-4d37-450f-8992-26710a12986f_1200x858.webp)

vedi esempio 👉🏼 [Gen-2](https://research.runwayml.com/gen2)

#### Avatar

- videochiamate
    
- videogiochi
    
- viaggi didattici / storici
    
- metaverso
    

Esempi:

- [Synthesia](https://www.synthesia.io/) Avatars (125), Voices (120), Video Templates ([mio esempio](https://share.synthesia.io/3ce08f85-4ee2-4bc1-a0e8-560458bdea8d))
    
- [Rephrase](https://www.rephrase.ai/) Text-to-video
    
- [Deepswap](https://www.deepswap.ai/) swap faces in video
    

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78dd4da9-3a8c-455b-ab73-9360923b0dce_1127x695.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F78dd4da9-3a8c-455b-ab73-9360923b0dce_1127x695.webp)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22c9e0d9-4f6e-4b40-b275-75e695623f29_750x534.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F22c9e0d9-4f6e-4b40-b275-75e695623f29_750x534.webp)

vedi [video MegaPortraits](https://www.youtube.com/watch?v=9D5ulvdg0jM)

#### Deep Fake video

- 👉🏼 [video Obama](https://youtu.be/cQ54GDm1eL0?t=32)
    
- [deepfakesweb](https://deepfakesweb.com/)
    

### Voce

- Sintesi vocale (TTS): conversione del testo scritto in parlato parole, assistente per utenti ipovedenti
    
- Assistenti virtuali: migliorare l'esperienza dell'utente (Siri, Alexa o Google Assistant).
    
- Audiolibri
    
- Clonazione vocale: creazione di voci personalizzate da utilizzare nelle animazioni, giochi o applicazioni personalizzate.
    

Esempi:  
**VALL-E**  
analizza 3 secondi della tua voce e poi potrà dire qualsiasi cosa

[SuperTone AI](https://supertone.ai/)  
👉🏼 [ascoltiamo una demo](https://supertone.ai/) di Freddie Mercury che canta in coreano.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d35fd16-a88a-40a2-815d-37bb71cb082d_1225x697.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0d35fd16-a88a-40a2-815d-37bb71cb082d_1225x697.webp)

### Musica

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0bf0a187-2513-479b-a32a-c33cf0763403_1227x650.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0bf0a187-2513-479b-a32a-c33cf0763403_1227x650.webp)

[MusicLM](https://google-research.github.io/)  
crea musica a partire da una descrizione testuale

👉🏼 esempio di MuseNet[A Little Bach AI Music](https://www.youtube.com/watch?v=jMe9X9rJjyE)

[SoundDraw](https://soundraw.io/)  
👉🏼 [example](https://soundraw.io/edit_music?length=10&tempo=normal,high,low&mood=Elegant)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac746d74-3e2c-42db-a864-4accce35fe93_1000x409.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fac746d74-3e2c-42db-a864-4accce35fe93_1000x409.webp)

[AIVA](https://aiva.ai/)  
composizione di colonne sonore

### Modelli 3D

- Videogiochi: creare personaggi, paesaggi e ambienti realistici - vedi [Ziva FX](https://youtu.be/lk3THQfxwuc)
    
- Architettura e design del prodotto: modelli 3D di città, edifici, prodotti e prototipi.
    
- Applicazioni mediche: modelli 3D dell'anatomia umana per la ricerca, l'istruzione e la pianificazione chirurgica. anche per creare impianti e protesi personalizzati per i pazienti.
    

Esempi:

**Blender + StabilityAI**

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c0ba07d-6ac7-4198-9873-263b98b81aaa_1600x716.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c0ba07d-6ac7-4198-9873-263b98b81aaa_1600x716.webp)

genera automaticamente i materiali e le textures

- [Artomatix](https://rb.gy/fhsj7) : ArtEngine in Unity
    
- [Skyboxes](https://skybox.blockadelabs.com/)
    

### Videogames

i videogiochi sono i medium più complessi e multimediali, in tempo reale e interattivi

**Flight Simulator**  
con [https://blackshark.ai/](https://blackshark.ai/)

 hanno ricostruito in 3D tutta la Terra.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8906afd-c1f4-409f-bd75-177d32c00313_1024x573.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd8906afd-c1f4-409f-bd75-177d32c00313_1024x573.webp)

**[Nyric by Lovelace Studio](https://lovelacestudio.com/)**  
GENERATIVE AI PLATFORM FOR VR

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6079f075-58e6-459c-a1e2-695846957ae2_1500x491.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6079f075-58e6-459c-a1e2-695846957ae2_1500x491.jpeg)

**Agenti / Giocatori (Unity ML-Agents)**

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F843b8258-9800-4810-8dec-7e1ccd85dcd5_1512x730.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F843b8258-9800-4810-8dec-7e1ccd85dcd5_1512x730.webp)

Altri esempi:

- [ludo.ai](https://ludo.ai/)
    
- [AI Dungeon](https://aidungeon.io/)
    

### Task (azioni)

**Project JARVIS**.  
un assistente personale in grado di creare sequenze di comandi selezionando e integrando diversi sistemi.  
[github.com/microsoft/JARVIS](https://github.com/microsoft/JARVIS)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4bae267-0126-4144-9783-8bf45ea3eecf_1246x1240.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd4bae267-0126-4144-9783-8bf45ea3eecf_1246x1240.webp)

Altri esempi:

- [Bardeen](https://www.bardeen.ai/) Automatizzazione di procedure online
    

### Codice di programmazione

[GitHub Copilot](https://github.com/features/copilot)  
Il tuo assistente alla programmazione: scrivi cosa vuoi che faccia e lui scrive il codice, praticamente in ogni linguaggio.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63be3bd8-cdab-4bce-b39e-632dd822b6dc_1476x959.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F63be3bd8-cdab-4bce-b39e-632dd822b6dc_1476x959.webp)

[Debuild](https://debuild.app/)  
crea un'app web completa in pochi secondi

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0a60a50-8fca-45cb-9107-75ac94048d2a_1476x959.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0a60a50-8fca-45cb-9107-75ac94048d2a_1476x959.webp)

### Scienza

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f499a3b-209b-4e89-8db6-bd913fad01f0_1000x1000.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9f499a3b-209b-4e89-8db6-bd913fad01f0_1000x1000.jpeg)

AlphaFold e Meta AI hanno costruito dei modelli da 15 miliardi di parametri per l'analisi e il sequenziamento della proteine. Migliorando ed accelerando i processi fino a 60 volte. Impatto sulla medicina, chimica, energie rinnovabili. ([fonte](https://www.science.org/doi/10.1126/science.ade2574))

### Robot autonomi

👉🏼 [Vedi come imparano a giocare a calcio](https://youtu.be/efw8xuex4uI?t=13) con il Reinforced Learning

## Conclusione

> L'ultimo decennio è stato definito da User Generated Content (UGC). Il prossimo sarà costruito su AI Generated Content (AIGC)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74f4a5ca-53f9-4b8f-a12a-2d8985fea282_716x944.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F74f4a5ca-53f9-4b8f-a12a-2d8985fea282_716x944.webp)

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc9935e42-7874-4c50-8fc7-ce495e76a9f2_1000x851.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc9935e42-7874-4c50-8fc7-ce495e76a9f2_1000x851.webp)

Attenzione ai "gorilla nell'algoritmo" (un problema delle prime AI che, non avendo elaborato materiale equilibrato, aveva dato dei problemi (scandalosi) nel riconoscere immagini che non aveva in memoria).. questo tema è alla base di tutto il tema del _bias,_ ovvero deformazione di base intrinseca ai dati con cui sono state allenate.

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a51eaed-2bc2-4f7a-bf2e-7d7a2ddf8738_804x634.webp)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a51eaed-2bc2-4f7a-bf2e-7d7a2ddf8738_804x634.webp)

> Gli output della GenAI sono il frutto dell'elaborazione della produzione della nostra umanità, magari riconnesso in modo originale e imprevedibile
> 
> Oggi è più un problema di immaginazione e curiosità, che non di tecnologia e risorse.  
> Dobbiamo imparare a descrivere bene quello che vogliamo...  
> e fare attenzione a quello che desideriamo.

Se vuoi continuare a saperne di più, puoi iscriverti alla mia **newsletter** [2042](https://2042.substack.com/).

Baci e abbracci e condividete senza un domani.

Stefano

ah e così non vi basta eh? allora ecco il giouchino:

[

![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5df210d3-f04d-4c85-b80e-482aa5f3b546_1184x1102.jpeg)



](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5df210d3-f04d-4c85-b80e-482aa5f3b546_1184x1102.jpeg)

[![](https://substackcdn.com/image/fetch/w_80,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Ff37ba0c0-352f-4bdd-b27d-7cb21153c1df_601x600.jpeg)](https://substack.com/profile/7620861-stefano-cecere?utm_source=post-reactions-face)