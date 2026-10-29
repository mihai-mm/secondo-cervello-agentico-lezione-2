---
name: log
description: Salva a fine sessione il lavoro fatto su un cliente, allineando tutto - la voce di oggi nel diario della settimana, lo Stato corrente con i prossimi passi spuntati, le decisioni prese in MEMORY, i file nuovi nella mappa e, nel profilo, le correzioni che hai dato a Claude sul modo di lavorare. Usala quando dici "salva", "registra", "logga il lavoro", "chiudiamo qui" oppure /log.
---

# Log - salva il lavoro

Sei l'assistente che a fine sessione mette al sicuro il lavoro fatto su un cliente, **non in un posto solo ma allineando tutto**. Il valore è che la prossima volta (o un collega) riapre il cliente e trova un quadro aggiornato, non una foto vecchia. È il gesto che chiude il cerchio aperto da `/riprendi-progetto`.

Fa per esteso quello che il `CLAUDE.md` del vault chiama «Salvare il lavoro».

## Cosa fai

1. **Capisci cosa salvare.** Ripercorri la conversazione: file prodotti, decisioni prese dalla persona, fatti nuovi, prossimi passi fatti o nati. Se ha lavorato su più clienti, salvi ognuno nella sua cartella. Se non c'è niente di concreto, dillo in una riga e fermati.
2. **Mostra cosa scriverai, poi aspetta il sì.** Un elenco breve, file per file: cosa aggiungi e dove, comprese le cose imparate sulla persona (punto 5). Se in «Le tue scelte» è attivo il tempo della sessione, chiedi nella stessa domanda quanto ci ha lavorato.
3. **Diario della settimana** (`attivita/AAAA-Www.md` del cliente):
   - se il file della settimana corrente non c'è, crealo con la forma di quelli che ci sono (frontmatter `tipo: diario` e `aggiornato`, titolo `# [Cliente] - settimana NN del AAAA`) e ricopia in cima lo `## Stato corrente` dell'ultimo file, prossimi passi compresi; il file vecchio non si tocca più. Mentre ricopi, controlla che lo Stato corrente non contraddica `MEMORY.md` (numeri, decisioni marcate «SUPERATA»): se lo contraddice, non ricopiare l'errore in silenzio, mostralo alla persona e chiedi come scriverlo;
   - aggiungi sotto lo Stato corrente la voce di oggi, `## AAAA-MM-GG`, in cima ai giorni: cosa è stato fatto, in poche righe (e il tempo della sessione, se in «Le tue scelte» è attivo);
   - aggiorna lo `## Stato corrente`: fase, dove siamo, cosa blocca; nei **prossimi passi** spunta quelli fatti (`- [x]`) e aggiungi quelli nuovi. Quando una fase si chiude, scrivi la fase nuova.
4. **`MEMORY.md`**: solo le decisioni **prese dalla persona**, con data, motivo e fonte. Una richiesta del cliente non ancora decisa resta nel diario. Se una decisione nuova ne sostituisce una vecchia, la vecchia si marca «SUPERATA il AAAA-MM-GG» con il rimando alla nuova.
5. **Cosa hai imparato sulla persona**, se in «Le tue scelte» è attivo. Ripercorri la conversazione e cerca le correzioni sul modo di lavorare («no, scrivilo più corto», «non mandarmi mai la bozza senza il prezzo») e le preferenze che valgono anche per altri clienti. Proponile nell'elenco del punto 2, una riga ciascuna, e con il sì aggiungile a `_claude/PROFILO.md`, nella sezione che c'entra (per esempio «Come lavoro e come decido»), con la data. Una preferenza che vale per un solo cliente va nel `CLAUDE.md` di quel cliente. Se non ce ne sono, non dire niente. È così che il tuo Claude impara: la correzione di oggi non la devi ripetere la settimana prossima.
6. **Mappa del cliente**: il link a ogni file nuovo, e la riga del diario se è nato un file di settimana.
7. **`Home.md`**: aggiorna la riga del cliente solo se cambia lo stato (in pausa, chiuso, fase nuova).
8. **Rileggi e riepiloga** in chat in tre righe: cosa hai salvato e dove.
9. **Bozza per il cliente**, se in «Le tue scelte» è attiva: un messaggio breve di aggiornamento (cosa è stato fatto, cosa serve da lui, il prossimo passo), nel tono del `CLAUDE.md` del cliente. Lo mostri in chat: lo manda la persona, tu non mandi niente.

## Regole

- **Non salvare a metà.** Se aggiorni il diario ma non lo Stato corrente, la prossima volta si trova una foto vecchia. Allinea sempre.
- Il diario si scrive in avanti: un errore si corregge con una nota datata, non riscrivendo i giorni passati. Lo Stato corrente invece si aggiorna.
- Le decisioni stanno in `MEMORY.md`, il racconto di cosa è stato fatto nel diario. Non confonderli.
- Linguaggio semplice. Date assolute, mai «oggi» o «ieri» nei file.
- Salva; non recupera (c'è `/riprendi-progetto`) e non chiude la giornata (c'è `/shutdown`).

## Le tue scelte

La guida «Crea i tuoi rituali» le compila con la persona. Si cambiano quando vuole («nel log aggiungi il tempo della sessione»).

- **Cosa hai imparato sulla persona**: sì.
- **Tempo della sessione nel diario**: no.
- **Bozza di aggiornamento per il cliente**: no.
