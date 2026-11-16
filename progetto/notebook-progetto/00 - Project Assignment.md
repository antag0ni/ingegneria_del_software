### Obiettivo del Progetto

Sviluppare un'applicazione desktop dotata di **interfaccia grafica (GUI)** per la **prenotazione di aule universitarie** di un dipartimento, con salvataggio dei dati su file.

### Scadenze e Fasi (Deliverables)

Il progetto va svolto in gruppi da **4 studenti** (eccezionalmente 3) e prevede le seguenti tappe:

| **Scadenza**       | **Fase**                                                                | **Attività principali**                                                                                                                                                                       |
| ------------------ | ----------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **23 Novembre**    | **[[01 - Project Setup\|Project Setup]]**                               | Formazione gruppi, scelta del portavoce, creazione repository GitHub **pubblico** (in lettura) configurato con **Maven** e compilazione del Google Sheet del corso.                           |
| **30 Novembre**    | **[[02 - Requirements Engineering\|Requirements Engineering]]**         | Redazione e caricamento su GitHub del documento dei requisiti (casi d'uso, diagrammi dei casi d'uso, requisiti funzionali e non funzionali con priorità e identificativi).                    |
| **7 Dicembre**     | **[[03 - Design & Design di dettaglio\|Design & Design di dettaglio]]** | Caricamento del documento di design (diagrammi delle classi, di sequenza e commenti su coesione/accoppiamento). Creazione degli scheletri delle classi su GitHub documentati con **Doxygen**. |
| **14 Dicembre**    | **[[04 - Implementazione e Testing\|Implementazione e Testing]]**       | Sviluppo completo delle classi, scrittura ed esecuzione degli **Unit Test con JUnit** (esclusa la GUI) e aggiornamento documentazione su GitHub.                                              |
| **15–18 Dicembre** | **[[05 - Discussione del progetto\|Discussione del progetto]]**         | Presentazione di **8 minuti** per team con illustrazione di casi d'uso, diagrammi, eventuali refactoring e demo funzionante.                                                                  |

### Criteri di Valutazione

La valutazione finale è suddivisa equamente tra **contributo individuale (50%)** — verificato tramite la frequenza dei commit su GitHub e una valutazione confidenziale tra pari — e **qualità complessiva del progetto (50%)**, ripartita come segue:

- **Qualità del Design:** 30%
- **Qualità dei Requisiti:** 20%
- **Qualità dell'Implementazione (inclusa usabilità GUI):** 20%
- **Qualità dei Test:** 20%
- **Uso degli strumenti (Git, Doxygen, Maven):** 10%

### Funzionalità Richieste

L'applicazione deve gestire tre entità principali, salvate su file:

1. **Docenti:** E-mail istituzionale (univoca), nome e cognome.
2. **Aule:** Codice identificativo univoco, nome, edificio, piano e capienza.
3. **Prenotazioni:** Aula, docente responsabile, tipo di attività (es. lezione, esame, seminario), denominazione attività, data/ora di inizio e fine, eventuale ricorrenza settimanale e data di termine.

**Operazioni previste tramite GUI:**

- **Gestione Aule:** Inserimento, modifica, cancellazione, visualizzazione della lista e ricerca (per nome, codice o capienza minima).
- **Gestione Docenti:** Inserimento, modifica, cancellazione, visualizzazione ordinata (per cognome e nome) e ricerca (per cognome o codice/identificativo).
- **Gestione Prenotazioni:**
    - Ricerca delle aule disponibili in una data e fascia oraria.
    - Inserimento di prenotazioni singole o ricorrenti.
    - Visualizzazione ordinata per data/ora con filtri per aula o docente.
    - Cancellazione di una singola prenotazione o di tutte le occorrenze future di una serie ricorrente.
- **Vincoli di integrità:** Nessuna sovrapposizione consentita (un'aula non può ospitare più docenti contemporaneamente e un docente non può trovarsi in più aule nello stesso momento).

# TOOLS:

- **Git e GitHub:** Per il controllo di versione e la collaborazione del team. Il repository deve essere pubblicamente accessibile in lettura e utilizzato da ciascun membro con commit frequenti per tracciare il contributo individuale.
- **Apache Maven:** Per la configurazione, la compilazione del progetto e l'esecuzione automatizzata dei test.    
- **Doxygen:** Per generare la documentazione tecnica delle interfacce pubbliche delle classi a partire dai commenti nel codice sorgente.
- **JUnit:** Per la realizzazione ed esecuzione degli Unit Test automatizzati su tutte le classi (ad eccezione dell'interfaccia grafica).
- **Libreria GUI Java (es. JavaFX o Swing):** Per sviluppare l'interfaccia grafica desktop richiesta dall'applicazione (non è imposta una libreria specifica nelle slide, purché sia compatibile con la compilazione tramite Maven).
- **Strumento di modellazione UML (es. StarUML, PlantUML, Draw.io, Astah):** Per disegnare i diagrammi dei casi d'uso, delle classi e di sequenza da inserire nei documenti di Requirements Engineering e Design.
- **Google Sheets:** Da compilare nella fase iniziale di setup tramite il link fornito sulla piattaforma e-learning del corso per registrare i dati del gruppo.