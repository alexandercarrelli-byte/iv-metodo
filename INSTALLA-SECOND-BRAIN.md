# Installazione del Second Brain di IV — istruzioni per il Claude che la esegue

> Per i 5 del Second Brain, il giorno della formazione. **Le esegui tu, Claude**, un passo alla volta,
> dicendo al tuo possessore cosa stai facendo e perché. Lui non deve scrivere comandi: clicca solo
> dove glielo chiedi tu. Se un passo non riesce, **non improvvisare**: scrivi cosa è successo e
> fermati — si finisce nella sessione dedicata con Alexander (piano B).

## 0. Dove sei

La sessione deve essere aperta nella cartella **`Documenti/IV Second Brain`**
(Mac: `~/Documents/IV Second Brain`; Windows: `C:\Users\<nome>\Documents\IV Second Brain`, oppure
dentro OneDrive se lì sta la cartella Documenti: va bene lo stesso). Deve essere **vuota**: se non
lo è, fermati e chiedi.

Chiedi al possessore il nome del suo spazio di lavoro: è `sb-<nome>-<cognome>`
(per esempio `sb-matteo-branchini`). Lo trova anche nella mail di invito di GitHub.

## 1. Git

`git --version`.
- **Mac**, se manca: `xcode-select --install`. Si apre una finestra di sistema: il possessore clicca
  «Installa» e aspetta qualche minuto.
- **Windows**, se manca: il possessore scarica e installa **Git for Windows** da
  https://git-scm.com/download/win, con le opzioni proposte. Poi chiude e riapre la sessione.

## 2. L'accesso a GitHub

I due repo sono privati: per scaricarli GitHub deve sapere chi è il possessore.

- **Mac** — serve GitHub CLI. `gh --version`; se manca: con Homebrew `brew install gh`; senza
  Homebrew il possessore scarica il pacchetto `.pkg` per macOS dall'ultima versione in
  https://github.com/cli/cli/releases/latest e lo installa con doppio clic. Poi lancia
  `gh auth login --hostname github.com --git-protocol https --web` **in background**: stampa un
  codice di otto caratteri e il link `https://github.com/login/device`. **Mostra il codice al
  possessore**, lui apre il link, entra con il suo account GitHub, incolla il codice e autorizza.
  Quando il comando finisce: `gh auth setup-git`.
- **Windows** — Git for Windows ha già dentro il gestore delle credenziali: al primo download del
  passo 3 si apre da solo il browser per entrare in GitHub; il possessore accede e autorizza.

**Controllo**: `git ls-remote https://github.com/alexandercarrelli-byte/second-brain-iv` deve
rispondere senza errori. Se dice che il repo non esiste, quasi sempre l'invito non è stato accettato:
il possessore lo trova nella mail di GitHub o su https://github.com/notifications.

## 3. Scarica i due repo

Dentro la cartella, in quest'ordine:

1. `git clone https://github.com/alexandercarrelli-byte/second-brain-iv .`
   (il punto finale vuol dire «qui dentro»: la cartella principale **è** il repo comune)
2. `git clone https://github.com/alexandercarrelli-byte/sb-<nome>-<cognome> aziendale`
   (lo spazio di lavoro del possessore, nella sottocartella `aziendale`)

## 4. Fine

Di' al possessore di **chiudere questa sessione e riaprirla nella stessa cartella**, e di rispondere
sì a «Trust this folder» se ricompare. Al riavvio leggerai il `CLAUDE.md` del progetto e farai da
solo il controllo di primo avvio (`regole/05-primo-avvio.md`): sono le istruzioni scritte da
Alexander, uguali per tutti.
