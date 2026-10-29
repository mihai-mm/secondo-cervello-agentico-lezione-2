# Il tuo Project Manager

Lezione 2. Nella Lezione 1 hai costruito i primi collaboratori della squadra: il **Commerciale** (dalla call alla proposta) e l'**Account Manager** (una memoria per ogni cliente).

Oggi sali di un livello. Non più un cliente alla volta, ma **tutti insieme**. Arriva il collaboratore che tiene il filo di tutto: il tuo **Assistente personale e Project Manager**.

Il filo della lezione è una storia. **Alberto** è il titolare di Bussola, l'agenzia dove lavorano anche Luca e Paola. È una piccola azienda e lui non segue un cliente solo: li tiene insieme tutti. Lunedì mattina apre il portatile e ha cinque clienti in testa, ognuno con la sua storia, le sue decisioni prese settimane fa e già sfumate. Lo seguiamo per una giornata tipo: apre la giornata, recupera un cliente, lavora, salva, chiude la sera, chiude la settimana. Ogni gesto è un rituale che poi rifai sui tuoi clienti veri.

Due idee reggono tutta la lezione:

- **Un secondo cervello che ricorda al posto tuo.** Ogni cliente ha la sua cartella, e Claude la rilegge ogni volta che lo riapri. Tu non tieni più tutto a mente.
- **Dei rituali.** Comandi che aprono e chiudono la giornata e la settimana, così il filo non si spezza mai tra un giorno e l'altro, tra un cliente e l'altro.

## Il problema: cinque clienti, un lunedì che ricomincia da capo

Alberto non ha un problema di fatica. Ha un problema di **filo**.

Ogni cliente è un progetto, una storia, una decisione presa due settimane fa che ora fa fatica a ricordare. Prima di fare qualsiasi cosa, ogni mattina, mezz'ora solo per ricostruire dov'è rimasto con ognuno: riaprire email, file, appunti, rimettere insieme i pezzi.

Non è il lavoro a stancarlo. È il continuo **«ripartire da capo»**. E più clienti aggiungi, più quella mezz'ora cresce. C'è anche un rischio in più: un team di collaboratori AI lavora in fretta, e se nessuno tiene il filo i pezzi si perdono ancora più velocemente.

Il resto della lezione è la cura: un rituale per ogni momento della giornata, e una memoria che tiene il filo al posto tuo.

## Aprire la giornata: `/buongiorno`

Il primo rituale. Quello che trasforma il lunedì caotico in una lista chiara.

**Il problema.** Per sapere cosa fare oggi dovresti aprire cinque cartelle a mano, controllare cosa resta da fare per ogni cliente, guardare il calendario e mettere tutto in fila. Ogni mattina, da capo.

**L'idea che sblocca tutto: un comando, e la giornata si apre da sola.** Dici «Buongiorno» e Claude guarda:

1. i **prossimi passi** di ogni cliente, scritti nel suo diario;
2. il tuo **calendario** della giornata, se l'hai collegato;
3. la **chiusura di ieri sera**, se l'hai fatta;
4. le **priorità della settimana**, le due o tre cose che contano di più.

Li mette insieme e ti restituisce il piano: ecco le cose di oggi, in ordine, cliente per cliente. Poi fa la cosa che cambia tutto: **ti propone su cosa concentrarti**, con il motivo («la scheda del Modulo 3: Crescenda è ferma da due settimane»), e tu confermi o cambi. Non ti scarica solo una lista e non ti chiede di scegliere da zero: ti porta una proposta, così la giornata ha un fuoco.

Quel piano non resta un pensiero che svanisce: viene **scritto** nella nota di oggi, in `Daily/`.

### Due assi: il cliente e la giornata

Qui incontri i due modi in cui il tuo secondo cervello è organizzato:

- l'**asse cliente**: la cartella di ogni cliente in `1-Projects/`, con la sua memoria. È quella che hai costruito nella Lezione 1.
- l'**asse giornata**: la **nota del giorno** in `Daily/`, dove finisce il piano di oggi. Taglia tutti i clienti: è la tua giornata, non quella di un cliente solo.

`/buongiorno` lavora sull'asse giornata leggendo l'asse cliente.

