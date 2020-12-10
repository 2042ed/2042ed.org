# Formati e Interscambio
- Code of Conduct: regole di partecipazione e comunicazione
- changelog https://keepachangelog.com
- commit syntax https://www.conventionalcommits.org

## Interoperability
formati aperti e formati chiusi

## Future Proof

## Come posso fare un buon changelog?

### Linee guida
- I changelog sono _per le persone_, non per le macchine.
- Dovrebbe esserci una voce per ogni singola versione.
- Le modifiche dello stesso tipo dovrebbero essere raggruppate.
- Versioni e sezioni dovrebbero essere collegabili.
- L'ultima versione viene per prima.
- Viene mostrata la data di release di ogni versione.
- Si dichiara se il progetto segue il [Versionamento Semantico](https://semver.org/).

### Tipologie di cambiamenti
- `Added` per le nuove funzionalità.
- `Changed` per le modifiche a funzionalità esistenti.
- `Deprecated` per le funzionalità che saranno rimosse nelle future release.
- `Removed` per funzionalità rimosse in questa release.
- `Fixed` per tutti i bug fix.
- `Security` per invitare gli utilizzatori ad aggiornare in caso di vulnerabilità.

## Markdown
in contrapposizione al markup dell'html, è stato creato il markdown dove la base è testo semplice con pochissime convenzioni che permettono al contenuto di essere convertito nei formati più utili (html, doc, pdf, ePub) garantendo un versioning perfetto e una preservazione e portabilità ottimali

GitHub ha determinato massicciamente l'adozione dello standard MarkDown per la documentazione e la scrittura in generale e ormai moltissimi siti vengono generati con Static Site Generators (vedi Jekyll o Hugo) a partire da contenuti (pagine e posts) scritti in Markdown, e la maggior parte degli editor di testo lo supportano nativamente.

---

**links**  
- dal creatore di Markdown: https://daringfireball.net/projects/markdown/syntax
- Jekyll è il rendering engine delle GitHub pages: https://jekyllrb.com
- corso markdown: https://lab.github.com/githubtraining/communicating-using-markdown
