---
title: Storytelling interattivo
date: 2026-02-02
updated: 2026-05-05
description: "Yarn Spinner per scrivere storie interattive didattiche"
type: book
weight: 92
toc: true
---

# Storytelling interattivo

Le storie non servono solo a rendere un gioco più interessante. Nei giochi didattici aiutano a dare **contesto**, a far emergere **conflitti significativi**, a motivare il giocatore e a trasformare una scelta in un momento di riflessione.

Se in un serious game vogliamo sviluppare conoscenze, atteggiamenti o capacità decisionali, la narrazione interattiva può diventare una vera meccanica di apprendimento.

## Perché usare storie interattive nel GBL

Una buona storia interattiva può:

- creare coinvolgimento emotivo
- mettere il giocatore davanti a dilemmi realistici
- far sperimentare conseguenze in un ambiente sicuro
- collegare contenuti astratti a contesti concreti
- favorire debrief, auto-riflessione e discussione di gruppo

Questo è particolarmente utile quando gli obiettivi didattici non sono solo cognitivi, ma anche sociali, etici, civici o relazionali.

## Narrative design didattico

Prima di scrivere dialoghi, conviene progettare il sistema di apprendimento.

### 1. Obiettivo di apprendimento

Chiediti:

- cosa deve capire o saper fare il giocatore alla fine?
- quale errore o preconcetto vogliamo far emergere?
- quale situazione concreta può mettere in gioco questa competenza?

### 2. Conflitto significativo

Le scelte migliori non sono quelle "giuste" contro quelle "stupide", ma quelle che mettono in tensione:

- tempo vs accuratezza
- interesse personale vs bene comune
- impulsività vs verifica
- conformismo vs pensiero critico

### 3. Conseguenze leggibili

Ogni scelta dovrebbe produrre almeno uno di questi effetti:

- una conseguenza narrativa
- un cambiamento di stato
- un feedback dal mondo di gioco
- un momento di riflessione o debrief

### 4. Debrief

Nel Game Based Learning il significato educativo spesso si consolida **dopo** la scelta. Per questo è utile prevedere:

- un confronto finale con il tutor o con altri giocatori
- una sintesi delle decisioni prese
- una domanda aperta di trasferimento al mondo reale

## Perché Yarn Spinner