> **La skill `/buongiorno`**
> - **Cosa le dai**: niente, è lei che va a leggere: i prossimi passi di ogni cliente e il calendario, se collegato.
> - **Cosa fa**: monta il piano del giorno (cosa fare, per quale cliente, in che ordine) e ti propone su cosa concentrarti. Il lunedì apre anche le settimane nuove dei clienti.
> - **Dove finisce**: nella nota di oggi, `Daily/AAAA-MM-GG.md`, che resta scritta.

## Recuperare un cliente: `/riprendi-progetto`

Il cuore della lezione. Il «recupera il contesto» che Alberto cercava da sempre.

**Il problema.** Prima cosa in lista: un cliente che non tocchi da due settimane, e in mezzo altri quattro. Dove eravamo rimasti? A che punto è il progetto? Cosa avevamo deciso? Una volta avresti riaperto tutto a mano per ricostruire.

**L'idea che sblocca tutto: chiedi e basta.** Dici «Riprendiamo Crescenda» e Claude apre la cartella del cliente e ti racconta dove siete: a che fase è il progetto, cosa è stato deciso, qual è il prossimo passo, cosa è rimasto in sospeso. In trenta secondi sei di nuovo dentro.

Una cosa importante: Claude non parte a testa bassa. Prima ti **mostra lo stato che ha ricostruito**, con il file da cui viene ogni informazione, e ti segnala se trova qualcosa che non torna (per esempio una decisione recente che contraddice il riepilogo della settimana). Poi aspetta la tua conferma e solo allora propone due o tre mosse. Sei tu a decidere, lui prepara il terreno.

> **La skill `/riprendi-progetto`**
> - **Cosa le dai**: il nome del cliente da riprendere.
> - **Cosa fa**: rilegge i file della cartella del cliente e ti ricostruisce «dove eravamo e qual è la prossima mossa», segnalando le cose da chiarire.
> - **Dove finisce**: te lo racconta in chat. Non scrive niente senza il tuo sì.

## Come fa Claude a ricordare: la memoria di progetto

Fermati un attimo. Come faceva Claude a sapere tutto questo del cliente? **Nessuna magia, ma un metodo di lavoro.** Ha riletto i file della cartella: gli stessi che tu e il tuo team gli avete fatto salvare nelle sessioni precedenti. È tutto lì, scritto, e Claude lo rilegge ogni volta che riapri il cliente.

Vale la pena aprire il cofano, perché è il motore di tutta la lezione.

**1. Il vault ha le sue regole.** Il `CLAUDE.md` del vault, con `PROFILO.md` e `SOUL.md` in `_claude/`, dice a Claude come lavori, sempre, su qualunque cliente. Li hai preparati nella Lezione 0. Se le regole sono scritte bene, Claude lavora solo su ciò che serve: risparmi tempo e ottieni risultati migliori.

**2. La cartella del cliente è la sua memoria.** Dentro ci sono pochi file, ognuno con un ruolo:

- `CLAUDE.md` del cliente: chi è e le regole con cui lavorarci.
- `MEMORY.md`: le decisioni prese, con data e motivo, e i numeri importanti.
- la **mappa** (il file con il nome della cartella): da lì raggiungi ogni suo file.
- `calls/`, `reports/`, `materials/`: le chiamate, ciò che produci, ciò che ricevi.
- il **diario** in `attivita/`, un file per settimana, con in cima lo **`Stato corrente`**: la fase, dove siamo, cosa blocca e i **prossimi passi**. È la fonte che `/riprendi-progetto` legge per prima.

**3. Una regola tiene tutto leggibile: la settimana nuova.** Ogni settimana nasce un file nuovo del diario, e lo Stato corrente viene ricopiato in cima. Le settimane vecchie restano lì, congelate: sono la storia del cliente. Così quando Claude recupera il contesto **non si perde in mesi di appunti vecchi**: trova subito, in cima, dove siete oggi. Non è un vezzo: è ciò che tiene veloce il «riprendiamo il cliente» anche dopo mesi di lavoro.

È questo che fa la differenza tra «ricomincio da capo» e «so sempre dove siamo».

> Una nota per il futuro: qui Claude conosce ogni **cliente** perché ne rilegge la cartella. Il `SOUL.md` della Lezione 0 è l'inizio di una memoria più profonda, quella che conosce **te** attraverso tutti i progetti. La facciamo crescere nella Lezione 5.

## I prossimi passi stanno nel diario

Per tenere le cose da fare in ordine non ti serve un gestionale: bastano i **prossimi passi** nello Stato corrente di ogni cliente. Sono caselle da spuntare.

