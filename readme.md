## DB STRUCTURE
Modellare la struttura di un database per memorizzare tutti i dati riguardanti una università:
- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni Corso può essere tenuto da diversi Insegnanti;
- ogni Corso prevede più appelli d'Esame;
- ogni Studente è iscritto ad un solo Corso di Laurea;
- ogni Studente può iscriversi a più appelli di Esame;
- per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.

Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.
Utilizzare https://www.drawio.com/ per la creazione dello schema come visto in classe ed esportare quindi il diagramma in png caricandolo nella repo come fatto nel live coding questa mattina

## tables name
- departments (more than one)
- main_courses (more than one)
- sub_courses (for each main courses)
- teachers (can do more than one courses)
- exam appels (for each courses)
- students (subscribed in only one courses and can register for multiply exam appeals)

## tables structure
(nomi delle colonne e tipo di dati che sono accettati)
## departments
- id | bigint - auto_increment - primary_key (unique, not null)
- name | varchar (50) - not null
- main courses id | varchar (255) - not null
- description | text(500) - null

## main_courses
- id | bigint - auto_increment - primary_key (unique, not null)
- departments id | bigint - primary_key (unique, not null)
- name | varchar (50) - not null
- sub courses | varchar (255) - not null
- description | text(500) - null

## sub_courses
- id | bigint - auto_increment - primary_key (unique, not null)
- main courses id | bigint - primary_key (unique, not null)
- name | varchar (50) - not null
- topics covered | varchar (255) - not null
- cost | float (8,2) - not null
- capacity | tinyint - null
- numbers of exam appels | tinyint - not null
- course duration | tinyint - not null
- partecipants (students id) | bigint - primary_key (unique, not null)

## teachers
- id | bigint - auto_increment - primary_key (unique, not null)
- name | varchar (50) - not null
- surname | varchar (50) - not null
- courses he teaches | varchar (255) - null
- role | varchar (50) - null

## exam appels
- id | bigint - auto_increment - primary_key (unique, not null)
- type of courses | varchar (50) - not null
- partecipants (students id) | text(500) - null
- date of exam | datetime - null
- vote | tinyint - not null

## students
- id | bigint - auto_increment - primary_key (unique, not null)
- name | varchar (50) - not null
- surname | varchar (50) - not null
- aob | date - not null
- address | varchar (50) - null
- email | varchar (50) - null
- cell | varchar(14) - null
- year of attendance | tinyint - null






