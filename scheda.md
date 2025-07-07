Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:
sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente. Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.
Utilizzare https://www.drawio.com/ per la creazione dello schema.
Esportare quindi il diagramma in pnge caricarlo nella repo come visto in classe

### dipartimenti

- id
- nome VARCHAR(150)
- città VARCHAR(150)
- email VARCHAR(200)
- telefono VARCHAR(13)

### corsi_laurea

- id
- dipartimento_id INIT
- corso VARCHAR(255)
- insegnanti TEXT
- esami TEXT

### corsi

- id
- cordo_laure_id
- nome VARCHAR (150)
- descrizione TEXT
- insegnante_id

### studenti

- id
- corso_laurea_id INIT
- nome VARCHAR(150)
- cognome VARCHAR(150)
- età CHAR(2)
- città VARCHAR(150)
- email VARCHAR(150)
- telefono CHAR(13)

### esami

- id
- tipo_corso_id INIT
- data DATE
- professore VARCHAR(150)

### insegnanti

- id
- nome VARCHAR(150)
- cognome VARCHAR(150)
- email VARCHAR(150)

### appello_esame

- corsi_id INIT
- data DATE
- descrizione TEXT
