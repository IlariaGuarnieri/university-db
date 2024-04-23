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