```
## Stato corrente

- **Fase:** Erogazione dei moduli (2 di 5 fatti)
- **Dove siamo:** Modulo 2 erogato, ora si prepara il Modulo 3 sulla distribuzione.
- **Cosa blocca:** manca la data dell'incontro con Giulia.
- **Prossimi passi:**
  - [x] Raccogliere il feedback dei primi due moduli
  - [ ] Scrivere la scheda operativa del Modulo 3 e mandarla a Giulia
  - [ ] Fissare con Giulia la data del Modulo 3
```

Spunti un passo quando lo chiudi, ne aggiungi uno quando nasce. Quando una fase si chiude, scrivi la fase nuova. Il progetto avanza, e lo vedi a colpo d'occhio. E siccome i prossimi passi vivono accanto al resto della memoria del cliente, `/buongiorno` li trova la mattina e `/riprendi-progetto` li ritrova dopo settimane.

Se usi già un gestore dei task (ClickUp, Notion, Todoist...), puoi collegarlo a Claude e usare quello al posto delle caselle: diglielo, e lo scrive nel `CLAUDE.md` del vault.

## Collegare i tuoi strumenti

Finora il lavoro è vissuto dentro il vault. Ma il lavoro vero è anche fuori: i materiali di un cliente sono su Drive, gli appuntamenti nel calendario, i nuovi contatti in una tabella.

**Il problema.** Se Claude non li raggiunge, torni tu a fare il ponte a mano.

**L'idea che sblocca tutto: Claude usa gli strumenti che già usi.** Non li sostituisce, ci si collega. Oggi vediamo i modi più semplici; quelli più avanzati li vediamo nella Lezione 3, con Paola.

Cosa colleghi tipicamente:

- **il calendario**: `/buongiorno` legge gli appuntamenti di oggi;
- **Google Drive**: i file del cliente, letti senza scaricarli a mano;
- **una tabella come CRM** (per esempio Airtable o un foglio Google): clienti, contatti e lead gestiti come in un gestionale;
- **un gestore dei task**, se già ne usi uno.

## Salvare il lavoro: `/log`

Hai lavorato un'ora su un cliente. Prima di passare al successivo, un comando: **«Salva.»**

**Il problema.** Alla fine di una sessione, quello che hai fatto è ancora fresco nella conversazione. Se chiudi senza salvare, la prossima volta riparti da una foto vecchia.

**L'idea che sblocca tutto: un comando salva in più posti.** `/log` fa una cosa precisa:

- scrive nel **diario della settimana** cosa hai fatto oggi;
- aggiorna lo **`Stato corrente`**: la fase, dove siamo, e spunta i **prossimi passi** fatti;
- tiene allineato il resto: aggiunge il link al documento nuovo nella **mappa** e, se hai preso una decisione, la segna in `MEMORY.md` con la data e il motivo;
- e impara: se durante il lavoro hai corretto Claude sul tuo modo di lavorare («scrivilo più corto»), ti propone di segnarlo nel tuo **`PROFILO.md`**. La correzione di oggi non la ripeti la settimana prossima.

Perché tutto questo? Per un motivo solo: **niente pezzi scollegati.** Se salvassi il lavoro ma non aggiornassi lo Stato corrente, la prossima volta riapriresti il cliente e troveresti una fotografia vecchia. Salvare *e* allineare, sempre.

È il gesto che chiude il cerchio aperto al mattino: **salvi oggi, recuperi domani.** E lo ritrova anche un collaboratore, se mette mano lui al cliente.

> **La skill `/log`**
> - **Cosa le dai**: niente, oppure due parole su cosa avete fatto.
> - **Cosa fa**: ti mostra cosa scrive e dove, poi salva il lavoro nella cartella del cliente, tutto allineato.
> - **Dove finisce**: nella cartella del cliente, pronto per la prossima volta.

## Chiudere la giornata: `/shutdown` (facoltativo)

A fine giornata non chiudi solo il portatile. Dai un ultimo comando per tirare le somme.

Claude ti fa il **recap di cosa hai fatto oggi** sui vari clienti, e poi due domande per preparare domani: cosa è rimasto aperto, cosa va spinto. Cinque minuti.

Domani mattina, quando aprirai la giornata, non partirai dal vuoto: partirai da dove hai deciso. È il **gemello serale del buongiorno**: uno apre, l'altro chiude. Vive nella nota di oggi, non nella cartella di un cliente.

