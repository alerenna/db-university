## TRACCIA

- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni Corso può essere tenuto da diversi Insegnanti;
- ogni Corso prevede più appelli d'Esame;
- ogni Studente è iscritto ad un solo Corso di Laurea;
- ogni Studente può iscriversi a più appelli di Esame;
- per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.

# TASKS #
Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni.

Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.-


## departments
* columns
id - PK - AI - NN - BIGINT
name VARCHAR(100) - NN
address VARCHAR(100) - NN

## programs
* columns
id - PK - AI - BIGINT
name VARCHAR(100) - NN
department_id - FK - NN - BIGINT

## courses
* columns
id PK - AI - NN - BIGINT
name VARCHAR(100) - NN
program_id - FK - NN - BIGINT

## teachers
* columns
id PK - AI - NN - BIGINT
name VARCHAR(100) - NN
lastname VARCHAR(100)  - NN
email VARCHAR(50)  - NN
phone - VARCHAR(15) - N
address- VARCHAR(100) - N

## exams
* columns
id PK - AI - NN - BIGINT
name - VARCHAR(100) - NN
date - DATETIME
course_id - FK - NN - BIGINT

## students
* columns
id PK - AI - NN - BIGINT
name VARCHAR(100) - NN
lastname VARCHAR(100)  - NN
email VARCHAR(50)  - NN
phone - VARCHAR(15) - N
address- VARCHAR(100) - N
program_id - FK - NN - BIGINT

___________
* PIVOT

## course_teacher
id PK - AI - NN - BIGINT
course_id - FK - NN - BIGINT
teacher_id - FK - NN - BIGINT

## exam_student
id PK - AI - NN - BIGINT
exam_id - FK - NN - BIGINT
student_id - FK - NN - BIGINT
