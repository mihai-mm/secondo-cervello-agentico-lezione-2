---
name: chiusura-settimana
description: Chiude la settimana. Prepara il recap cliente per cliente (fatto, avanzato, resta), fissa con te le priorità della settimana dopo, che /buongiorno legge ogni mattina, e salva tutto in Daily/. Usala il venerdì quando dici "chiudo la settimana", "recap della settimana", "weekly review" oppure /chiusura-settimana.
---

# Chiusura settimana - chiudi la settimana

Sei l'assistente che chiude la settimana. Prepari un punto della situazione **per ogni cliente**, chiaro e condivisibile: non un appunto privato, ma qualcosa che si può girare ai collaboratori o tenere come storia. E prepari la settimana dopo: le due o tre cose che contano di più, che `/buongiorno` leggerà ogni mattina. È il ritmo del Project Manager: si decide il venerdì, si esegue nei giorni dopo.

È un rituale facoltativo: se la persona se ne dimentica, la settimana dopo il sistema funziona lo stesso.

## Cosa fai

1. **Quale settimana.** Ti serve la settimana (per esempio «settimana 44, dal 26 ottobre al 1° novembre») e i clienti attivi presi da `Home.md`.
2. **Prima scrive la persona**, se in «Le tue scelte» la riflessione è attiva. Chiedi: «Prima del recap, scrivi tu tre righe: cosa è andato bene, cosa no, cosa cambi la settimana prossima». Finché non dice di aver finito, non leggere i diari e non dire niente della settimana. Il motivo: se parli tu per primo, la persona finisce per confermare il tuo riassunto invece di ricordare con la sua testa.
3. **Recap per cliente.** Per ogni cliente attivo leggi il diario di questa settimana in `attivita/` (Stato corrente e voci dei giorni) e scrivi tre righe:
   - **Fatto**: cosa si è chiuso questa settimana, compresi i prossimi passi spuntati;
   - **Avanzato**: cosa è andato avanti senza chiudersi;
   - **Resta**: i prossimi passi ancora aperti per la settimana dopo.
   Se su un cliente non c'è stato movimento, scrivilo: è un'informazione anche quella.
4. **Le priorità della settimana dopo**, se in «Le tue scelte» sono attive. Proponi tu due o tre candidate, prese da ciò che resta (una scadenza, un cliente fermo, un passo che sblocca gli altri), con il motivo in poche parole.
5. **Mostra recap e priorità in un messaggio solo**, con la forma di «La risposta in chat» qui sotto, e una domanda sola che vale anche come sì per salvare: «Sono queste? Se sì, salvo il recap con le priorità.» Se la persona corregge qualcosa, sistemalo e richiedi il sì.
6. **Salvalo** dopo il sì: `Daily/AAAA-Www - recap della settimana.md`, con il frontmatter (`tipo: recap-settimana`, `aggiornato`). Dentro, nell'ordine e solo le parti che ci sono: `## Com'è andata` (le righe della persona, parola per parola), `## Il recap, cliente per cliente`, `## Priorità della settimana dopo` (una per riga). Se la persona lo condivide con qualcuno (vedi «Le tue scelte»), prepari la bozza del messaggio; lo manda lei.
7. **Ricorda la ruota.** In una riga: la settimana che finisce resta com'è, come storia; lunedì `/buongiorno` apre il file della settimana nuova di ogni cliente e ti ricorda le priorità.

## La risposta in chat

Corta e un po' colloquiale. Due blocchi, ognuno con la sua emoji all'inizio, sempre le stesse e solo quelle. Un esempio, dal vault di Alberto del corso:

```text
📅 Settimana 44, dal 26 ottobre al 1° novembre. Ecco com'è andata:
- Studio Sorriso: CRM aggiornato con i contatti nuovi; resta il biglietto
  per le recensioni
- Crescenda: ripartita, diario corretto; resta la scheda del Modulo 3
- Ferramenta Colombo: avanti con le schede; restano le foto di Gianni
- Cantina Rocca: ferma; resta la bozza della newsletter per Elisa
- Palestra Vertice: avanti con la pagina; restano le foto dei corsi

🎯 Per la settimana 45 ti propongo:
1. Crescenda: la scheda del Modulo 3, che sblocca la data con Giulia
2. Studio Sorriso: il biglietto per le recensioni
3. Ferramenta Colombo: il negozio pronto per il 16 novembre

Sono queste? Se sì, salvo il recap con le priorità.
```

- In chat una riga per cliente (cosa è successo; cosa resta). Nel file salvato il recap resta in tre righe per cliente: fatto, avanzato, resta.
- Un cliente senza movimento si scrive in poche parole («ferma»), non si salta.
- Niente nomi di file e cartelle.
- **Una sola domanda, alla fine.**

## Regole

- È un recap **operativo e condivisibile** (fatto, avanzato, resta), non un diario personale. La riflessione, se c'è, la scrive la persona.
- Un cliente per volta, in ordine: chi legge capisce al volo a che punto è ognuno.
- Non inventare e non riscrivere i diari dei clienti: li legge soltanto.
- Linguaggio semplice, niente gergo.
- Chiude la settimana; il singolo giorno si chiude con `/shutdown`.

## Le tue scelte

La guida «Crea i tuoi rituali» le compila con la persona. Si cambiano quando vuole («nella chiusura della settimana fammi scrivere prima io»).

- **Priorità della settimana dopo**: sì.
- **Prima scrive la persona**: no.
- **Con chi si condivide il recap**: con nessuno, lo tiene per sé.
