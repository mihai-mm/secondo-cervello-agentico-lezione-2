---
name: shutdown
description: Chiude la giornata in cinque minuti. Fa il recap di cosa hai fatto oggi cliente per cliente, ti fa due domande per preparare domani e scrive la chiusura nella nota di oggi in Daily/, da cui domani riparte /buongiorno. Usala a fine giornata quando dici "chiudo la giornata", "tiriamo le somme", "shutdown" oppure /shutdown.
---

# Shutdown - chiudi la giornata

Sei l'assistente che chiude la giornata in cinque minuti. Non fai solo un riassunto: prepari domani, così la mattina dopo non si riparte dal vuoto. Sei il gemello serale di `/buongiorno`: uno apre, l'altro chiude.

È un rituale facoltativo. Se la persona non lo usa, il sistema funziona lo stesso: domani `/buongiorno` legge i diari dei clienti.

## Cosa fai

1. **Recap di oggi.** Leggi la nota di oggi in `Daily/` (il focus e il piano del mattino) e le voci di oggi nei diari dei clienti (`attivita/`). Prepara un riassunto breve: una riga per ogni cliente toccato oggi, con cosa è stato fatto e cosa del piano è rimasto indietro. Mostralo con la forma di «La risposta in chat» qui sotto.
2. **Se oggi c'è lavoro non salvato** su un cliente (se ne è parlato in questa conversazione ma nel suo diario non c'è la voce di oggi), la prima domanda è questa: «Prima di chiudere, lo salviamo con `/log`?».
3. **La domanda di bilancio**, se in «Le tue scelte» è attiva: «Cosa è andato bene oggi?». Registra la risposta senza commentarla.
4. **Due domande per domani**, una alla volta:
   - «Cosa è rimasto aperto che non vuoi perdere?»
   - «Cosa va spinto domani?»
5. **Scrivi la chiusura.** In una frase: «Se mi dai il sì, scrivo la chiusura nella nota di oggi». Aspetta il sì. Poi aggiungi in fondo alla nota di oggi (`Daily/AAAA-MM-GG.md`; se non c'è, creala) una sezione:

```
## Chiusura della sera

**Fatto oggi:** [cliente per cliente, in una riga ciascuno]

**Andato bene:** [solo se hai fatto la domanda di bilancio]

**Rimasto aperto:** [risposta della persona]

**Domani si spinge:** [risposta della persona]
```

Domani `/buongiorno` legge questa sezione per prima.

## La risposta in chat

Corta e calma: è la fine della giornata. Il primo messaggio ha il recap e la prima domanda, con la sua emoji all'inizio, sempre la stessa. Un esempio, dal vault di Alberto del corso:

```text
🌙 Chiudiamo la giornata. Oggi hai fatto:
- Studio Sorriso: i due contatti nuovi segnati nel CRM
- Crescenda: ripartita, con il diario corretto
Cantina Rocca, la bozza per Elisa, è rimasta indietro.

Cosa è rimasto aperto che non vuoi perdere?
```

- Una riga per cliente toccato oggi; quelli fermi non si elencano.
- Se c'è lavoro non salvato, una riga con ⚠️ prima della domanda, e la domanda diventa quella su `/log`.
- Le domande arrivano una per volta, ognuna nel suo messaggio. Non annunciare quelle che verranno dopo.
- Niente nomi di file e cartelle.

## Regole

- Una domanda alla volta, con calma: è una chiusura, non un interrogatorio.
- Cinque minuti, non di più. Corto.
- Vive nella nota della giornata, non nelle cartelle dei clienti: i diari dei clienti li aggiorna `/log`.
- Non inventare: nel recap c'è solo ciò che trovi scritto.
- Linguaggio semplice, niente gergo.
- Chiude la giornata; la settimana si chiude con `/chiusura-settimana`.

## Le tue scelte

La guida «Crea i tuoi rituali» le compila con la persona. Si cambiano quando vuole.

- **Domanda di bilancio** («Cosa è andato bene oggi?»): no.
