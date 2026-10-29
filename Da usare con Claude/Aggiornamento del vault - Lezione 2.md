# Aggiornamento del vault - Lezione 2

Questo file aggiorna il tuo vault per la Lezione 2, come l'aggiornamento di un programma: insegna al tuo Claude come lavora un Project Manager. Non lo leggi tu: lo applica Claude, quando segui `INIZIA QUI.md` o la guida «Crea i tuoi rituali».

Cosa cambia, in breve:

- nasce la cartella `Daily/`, con una nota per ogni giornata (il piano del mattino e la chiusura della sera);
- nel diario di ogni cliente lo `Stato corrente` tiene anche la **fase** e i **prossimi passi**, da spuntare: sono i tuoi task;
- il `CLAUDE.md` del vault conosce i cinque rituali: `/buongiorno`, `/riprendi-progetto`, `/log`, `/shutdown`, `/chiusura-settimana`.

Le skill dei rituali si installano dopo, una alla volta, con la guida: Claude te le spiega e le adatta al tuo modo di lavorare prima di installarle.

---

## Per Claude: come applicare l'aggiornamento

1. **Controlla se è già applicato**: nel `CLAUDE.md` alla radice del vault cerca il titolo `## I RITUALI DEL PROJECT MANAGER`. Se c'è, l'aggiornamento è fatto: dillo in una riga e fermati qui.
2. **Spiega in tre righe** cosa cambierà nel `CLAUDE.md` (le tre modifiche qui sotto) e che nessun file della persona viene toccato. Aspetta il sì.
3. **Applica le tre modifiche**, senza cambiare il resto del file. Se la persona ha già scritto regole diverse su questi punti (per esempio usa un gestore dei task collegato al posto dei prossimi passi nel diario), non sovrascriverle: mostrale la differenza e chiedi cosa tenere.
4. **Aggiorna la data** `aggiornato:` in cima al `CLAUDE.md`.
5. **Rileggi** il file e di' come verificarlo: «apri `CLAUDE.md`: subito dopo la sezione SALVARE IL LAVORO trovi I RITUALI DEL PROJECT MANAGER».

Non creare ancora la cartella `Daily/`: nasce da sola al primo `/buongiorno`.

### Modifica 1 - La tabella delle cartelle

Nella tabella di «COME È ORGANIZZATO IL VAULT», aggiungi questa riga subito dopo quella di `4-Archives/`. Se la tabella o la riga non ci sono, mostra alla persona dove la metteresti e chiedi:

```
| `Daily/` | la nota di ogni giornata, `AAAA-MM-GG.md`: il piano del mattino e la chiusura della sera. Nasce al primo `/buongiorno` |
```

### Modifica 2 - La sezione nuova

Aggiungi questa sezione subito dopo la fine di «SALVARE IL LAVORO» (prima di «COME LAVORARE»). Se quelle sezioni non ci sono, mettila prima di «MANUTENZIONE» o in fondo al file.

```
## I RITUALI DEL PROJECT MANAGER

Dalla Lezione 2 del corso: il modo di tenere insieme più clienti senza ripartire da capo ogni mattina.

**I task stanno nel diario.** In ogni progetto, lo `## Stato corrente` in cima al diario della settimana dice:

- **Fase:** a che punto è il progetto (per esempio «Erogazione dei moduli, 2 di 5 fatti»);
- **Dove siamo** e **cosa blocca**, in una o due righe ciascuno;
- **Prossimi passi:** le cose da fare, una per riga, come caselle: `- [ ]` da fare, `- [x]` fatto. Si spuntano quando si chiudono, si aggiungono quando nascono.

**Quando salvi**, anche a parole senza `/log`: spunta nello Stato corrente i prossimi passi fatti e aggiungi quelli nati.

**La settimana nuova.** Il diario ha un file per settimana. Alla prima apertura di una settimana nuova (di solito con `/buongiorno` del lunedì, altrimenti con il primo salvataggio) nasce il file nuovo e ci si ricopia in cima lo `## Stato corrente` dell'ultimo file, prossimi passi aperti compresi, dopo aver controllato che non contraddica `MEMORY.md` (se lo contraddice, si chiede alla persona come scriverlo). Il file vecchio resta com'è: è la storia del progetto.

**La giornata.** In `Daily/AAAA-MM-GG.md` c'è la nota del giorno: il focus della mattina, il piano cliente per cliente e, se la persona chiude la giornata, la chiusura della sera. I recap della settimana stanno in `Daily/AAAA-Www - recap della settimana.md`, con le priorità della settimana dopo.

**I rituali**, ognuno con la sua procedura in `.claude/skills/` (si installano con la guida della Lezione 2):

| Quando | Rituale | Cosa fa |
|---|---|---|
| La mattina | `/buongiorno` | apre la settimana nuova se serve, legge gli Stati correnti, monta il piano del giorno, propone il focus, scrive la nota di oggi |
| Quando riprendi un cliente | `/riprendi-progetto` | rilegge la cartella del cliente, ricostruisce dove siete, segnala cosa non torna, propone 2-3 mosse. Scrive solo la settimana nuova o la correzione dello Stato corrente, con il tuo sì |
| A fine sessione | `/log` | fa per esteso «Salvare il lavoro»: diario, Stato corrente con i prossimi passi spuntati, MEMORY, mappa, e le correzioni sul modo di lavorare nel `PROFILO.md` con il tuo sì |
| La sera (facoltativo) | `/shutdown` | recap della giornata e due domande per domani, nella nota di oggi |
| Il venerdì (facoltativo) | `/chiusura-settimana` | recap fatto, avanzato, resta per ogni cliente, da condividere, e le priorità della settimana dopo |

Se un rituale non c'è ancora in `.claude/skills/`, segui comunque queste regole quando la persona chiede le stesse cose a parole.
```

### Modifica 3 - La tabella delle procedure

Nella tabella di «LE PROCEDURE» aggiungi queste righe sotto quella di `porta-i-tuoi-file` (se la tabella non c'è, mostra alla persona dove la metteresti e chiedi), **solo per i rituali già installati** in `.claude/skills/` (la guida le aggiunge una alla volta mentre li installa):

```
| «Buongiorno», «apro la giornata», «cosa faccio oggi» | `buongiorno` | piano in chat e focus proposto; scrive la nota di oggi dopo il tuo sì |
| «Riprendiamo [cliente]», «dove eravamo con…» | `riprendi-progetto` | quadro e discrepanze in chat; scrive solo con il tuo sì |
| «Salva», «registra», «chiudiamo qui» | `log` | ti mostra cosa scrive e dove; scrive dopo il tuo sì |
| «Chiudo la giornata», «tiriamo le somme» | `shutdown` | due domande, poi la chiusura nella nota di oggi dopo il tuo sì |
| «Chiudo la settimana», «recap della settimana» | `chiusura-settimana` | recap in chat; lo salva dopo il tuo sì |
```

Se la frase sopra la tabella dice «Per ora ce n'è una», correggila in «Queste sono quelle installate».
