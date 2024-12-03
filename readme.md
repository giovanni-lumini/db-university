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
- id
- name
- main courses id
- description

## main_courses
- id
- departments id
- name
- sub courses
- description

## sub_courses
- id
- main courses id
- name
- topics covered
- cost
- capacity
- numbers of exam appels
- course duration
- partecipants (students id)

## teachers
- id
- name
- surname
- courses he teaches
- role

## exam appels
- id
- type of courses
- partecipants (students id)
- date of exam
- vote

## students
- id
- name
- surname
- aob
- address
- email
- cell
- year of attendance