> **La skill `/shutdown`**
> - **Cosa fa**: recap della giornata e due domande per domani.
> - **Dove finisce**: nella nota di oggi, da cui riparte il buongiorno di domani.

## Chiudere la settimana: `/chiusura-settimana` (facoltativo)

Venerdì pomeriggio, l'ultimo rituale. Un comando, e Claude ti prepara il recap settimanale: **per ogni cliente, cosa è stato fatto, cosa è avanzato, cosa resta.**

Non è un appunto privato: è un punto della situazione che puoi **girare ai collaboratori** o tenere come storia.

Poi guarda avanti: ti propone **le due o tre priorità della settimana dopo**, tu le confermi o le cambi. Da lunedì `/buongiorno` te le ricorda ogni mattina e ti dice quale lavoro le spinge. Si decide il venerdì, si esegue nei giorni dopo.

E intanto la ruota gira: la settimana che finisce resta com'è, e lunedì `/buongiorno` apre quella nuova con lo Stato corrente già ricopiato in cima. Apri lunedì, chiudi venerdì. Se ti dimentichi, funziona lo stesso.

> **La skill `/chiusura-settimana`**
> - **Cosa fa**: prepara il recap della settimana per ogni cliente (fatto, avanzato, resta) e fissa con te le priorità della settimana dopo.
> - **Dove finisce**: in `Daily/`, pronto da condividere o da archiviare.

## Il tuo Project Manager è al lavoro

Fai un passo indietro e guarda cosa hai messo in piedi. Una giornata intera, tenuta insieme da pochi comandi:

- la mattina **apri** con `/buongiorno` e confermi il fuoco del giorno;
- **recuperi** un cliente in trenta secondi con `/riprendi-progetto`;
- **lavori** con gli strumenti collegati;
- **salvi** con `/log`, tutto allineato;
- se vuoi, la sera **chiudi** con `/shutdown` e il venerdì **chiudi la settimana** con `/chiusura-settimana`.

Il filo non lo tieni più tu a memoria: lo tiene il **sistema**. Tu fai la parte che conta: le scelte, i clienti, la squadra. E ritrovi la serenità di sapere che nessun pezzo è rimasto in giro.

**Ora tocca a te.** Nell'esercitazione aggiorni il tuo vault e metti questi rituali sul tuo secondo cervello, con Claude che te li spiega e li adatta a come lavori. La prossima volta, nella Lezione 3, arriva Paola, l'Analista: far parlare gli strumenti tra loro e trasformare i dati in report e slide.

## Cosa ti porti a casa oggi

- **Il problema del Project Manager**: tanti clienti in parallelo, il contesto che si disperde, mezz'ora ogni mattina a «ripartire da capo». La cura: rituali e un secondo cervello che ricorda al posto tuo.
- **`/buongiorno`** apre la giornata: legge i prossimi passi di ogni cliente e il calendario, monta il piano e ti propone su cosa concentrarti. Il piano va nella nota di oggi, in `Daily/`.
- **Due assi**: il cliente (la sua cartella) e la giornata (la nota di oggi).
- **`/riprendi-progetto`** ricostruisce un cliente in trenta secondi: ti mostra lo stato con le fonti, segnala le cose da chiarire, propone la mossa solo dopo la tua conferma.
- **La memoria di progetto** è la cartella del cliente: `CLAUDE.md` (chi è e le regole), `MEMORY.md` (decisioni e numeri), la mappa, e il diario in `attivita/` con lo Stato corrente in cima. Sopra, le regole del vault.
- **La settimana nuova**: ogni settimana un file nuovo del diario, Stato corrente ricopiato in cima, le vecchie congelate. Tiene veloce il recupero del contesto.
- **I prossimi passi nel diario**: caselle da spuntare nello Stato corrente, al posto di un gestionale.
- **Collegare i tuoi strumenti**: calendario, Drive, una tabella come CRM, un gestore dei task se già lo usi.
- **`/log`** salva in più posti con un comando (diario, Stato corrente con i passi spuntati, decisioni, mappa), tutto allineato. Salvi oggi, recuperi domani.
- **`/shutdown`** e **`/chiusura-settimana`**, facoltativi: chiudono la giornata e la settimana.
- **Il tuo Project Manager**: apri, recupera, lavora, salva, chiudi. Il filo lo tiene il sistema.
