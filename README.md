Dopo aver creato un nuovo database nel vostro phpMyAdmin e aver importato lo schema allegato, eseguite le query del file allegato.
**Cosa consegnare?**
Dopo aver testato le vostre query con phpMyAdmin, riportatele in un file txt e caricatelo nella vostra repo.

1. Selezionare tutti gli studenti nati nel 1990 (160)
SELECT `date_of_birth`
FROM `students`
WHERE YEAR (`date_of_birth`) = '1990'

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
SELECT `cfu`
FROM `courses`
WHERE (`cfu`) > '10'

3. Selezionare tutti gli studenti che hanno più di 30 anni
SELECT *
FROM `students`
WHERE YEAR (`date_of_birth`) < '1994'

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)
SELECT * 
FROM `courses`
WHERE `period` = 'I semestre'
AND `year` = 1

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)
SELECT * 
FROM `exams` 
WHERE `date` = '2020-06-20'
AND HOUR(`hour`) >= 14

6. Selezionare tutti i corsi di laurea magistrale (38)
SELECT * 
FROM `degrees` 
WHERE `level` = 'magistrale'

7. Da quanti dipartimenti è composta l'università? (12)
SELECT COUNT(*)
FROM `departments`

8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
SELECT * 
FROM `teachers` 
WHERE `phone` IS NULL

BONUS
===

1. Contare quanti iscritti ci sono stati ogni anno
SELECT COUNT(*), YEAR (`enrolment_date`)
FROM `students`
GROUP BY YEAR (`enrolment_date`); 

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
SELECT COUNT(*), `office_address`
FROM `teachers` 
GROUP BY `office_address`
