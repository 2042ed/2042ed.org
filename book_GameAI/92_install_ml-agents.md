
# installare ml-agents
procedure per installare Python + ml-agents su Windows 64 bit

useremo la versione Verified Package 1.0.6.
docs ufficiali: <https://github.com/Unity-Technologies/ml-agents/blob/release_2_verified_docs/docs/Readme.md>

## metodo 1: diretto (più veloce)
scaricare Windows x86-64 executable installer da https://www.python.org/downloads/windows/ ,durante l'installazione attivare il checkbox: ADD TO PATH

eseguire "prompt ti comandi" as Administrator
verificare che esista Python eseguendo il comando: `python`
verificare che esista il comando pip esegundo il comando: `pip -V`

```
pip install --upgrade pip
pip3 install mlagents
```

entrare nella directory del progetto ml-agents: 
`cd C:/blabla bla/ml-agents/`

provare a lanciare il comando `mlagents-learn`

deve comparire il logo UNITY


## metodo 2: con virtual environments (consigliato)
se volete compartimentare le installazioni di Python e relativi moduli, ad esempio per avere diverse versioni separate, si usano i virtual Environments, ovvero delle directory con dentro tutta la config.

L'installazione e configurazione è spiegata qui:
<https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Using-Virtual-Environment.md>


## metodo 3: via Anaconda
se non dovesse funzionare il metodo 1, o non avete dimestichezza con la Shell e comandi, c'è la possibilità di usare Anaconda che è un ambiente di gestione pacchetti Python, e che usavamo fino all'anno scorso. poi non so perché l'hanno deprecato, ma è tutt'ora funzionate.
le istruzioni molto dettagliate sono qui: 
https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation-Anaconda-Windows.md
