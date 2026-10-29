# Skill pronte

Qui trovi i cinque rituali del Project Manager già fatti. Funzionano così come sono, ma **la strada consigliata è installarli con la guida «Crea i tuoi rituali»**: Claude te li spiega, ti fa una o due domande e li adatta al tuo modo di lavorare prima di installarli. Un rituale che hai adattato tu ti somiglia di più.

Prima di installarli, il vault va aggiornato alla Lezione 2 (`Da usare con Claude/Aggiornamento del vault - Lezione 2.md`): le skill cercano i prossimi passi nel diario dei clienti e la nota del giorno in `Daily/`, come dice il `CLAUDE.md` aggiornato.

## Cosa c'è

- **`buongiorno/`**: la mattina. Legge lo Stato corrente di ogni cliente, monta il piano del giorno, ti propone su cosa concentrarti e scrive la nota di oggi in `Daily/`. Ti ricorda le priorità della settimana. Il primo buongiorno della settimana apre anche le settimane nuove dei clienti.
- **`riprendi-progetto/`**: quando riprendi un cliente. Rilegge la sua cartella, ti dice dove eravate e cosa non torna, e ti propone due o tre mosse. Non scrive niente senza il tuo sì.
- **`log/`**: a fine sessione. Salva il lavoro nel diario del cliente, aggiorna lo Stato corrente e spunta i prossimi passi, segna le decisioni in `MEMORY.md` e collega i file nuovi. Le correzioni che dai a Claude sul tuo modo di lavorare le propone per il tuo profilo: così non le ripeti.
- **`shutdown/`** (facoltativo): la sera. Recap della giornata e due domande per domani, nella nota di oggi.
- **`chiusura-settimana/`** (facoltativo): il venerdì. Fatto, avanzato, resta per ogni cliente, da condividere con il team, e le priorità della settimana dopo, che `/buongiorno` ti ricorda ogni mattina.

In fondo a ogni skill c'è la sezione **«Le tue scelte»**: cosa leggere oltre ai diari (il calendario, la posta), le priorità, la domanda personale e così via. Le skill pronte hanno le scelte di partenza; la guida le cambia con te, e puoi cambiarle quando vuoi chiedendolo a Claude («nel buongiorno togli la domanda personale»).

## Come si installa

1. Apri il tuo vault e vai nella cartella `.claude/skills/`. Se non la vedi, è normale: le cartelle che iniziano con un punto sono nascoste. Nel Finder premi Cmd+Maiusc+punto per mostrarle.
2. Copia dentro la cartella del rituale (tutta, con il file `SKILL.md` dentro). Il risultato deve essere, per esempio, `.claude/skills/buongiorno/SKILL.md`.
3. Apri una conversazione nuova nella cartella del vault e scrivi `/`: nel menu deve comparire il rituale. Se non compare, scrivi `/reload-skills`.

Se preferisci, chiedilo a Claude: «installa la skill buongiorno da skill-pronte in .claude/skills/: spiegamela prima». Claude ti dice cosa scrive e dove, e aspetta il tuo sì. L'app può mostrarti una richiesta di permesso, perché `.claude/` è una cartella speciale: va consentita.

Nessun rituale manda messaggi a nessuno. Tutti ti chiedono prima di scrivere un file.
