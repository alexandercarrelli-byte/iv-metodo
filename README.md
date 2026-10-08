# IV Metodo

Il modo in cui Alexander Carrelli lavora con l'IA, scritto perché il Claude di ogni persona di
Imprenditore Vero lavori allo stesso modo. Lo mantiene Alexander: per tutti è **in sola lettura**.

## Installazione (una volta sola)

1. Clona questo repo in `~/iv-metodo` (senza spazi nel nome).
2. Nel file `~/.claude/CLAUDE.md` (crealo se non c'è) aggiungi la riga:

   `@~/iv-metodo/CLAUDE.md`

   Da lì Claude Code lo legge in **ogni** sessione, in qualunque cartella. ⚠️ **Questa riga la scrive la
   persona a mano, non Claude**: Claude Code la blocca per sicurezza («Instruction Poisoning»), perché fa
   leggere istruzioni di un repo esterno. Mac, nel Terminale: `echo '@~/iv-metodo/CLAUDE.md' >> ~/.claude/CLAUDE.md`.
   Windows, in PowerShell: `Add-Content -Path "$HOME\.claude\CLAUDE.md" -Value '@~/iv-metodo/CLAUDE.md' -Encoding ascii`.
3. Crea la cartella `~/IV/` con dentro `lavoro/` e `personale/`: è la tua memoria, resta sul tuo
   computer e nessun altro la vede.

Gli aggiornamenti arrivano da soli: a inizio sessione il Claude fa `git pull` del metodo.
