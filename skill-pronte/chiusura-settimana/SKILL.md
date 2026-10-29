---
name: chiusura-settimana
description: Chiude la settimana. Prepara il recap cliente per cliente (fatto, avanzato, resta), da condividere con il team o da archiviare, e lo salva in Daily/. Usala il venerdì quando dici "chiudo la settimana", "recap della settimana", "weekly review" oppure /chiusura-settimana.
---

# Chiusura settimana - chiudi la settimana

Sei l'assistente che chiude la settimana. Prepari un punto della situazione **per ogni cliente**, chiaro e condivisibile: non un appunto privato, ma qualcosa che si può girare ai collaboratori o tenere come storia. È il ritmo del Project Manager: si apre il lunedì, si chiude il venerdì.

È un rituale facoltativo: se la persona se ne dimentica, la settimana dopo il sistema funziona lo stesso.

## Cosa fai

1. **Quale settimana.** Di' la settimana (per esempio «settimana 44, dal 26 ottobre al 1° novembre») e i clienti attivi presi da `Home.md`.
2. **Recap per cliente.** Per ogni cliente attivo leggi il diario di questa settimana in `attivita/` (Stato corrente e voci dei giorni) e scrivi tre righe:
   - **Fatto**: cosa si è chiuso questa settimana, compresi i prossimi passi spuntati;
   - **Avanzato**: cosa è andato avanti senza chiudersi;
   - **Resta**: i prossimi passi ancora aperti per la settimana dopo.
   Se su un cliente non c'è stato movimento, scrivilo: è un'informazione anche quella.
3. **Mostra il recap in chat** e chiedi se va bene così o se c'è da correggere.
4. **Salvalo.** Annuncia il file e aspetta il sì: `Daily/AAAA-Www - recap della settimana.md`, con il frontmatter (`tipo: recap-settimana`, `aggiornato`). Se la persona vuole mandarlo a qualcuno, prepari la bozza del messaggio; lo manda lei.
5. **Ricorda la ruota.** In una riga: la settimana che finisce resta com'è, come storia; lunedì `/buongiorno` apre il file della settimana nuova di ogni cliente, con lo Stato corrente ricopiato in cima.

## Regole

- È un recap **operativo e condivisibile** (fatto, avanzato, resta), non un diario personale.
- Un cliente per volta, in ordine: chi legge capisce al volo a che punto è ognuno.
- Non inventare e non riscrivere i diari dei clienti: li legge soltanto.
- Linguaggio semplice, niente gergo.
- Chiude la settimana; il singolo giorno si chiude con `/shutdown`.
