# Kanban Board
*Gorgo Lab - Strumenti di Coordinamento*

## A chi si rivolge questo strumento

Questo template si rivolge a quei Maintainer che hanno avviato un progetto con 2-3 collaboratori che durerà più di 3-4 settimane nonchè per quelle attività in cui si inizia a perdere traccia di "chi fa cosa" o di quali sono le priorità.

Non è obbligatorio. Se vi coordinate già bene a modo vostro, perfetto. Questo è uno strumento che Gorgo Lab mette a disposizione per chi ne ha bisogno.

## I tre elementi essenziali

Per coordinare un piccolo team servono solo tre cose:

1. **Board condivisa** - Tutti vedono cosa c'è da fare, chi lo sta facendo, cosa è fatto
2. **Comunicazione asincrona** - Un posto dove parlare del progetto
3. **Definition of Done** - Sapere quando un task è davvero finito

### 1. Kanban Board

#### Cos'è

Una bacheca (fisica e/o digitale) con tre colonne. Il primo passo è scomporre il progetto in task: piccole attività concrete e completabili da una persona in poche ore o giorni. Vedi dopo per alcuni esempi.

| TODO | DOING (max 2-3) | DONE |
|------|-----------------|------|
| Disegno CAD parte Y<br>Ordine viti<br>Test motore | Taglio legno (Marco)<br>Saldatura (Sara) | Disegno CAD parte X |

#### Come funziona

**TODO (Da fare)**

Contiene tutti i task individuati che devono essere fatti, ordinati per priorità (più importante in alto). Solitamente il Maintainer decide l'ordine.

**DOING (In corso)**

Contiene i task su cui qualcuno sta ancora lavorando. Ogni task indica il nome di chi se ne sta occupando. E' importante stabilire un limite massimo di task (vedi dopo) in questa colonna per evitare la troppa dispersione.

**DONE (Fatto)**

Qui vengono raccolti tutti i task ultimati e verificati. Ricorda di celebrare i progressi!

#### Regole base

**1. Una card = un task concreto**

- ❌ Troppo vago: "Fare elettronica"
- ✅ Concreto: "Saldare 4 LED al PCB"

**2. Spostamento / "Pull System"**

Quando un task finisce in DOING, ne tira (pull) un altro da TODO in DOING. Questo flusso continuo è chiamato "Pull System".

**3. WIP Limit (Work In Progress)**

Il WIP Limit è il numero massimo di task nella colonna DOING. Esiste perchè è meglio sforzarsi a finire 2 cose che averne 5 a metà. Il Maintainer può decidere un limite diverso, ma solitamente si consiglia 2-3 task contemporanei.

#### Dove realizzarlo

Il Gorgo Lab ti mette a disposizione un'istanza dell'applicazione Trello pre-configurata che puoi usare anche da remoto. Chiedi al personale per avere l'accesso. In alternativa nulla ti vieta di usare una lavagna bianca, un poster con post-it o un foglio: hanno il vantaggio di essere sempre visibile a chi passa al makerspace e non richiede alcun setup tecnologico.

### 2. Comunicazione Asincrona

Quando un team lavora senza un canale dedicato, la comunicazione si frantuma in mille pezzi. Alcune decisioni vengono prese di persona al makerspace, ma chi non era presente quel giorno resta all'oscuro. Altre informazioni viaggiano su chat WhatsApp personali tra due membri, mentre il terzo non sa nulla. Altre ancora semplicemente si perdono, dimenticate tra una sessione e l'altra. Il risultato è confusione, duplicazione di lavoro e la classica frase "Ah, non lo sapevo".

Serve un posto unico e condiviso dove tutto ciò che riguarda il progetto viene discusso. Può essere un gruppo Whatsapp creato ad-hoc nella community Gorgo Lab, o un thread Telegram, Discord o Slack, o la sezione commenti di Trello se usate già il board digitale. L'importante è che sia uno solo e che tutti sappiano che lì si parla del progetto. Decisioni, dubbi, aggiornamenti, resoconti di riunioni, foto di prototipi, link a risorse: tutto in un posto. Chi non era presente può recuperare, chi ha un dubbio può chiedere, nessuna informazione si perde.

### 3. Definition of Done

#### Il problema

Senza criteri chiari su cosa significa "fatto", ogni persona interpreta diversamente il completamento di un task. Questo genera incomprensioni, rilavorazioni e attriti evitabili.

#### La soluzione

All'inizio del progetto, il Maintainer definisce cosa significa "finito" sia per il progetto completo che per i singoli task. Bastano poche righe condivise con il team. Ogni card sul board dovrebbe avere criteri chiari scritti nella descrizione o nei commenti.

**Esempio - Task: "Saldare PCB"**

✅ DONE: "Tutti i componenti saldati, continuità testata con multimetro, nessun ponte di stagno"  
❌ NOT DONE: "Saldato ma non testato"

#### Perché serve

Definire il termine "fatto" evita incomprensioni che portano a rifare il lavoro, previene blocchi al progresso e permette di celebrare i veri completamenti. Quando una card va in DONE, tutti sanno che è davvero finita e si può procedere.

**Esempi:**

**Progetto: Lampada LED custom**

- ✅ DONE = Lampada si accende, cambia colori, spenta con interruttore
- ❌ NOT DONE = Si accende ma colori non funzionano

**Progetto: Banco da lavoro**

- ✅ DONE = Costruito, stabile, testato con peso, verniciato
- ❌ NOT DONE = Costruito ma non testato


**Progetto: Robot braccio Arduino**

- ✅ DONE = Braccio si muove su 3 assi, codice su GitHub, video demo
- ❌ NOT DONE = Si muove ma non è documentato

## Uso Avanzato (opzionale)

Se il vostro progetto diventa più complesso o dura più di 2 mesi, potreste aggiungere altre colonne come ad esempio:

### Colonna WAITING

Per task bloccati da cause esterne:

| TODO | WAITING | DOING (max 2-3) | DONE |
|------|---------|-----------------|------|
|      | Ordine viti (in attesa del bando) |                 |      |

Utile per vedere cosa vi rallenta sistematicamente e se ci sono colli di bottiglia ripetuti.

### Metriche Kanban

Se volete ottimizzare il flusso di lavoro attraverso l'analisi di dati concreti (non necessario per la maggior parte dei progetti, ma utile per progetti lunghi o ripetitivi), dovrete raccogliere alcune metriche nel tempo. Questo significa annotare quando ogni task inizia e finisce, quanti task vengono completati ogni settimana, e dove si verificano i blocchi più frequenti. Solo con questi dati numerici potrete identificare pattern sistematici e prendere decisioni basate su evidenze oggettive anziché su impressioni:

- **Cycle Time:** Quanto tempo impiega una card da DOING a DONE?
- **Throughput:** Quante card completate a settimana?
- **Blocchi ricorrenti:** Quali task finiscono sempre in WAITING?

### Retrospettive mensili

Una volta al mese, dedicate 30 minuti a riflettere insieme su come sta procedendo il lavoro. Analizzate cosa ha funzionato bene e merita di essere mantenuto, cosa non ha funzionato e ha creato rallentamenti o frustrazioni, e soprattutto quali azioni concrete potete mettere in campo il mese successivo per migliorare. Il valore di questo esercizio sta nel documentare le decisioni prese e nell'applicarle davvero nei giorni seguenti. Una retrospettiva senza azioni concrete è solo una chiacchierata che non cambia nulla.

