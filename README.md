Dopo aver creato un nuovo database nel vostro phpMyAdmin e aver importato lo schema allegato, eseguite le query del file allegato.
**Cosa consegnare?**
Dopo aver testato le vostre query con phpMyAdmin, riportatele in un file txt e caricatelo nella vostra repo.

1. Selezionare tutti gli studenti nati nel 1990 (160)
SELECT `date_of_birth`
FROM `students`
WHERE YEAR (`date_of_birth`) = '1990'

2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
