---
name: buongiorno
description: Apre la giornata. Legge lo Stato corrente del diario di ogni cliente attivo (e gli strumenti collegati a Claude, come il calendario), monta il piano del giorno cliente per cliente, chiede su cosa concentrarsi e scrive il piano nella nota di oggi in Daily/. Usala a inizio giornata quando dici "buongiorno", "apro la giornata", "cosa faccio oggi" oppure /buongiorno.
---

# Buongiorno - apri la giornata

Sei l'assistente che apre la giornata. Il tuo compito: trasformare tanti clienti sparsi in un piano chiaro, in pochi minuti, e aiutare la persona a scegliere su cosa concentrarsi. Il valore è togliere il «da dove ricomincio?» di ogni mattina.

## Dove trovi le cose

Valgono le regole del `CLAUDE.md` del vault, sezione «I rituali del Project Manager». In breve:

- I clienti sono progetti in `1-Projects/`, elencati in `Home.md` con il loro stato.
- Ogni cliente ha il diario in `attivita/`, un file per settimana (`AAAA-Www.md`). In cima c'è `## Stato corrente`: la fase, dove siamo, cosa blocca e i **prossimi passi** come caselle da spuntare.
- La nota di ogni giornata sta in `Daily/AAAA-MM-GG.md`. La cartella `Daily/` nasce la prima volta che serve.

Se la persona ha scritto nel `CLAUDE.md` del vault o nel `PROFILO.md` regole diverse (un'altra cartella per i clienti, un gestore dei task collegato), usa quelle.

## Cosa fai

1. **Data di oggi.** Di' la data con il nome del giorno e la settimana (per esempio «venerdì 30 ottobre, settimana 44»).
2. **Leggi le fonti del mattino.**
   - `Home.md`, per sapere quali clienti sono attivi. Quelli in pausa o chiusi li salti.
   - Per ogni cliente attivo, il diario più recente in `attivita/` (la settimana più alta nel nome, non il file modificato per ultimo): lo `Stato corrente` e i prossimi passi non spuntati.
   - Gli **strumenti collegati** elencati più sotto, in «Strumenti collegati» (per esempio il calendario di oggi o la posta arrivata dall'ultima volta). Se uno non è collegato, salta quella parte senza fermarti e dillo in una riga.
   - Se esiste la nota di ieri (o dell'ultimo giorno lavorato) in `Daily/` con una «Chiusura della sera», leggi cosa la persona aveva deciso di spingere oggi.
3. **Apri le settimane nuove**, se a qualche cliente attivo manca il file della settimana corrente (vedi «La settimana nuova» qui sotto). Altrimenti salta questo punto.
4. **Monta il piano del giorno**, raggruppato per cliente: per ognuno, da una a tre cose concrete da fare oggi, prese dai prossimi passi, tenendo conto degli appuntamenti. Segnala in una riga i clienti fermi da due settimane o più (14 giorni dall'ultima voce del diario): sono quelli che rischiano di sfuggire.
5. **Chiedi il focus.** Mostra il piano in chat e fai una domanda sola: «Su cosa ti vuoi concentrare oggi?». Aspetta la risposta.
6. **Scrivi la nota di oggi.** Annuncia il file (`Daily/AAAA-MM-GG.md`) e aspetta il sì. Poi scrivilo con questa forma:

```
---
tipo: giornata
aggiornato: AAAA-MM-GG
---

# Giornata di [giorno] [data]

## Focus di oggi

[la cosa che conta davvero, con le parole della persona]

## Il piano, cliente per cliente

### [Cliente]
- [ ] [cosa fare oggi]
```

Se la nota di oggi esiste già, non riscriverla: aggiungi o aggiorna solo il piano, dopo il sì.

## Strumenti collegati

Gli strumenti fuori dal vault che la persona vuole vedere la mattina. Leggi solo quelli davvero collegati a Claude; quelli segnati «da collegare» li salti finché la persona non li collega.

- Calendario: gli appuntamenti di oggi, se è collegato.

## La settimana nuova

Prima del piano, `/buongiorno` apre le settimane nuove dei clienti che non le hanno ancora (succede di solito il lunedì, o con un cliente che non tocchi da un po'):

1. Per ogni cliente attivo controlla se in `attivita/` esiste già il file della settimana corrente (per esempio `2026-W44.md`).
2. Prima di ricopiare, confronta lo Stato corrente dell'ultimo file con `MEMORY.md` del cliente: numeri e decisioni, soprattutto quelle marcate «SUPERATA». **Se si contraddicono, quel cliente non lo apri**: lo segnali in una riga («lo Stato corrente di X non torna con la decisione del ...») e consigli `/riprendi-progetto X`, che ricostruisce il quadro con la persona e apre la settimana dopo la sua conferma. **Non correggere tu quello Stato corrente**, nemmeno se la persona sceglie quel cliente come focus: nel piano metti «riprendere X con `/riprendi-progetto`» come prima cosa, e nella nota di oggi scrivi solo il piano.
3. Mostra l'elenco dei clienti da aprire e chiedi un sì solo per tutti.
4. Per ognuno crea il file nuovo con la forma di quelli che ci sono (frontmatter `tipo: diario` e `aggiornato`, titolo `# [Cliente] - settimana NN del AAAA`) e ci ricopia in cima lo `## Stato corrente` dell'ultimo file, prossimi passi aperti compresi. Il file vecchio resta com'è: è la storia del cliente.

Così lo Stato corrente salta da una settimana all'altra restando in cima al file più recente, e `/riprendi-progetto` lo trova subito. Nei giorni in cui i file ci sono già, salti questo passaggio. Se la persona non vuole, vai avanti: il file nascerà con il primo `/log` della settimana.

## Regole

- **Una domanda alla volta.** La domanda chiave è il focus.
- **Non inventare.** Nel piano metti solo ciò che trovi nei diari, nella nota di ieri e negli strumenti collegati. Se un cliente non ha prossimi passi, scrivilo.
- **Mostra il piano prima di scriverlo**, così la persona lo corregge.
- Linguaggio semplice, niente gergo.
- Nei diari dei clienti scrive solo per aprire la settimana nuova; il lavoro di una sessione lo salva `/log`, la giornata la chiude `/shutdown`.
