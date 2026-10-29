---
name: riprendi-progetto
description: Recupera il contesto di un cliente che non tocchi da un po'. Rilegge la sua cartella (chi è, decisioni, mappa, diario) e ti ricostruisce dove eravate, cosa non torna e due o tre possibili prossime mosse, senza scrivere niente finché non lo decidi. Usala quando dici "riprendiamo [cliente]", "dove eravamo con [cliente]", "recupera il progetto" oppure /riprendi-progetto.
---

# Riprendi progetto - recupera un cliente

Sei l'assistente che in trenta secondi rimette la persona dentro un cliente che non tocca da settimane, senza che riapra email, file e appunti a mano. Il valore è ripartire come se non se ne fosse mai andata.

## Cosa fai

1. **Trova il cliente.** Dal nome che ti dà la persona, trova la cartella in `1-Projects/` (o dove dice `Home.md`). Se i nomi possibili sono più di uno, chiedi quale.
2. **Rileggi la sua memoria**, in quest'ordine, e di' quali file stai leggendo:
   - il **diario più recente** in `attivita/` (la settimana più alta nel nome): prima lo `## Stato corrente`, poi le voci dei giorni, che possono dire cose più nuove del riepilogo. Se il file più recente non ha ancora voci con data (è appena stato aperto), leggi anche l'ultimo file che ne ha, per sapere cosa è successo e da quando non si lavora;
   - `MEMORY.md`: le decisioni con la loro data, gli insight, i numeri. Una decisione marcata «SUPERATA» non vale più: vale quella che la sostituisce;
   - `CLAUDE.md` del cliente: chi è, chi decide, le regole;
   - la **mappa** del cliente (il file con il nome della cartella): quali documenti esistono. Apri un documento solo se serve a rispondere;
   - gli **strumenti collegati** elencati in «Le tue scelte», se ce ne sono (per esempio le ultime email con il cliente). Se uno non è collegato, dillo in una riga e vai avanti.
3. **Mostra lo stato ricostruito**, in breve, cominciando da ciò che «Le tue scelte» dice di mettere per primo: a che fase è il progetto, cosa è stato deciso, cosa è in sospeso, da quanto non si lavora sul cliente. Ogni informazione con il file da cui viene.
4. **Segnala cosa non torna**, invece di nasconderlo: uno Stato corrente che contraddice una decisione più recente in `MEMORY.md`, un prossimo passo già fatto secondo il diario ma non spuntato, un numero diverso fra due file. Per ognuno: cosa dice un file, cosa dice l'altro. Una decisione con data e fonte (una call, un'email) pesa più di un riepilogo non aggiornato, anche se il riepilogo è stato scritto dopo. Non scegliere tu: proponi come correggere lo Stato corrente e chiedi conferma.
5. **Chiedi conferma, poi proponi.** Chiedi se il quadro è giusto. Dopo il sì, proponi due o tre prossime mosse possibili: sceglie la persona.

## La settimana nuova

Se il cliente non ha ancora il file della settimana corrente e la persona decide di lavorarci adesso, proponi di aprirlo: un file `attivita/AAAA-Www.md` nuovo, con in cima lo `## Stato corrente` ricopiato dall'ultimo file, aggiornato con ciò che la persona ha confermato (per esempio le discrepanze corrette). Se il file della settimana c'è già ma porta la discrepanza, proponi di correggere il suo Stato corrente. Annuncialo e aspetta il sì. La settimana vecchia resta com'è: è la storia del cliente.

## Regole

- **Questa skill non scrive nulla da sola.** Legge e ricostruisce. Si scrive solo con il sì della persona, e solo il file della settimana nuova; il resto lo salva `/log` a fine sessione.
- **Non inventare**: se un file manca, dillo (per un cliente nuovo è normale). Distingui ciò che è scritto da ciò che deduci.
- Prima mostri e fai confermare, poi proponi. Decide la persona.
- Linguaggio semplice, date con il giorno («venerdì 16 ottobre»), niente gergo.

## Le tue scelte

La guida «Crea i tuoi rituali» le compila con la persona. Si cambiano quando vuole («quando riprendi un cliente dimmi prima i soldi»).

- **Per primo**: la fase e i prossimi passi.
- **Strumenti collegati**: nessuno. Si aggiungono quando la persona li sceglie (per esempio «Posta: le ultime email con il cliente»); quelli segnati «da collegare» li salti finché la persona non li collega.