[Yarn Spinner](https://www.yarnspinner.dev/) è un sistema open source per scrivere dialoghi e storie ramificate in file di testo `.yarn`.

È adatto a un corso breve perché:

- la sintassi è leggibile anche da chi non programma molto
- permette nodi, scelte, salti, variabili e condizioni
- funziona bene in workflow iterativi
- ha una estensione ufficiale per VS Code con evidenziazione sintattica e vista a grafo
- si integra bene con Unity

## Sintassi minima

Un file Yarn contiene uno o più **nodi**. Ogni nodo ha almeno un titolo, un corpo e una chiusura.

```yarn
title: Start
---
Tutor: Benvenuto nel laboratorio.
Tutor: Oggi prenderai alcune decisioni.

-> Sono pronto.
	Tutor: Bene, iniziamo.
-> Ho bisogno di più contesto.
	Tutor: Ti guiderò passo passo.
===
```

Elementi base:

- `title:` definisce il nome del nodo
- `---` apre il contenuto del nodo
- `===` chiude il nodo
- `->` introduce una scelta
- l'indentazione sotto una scelta indica cosa succede se viene selezionata

## Variabili e condizioni

Le variabili servono a ricordare lo stato del dialogo e a rendere il racconto adattivo.

```yarn
title: Start
---
<<declare $consapevolezza = 0>>
<<declare $ha_verificato = false>>

Tutor: Hai trovato un post molto condiviso.

-> Lo inoltro subito.
	<<set $consapevolezza to $consapevolezza - 1>>
	Tutor: Hai agito rapidamente, ma senza verifica.
-> Controllo la fonte.
	<<set $consapevolezza to $consapevolezza + 1>>
	<<set $ha_verificato to true>>
	Tutor: Ottimo, stai cercando elementi affidabili.

<<if $ha_verificato>>
	Tutor: Questo atteggiamento riduce il rischio di disinformazione.
<<else>>
	Tutor: Velocità e sicurezza non coincidono sempre.
<<endif>>
===
```

## Esempio: cittadinanza digitale

Questo esempio mostra una micro-storia educativa su verifica delle fonti e responsabilità online.

```yarn
title: Start
---
<<declare $credibilita = 0>>
<<declare $ha_controllato_la_fonte = false>>

Compagna: Hai visto questo post? Dice che domani la scuola chiude.
Compagna: Lo giro subito a tutti?

-> Sì, così avvisiamo il gruppo velocemente.
	<<set $credibilita to $credibilita - 1>>
	Tu: Meglio correre.
	<<jump Finale>>

-> Aspetta, prima controlliamo la fonte.
	<<set $credibilita to $credibilita + 1>>
	<<set $ha_controllato_la_fonte to true>>
	Tu: Cerchiamo una conferma ufficiale.
	<<jump Verifica>>
===

title: Verifica
---
Compagna: Da dove partiamo?

-> Dal sito della scuola.
	<<set $credibilita to $credibilita + 1>>
	Tu: Verifichiamo autore, data e canale ufficiale.
	<<jump Finale>>

-> Dai commenti sotto il post.
	Tu: Se tutti lo scrivono, forse è vero.
	<<jump Finale>>
===

title: Finale
---
<<if $credibilita >= 2>>
	Tutor: Hai adottato una buona pratica di fact-checking.
	Tutor: Non ti sei limitato al contenuto, hai valutato la fonte.
<<else>>
	Tutor: Hai privilegiato la rapidità rispetto all'affidabilità.
	Tutor: Nel mondo reale questo può amplificare la disinformazione.
<<endif>>

<<if $ha_controllato_la_fonte>>
	Tutor: Domanda finale: quali segnali userai la prossima volta per capire se una fonte è attendibile?
<<else>>
	Tutor: Domanda finale: cosa ti ha spinto a condividere prima di verificare?
<<endif>>
===
```

## Pattern utili per il design didattico

### Scelta + conseguenza + riflessione

Una formula semplice ma efficace:

1. presentare un dilemma
2. registrare la scelta
3. mostrare una conseguenza
4. chiudere con una domanda di debrief

### Variabili come indicatori educativi

Le variabili non devono misurare solo vittoria o sconfitta. Possono tracciare:

- accuratezza
- empatia
- collaborazione
- prudenza
- curiosità
- qualità dell'argomentazione

### Fallimento utile

In un gioco didattico la scelta meno efficace non va punita in modo moralista. Va resa leggibile, discussa e trasformata in apprendimento.

## Workflow consigliato

Per un piccolo team o un laboratorio:

1. scrivere prima la mappa dei nodi su carta o lavagna
2. identificare dove il giocatore impara davvero qualcosa
3. tenere pochi rami, ma differenziati in modo chiaro
4. testare i dialoghi ad alta voce
5. osservare non solo cosa sceglie il giocatore, ma **perché** lo fa

## Errori frequenti

- scrivere dialoghi lunghi senza decisioni significative
- confondere la scelta narrativa con una domanda a quiz
- creare troppi rami difficili da mantenere
- rendere "giusta" una sola risposta in modo troppo evidente
- dimenticare il debrief finale

## Laboratorio rapido

Esercizio: progetta una micro-storia di 3 nodi su un tema educativo.

Vincoli:

- 1 protagonista
- 1 conflitto
- 2 scelte iniziali
- 1 variabile
- 2 finali diversi
- 1 domanda finale di riflessione

Temi possibili:

- uso consapevole dei social
- gestione di un conflitto in classe
- scelta sostenibile in città
- decisione etica in un team di progetto

## Risorse

- [Yarn Spinner](https://www.yarnspinner.dev/)
- [Documentazione Yarn Spinner](https://docs.yarnspinner.dev/)

